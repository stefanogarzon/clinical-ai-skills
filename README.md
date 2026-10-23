# Clinical AI skills

Free [Claude](https://claude.ai) skills for clinicians doing research — built to use AI the careful way: the AI does the legwork, **you** make every decision, and nothing is cited without a source you can check.

By Stefano Garzon, interventional cardiologist ([@stefano_garzon](https://x.com/stefano_garzon)).

| Skill | What it does | Download |
|---|---|---|
| **sr-screening** | Systematic reviews: from the clinical question to a data-extraction table and PRISMA 2020 counts | [sr-screening.zip](skills/sr-screening.zip) |
| **claim-check** | One claim or question while you write: finds the evidence in PubMed, quotes the exact passage, keeps an Excel evidence table per manuscript | [claim-check.zip](skills/claim-check.zip) |

## Principles shared by all skills

- **Nothing excluded, cited or marked verified without you.** The AI proposes; you approve.
- **No number or quote without its source.** Every passage is checked by code against the article text — not typed from the AI's memory.
- **Contradicting evidence is shown, not hidden.**
- **It teaches as it goes**: PICO, search strings, where to export, how to get full texts.
- **You click, not type**: choices come as buttons and interactive pages beside the chat.

## Install (5 minutes)

1. Download the `.zip` of the skill (table above).
2. In Claude: **Settings → Capabilities** → turn on *Code execution and file creation*.
3. **Settings → Capabilities → Skills → Upload skill** → choose the zip.
4. Recommended: pick **Sonnet** in the model menu; for claim-check, also turn on the **PubMed** connector (Settings → Connectors).
5. Open a new chat and describe what you want to do.

Your progress lives in a file the skill gives you at the end of each session (`project.json` for sr-screening, an `.xlsx` for claim-check). Download it and upload it next time.

## sr-screening — systematic review screening

1. Frame the question (PICO) and testable eligibility criteria
2. Search strings for PubMed, Embase and Cochrane, explained; you run them and upload the exports
3. Import and de-duplication
4. Calibration: you screen ~40 records blind, the AI shows where it disagrees with you
5. Title/abstract and full-text screening in batches — RCT and outcome badges, highlighted evidence, you approve
6. Data extraction with page + verbatim quote for every value
7. Exports: extraction table (CSV/XLSX), PRISMA counts, decision log, RIS of included studies

Does not do meta-analysis, risk of bias, or dual independent screening.

## claim-check — evidence for one sentence

- **Claim mode** (*"exercise training reduces hospitalisation in HFpEF"*): articles that support, contradict or partially support it — contradicting ones first.
- **Question mode** (*"what is known about frailty in TAVI patients?"*): short summaries to pick from, then full text and exact passages.
- Per-manuscript Excel: claim, verdict, finding, verbatim passage, design/N, Vancouver reference, PMID/DOI, search used, Verified (only you), notes; plus a "Seen, not added" sheet for evidence you chose not to cite.
- Exports a Vancouver reference list and a DOI block for Zotero (*Add Item by Identifier*).

PubMed (and PubMed Central full text) only. A targeted search, not a systematic review.

## Limits

Usage limits of your Claude plan apply. The AI's confidence and summaries are labelled as AI output; the verbatim checks and your approval are what make the results trustworthy. These tools do not replace a methodologist.

## License

Code inside the zips: MIT ([LICENSE](LICENSE)). Skill text and documentation: CC BY 4.0 ([LICENSE-docs](LICENSE-docs)).
