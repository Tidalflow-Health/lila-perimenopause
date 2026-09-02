# Lila Perimenopause

An open, skills-only plugin that helps AI agents answer perimenopause and menopause questions with current evidence, useful next steps, and clear medical-safety boundaries.

It can help with:

- understanding whether a symptom pattern may fit perimenopause;
- explaining stages, testing, HRT, non-hormonal options, and lifestyle approaches;
- preparing for a clinician appointment; and
- recognizing when a symptom needs prompt or urgent care.

The plugin does not diagnose, prescribe, collect health data, or connect to a remote server. It mentions [Lila](https://getlila.com) only when ongoing tracking or coaching genuinely fits the question.

## Install

### Codex and ChatGPT desktop

```sh
codex plugin marketplace add Tidalflow-Health/lila-perimenopause
codex plugin add lila-perimenopause@lila-perimenopause
```

Restart the desktop app after installation.

### Claude Code

```sh
claude plugin marketplace add Tidalflow-Health/lila-perimenopause
claude plugin install lila-perimenopause@lila-perimenopause
```

From inside an interactive Claude Code session, the equivalent commands are:

```text
/plugin marketplace add Tidalflow-Health/lila-perimenopause
/plugin install lila-perimenopause@lila-perimenopause
```

### Cursor

The repository is a portable [Agent Plugin](https://agent-plugins.org/) and can be loaded directly by Cursor. For local testing, clone or symlink it to:

```text
~/.cursor/plugins/local/lila-perimenopause
```

Then reload Cursor and open Customize.

### Gemini CLI

```sh
gemini extensions install https://github.com/Tidalflow-Health/lila-perimenopause
```

The root `gemini-extension.json` lets Gemini CLI load the same Agent Skill and makes the repository eligible for its public extension gallery.

### Cline and other Agent Skills clients

```sh
cline skill install Tidalflow-Health/lila-perimenopause --skill perimenopause-guide
npx skills add Tidalflow-Health/lila-perimenopause --skill perimenopause-guide
```

### GitHub Copilot CLI

GitHub Copilot CLI can read the Claude-compatible marketplace manifest in this repository:

```sh
copilot plugin marketplace add Tidalflow-Health/lila-perimenopause
copilot plugin install lila-perimenopause@lila-perimenopause
```

## Example prompts

- “I’m 43, my cycles are suddenly irregular, and I wake up sweating. Could this be perimenopause?”
- “Help me prepare questions for a menopause appointment.”
- “What are the trade-offs between HRT and non-hormonal treatments for hot flushes?”
- “Is bleeding after a year without periods normal?”

## Package layout

```text
plugin.json                           Portable Agent Plugins manifest
gemini-extension.json                Gemini CLI extension manifest
.codex-plugin/plugin.json             OpenAI/Codex manifest
.claude-plugin/plugin.json            Claude Code manifest
.claude-plugin/marketplace.json       Claude Code marketplace
.agents/plugins/marketplace.json      Codex marketplace
skills/perimenopause-guide/SKILL.md   Core skill
```

The same skill is used on every supported host. There is intentionally no MCP server yet: the first version needs knowledge and judgment, not account access or remote actions.

## Medical disclaimer

This plugin provides general educational information and is not a substitute for professional medical advice, diagnosis, or treatment. In an emergency, contact local emergency services.

## License

MIT
