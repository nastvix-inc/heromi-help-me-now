# Building the HeroMi link

HeroMi's free Help Me Now at https://heromi.app/help-me-now works without an account. A link can open it already filled in, so the parent lands on the next unanswered step instead of starting over.

## Format

```
https://heromi.app/help-me-now?age=<age>&behavior=<behavior>&trigger=<trigger>&context=<context>&utm_source=claude&utm_medium=plugin&utm_campaign=help-me-now
```

Always keep the three `utm_` parameters. Every other parameter is optional. The page ignores any value it does not recognise, so a wrong value never breaks the link; it only skips that step.

The order matters: `trigger` is only used when `behavior` is set, and `context` only when `trigger` is set. Leave out anything you are not sure of rather than guessing.

## `age`

A whole number from 2 to 12. Leave it out if you do not know the age or the child is outside that range.

## `behavior` and `trigger`

Pick the behaviour, then one of the triggers listed for it. Use `unknown` for "something else" or "not sure".

| `behavior` | The child is | Allowed `trigger` values |
| - | - | - |
| `crying_meltdown` | Crying or melting down | `denied_request` (did not get what they wanted), `had_to_stop` (had to stop or leave something), `tired` (tired, hungry, or too much going on), `unknown` |
| `refusing` | Refusing | `had_to_stop` (had to stop something or go somewhere), `limit` (a limit or "no"), `routine_task` (a routine task: bedtime, dressing, teeth, school), `unknown` |
| `upset_cant_calm` | Upset and cannot calm down | `overwhelmed`, `scared`, `unexpected_change`, `unknown` |
| `aggressive` | Hitting, pushing, throwing | `denied_request`, `overwhelmed` (overwhelmed or frustrated), `limit`, `unknown` |
| `shutdown` | Shut down or frozen | `overwhelmed`, `scared`, `unexpected_change`, `unknown` |
| `scared_anxious` | Scared or anxious | `scared` (something specific scared them), `unexpected_change`, `sensory_overload` (too much noise or stimulation), `unknown` |
| `unknown` | Not sure | `tired`, `hungry`, `overwhelmed`, `unknown` |

### Another child was involved (ages 6 to 12 only)

Set `trigger=social_conflict`, add `peer`, and set `behavior` to how the child is reacting: `crying_meltdown` (crying or very upset), `aggressive` (angry or arguing), `shutdown` (shut down or quiet), or `refusing` (refusing to talk about it).

| `peer` | What happened |
| - | - |
| `excluded` | Left out |
| `unfair` | Something felt unfair |
| `conflict_one_kid` | They argued over something |
| `aggression_received` | Another child hurt or scared them |

For children under 6, or a sibling, leave out `trigger` and `peer` and use the behaviour only.

## `context`

`home`, `playground`, `store`, `public_place`, `on_the_way`, `visiting`, `daycare` (ages 5 and under), `school` (6 and up), `after_school` (6 and up), `unknown`.

## Parent branch

The parent branch cannot be pre-filled. Link to the page with the tracking parameters only:

```
https://heromi.app/help-me-now?utm_source=claude&utm_medium=plugin&utm_campaign=help-me-now
```

## Examples

- 4-year-old, meltdown in a store after a "no":
  `https://heromi.app/help-me-now?age=4&behavior=crying_meltdown&trigger=denied_request&context=store&utm_source=claude&utm_medium=plugin&utm_campaign=help-me-now`
- 3-year-old will not go to bed:
  `https://heromi.app/help-me-now?age=3&behavior=refusing&trigger=routine_task&context=home&utm_source=claude&utm_medium=plugin&utm_campaign=help-me-now`
- 8-year-old left out at the playground:
  `https://heromi.app/help-me-now?age=8&behavior=crying_meltdown&trigger=social_conflict&peer=excluded&context=playground&utm_source=claude&utm_medium=plugin&utm_campaign=help-me-now`

## Other HeroMi pages

Mention these only when the parent asks for more reading, tools or an app:

- Parent Guide (free articles): https://heromi.app/parent-guide
- How HeroMi works: https://heromi.app/how-it-works
