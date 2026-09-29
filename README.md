# HeroMi Help Me Now: Parenting in Hard Moments

Tantrum, meltdown, hitting, refusing, or about to lose it yourself? Calm, shame-free steps and exact words to say, for kids aged 2 to 12.

Your child is screaming on the supermarket floor, refusing to get dressed, hitting their sibling, or frozen at the school gate. Or you are the one about to snap. Tell Claude what is happening, in your own words and your own language, and you get:

- **What's happening**, from your child's side, without blame
- **What to do right now**, in 2 to 4 short steps
- **What to say**, with exact words that fit your child's age
- **What to avoid**, the phrases that usually make it worse
- **After this moment**, how to reconnect and repair
- **One practice for today**, small enough to actually do

When you are the one struggling (overwhelmed, angry, guilty after yelling, exhausted), you get grounding steps, words to say to yourself, and permission to pause.

The method comes from [HeroMi](https://heromi.app), a parenting-support app. It covers about 30 common child situations (transitions, frustration, overwhelm, refusing, hitting, shutting down, worries, conflicts with other children, school) and 17 parent situations, with advice adapted to four age bands: 2-3, 4-5, 6-8 and 9-12.

## Principles

- Never shames the parent or the child.
- No diagnoses or clinical labels, and no punishment advice.
- Short enough to read with one hand while the other is holding your child.
- Checks for safety first. If someone may be in danger, it points you to emergency services and crisis lines instead of giving parenting tips.

This plugin is not medical, psychological or emergency advice. If you are worried about your child's health or development, talk to your child's doctor.

## Try it

Once the plugin is installed, just describe the moment. For example:

1. "My 4-year-old is screaming on the floor of the supermarket because I said no to candy."
2. "My 7 year old cries at the school gate every morning and won't go in."
3. "I just yelled at my kids and I feel terrible."
4. "My 2-year-old keeps hitting me when I tell him it's time to leave the park."
5. "My daughter is 9 and came home saying nobody at school will play with her."

## What the plugin does and does not do

- It is a single skill: instructions and reference notes for Claude. It contains no code, runs no commands, and makes no network requests.
- It does not store or send anything. What you write stays in your conversation with Claude.
- After a full answer, Claude may add **one** optional link to HeroMi's free Help Me Now page (heromi.app/help-me-now), which walks through the same moment step by step and can build a practice plan. No account is needed to use it. The link can include your child's age and the kind of situation (for example `age=4&behavior=crying_meltdown&context=store`) so the page opens on the right step, plus `utm_source=claude` so HeroMi can see the visit came from this plugin. Nothing is sent unless you choose to open the link. HeroMi removes the child's age and situation from the address bar before any analytics can read it; see [HeroMi's privacy policy](https://heromi.app/privacy).
- If you say you do not want links, Claude will not mention HeroMi again in that conversation.

## Contents

```
.claude-plugin/plugin.json
skills/help-me-now/SKILL.md                    the method and response format
skills/help-me-now/references/situations.md    situations and age bands
skills/help-me-now/references/safety.md        safety check and crisis resources
skills/help-me-now/references/heromi-links.md  how the optional HeroMi link is built
```

## Feedback

Open an issue in this repository, or visit [heromi.app](https://heromi.app).

## License

MIT, see [LICENSE](LICENSE).
