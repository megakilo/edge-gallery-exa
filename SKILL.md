---
name: exa-search
description: Search the web using the Exa AI search engine to find relevant, high-quality results for any topic, question, or research query.
metadata:
  require-secret: true
  require-secret-description: Enter your Exa API key. Get one at https://dashboard.exa.ai/api-keys
  homepage: https://exa.ai
---

# Exa Web Search

## Instructions

Call the `run_js` tool using `index.html` and a JSON string for `data` with the following fields:
- **query**: Required. The search query string. Formulate a clear, specific search query based on the user's request. Use natural language — Exa works best with descriptive queries rather than keyword-style queries.
- **numResults**: Optional. Number of results to return (1–10). Defaults to 5.
- **category**: Optional. A category to focus results on. One of: "research paper", "news", "company", "people", "personal site", "financial report". Only include if the user's query clearly fits one of these categories.

**Constraints:**
- Summarize the search results in a clear, well-structured response using the SAME language as the user's original prompt.
- Include the title, URL, and a brief description for each result so the user can evaluate relevance.
- If highlights or summaries are available in the results, use them to provide richer answers.
- For time-sensitive queries, mention that results may vary based on Exa's index freshness.
