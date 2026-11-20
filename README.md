# HenryCrawl Data for AI & RAG MCP: YouTube, Reddit, RSS, Telegram, Trends

10 LLM-ready data tools: YouTube transcripts, Reddit threads, full-text RSS, Telegram, Google Trends, App Store reviews.

**For:** AI-agent builders, RAG pipelines, social listening and market research.
**10 tools**, pay per result (no subscription), callable from Claude, ChatGPT, Cursor or any MCP client.

| Tool | Price |
|---|---|
| [YouTube Transcript for LLM & RAG (Multilingual)](https://apify.com/henrycrawl/youtube-transcript-llm) | $0.003 per transcript ($3 per 1,000) |
| [YouTube Scraper for AI Agents: Search, Channels, Comments](https://apify.com/henrycrawl/youtube-data-llm) | $0.0015 per video (full details) ($1.50 per 1,000) |
| [Reddit Scraper for AI Agents: Posts, Search, Comments](https://apify.com/henrycrawl/reddit-scraper-llm) | $0.002 per post ($2 per 1,000) |
| [RSS & News Full-Text for LLM & RAG (Multilingual)](https://apify.com/henrycrawl/rss-news-fulltext-rag) | $0.0025 per full-text article ($2.50 per 1,000) |
| [Telegram Channel Scraper for LLM & RAG (No Login)](https://apify.com/henrycrawl/telegram-channel-rag) | $0.0006 per post ($0.60 per 1,000) |
| [Google Trends for AI Agents: Interest, Related, Trending](https://apify.com/henrycrawl/google-trends-llm) | $0.002 per keyword analysed ($2 per 1,000) |
| [App Store Reviews Scraper for AI & Sentiment (175 Countries)](https://apify.com/henrycrawl/app-store-reviews-ai) | $0.0005 per review ($0.50 per 1,000) |
| [Google Ads Transparency for AI Agents: Ads by Brand](https://apify.com/henrycrawl/google-ads-transparency-llm) | $0.0015 per ad ($1.50 per 1,000) |
| [AI Brand Visibility Tracker - ChatGPT, Gemini, Claude (GEO)](https://apify.com/henrycrawl/ai-brand-visibility-tracker) | $0.01 per answer analysed ($10 per 1,000) |
| [Naver Search API: Korean News & Blog Results](https://apify.com/henrycrawl/naver-search-news-blog) | $0.002 per search result ($2 per 1,000). Error rows and blocked pages are not charged. |


## Remote MCP server for the whole bundle
Remote URL (Claude "Add custom connector", Cursor, any MCP client):

```
https://mcp.apify.com/?tools=henrycrawl/youtube-transcript-llm,henrycrawl/youtube-data-llm,henrycrawl/reddit-scraper-llm,henrycrawl/rss-news-fulltext-rag,henrycrawl/telegram-channel-rag,henrycrawl/google-trends-llm,henrycrawl/app-store-reviews-ai,henrycrawl/google-ads-transparency-llm,henrycrawl/ai-brand-visibility-tracker,henrycrawl/naver-search-news-blog
```

Claude Desktop (`claude_desktop_config.json`), using your own Apify token: each call is billed to your Apify account at the prices above.

```json
{
  "mcpServers": {
    "henrycrawl-du-lieu-ai-rag": {
      "command": "npx",
      "args": [
        "-y",
        "mcp-remote",
        "https://mcp.apify.com/?tools=henrycrawl/youtube-transcript-llm,henrycrawl/youtube-data-llm,henrycrawl/reddit-scraper-llm,henrycrawl/rss-news-fulltext-rag,henrycrawl/telegram-channel-rag,henrycrawl/google-trends-llm,henrycrawl/app-store-reviews-ai,henrycrawl/google-ads-transparency-llm,henrycrawl/ai-brand-visibility-tracker,henrycrawl/naver-search-news-blog",
        "--header",
        "Authorization:Bearer ${APIFY_TOKEN}"
      ],
      "env": {
        "APIFY_TOKEN": "<your Apify API token>"
      }
    }
  }
}
```


## Key features
- YouTube URL in, clean transcript with timestamps out
- Reddit, Telegram and RSS full text returned in LLM-ready JSON
- Google Trends, App Store reviews and Google Ads data without API keys
- Pay per result, no subscription

## Example uses
- Ask Claude: 'summarise what r/LocalLLaMA said about this model this week, with links'
- Feed YouTube transcripts and full-text news into a RAG index for research

## FAQ
**How am I billed?**
Each call runs an Apify actor on your own Apify account, billed per row returned (from $0.50 per 1,000). No subscription.

**Do I need API keys for YouTube, Reddit or Telegram?**
No, except the brand-visibility tracker, which uses your own AI provider keys.

**Is there free usage?** New Apify accounts get monthly free platform credit, enough to try every tool.

---
Built and maintained by **HenryCrawl** ([Apify Store](https://apify.com/henrycrawl)). Issues and feature requests: open a GitHub issue here.
