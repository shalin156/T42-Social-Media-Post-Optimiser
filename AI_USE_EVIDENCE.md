# AI Use Evidence — T42 Social Media Post Optimiser

This file documents how ChatGPT was used during the T42 project. It is a project evidence record derived from the completed workbook's `AI Use Log`; it is **not** a fabricated URL and it is **not** presented as a verbatim exported chat transcript.

## Project

- **Task:** Social Media Post Optimiser
- **Dataset:** 250 social posts
- **AI tool used:** ChatGPT (GPT-5.6 Sol)
- **Verification method:** Spreadsheet calculations and pivot-style summaries in the completed workbook
- **Human review:** AI suggestions were accepted, revised, or rejected after numerical verification

## Verified headline results

| Item | Verified result |
|---|---:|
| Overall average engagement rate | 7.57% |
| Best format for engagement efficiency | Carousel — 8.08% |
| Best topic | Founder story — 8.11% |
| Best exact posting hour | 17:00 — 9.05% (n=12) |
| Best broad posting window | 12:00–16:59 — 7.75% |
| Best format for raw scale | Reel — 22,449 avg reach; 1,715 avg engagements |

## AI interaction record

### 1. High reasoning; attached workbook
**Prompt used**  
Analyse the attached T42 social media post optimiser workbook, identify its structure, required deliverables and any risks before editing it.

**What the AI output did well / badly**  
Correctly identified 250 posts, the required outputs and the minimum 15-entry AI-use log.

**What was changed or verified next**  
Moved from workbook structure to metric design so the analysis would not confuse reach with engagement.

**Decision:** Kept

### 2. Spreadsheet analysis
**Prompt used**  
Define a defensible engagement metric using the available columns: reach, likes, comments, shares and link clicks.

**What the AI output did well / badly**  
Proposed total engagement = likes + comments + shares + link clicks and engagement rate = total engagement / reach.

**What was changed or verified next**  
Kept both raw engagement and engagement rate because each answers a different business question.

**Decision:** Kept

### 3. Verification pass 1
**Prompt used**  
Rank formats by raw engagement per post only and explain the winner.

**What the AI output did well / badly**  
Reels appeared strongest because they had the highest average raw engagement.

**What was changed or verified next**  
Rejected raw-only ranking because reels also have much higher reach; normalized by reach next.

**Decision:** Rejected

### 4. Verification pass 2
**Prompt used**  
Re-rank formats using average engagement rate and weighted engagement rate, and compare the result with the raw-engagement ranking.

**What the AI output did well / badly**  
Showed Carousel as the best engagement-efficiency format while Reel remained best for scale.

**What was changed or verified next**  
Kept the two-metric interpretation to avoid a misleading single winner.

**Decision:** Kept

### 5. Pivot-style aggregation
**Prompt used**  
Calculate post count, average reach, average engagement, average engagement rate and weighted engagement rate for every topic.

**What the AI output did well / badly**  
Identified Founder story as the strongest topic on average engagement rate with a meaningful sample.

**What was changed or verified next**  
Used sample count in the final recommendation instead of ranking percentages without context.

**Decision:** Kept

### 6. Time analysis
**Prompt used**  
Group posting times into practical dayparts and compare engagement rates; also round timestamps and check exact hours separately.

**What the AI output did well / badly**  
Found 17:00 as the best exact observed hour (9.05%, n=12) and Afternoon as the best broad window (7.75%).

**What was changed or verified next**  
Used the exact 17:00 result for the test playbook and kept the broad afternoon window as a fallback; documented the smaller hour-level sample.

**Decision:** Kept

### 7. Robustness check
**Prompt used**  
Find the best format-topic-time combination, but require a minimum sample size so a tiny cell does not become the main rule.

**What the AI output did well / badly**  
Best combination with at least five posts was Carousel + Founder story + Night, but only n=5.

**What was changed or verified next**  
Rejected it as the permanent rule and preferred stronger factor-level evidence for the default playbook.

**Decision:** Rejected

