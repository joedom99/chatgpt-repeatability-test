# The Same Answer, Ten Different Stories: Non-Determinism in Generative AI Search

[![Runs](https://img.shields.io/badge/Runs-10-blue)](https://github.com/joedom99/chatgpt-repeatability-test)
[![Model](https://img.shields.io/badge/Model-GPT--5.6%20Sol-412991?logo=openai&logoColor=white)](https://openai.com/)
[![Tested](https://img.shields.io/badge/Tested-10%20Sept%202026-informational)](https://github.com/joedom99/chatgpt-repeatability-test)
[![Data](https://img.shields.io/badge/Data-CSV-150458?logo=pandas&logoColor=white)](runs.csv)
[![Verified](https://img.shields.io/badge/Verified-Internet%20Archive-orange)](https://web.archive.org/web/20240810202153/https://www.scoresandstats.com/expert-betting-guide/why-weighted-average-cost-of-marketing-is-an-important-kpi/)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-green.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Blog](https://img.shields.io/badge/Blog-Marketing%20Data%20Science-teal)](https://blog.marketingdatascience.ai)

Supporting data for the article **"The Same Answer, Ten Different Stories: Non-Determinism in Generative AI Search"** on the [Marketing Data Science blog](https://blog.marketingdatascience.ai) by Joe Domaleski.

## What This Is

Generated answers are stochastic. Everybody says so, and almost nobody shows you what that looks like on a question where the right answer is already known. This repository does that.

In May 2025 I published an article introducing a metric I call the **Weighted Average Cost of Marketing (WACM)**. On the morning of September 10, 2026, I asked ChatGPT who originated that term. Then I asked nine more times, in ten separate temporary chats, over **18 minutes**.

The headline conclusion never moved. Almost everything supporting it did.

- All **10 of 10** runs attributed the WACM framework to me
- All **10 of 10** cited the May 11, 2025 article specifically, not the publication home page
- The one piece of prior art in the story was described **five different ways**
- **3 of 10** runs assigned that page a publication date that does not hold up
- **0 of 10** runs resolved its actual chronology correctly
- Reported working time ranged from **13 seconds to 31 seconds**

No two runs used the same set of supporting sources.

Everything here is raw. If you want to check my numbers or disagree with how I coded a run, the screenshots are sitting next to the table.

## What's Inside

1. **Ten screenshots.** Every run, in order, unedited. `run-01.png` through `run-10.png`.
2. **The coded table.** `runs.csv`, one row per run, thirteen columns. This is what the article's figures are built from.
3. **Source evidence.** The listing card carrying the disputed date, the article page that carries no date, and the Internet Archive capture that settles it.
4. **Configuration evidence.** The ChatGPT settings in force for all ten runs, so "memory was off" is documented rather than asserted.

## The Prompt

Every run used this string, pasted identically:

```
Who originated the term "weighted average cost of marketing" and where did it first appear?
```

## Test Conditions

| Setting | Value |
| --- | --- |
| Model | GPT-5.6 Sol |
| Reasoning effort | Medium |
| Chat type | Temporary, one fresh chat per run |
| Saved memories | Off |
| Chat history reference | Off |
| Custom instructions | Cleared |
| Fast answers | Disabled |
| Location | Fayette County, Georgia |
| Window | 10:28 to 10:47 a.m., 10 Sept. 2026 |

Separate chats matter more than they sound. Asking the same question ten times inside one conversation lets the model see its own earlier answers, which measures consistency rather than repeatability.

## The Runs

| Run | Time | Worked | Prior reference | Opened by | Screenshot |
| --- | --- | --- | --- | --- | --- |
| 1 | 10:28:41 | 28s | mentioned, no date | earlier use | [run-01.png](run-01.png) |
| 2 | 10:30:28 | 19s | early 2025, from site archive | asking what I meant | [run-02.png](run-02.png) |
| 3 | 10:32:44 | 13s | not mentioned | crediting me | [run-03.png](run-03.png) |
| 4 | 10:34:58 | 26s | mentioned, no date | earlier use | [run-04.png](run-04.png) |
| 5 | 10:36:20 | 19s | dated March 12, 2025 | earlier use | [run-05.png](run-05.png) |
| 6 | 10:38:08 | 31s | cannot establish | crediting me | [run-06.png](run-06.png) |
| 7 | 10:39:49 | 15s | not mentioned | crediting me | [run-07.png](run-07.png) |
| 8 | 10:41:04 | 25s | dated March 12, 2025 | earlier use | [run-08.png](run-08.png) |
| 9 | 10:45:11 | 27s | mentioned, no date | crediting me | [run-09.png](run-09.png) |
| 10 | 10:46:46 | 29s | dated March 12, 2025 | earlier use | [run-10.png](run-10.png) |

## Key Results

| Quantity | Value |
| --- | --- |
| Runs | 10 |
| Attributed WACM to Domaleski | **10 / 10** |
| Cited the May 11, 2025 article at article level | **10 / 10** |
| Cited the publication home page instead | 0 / 10 |
| Distinct characterizations of the prior reference | **5** |
| Runs assigning it March 12, 2025 | 3 / 10 |
| Runs reporting it as undated | 3 / 10 |
| Runs not mentioning it at all | 2 / 10 |
| Runs estimating early 2025 from the site archive | 1 / 10 |
| Runs saying the chronology could not be settled | 1 / 10 |
| Runs that resolved the chronology correctly | **0 / 10** |
| Opened by crediting me | 4 / 10 |
| Opened with an earlier use of the phrase | 5 / 10 |
| Opened by asking what I meant | 1 / 10 |
| Referenced my June 8, 2025 follow-up article | 5 / 10 |
| Of those, gave a date | 3 / 5 |
| Reproduced the Modigliani and Miller (1958) citation | 1 / 10 |
| Working time, shortest | 13s |
| Working time, longest | 31s |
| Working time, mean | 23.2s |
| Runs sharing an identical source set | **0** |

Citation badge counts across all ten runs: Medium **10**, Scores And Stats **8**, Texas Tech **8**, USDA Library **2**, Penn State **1**.

## How the Coding Works

Each row in `runs.csv` records one run. The columns that need explaining:

| Column | Values |
| --- | --- |
| `scoresandstats_treatment` | `dated`, `mentioned_no_date`, `archive_inferred`, `cannot_establish`, `not_mentioned` |
| `opening_frame` | `credits_domaleski`, `earlier_use_first`, `disambiguation` |
| `citation_level` | `article` if the citation pointed to a specific piece, `root` if it pointed to the home page |
| `source_badges` | the citation badges shown in the response, semicolon separated |

The coding is mine and it involves judgment. The screenshots are here so you can disagree with it.

## What I Found When I Checked

The Scores and Stats article carries no byline and no publication date. The **March 12, 2025** date appears on the section index page that lists it, alongside four other marketing articles carrying the same date, above images stored in 2021 and 2023 upload directories. That points to a migration or re-indexing timestamp, not a publication date.

The Internet Archive holds one capture of the page, dated **August 10, 2024**, which puts it online nine months before my article. A capture proves a page existed by that date. It does not establish when the page was first published.

No run identified this. Nothing was fabricated. Every figure reported came from a page that had actually been retrieved. The failure was interpretation, and the evidence needed to catch it sat on the same screen as the date.

One detail that looks like an error and is not: my blog runs on Medium with a custom domain, so citation badges display a Medium icon. The links resolve to `blog.marketingdatascience.ai`. The icon is a rendering artifact, not an attribution error.

## Limitations

Ten runs, one question, one model, one morning, one location. That is enough to show repeatability is worth testing and not enough to make claims about generative search in general.

I am also measuring a claim about my own work, which is a conflict of interest. That is the reason everything is published here rather than summarized.

A chat interface shows which sources made it into the answer. It does not show which were retrieved and then set aside. A follow-up study using the API will address that.

## Related Articles

- [Marketing Data Science blog](https://blog.marketingdatascience.ai) - the full article archive
- [Weighted Average Cost of Marketing (WACM): A Risk-Adjusted Hurdle Rate for Smarter Marketing Investments](https://blog.marketingdatascience.ai/weighted-average-cost-of-marketing-wacm-a-risk-adjusted-hurdle-rate-for-smarter-marketing-948b05e45186) - the article whose attribution is being tested here
- [Is It Worth It? How to Run a Cost-Benefit Analysis for Better Marketing Decisions](https://blog.marketingdatascience.ai/is-it-worth-it-how-to-run-a-cost-benefit-analysis-for-better-marketing-decisions-5a8dd38216e2) - the June 8, 2025 follow-up that five runs referenced
- [SEO, AEO, and GEO: A Marketer's Guide to Search Visibility](https://blog.marketingdatascience.ai/seo-aeo-and-geo-a-marketers-guide-to-search-visibility-2f96b61ffa98) - the guide that argued a single prompt run is an anecdote, which this test checks
- [Essential Marketing Analytics for Small Businesses](https://blog.marketingdatascience.ai/essential-marketing-analytics-for-small-businesses-a-guide-to-what-really-matters-68ed6f5e26a6) - what to track when you are starting from nothing
- [When the Numbers Look Wrong: A Marketer's Guide to Anomaly Detection](https://blog.marketingdatascience.ai/when-the-numbers-look-wrong-a-marketers-guide-to-anomaly-detection-3895e22f2fe7) - what to do when a measurement moves and you do not know why

## License

Documentation and coded data in this repository are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Screenshots are of ChatGPT output, included for verification and commentary.

## Author

**Joe Domaleski** - [Marketing Data Science](https://blog.marketingdatascience.ai) | [Medium](https://medium.com/@marketingdatascience) | [GitHub](https://github.com/joedom99)
