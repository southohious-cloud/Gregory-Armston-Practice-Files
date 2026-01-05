# Business Automation Workflows

## 1. Lead Intake & Research Workflow
**Triggers:** New entry in Google Sheets or Typeform.
1.  **Extraction:** Scrape the lead's website URL using `utils/scraper.py`.
2.  **Analysis:** Pass data to `Research Agent` (via `PROMPTS.md`).
3.  **Action:** If lead fits "Target Profile," draft a personalized email.
4.  **Logging:** Save result to `data/outreach_log.csv`.

---

## 2. Meeting-to-Task Pipeline
**Triggers:** New `.mp3` or `.txt` file uploaded to `/data/transcripts`.
1.  **Summarization:** `Summary Agent` extracts action items.
2.  **Assignment:** Identify who is responsible for each task.
3.  **Integration:** Push tasks to Trello or Notion API.
