---
name: reddit-ai-tools
description: Find today's top Reddit stories that announce or meaningfully introduce new AI tools, products, models, or capabilities, and return source links with concise descriptions. Use when the user asks for Reddit AI tool launches, today's AI tool stories, or a daily Reddit roundup of new AI tools.
---

# Reddit AI Tools

Find the strongest Reddit posts from today that are about newly released or newly announced AI tools, then report the original Reddit links and short, evidence-based descriptions.

## Workflow

1. Establish the current date and timezone for the user. If unavailable, use UTC and state the date basis.
2. Search Reddit's current top stories, prioritizing Reddit's `r/all` top feed and relevant communities such as `r/ArtificialIntelligence`, `r/LocalLLaMA`, `r/MachineLearning`, `r/ChatGPT`, `r/StableDiffusion`, and `r/opensource`. Use Reddit's native search or top feeds when available; otherwise use web search targeted to Reddit and clearly describe that source limitation.
3. Restrict candidates to posts published during the current calendar day in the user's timezone. Prefer the top-ranked posts by Reddit engagement within that window; do not treat an all-time popular post as a story of today.
4. Include only posts that announce, launch, or give a substantive first look at a new AI product, app, model, agent, or developer tool. Exclude general AI news, opinion, memes, tutorials about established tools, and promotional posts without concrete product details.
5. Open candidate posts and verify the title, date, destination link, and enough post content to write a faithful description. Prefer the Reddit permalink as the headline link; include the product link separately when the post provides one. Do not infer launch status or capabilities from a title alone.
6. Deduplicate reposts and cross-posts about the same tool. Rank the remaining items by Reddit prominence and usefulness, not by the number of keyword matches. If none qualify, say so plainly.

## Response format

Start with `Reddit AI tools — <date> (<timezone>)` and one sentence describing the search scope. Then list up to 10 qualifying stories, each as:

- **[Post title](Reddit permalink)** — One sentence describing what the tool is and what is new, based on the post. Add `Product: [link]` when a product link is present.

Keep descriptions concise, distinguish the poster's claims from independently verified facts, and omit unsupported claims. If Reddit access or current ranking data is unavailable, explain the limitation and do not present search-engine results as Reddit's definitive top stories.
