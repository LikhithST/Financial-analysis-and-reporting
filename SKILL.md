---
name: indian-financial-analysis
description: Write, structure, and format notes on Indian financial analysis and reporting — equity research notes, company/sector analysis, quarterly results commentary, financial statement summaries, and ratio analysis for Indian companies. Use this whenever the user asks to analyze an Indian company or sector, summarize Indian quarterly/annual results, write an equity/credit research note, interpret Ind AS financial statements, or produce any financial reporting note involving Indian conventions (INR lakhs/crores, Indian fiscal year, Schedule III formats, SEBI/RBI/Ind AS references). Make sure to use this skill even if the user just pastes numbers from an Indian company's results and asks for "notes" or "analysis," or mentions BSE/NSE, Nifty/Sensex, or any Indian ticker.
---

# Indian Financial Analysis & Reporting Notes

A skill for producing analyst-quality notes on Indian companies, sectors, and financial statements, following Indian market conventions rather than US/global defaults.

## Core conventions to always apply

These are the details that most commonly get defaulted wrong (to US conventions) if not deliberately applied.

### 1. Number formatting — lakhs and crores
- Indian financial reporting uses the **lakh (1,00,000)** and **crore (1,00,00,000 = 10 million)** system, not thousands/millions.
- Use Indian digit grouping: `1,23,45,678` not `12,345,678`.
- Default unit for company financials: **₹ crore** (large caps) or **₹ lakh** (smaller companies/SMEs). State the unit explicitly in every table header — never leave it implicit.
- When converting between systems for clarity: 1 crore = 10 million; 1 lakh = 100,000. Show both if the audience may be non-Indian.
- Currency symbol: ₹ or "Rs." — be consistent within a document. Use "INR" in cross-currency contexts.

### 2. Fiscal year
- Indian fiscal year (FY) runs **1 April to 31 March**. FY24 = April 2023–March 2024 (confirm with user which convention they mean, as some write FY23 for the same period — always state your convention once at the top of the note).
- Quarters: Q1 (Apr–Jun), Q2 (Jul–Sep), Q3 (Oct–Dec), Q4 (Jan–Mar). Q4 and full-year results are typically reported together in April/May.
- Always label quarters clearly, e.g. "Q3FY25" or "3QFY25" (Oct–Dec 2024).

### 3. Accounting & reporting framework
- Listed Indian companies report under **Ind AS** (Indian Accounting Standards, converged with IFRS). Smaller/unlisted companies may still use **Indian GAAP**. Note which applies.
- Financial statements follow **Schedule III of the Companies Act, 2013** format (Division I for Ind AS-compliant companies, Division II for others) — this dictates line-item ordering and terminology (e.g., "Other Comprehensive Income," "Exceptional Items" shown separately below operating profit).
- Banks/NBFCs follow RBI-prescribed formats, not Schedule III — flag this distinction if analyzing a financial-sector company.
- Common India-specific line items to recognize: Other Income (often significant — separate operating vs non-operating), Exceptional/Extraordinary Items, Minority Interest (Non-Controlling Interest), Deferred Tax, GST-related adjustments (revenue is typically reported net of GST post-2017, unlike pre-GST excise-inclusive figures — flag if comparing across FY18 boundary).

### 4. Key regulators and reference points
- **SEBI** — market regulator (listing, disclosure, insider trading, mutual funds).
- **RBI** — banking/NBFC regulator, monetary policy, repo rate.
- **MCA** — Companies Act compliance, Schedule III.
- **ICAI** — sets Ind AS/accounting standards.
- Stock exchanges: **NSE** (Nifty 50 benchmark) and **BSE** (Sensex benchmark). Always name the exchange when quoting a price or market cap.
- Corporate tax rate context: mention the applicable regime only if tax analysis is central (rates change by budget year — verify current rate via search rather than assuming).

## Structure for a standard equity/company note

Unless the user specifies otherwise, structure notes as:

1. **Snapshot** — Company name, sector, exchange/ticker (NSE/BSE), CMP (current market price), market cap (₹ cr), FY/quarter being discussed.
2. **Headline numbers** — Revenue, EBITDA, EBITDA margin, PAT (Profit After Tax), EPS — each with YoY and QoQ change. Present as a table.
3. **Segment/business commentary** — Break down by segment if disclosed (common for conglomerates, IT services, banks).
4. **Key ratios** — Prefer ratios used in Indian analyst convention:
   - EBITDA margin, PAT margin
   - RoE, RoCE (RoCE especially favored in Indian analysis over RoIC)
   - Debt/Equity, Interest Coverage
   - For banks: NIM (Net Interest Margin), GNPA/NNPA (Gross/Net Non-Performing Assets), CASA ratio, CRAR/CAR
   - Valuation: P/E, P/B, EV/EBITDA — mention if trailing (TTM) or forward
5. **Drivers/commentary** — Management commentary highlights, one-offs/exceptional items called out separately, guidance if given.
6. **Risks/watch items** — Regulatory, commodity, currency (especially USD/INR for IT/pharma exporters or import-heavy sectors), monsoon (for rural-facing consumer/agri names) as relevant.
7. **Note on sourcing** — If figures came from a results PDF/press release/exchange filing, name the source and date.

Adapt or drop sections the user doesn't need — this is a default scaffold, not a rigid template.

## Ratio formulas (Indian-context defaults)

