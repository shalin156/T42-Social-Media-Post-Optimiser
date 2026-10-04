# T42 - Social Media Post Optimiser

AI-Powered Developer Tools mini project using the supplied 250-row synthetic social-media dataset.

## Project objective

The project identifies which **post format, topic, and posting time** are associated with stronger engagement, asks an LLM to explain the patterns, verifies the explanations with spreadsheet calculations, generates 10 new posts from the winning pattern, and converts the findings into a practical posting-rules card.

## Engagement metric

- **Total engagement** = Likes + Comments + Shares + Link Clicks
- **Engagement rate** = Total engagement / Reach
- **Weighted engagement rate** = Sum of engagement / Sum of reach

The project separates **engagement efficiency** from **raw scale** so high-reach posts do not automatically appear better.

## Verified findings

| Question | Result | Evidence |
|---|---:|---:|
| Overall average engagement rate | **7.57%** | 250 posts |
| Best format for engagement efficiency | **Carousel - 8.08% ER** | 61 posts |
| Best topic | **Founder story - 8.11% ER** | 34 posts |
| Best exact posting hour | **17:00 - 9.05% ER** | 12 posts |
| Best broad posting window | **12:00-16:59 - 7.75% ER** | 42 posts |
| Best weekday (bonus) | **Wednesday - 8.46% ER** | 31 posts |
| Best format for raw scale | **Reel** | 22,449 avg reach; 1,715 avg engagements |

### Recommended test pattern

**Founder Story + Carousel + 17:00**, preferably on Wednesday.

The 17:00 finding is treated as a **test hypothesis**, not a causal law. If the team needs a broader scheduling window, **12:00-16:59** is the strongest broad bucket.

## Workbook contents

The completed workbook contains:

- `Task Brief` - original assignment brief and rubric
- `Posts` - original 250-row dataset
- `Data Dictionary` - original column dictionary
- `AI Use Log` - 15 documented AI-use / iteration entries
- `Analysis Data` - derived engagement metrics, rounded hour, time bucket and weekday
- `Engagement Analysis` - KPI dashboard, verified winners, LLM-vs-pivot checks and charts
- `Pivot Verification` - detailed verification tables for format, topic, time, platform, weekday and combinations
- `New Post Drafts` - 10 AI-assisted posts using the winning factor pattern
- `Posting Rules` - one-page operating card for the social team
- `Post Optimizer` - interactive dropdown-based rule scorer / working build

## Working build

Open the `Post Optimizer` sheet and select:

1. Format
2. Topic
3. Exact posting hour

The workbook returns the historical engagement rate for each factor, lift versus the 7.57% baseline, a transparent composite score, and a recommendation.

> The score is an explainable historical heuristic, not a causal or machine-learning forecast.

## AI verification approach

The analysis used the LLM for pattern explanations and draft generation, but accepted numerical claims only after checking them against spreadsheet calculations. Important iteration steps included:

- Rejecting a raw-engagement-only ranking because it unfairly favoured high-reach Reels.
- Re-ranking with engagement rate, which identified Carousel as the efficiency winner.
- Rejecting a five-post three-factor cell as too small to become a permanent rule.
- Correcting Excel timestamp floating-point drift before extracting posting hours, preventing intended 17:00 posts from being misclassified.

## Responsible AI and limitations

- Dataset is synthetic and contains only 250 posts.
- Results show association, not causation.
- Platform algorithm, audience, product, season, campaign objective and creative quality can confound results.
- AI-generated posts are labelled as drafts and require human review.
- Product, health, safety and performance claims must be verified before publication.

## Repository files

- `T42_Social_Media_Post_Optimiser_Completed.xlsx` - main working build and deliverables
- `T42_Social_Media_Post_Optimiser_Report.pdf` - 5-page submission report
- `T42_Social_Media_Post_Optimiser_Report.docx` - editable report source
- `README.md` - repository documentation
- `AI_USE_EVIDENCE.md` - documented AI prompts, verification decisions and human changes

## Before final submission

1. Open the workbook once in Microsoft Excel and confirm the `Post Optimizer` dropdowns recalculate normally.
2. Keep `AI_USE_EVIDENCE.md` in the same GitHub repository; the workbook's `AI Use Log` already points to it.
3. Upload the workbook, report files, `README.md`, and `AI_USE_EVIDENCE.md` to GitHub.
4. Confirm the repository visibility required by your faculty and copy the GitHub repository link into the submission form.
