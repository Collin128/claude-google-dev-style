# Google developer style for Claude Code

A custom [output style](https://code.claude.com/docs/en/output-styles) that makes Claude Code communicate according to the [Google developer documentation style guide](https://developers.google.com/style).

The style sets `keep-coding-instructions: true`, so Claude Code's built-in software engineering behavior stays intact. Only the communication changes: second person, active voice, present tense, sentence-case headings, serial commas, no filler words like "simply" or "just", and consistent code formatting.

## Install

To install the style for all projects, copy the style file to your user-level output styles directory:

```bash
mkdir -p ~/.claude/output-styles
curl -fsSL https://raw.githubusercontent.com/GITHUB_USER/claude-google-dev-style/main/google-dev-style.md \
  -o ~/.claude/output-styles/google-dev-style.md
```

Replace `GITHUB_USER` with the account that hosts this repository.

To install the style for a single project, copy `google-dev-style.md` into that project's `.claude/output-styles/` directory instead.

## Activate

1. Run `/config` in Claude Code.
2. Select **Google developer style** under **Output style**.
3. Run `/clear` or start a new session.

To skip the menu, set the style in a settings file such as `.claude/settings.local.json`:

```json
{
  "outputStyle": "Google developer style"
}
```

## Limitations

Output styles apply to the main conversation only. Subagents run their own system prompts, so they don't inherit this style. If you want a custom subagent to follow the same rules, copy the rule sections from `google-dev-style.md` into that agent's Markdown file, or add a condensed version to `~/.claude/CLAUDE.md`, which loads for custom subagents.

## Attribution and license

The rules in this project are adapted from the [Google developer documentation style guide](https://developers.google.com/style), which Google publishes under the [Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/). This project is licensed under the same terms. See [LICENSE.md](LICENSE.md).