| Ratio | Formula | Notes |
|---|---|---|
| EBITDA Margin | EBITDA / Revenue from Operations | Use "Revenue from Operations," excludes Other Income |
| RoE | PAT / Average Shareholders' Equity | Average of opening+closing, or state if using closing only |
| RoCE | EBIT / Capital Employed | Capital Employed = Total Assets − Current Liabilities |
| NIM (banks) | Net Interest Income / Average Interest-Earning Assets | Annualize if quarterly |
| GNPA Ratio | Gross NPAs / Gross Advances | Asset quality metric, closely watched |
| CRAR | Total Capital / Risk-Weighted Assets | RBI minimum thresholds apply |

## Write for an accounting beginner

Assume the reader has no formal accounting background. This changes how terms and numbers are handled, not how rigorous the analysis is — don't dumb down the substance, just make it accessible:

- **Define every technical term on first use**, briefly and in plain words, right where it appears — not in a separate glossary the reader has to jump to. E.g., "EBITDA (profit before interest, tax, depreciation, and amortization — a rough measure of core operating profit)".
- **Expand every acronym on first use**: "RoE (Return on Equity)", "GNPA (Gross Non-Performing Assets — loans the bank isn't collecting on)", "YoY (year-on-year, i.e. vs. the same period last year)".
- **Explain what a ratio *means*, not just its formula.** After giving a ratio, add a one-line plain-English read: "RoE of 18% means the company generates ₹18 of profit for every ₹100 shareholders have invested."
- **Say whether a number is good, bad, or normal**, with a quick reason — a beginner can't tell if "GNPA of 3.2%" is fine or alarming without context (e.g., "below the ~5% level regulators watch closely").
- **Avoid stacking jargon in one sentence.** If a sentence needs 3+ defined terms, break it into two sentences so each new idea lands separately.
- **Use small analogies where they help**, especially for structural concepts (e.g., explain "Other Comprehensive Income" as "gains/losses the company made but hasn't 'cashed in' yet, so they're kept separate from normal profit").
- Keep the lakh/crore, Ind AS/Schedule III, and other India-specific conventions from above — but explain them too, since a beginner (Indian or not) may not know them either. E.g., "1 crore = ₹1,00,00,000 = 10 million."
- It's fine for the note to run slightly longer than a pure-expert version to fit these explanations — but keep them tight (one clause or one short sentence per term), not full paragraphs, to preserve the README's scannability.

## Writing style

- Be precise about whether a change is **YoY** (year-on-year) or **QoQ** (quarter-on-quarter) — never mix without labeling.
- State assumptions explicitly (e.g., "assuming FY24 = Apr 2023–Mar 2024").
- Don't invent numbers — if the user hasn't provided a figure and it's not something you can verify, flag it as unavailable rather than estimating silently.
- For anything time-sensitive (current stock price, latest repo rate, current tax rates, recent regulatory changes), search rather than rely on memory — these change frequently and Claude's training data may be stale.
- Keep tone neutral and analytical, in line with sell-side/buy-side research conventions — flag both positives and risks, avoid one-sided framing.

## Output format: write notes as a README.md

Default deliverable for this skill is a single **`README.md`** file per company/note, not a `.docx` or loose in-chat text. Follow efficient, scannable README conventions — the kind a reader skims in 30 seconds before deciding whether to read in full:

- **Title line** — `# CompanyName — FY/Quarter Note` as the single H1.
- **One-line summary** immediately under the title in italics: the single most important takeaway (e.g., *"Revenue beat, margins missed — flag input cost pressure."*).
- **At-a-glance table** near the top: CMP, Market Cap, Exchange, Rating/View if applicable — so the reader doesn't have to hunt for basics.
- **Table of contents** only if the note has 5+ sections; skip it for short notes (unnecessary TOC is noise, not efficiency).
- **Short sections with H2 (`##`) headers**, one topic each — Snapshot, Headline Numbers, Segment Commentary, Ratios, Risks, Sourcing (per the note structure above). No nested H4/H5 unless the section is genuinely long.
- **Tables over prose** for any numeric comparison (YoY/QoQ figures, ratios) — a table of 5 numbers beats a paragraph describing them.
- **Bullets over paragraphs** wherever a list of discrete points is being made (risks, drivers, guidance items). Reserve full paragraphs for actual narrative/analysis that doesn't decompose into a list.
- **Bold the number, not the sentence** — e.g., "Revenue grew **18% YoY** to **₹1,240 cr**" rather than bolding whole sentences, so a skim-reader's eye catches the figures.
- **No filler language** — cut throat-clearing phrases ("It is important to note that…", "In conclusion…"). Every line should carry information.
- **Code-block/quote callouts are not used** here (this isn't a technical README) — use blockquotes (`>`) sparingly, only for direct management-guidance quotes, and keep each under a sentence.
- End with a **Sourcing** line (small, italic) naming where the figures came from and as-of date — the README equivalent of a footer/license line.

Keep the whole file tight: prefer one screen-scroll per major section. If a note is ballooning past ~150 lines, that's a signal to push detail into a linked appendix table rather than keep expanding the main body.

## Producing the file

Create the note as an actual `README.md` file (via file creation tools) rather than only replying in chat, unless the user explicitly asks for an in-chat answer. Save it and present it to the user rather than pasting the full contents inline — the file *is* the deliverable.