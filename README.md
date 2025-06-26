# AI Content Curator

A web-based tool that uses Google's Gemini AI to intelligently process and curate newsletter content based on your custom rules and preferences.

## What It Does

The AI Content Curator helps you:

- **Filter newsletter content** based on your personal interests and preferences
- **Automatically categorize updates** with topic tags
- **Generate summaries** at different levels of detail (short, long, and full text)
- **Exclude unwanted content** based on your rules
- **Highlight important information** like key people, AI models, or novel ideas

### Key Features

- **Custom Processing Rules**: Define your own rules for content filtering and highlighting
- **Smart Topic Detection**: AI automatically identifies and tags content topics
- **Multiple Summary Levels**: Choose between short summaries, detailed summaries, or full text
- **Expandable Interface**: Click to expand/collapse different sections of processed content
- **Real-time Processing**: Watch content being processed with animated loading indicators
- **Secure API Key Handling**: Optional obfuscated URL parameters for sharing configurations

## How It Works

1. **Set Your Rules**: Define processing rules like "Don't show me political content" or "Highlight AI model updates"
2. **Process Rules**: The AI analyzes your rules and creates topic tags and filtering criteria
3. **Add Content**: Paste a Substack newsletter URL
4. **Process Article**: The AI scrapes, analyzes, and processes the content according to your rules
5. **Review Results**: Browse the curated content with smart summaries and topic tags

## Technology Stack

- **Frontend**: Pure HTML, CSS, and JavaScript with React (via CDN)
- **AI Processing**: Google Gemini 2.5 Flash/Pro models
- **Content Scraping**: Cloudflare Worker for URL text extraction (https://github.com/jimshare/cf-scraper)

## Getting Started

### Prerequisites

You'll need a Google Gemini API key to use this tool.

### Getting a Gemini API Key

1. **Visit Google AI Studio**: Go to [https://aistudio.google.com/](https://aistudio.google.com/)
2. **Sign In**: Use your Google account to sign in
3. **Create API Key**: 
   - Click on "Get API key" in the left sidebar
   - Click "Create API key in new project" (or select existing project)
   - Copy the generated API key (starts with `AIzaSy...`)
4. **Keep It Secure**: Store your API key securely - never share it publicly

### Running the Application

1. **Clone or Download**: Get the project files
2. **Open in Browser**: Simply open `index.html` in any modern web browser
3. **Enter API Key**: Paste your Gemini API key when prompted
4. **Start Processing**: Add your rules and begin curating content!

### Using the Key Generator (Optional)

For sharing configurations or convenience, you can use the key generator:

1. Open `key-generator.html` in your browser
2. Enter your Gemini API key
3. Click "Generate URL" to create a secure, obfuscated URL
4. Use the generated URL to access the main application with your API key pre-loaded

## File Structure

```
ai-content-curator/
├── index.html              # Main application
├── key-generator.html      # API key obfuscation tool
├── favicon.svg            # Site icon
└── README.md              # This file
```

## Usage Tips

### Writing Effective Rules

- **Be Specific**: "Highlight new AI models" works better than "AI stuff"
- **Use Exclusions**: "Don't show me political content" to filter unwanted topics  
- **Request Details**: "Give me more details on..." for topics you care about
- **People Focus**: "Highlight significant people involved" to track key figures

### Example Rules

```
Don't show me any political content
Highlight the significant people involved in all updates
Give me more details on updates related to new AI models
Only show me novel ideas from this post
Exclude any cryptocurrency or NFT content
```

## Supported Content

Currently supports:
- **Substack newsletters** (primary focus)
- Any URL that the Cloudflare Worker can scrape for text content

## Browser Compatibility

Works in all modern browsers that support:
- ES6+ JavaScript features
- Fetch API
- React 18 (loaded via CDN)
- CSS Grid and Flexbox

## Privacy & Security

- **Client-Side Processing**: Your API key and content stay in your browser
- **No Data Storage**: Nothing is stored on servers (except temporary scraping)
- **Optional Obfuscation**: Use the key generator for URL sharing
- **No Tracking**: No analytics or tracking scripts included

## Limitations

- Requires active internet connection for AI processing
- Subject to Gemini API rate limits and costs
- Content scraping depends on the source website's accessibility
- Processing time varies based on content length and complexity

## Contributing

This is a simple, self-contained application. To contribute:

1. Fork the repository
2. Make your changes to the HTML/CSS/JavaScript
3. Test thoroughly in multiple browsers
4. Submit a pull request with a clear description

## License

This project is licensed under the MIT License.

## Support

For issues or questions:
- Check the browser console for error messages
- Verify your Gemini API key is valid and has credits
- Ensure the Substack URL is accessible
- Try with different content to isolate issues