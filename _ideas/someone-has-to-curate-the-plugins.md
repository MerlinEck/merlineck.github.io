---
title: "Someone has to curate the plugins"
captured: 2026-11-17
status: published
thesis: "For the effective use of AI assistants like Copilot, Claude, ChatGPT and Cohere, an enterprise needs its own curated plugins, built with the company's processes and integrations in mind, behind a gateway that protects the firm from malicious skills, scripts or plugins and minimizes the supply chain and business continuity risks of public plugins the business starts to rely on."
source: "Follow-on to last week's post, Stop paying AI to rewrite the wheel (2026-11-10), which promised: \"reusable plugins only save money if someone curates them. That's the governance question ... and will be the subject of a future post.\""
url: "https://merlineck.github.io/blog/2026/11/24/someone-has-to-curate-the-plugins/"
---

## Hook

Pay off the promise from last week's post: reusable plugins only save money if someone curates them. This is the post about who does that, and how.

## Notes

- Worked example: my plugin-toolkit plugin, which builds, reviews, security-reviews, evals and releases the other plugins in my marketplace. https://github.com/MerlinEck/magical-plugin-marketplace/tree/main/plugins/plugin-toolkit
- The gateway in practice: a plugin only gets into the marketplace after a house-rules review and a security review.
- Hero image: screenshot of a final review run. Two background agents work through four reviewer roles each, without seeing each other's results. The house-rules half came back with 0 critical, 0 major, 0 minor (apart from the marketplace listing that the release step adds). The security half found no critical issues but raised five major hardening findings, all in the scripts. Good evidence that the gateway catches real problems.
- Hero image file still to be added to assets/images/ (the images skill can do that once the draft exists).
- Related: _posts/2026-09-25-shadow-it-plugin-marketplace.md (why a marketplace), drafts part-4 (supply chain risk) and part-6 (running it in practice).
