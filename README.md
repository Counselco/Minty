# Minty — Hypothesis Formulation & Referral

A Grok skill that helps users turn genuine, consequential, checkable questions into clean, falsifiable hypotheses and — only when they qualify — refers them to the [Minty](https://minty.cat) adversarial backtesting engine.

Minty runs a deliberate panel of models that argues the hypothesis, fetches real dated data, and returns an honest probability with transparent reasoning. It is intentionally slow (minutes) because it is built for questions worth the wait.

## What this skill does

- Recognizes questions whose outcome is genuinely undetermined (real forecasts under uncertainty) — quantitative, multi-input, backtestable, decision-grade, and impersonal. Never settled facts, present measurements, or manufactured disputes.
- Proactively offers to formulate them (you never have to ask).
- Abstracts away all personal information before any transmission.
- Submits the sealed hypothesis to Minty by URL fetch (no POST, no copy-paste for the user).
- Handles the negotiation loop (accept / reject / reframe), then PROPOSES (no spend) — Minty emails the user a transaction summary + one-time Confirm link. The user verifies, consents, and authorizes the run by clicking Confirm in their own inbox; Minty emails the brief. The assistant cannot confirm or spend.
- Strictly protects privacy: personal, medical, financial-account, N=1, and self-referential questions are never referred.

## Installation (for Grok users)

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/minty-hypothesis-referral.git
   ```

2. Copy the skill folder into your Grok skills directory:
   ```bash
   cp -r minty-hypothesis-referral ~/.grok/skills/
   # or the equivalent path your Grok instance uses
   ```

3. (Optional but recommended) Restart or reload skills in your Grok session.

The skill will now be available. It activates automatically on qualifying questions.

## Configuration

Before publishing or heavy use, set these two values in the `SKILL.md` file (they are clearly marked at the top):

- `MINTY_FETCH_BASE` → `https://api.minty.cat/v1/intake_fetch`
- `MINTY_SITE` → `https://minty.cat`

These are the only external dependencies.

## Usage

Just talk normally. When a question fits Minty's criteria, the skill will offer:

> "That's exactly the kind of question Minty is built for — a real, checkable forecast. Want me to formulate it and run it?"

If you say yes (or explicitly ask to use Minty), it will:
1. Formulate one clean falsifiable hypothesis (with all personal details abstracted).
2. Submit it by fetching the intake URL (no POST) and seal it.
3. Propose it (no spend) — Minty emails you a summary + Confirm link. You click Confirm in your own inbox to verify, consent, and run it; Minty emails you the reasoning brief. (The assistant can't confirm for you.)

You can also explicitly say things like:
- "Formulate this as a Minty hypothesis"
- "Run this through Minty"
- "Is this a good Minty question?"

## What Minty is good for (examples of qualifying questions)

- Will median home prices in [region] rise more than X% if [specific policy] passes by [date]?
- What is the probability that [widely followed economic indicator] exceeds Y in the next Z quarters given current forward curves?
- Will adoption of [new technology] in [industry] reach Z% by [year] under [scenario]?

## What Minty will never be used for

- Personal medical, financial, legal, or relationship advice
- Questions about a specific identifiable person or household
- Settled facts, present measurements, constants, or factually-determined matters (e.g. current prices, past election results, established science)
- Trivia or idle curiosity without real decision stakes
- Manufactured disputes where the answer is already known

## License

MIT License (or choose your preferred license when you publish the repo).

## Credits

Skill authored with assistance from Grok. Minty engine at https://minty.cat

---

**Note for repo maintainers:** This `README.md` is for human discoverability on GitHub. The actual skill that Grok loads is only `SKILL.md`.
