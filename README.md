# linkedin-writing

An agent skill for writing LinkedIn posts that sound like the person who built the thing, not a press release.

It covers the post shape (a two-line hook, one real story, links in the first comment), a personal voice file you fill in, and a small checker that catches links in the body, hashtags, emoji, em dashes and hype words.

## Install

**Claude Code, as a plugin:**

```
/plugin marketplace add shwetankg07/linkedin-writing
/plugin install writing-linkedin-posts@linkedin-writing
```

**Claude Code, Cursor, Codex and other agents, with the `skills` CLI:**

```bash
npx skills add shwetankg07/linkedin-writing
```

**By hand:**

```bash
git clone https://github.com/shwetankg07/linkedin-writing ~/Work/linkedin-writing
ln -s ~/Work/linkedin-writing ~/.claude/skills/writing-linkedin-posts
```

Then ask your agent to write a post about a repo or project. The skill loads on its own.

Fill in `voice.md` with your own rules (who you are, how you sound, words you never use), or put them in `voice.local.md` to keep them out of git. Until you do, it writes in plain neutral English.

## Files

- `SKILL.md`: the post shape and rules
- `voice.md`: your voice rules, blank until you fill it in. `voice.local.md` (ignored by git) wins when it exists.
- `examples/voice-shwetank.md`: my own voice file, as a filled-in example
- `check.py`: lints a draft, standard library only. Run `python3 check.py post.txt`, or `--selftest`.
- `examples/`: two posts that pass the checker

## License

MIT
