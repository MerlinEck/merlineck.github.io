---
title: "Someone has to curate the plugins"
description: "AI assistants pay off when a company runs its own curated plugins, built around its processes and integrations, behind a gateway that keeps malicious and fragile public plugins out."
status: drafting
idea: someone-has-to-curate-the-plugins
register: long-form
---

## Brief

The follow-on to "Stop paying AI to rewrite the wheel", which promised a post on who curates the plugins. For people who decide how their company rolls out [Copilot](https://www.microsoft.com/en-us/copilot), [Claude](https://claude.com/product/overview), [ChatGPT](https://chatgpt.com/) or [Cohere](https://cohere.com/). Takeaway: the value is in your own plugins, built around your processes and integrations, and they need a gateway in front of them. Ends with the plugin toolkit as proof that the gateway can be cheap to run. Sources section only for what you actually cite.

## Thesis

For the effective use of AI assistants like [Copilot](https://www.microsoft.com/en-us/copilot), [Claude](https://claude.com/product/overview), [ChatGPT](https://chatgpt.com/) and [Cohere](https://cohere.com/), an enterprise needs its own curated plugins, built with the company's processes and integrations in mind, behind a gateway that protects the firm from malicious skills, scripts or plugins and minimizes the supply chain and business continuity risks of public plugins the business starts to rely on.

## Outline

1. **Hook**
   - Last week's promise: reusable plugins only save money if someone curates them
   - The review run in the hero image: two agents, four reviewer roles each, five major hardening findings in the scripts

2. **Public plugins only get you halfway**
   - Generic plugins don't know your templates, systems or approval steps
   - The savings from last week come from company-specific plugins (the status deck)

3. **A plugin is code you let in**
   - Plugins run scripts on employees' machines
   - Malicious skills, scripts or plugins; unpinned or abandoned dependencies

4. **The day the public plugin disappears**
   - Teams quietly come to rely on a plugin someone else maintains
   - It changes, breaks or vanishes: a business continuity risk, not just a security one

5. **The gateway**
   - One curated marketplace as the only source
   - Nothing gets in without a house-rules review and a security review
   - Every plugin has an owner and a version

6. **What it looks like in practice: my plugin toolkit**
   - Build, review, security-review, eval, release in one plugin
   - Blind panels: reviewers don't see each other's results
   - The hero-image run: house rules clean, security found five major issues in the scripts

7. **Close**
   - Curation is the cost that makes reuse pay
   - [Match how your posts usually close: last week ended on "start small" and one concrete step]

## Personal angle to fill in

- [ ] Which plugin the hero-image review run was for, and what the five script findings actually were
- [ ] A number: how many plugins are in your marketplace, or how many issues the reviews have caught
- [ ] One thing you got wrong: a plugin or script you would have shipped without the review

## LinkedIn hooks

- [Hook idea: a first line under about 210 characters]
- [Hook idea: a different kind of first line]

## Actual Article

Plugins can be powerful levers for process improvement, but that power comes with responsibility. Last week I wrote about using plugins to stop paying AI to rebuild the same deck every week, and I ended with a promise: a follow up post . This is that post.

By plugins I mean what I described last week: a package that bundles instructions with scripts, reference material and assets. Your vendor might call it an agent, an app or a skill. Whatever the name, the curation question is the same.

## Instructions are modern code and have to be treated as such

A plugin carries two things that act on your behalf: scripts the computer runs, and instructions the AI follows. Both need review like any other software. Instructions are the easier half to miss, because they read like documentation. Picture a skill for drafting client emails whose examples use a real customer's name, email address and contract details. Nothing in it is malicious, yet every employee who installs it now carries that customer's data, and the AI may reuse it in the next email it writes.

The image at the top of this post shows what a review looks like on my own work. Before releasing [which plugin], I ran it through my own review: two agents, each with four reviewer roles. The house-rules review, which reads the skills and instructions, came back clean. The security review found five major issues in the scripts.

Most plugin demos skip this part. Once a team builds its week around a plugin, the business depends on it, whether or not anyone owns it. So for anyone rolling out an AI assistant, the real question is who decides which plugins get in, and who looks after them once they do.
