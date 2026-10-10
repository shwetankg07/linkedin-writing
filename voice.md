# Voice

Your personal rules go here. They override `SKILL.md`. Until you add some, the skill writes in plain,
neutral English and asks you about anything personal it needs.

To keep your rules out of git, put them in `voice.local.md` instead. The skill reads that file first
when it exists. `examples/voice-shwetank.md` shows a filled-in one.

## Who's writing

(One or two lines: what you do, who reads your posts.)

## Register

(How you sound. Formal or casual? Jokes? Lowercase?)

## Hard rules

(Things the skill must never write: titles you don't use, people not to name, what not to link.)

## Banned words

`check.py` warns on each of these, on top of its built-in hype list. One per line, like `- synergy`.
