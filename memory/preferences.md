# Preferences

User-specific quirks, style preferences, and working habits.
Updated when preferences are observed or explicitly stated.

## Communication

### Directives
- Prefers terse interaction, no unnecessary status updates
- No verbose memory update announcements (standing instruction)
- Don't explain what you're about to do — just do it

### User Voice
- **Cadence**: short, direct messages. Often single sentences. Rarely more than two lines.
- **Decision style**: fast and decisive. Says "bin it" not "let's reconsider." Makes architectural calls in one exchange.
- **Request framing**: imperative, assumes context. "push it", "yes", "update the md's" — trusts Claude to infer scope.
- **Vocabulary**: casual British English — "innit", "bin it", "let's". Technical when discussing architecture, informal otherwise.
- **Feedback style**: corrects immediately, moves on. "no claude code references", "we don't need verbose updates." No softening.
- **Pattern**: propose → decide → ship → iterate. Doesn't deliberate long. Values working software over perfect plans. Decision-action gap is zero — decides and implements in the same exchange.
- **Velocity**: ships continuously, not in batches. 14+ discrete deliverables in a single session. Each is a complete unit, not "worked on X."
- **Architectural boldness**: will rewrite something just built if a better approach emerges. Rewrote SKILL.md twice in one session without hesitation.
- **Naming**: values opinionated naming that communicates intent — "clone-and-go", "dog-fooder", "hydrate". Names are compressed explanations.
- **Expectations**: Claude should keep up with the pace, not slow things down with confirmations or summaries.

## Code & Technical

- Values separation of concerns (config.md vs preferences.md, agents vs main context)
- Prefers convention over configuration where possible
- Favours clone-and-go over manual setup

## Workflow

- High velocity, iterative refinement — built and shipped v1.0 in a single session
- Uses /plan for architectural decisions, skips it for small changes
- Manages two GitHub identities: raffi-ismail (admin) and leith-dev (public-facing commits)
- Delegates PR creation and review to agents — expects the full cycle (commit, PR, review, merge)

## Format

- Tables for structured data
- Short bullet points over paragraphs
- No emojis unless explicitly requested
