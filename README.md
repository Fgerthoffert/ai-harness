# ai-harness

Personal Skills, Agents and other AI resources for Agentic workflows by [Francois Gerthoffert](https://github.com/Fgerthoffert).

This repository is also a **GitHub Copilot CLI plugin marketplace**, making it easy to install the plugins it contains directly from the CLI.

---

## Plugins

### `fge-personal`

A personal plugin containing:

| Skill                                                                   | Description                                                                            |
| ----------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| [`writing-style`](./plugins/fge-personal/skills/writing-style/SKILL.md) | Applies Francois Gerthoffert's personal writing style when generating or editing text. |

---

## Installation

### Install via marketplace

Register this repository as a Copilot CLI marketplace:

```sh
copilot plugin marketplace add Fgerthoffert/ai-harness
```

Browse available plugins:

```sh
copilot plugin marketplace browse ai-harness
```

Then install the personal plugin:

```sh
copilot plugin install fge-personal@ai-harness
```

### Install directly

You can also install the plugin directly from the repository without registering the marketplace:

```sh
copilot plugin install Fgerthoffert/ai-harness
```

Or from the plugin subdirectory:

```sh
copilot plugin install Fgerthoffert/ai-harness:plugins/fge-personal
```

### Verify the installation

```sh
copilot plugin list
```

Or inside an interactive Copilot session:

```
/skills list
```

The plugin skills can then be invoked by name (for example `writing-style` or `marketplace-doctor`).

---

## Repository structure

```
.claude-plugin/
├── marketplace.json            # Primary marketplace manifest
└── plugin.json                 # Root plugin manifest (direct install)
.github/
└── plugin/
    └── marketplace.json        # Compatibility marketplace manifest
plugins/
└── fge-personal/
    ├── plugin.json             # Plugin manifest
    └── skills/
        ├── marketplace-doctor/
        │   └── SKILL.md         # Marketplace diagnostics skill
        └── writing-style/
            └── SKILL.md         # Writing style skill
```
