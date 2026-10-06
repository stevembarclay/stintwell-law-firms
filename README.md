# Stintwell for Law Firms

A plugin for Claude that works on the business side of a law firm: cash and owner pay, marketing, intake, operations, hiring, and where AI fits. You describe your firm and what's bothering you. It asks a few questions, names the one thing holding the firm back, and gets you moving on it, starting with one thing to do this week.

It covers the business of running a firm, not questions of law. Questions about client money, trust accounts, fee sharing with non-lawyers, writing to a regulator, a client's matter or what a state's law says go to ethics counsel or your state bar's ethics line.

**Don't act on its answers about trust accounts or client money; take them to ethics counsel.**

## How it works

The plugin has seven skills. Each one tells Claude to call the plugin's connector, `law-firm-method` at `https://sbos.stintwell.com/api/law-firm/mcp`, before answering, and to follow what it returns.

- **What it sends:** only the name of a skill and a step. It never sends your conversation, your firm's numbers, client names or case facts.
- **What it fetches:** the skill's instructions (tool `start`), then the steps it needs (tool `get_method`). Both tools are read-only.
- **The instructions are Stintwell's own work.** They tell Claude to use them but not to quote, reproduce or summarize them. The server also limits how much of the method one account can fetch in an hour or a day.
- **Sign-in:** connecting the connector opens our sign-in page. Enter your email, tick the box to accept the terms, and enter the one-time code we email you. There's no password.
- **What you need:** a Stintwell for Law Firms account (sign up with your email) and Claude on a paid plan.

## What Claude's install warning means

When you add the plugin, Claude shows a general warning that plugins may include components that run code. You can check what this one holds: seven text skills (each a short stub), one connector address, an icon and this README. It has no scripts and nothing to run on your computer. The connector receives only a skill name and a step name, and what it receives is described above.

## Try it

- "I run a 4-lawyer family law firm in Ohio, about $1.8M a year. Revenue is up but cash is always tight. Where do I start?"
- "We miss calls after hours and consults are not signing. What do I fix first?"
- "Can I use AI to answer our phones? What is safe with client data?"
- "Should I hire another associate?"

## Privacy, terms and support

- Privacy policy: https://sbos.stintwell.com/law-firm/privacy
- Terms of use: https://sbos.stintwell.com/law-firm/terms
- Support: help@stintwell.com

Not legal advice. Not affiliated with Anthropic; Claude is Anthropic's trademark. © 2026 Stintwell LLC.
