# The Same Answer, Ten Different Stories

[![Runs](https://img.shields.io/badge/Runs-10-blue)](https://github.com/joedom99/chatgpt-repeatability-test)
[![Model](https://img.shields.io/badge/Model-GPT--5.6%20Sol-412991?logo=openai&logoColor=white)](https://openai.com/)
[![Tested](https://img.shields.io/badge/Tested-10%20Sept%202026-informational)](https://github.com/joedom99/chatgpt-repeatability-test)
[![Data](https://img.shields.io/badge/Data-CSV-150458?logo=pandas&logoColor=white)](runs.csv)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Blog](https://img.shields.io/badge/Blog-Marketing%20Data%20Science-teal)](https://blog.marketingdatascience.ai)

Supporting data for the article **"The Same Answer, Ten Different Stories: Non-Determinism in Generative AI Search"** on the [Marketing Data Science blog](https://blog.marketingdatascience.ai) by Joe Domaleski.

## What This Is

Last year I coined a marketing term. On the morning of September 10, 2026, I asked ChatGPT ten times who came up with it, using the same prompt in ten separate temporary chats, to see how much the answer would move.

All ten runs gave me credit. The evidence behind that credit changed almost every time.

The article explains what happened and what it means. This repository is the raw material behind it, so you can check my numbers or disagree with how I read a run.

## What's Inside

- `run-01.png` through `run-10.png` - all ten runs, unedited, in order
- `runs.csv` - how I coded each run
- Source and configuration screenshots

## The Prompt

```
Who originated the term "weighted average cost of marketing" and where did it first appear?
```

GPT-5.6 Sol at Medium reasoning effort. Ten temporary chats, memory off, custom instructions cleared, Fast answers disabled. All ten runs between 10:28 and 10:47 a.m. on September 10, 2026, from Fayette County, Georgia.

## The Runs

| Run | Time | Worked | Screenshot |
| --- | --- | --- | --- |
| 1 | 10:28:41 | 28s | [run-01.png](run-01.png) |
| 2 | 10:30:28 | 19s | [run-02.png](run-02.png) |
| 3 | 10:32:44 | 13s | [run-03.png](run-03.png) |
| 4 | 10:34:58 | 26s | [run-04.png](run-04.png) |
| 5 | 10:36:20 | 19s | [run-05.png](run-05.png) |
| 6 | 10:38:08 | 31s | [run-06.png](run-06.png) |
| 7 | 10:39:49 | 15s | [run-07.png](run-07.png) |
| 8 | 10:41:04 | 25s | [run-08.png](run-08.png) |
| 9 | 10:45:11 | 27s | [run-09.png](run-09.png) |
| 10 | 10:46:46 | 29s | [run-10.png](run-10.png) |

## A Note on Scope

Ten runs, one question, one model, one morning. Enough to show that repeatability is worth testing, not enough to say much about generative search in general. I am also testing a claim about my own work, which is why everything is posted here rather than summarized.

## Related Articles

- [Marketing Data Science blog](https://blog.marketingdatascience.ai) - the full article archive
- [Weighted Average Cost of Marketing (WACM)](https://blog.marketingdatascience.ai/weighted-average-cost-of-marketing-wacm-a-risk-adjusted-hurdle-rate-for-smarter-marketing-948b05e45186) - the article being tested here
- [SEO, AEO, and GEO: A Marketer's Guide to Search Visibility](https://blog.marketingdatascience.ai/seo-aeo-and-geo-a-marketers-guide-to-search-visibility-2f96b61ffa98) - the guide this experiment follows up on

## License

MIT. See [LICENSE](LICENSE).

## Author

**Joe Domaleski** - [Marketing Data Science](https://blog.marketingdatascience.ai) | [Medium](https://medium.com/@marketingdatascience) | [GitHub](https://github.com/joedom99)
