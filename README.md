# Daily FT Market Briefing — n8n (Gmail Edition)

This variant sends the AI‑summarized FT.com market briefing via **Gmail** instead of Outlook.
Built on **n8n** with **Google Gemini** summarization and a **Gmail** send node.

## What changed vs Outlook version
- Replaced the *Microsoft Outlook* node with the **Gmail** node (`n8n-nodes-base.gmail`)
- Credential name expected: **Gmail account**
- Works with Gmail OAuth2 in n8n

## Quick start
1. Open n8n (Cloud or self-hosted)
2. **Import** → `workflow/ft-daily-market-briefing-gmail.workflow.json`
3. Set credentials:
   - Gemini API key → `Google Gemini(PaLM) Api account`
   - Gmail OAuth2 → `Gmail account`
4. In the **Gmail node**, set **To:** your Gmail address
5. Run once to test, then toggle **Active**

## Notes
- Subject defaults to **"Financial news from today."**
- HTML body is pulled from the previous AI node as `summaryHtml` (fallbacks included)
- Respect FT.com terms and fair‑use; use for personal briefing only

