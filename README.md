# Claude Code plugins from elecnix

Add this marketplace once to install any Claude Code plugin published under github.com/elecnix by name.

## Add the marketplace

From a shell:

```sh
claude plugin marketplace add elecnix/claude-plugins
```

Or inside a Claude Code session:

```
/plugin marketplace add elecnix/claude-plugins
```

## Install a plugin

```sh
claude plugin install gh-monitor@elecnix-plugins
```

## Plugins

| Plugin | Source | Description |
| --- | --- | --- |
| `gh-monitor` | [elecnix/claude-gh-monitor](https://github.com/elecnix/claude-gh-monitor) | Watches GitHub pull requests through the `gh monitor` CLI and sends each event to the session as it happens. |
| `agent-identity` | [elecnix/claude-agent-identity](https://github.com/elecnix/claude-agent-identity) | Assigns each session an agent handle such as cc-swift-koala-42. |
| `skills-lock-autoinstall` | [elecnix/skills-lock-autoinstall](https://github.com/elecnix/skills-lock-autoinstall) | Installs agent skills from a `skills-lock.json` lock file when a session starts. |
| `your-attention` | [elecnix/your-attention](https://github.com/elecnix/your-attention) | Gives a session an inbox where its questions arrive as cards, and sends your answers back to it. |

`gh-monitor` is a channel plugin, so Claude Code loads it only when you pass the development channel flag at launch:

```sh
claude --dangerously-load-development-channels plugin:gh-monitor@elecnix-plugins
```

`your-attention` is a channel plugin too:

```sh
claude --dangerously-load-development-channels plugin:your-attention@elecnix-plugins
```
