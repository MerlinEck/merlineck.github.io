---
layout: post
title: "Stop paying AI to rewrite the wheel"
description: "Companies aren't overspending on AI because the tools are too capable. They're paying it to rebuild the same work from scratch, over and over."
---

Companies aren't overspending on AI because the tools are too capable. They're overspending because they pay the AI to rebuild the same work from scratch, over and over.

The headlines this year tell the story. Companies on enterprise ChatGPT and Claude plans have started capping employees at $50 to $200 a month. Hit the limit and you're locked out until an admin approves more budget or the next month starts, and some employees hit it 15 days in ([GAI Insights](https://gaiinsights.substack.com/p/companies-are-implementing-monthly)). Accenture's Chief AI and Data Officer, Lan Guan, says clients "hit this unexpected cost wall" when they try to scale AI. Employees default to the most powerful, most expensive models, and "that single behavior, multiplied across a workforce, is where consumption costs quietly balloon" ([Fortune](https://fortune.com/2026/07/29/cfo-hitting-cost-wall-ai-tokens-accenture/)). Across the market, the message from CFOs is the same: ration the tokens.

Rationing treats the symptom. The cause is how we deploy these tools. We've reached the point on the maturity curve where "the AI can do it from scratch" has quietly become "the AI does it from scratch, every time, for every user." At scale, that is a very expensive habit.

## You don't build decks from scratch, why should AI?

Think about the last time you made a PowerPoint presentation yourself. You almost certainly didn't start from a blank slide.

- For the weekly status deck, you opened last week's file and updated the numbers and saved it as vFinalThisWeek12.pptx.
- For the quarterly town hall, you copied last quarter's presentation and swapped in the new highlights.
- For something truly new, you still started from the company template or a similar deck you had on hand, not a blank slide.

We reuse because rebuilding is slow. Yet when we hand the same job to generative AI, we often ask it to start from a blank page every time. Just because the tool can generate a full presentation from scratch doesn't mean that's what you wanted it to do.

## A deck is two things: content and presentation

Every presentation has two parts:

- Content is the substance: this week's numbers, the risks, the decisions, the story. It changes every time.
- Presentation is the container: the layout, the brand colors, the fonts, the chart styles, the slide order. It barely changes at all.

When an AI builds a deck from scratch, most of the effort goes into the presentation. The model writes code to lay out slides, reads formatting guidance, renders the result, and inspects it to fix overlaps and alignment. All of that consumes tokens. Then it does it again next week, for an identical layout.

The content, the part that actually needs intelligence, is often the smallest piece of the job.

## Plugins: mail merge for the AI era

The fix is an idea most offices have used for decades: mail merge. Keep the layout fixed, and only produce the part that changes.

Plugins make this practical for AI. A plugin can bundle more than instructions. It can carry scripts, reference material, and assets. For a weekly status deck, that means:

1. The template lives in the plugin as an asset: your branded deck with its layout already built.
2. A fill script maps structured content (say, a short JSON or Markdown file) onto the right slides and placeholders.
3. The AI writes only the content: this week's summary, numbers, risks, and next steps.

The script does the presentation work deterministically, the same way every time, at almost no token cost. The model spends its effort where judgment matters. The output is also more consistent, because the layout can't drift from week to week.

This isn't limited to decks. Monthly reports, client briefs, proposals, and SOPs all have the same split between a stable structure and changing content.

## Taking it further

Now the presentation is handled by a script, there are two more potential ways to reduce tokens.

Make the inputs deterministic too. In a status deck, gathering the data often costs more tokens than writing the slides. If a script or connector query **pulls the metrics directly**, the model doesn't have to search, read, and interpret raw sources each week. It only writes the narrative around numbers it's handed.

Route the remaining work to the **right model**. Filling a known structure is routine work, and routine work doesn't need a frontier model. Flagship models can cost about five times as much per token as their smaller siblings. They're usually slower, too. Anthropic rates its small Claude Haiku model "Fastest" and its flagship Claude Opus "Moderate" for latency ([Anthropic](https://platform.claude.com/docs/en/about-claude/models/overview)), and OpenAI tells developers to default to its flagship only "if cost and latency aren't a concern" ([OpenAI](https://developers.openai.com/api/docs/guides/model-selection)).

## The catch: someone has to own the plugins

This approach isn't free. It moves cost from tokens to maintenance, and that trade only pays off if it's managed.

- Templates need upkeep. When the brand changes or a team adds a new metric, the template and the fill script have to change with it.
- Scripts are code. A plugin that runs a script is executing code on someone's machine. That code needs review, versioning, and a clear owner, just like any other software in the organization.
- Someone has to spot the patterns. Most users won't recognize which of their tasks are repeatable enough to deserve a plugin. That takes a team looking across the organization, not individuals optimizing alone.

In other words, reusable plugins only save money if someone curates them. That's the governance question, I am thinking so much about right now, and will be the subject of a future post.

## Stop paying for the blank page

Cutting AI budgets is a blunt instrument. It makes everyone use the tools less, including for the work where they create real value.

The better move is to ask, for each recurring task: what part actually changes? Build that part with AI. Build everything else once, as a template and a script, and reuse it.

Start small. Pick the one report or deck your team rebuilds most often, and turn it into a plugin. Then compare the token cost of next month's version with last month's.

## Sources

- [Companies Are Implementing Monthly $ Limits for Claude and ChatGPT](https://gaiinsights.substack.com/p/companies-are-implementing-monthly), Paul Baier, GAI Insights, August 29, 2026
- [Models overview](https://platform.claude.com/docs/en/about-claude/models/overview), Claude Developer Platform documentation, Anthropic, accessed November 10, 2026
- [Model selection](https://developers.openai.com/api/docs/guides/model-selection), OpenAI API documentation, OpenAI, accessed November 10, 2026
- [CFOs are hitting a 'cost wall' on AI](https://fortune.com/2026/07/29/cfo-hitting-cost-wall-ai-tokens-accenture/), Sheryl Estrada, Fortune, July 29, 2026
