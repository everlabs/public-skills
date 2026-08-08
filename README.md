# Everlabs public skills

Skills by Everlabs for AI coding agents – Claude Code, Codex, Cursor, OpenCode, Gemini CLI, and any other harness that supports the [SKILL.md](https://agentskills.io) standard.

**Each skill lives in its own repository.** This page is the index. Splitting them up means a skill's issues, pull requests and release history belong to that skill alone, and contributing to one cannot disturb the others.

## Skills

### [video-to-spec](https://github.com/everlabs/video-to-spec)

*by Oleg Pasko @ Everlabs*

Turns a screen-recording walkthrough (Loom, QuickTime, anything ffmpeg reads) into reviewable user-story specifications – each task carrying the exact screenshots the speaker was looking at when they said it. Record yourself thinking out loud while browsing the product you want to improve; get back clarified, delegable specs your AI agents (or your team) can implement.

The video is cut into one frame per second, deduplicated down to the distinct screen states, and every transcript segment is matched to the screen that was visible when it was spoken. Specs are drafted from that timeline, then a single batch of clarifying questions confirms anything ambiguous before the folder is final. Captions are used when the recording has them; otherwise it transcribes locally, for free, without uploading anything.

```bash
git clone https://github.com/everlabs/video-to-spec.git ~/.claude/skills/video-to-spec
```

## Installing any of these

Every skill repository *is* a skill folder, so cloning it into your agent's skills directory is the whole install:

```bash
git clone <skill-repo-url> ~/.claude/skills/<skill-name>    # Claude Code
git clone <skill-repo-url> ~/.codex/skills/<skill-name>     # Codex
```

Cursor, OpenCode, Gemini CLI and others use the same layout at their own path. You can also just point your agent at a skill's repository and ask it to install it. Update later with `git pull` in that folder.

## Contributing

Open issues and pull requests on the individual skill's repository, not here – that repo holds nothing but the skill, so your change cannot affect anything else. Use this repo only for questions that span the whole collection, or to propose a new skill.

## License

MIT, both for this index and for each skill unless its own repository says otherwise.