### 8. LLM explanation
**Prompt used**  
Explain in business language why carousel, founder-story and afternoon patterns might occur, without claiming causation.

**What the AI output did well / badly**  
Produced plausible explanations around dwell time, narrative connection and browsing breaks.

**What was changed or verified next**  
Added a pivot-verification column so every explanation is explicitly checked against the data.

**Decision:** Kept

### 9. Content generation round 1
**Prompt used**  
Generate 10 new social posts that follow Carousel + Founder story + 17:00 and use products already present in the dataset.

**What the AI output did well / badly**  
Generated usable concepts but some drafts were too generic.

**What was changed or verified next**  
Added stronger hooks, slide-by-slide carousel structure and a single clear CTA to each draft; kept 17:00 as a test schedule rather than a causal rule.

**Decision:** Rejected

### 10. Content generation round 2
**Prompt used**  
Rewrite the 10 posts so each has a specific founder decision, problem or trade-off, a 5-7 slide structure and one measurable CTA.

**What the AI output did well / badly**  
Drafts became more concrete, scannable and directly usable by the social team.

**What was changed or verified next**  
Kept them but marked every post as AI draft requiring human review.

**Decision:** Kept

### 11. Rules-card design
**Prompt used**  
Turn the verified analysis into a one-page posting-rules card with default rules, scale rules, do/avoid guidance and a next A/B test.

**What the AI output did well / badly**  
Converted analytics into a practical operating card with thresholds and caveats.

**What was changed or verified next**  
Added exact percentages and sample-size cautions so the rules are auditable.

**Decision:** Kept

### 12. Working build
**Prompt used**  
Design a transparent spreadsheet-based post optimizer that lets a user choose format, topic and posting window and returns historical engagement-rate scores.

**What the AI output did well / badly**  
Created an explainable rule-based scoring concept instead of an opaque prediction.

**What was changed or verified next**  
Added a clear note that the composite score is a heuristic, not causal or machine-learning output.

**Decision:** Kept

### 13. Responsible AI review
**Prompt used**  
List the main limitations and responsible-AI checks needed before the social team uses these results.

**What the AI output did well / badly**  
Flagged synthetic data, observational bias, confounding, small cells and the need to review AI-written claims.

**What was changed or verified next**  
Integrated these limits into the dashboard, rules card and report rather than leaving them as a footnote.

**Decision:** Kept

### 14. Final verification
**Prompt used**  
Cross-check all headline numbers in the engagement analysis against the pivot tables and flag any contradiction.

**What the AI output did well / badly**  
Confirmed the main winners and identified the important Reel scale-vs-rate distinction.

**What was changed or verified next**  
Kept both metrics and avoided saying Reels were simply better or worse overall.

**Decision:** Kept

### 15. Submission packaging
**Prompt used**  
Prepare the project for GitHub with a completed workbook, concise README and a 3-5 page report that explains method, verification, recommendations and reflection.

**What the AI output did well / badly**  
Created a clear deliverable structure aligned with the rubric.

**What was changed or verified next**  
Added a repository evidence file documenting the actual AI prompts, verification steps and final decisions.

**Decision:** Kept

## Verification and responsible-use notes

- Numerical conclusions were not accepted purely because the LLM stated them; they were checked against workbook calculations.
- Raw engagement and engagement rate were kept separate because reach strongly affects absolute engagement totals.
- Small-sample combinations were not promoted to permanent rules simply because they had a high percentage.
- Timestamp floating-point drift was corrected before extracting the best exact posting hour.
- AI-generated post copy is treated as draft content requiring human review before publication.
- The dataset is synthetic and observational, so the results show association rather than causation.

## Repository evidence mapping

- `T42_Social_Media_Post_Optimiser_Completed.xlsx` → full `AI Use Log`, analysis, pivots, drafts, rules card and working optimizer.
- `T42_Social_Media_Post_Optimiser_Report.pdf` → concise explanation of method, results and limitations.
- `AI_USE_EVIDENCE.md` → this documented AI-use record.
