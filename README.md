# Mermaid Diagram Plugin for Claude Code

A Claude Code plugin that generates interactive HTML diagrams with Mermaid.js for visualizing flows, sequences, architectures, and processes.

## Installation

### Option 1: Install from Marketplace (Recommended)

First, add the plugin's marketplace, then install:

```bash
# Add the marketplace
claude plugin marketplace add agentic-coding-school/mermaid-diagram-plugin

# Install the plugin
claude plugin install mermaid-diagram@mermaid-diagram-marketplace
```

You can scope the installation to user-level (default), project-level, or local:

```bash
claude plugin install mermaid-diagram@mermaid-diagram-marketplace --scope project
```

### Option 2: Load Locally (For Development)

Clone this repository and load it with the `--plugin-dir` flag:

```bash
git clone https://github.com/agentic-coding-school/mermaid-diagram-plugin.git
claude --plugin-dir ./mermaid-diagram-plugin
```

> **Note:** `--plugin-dir` loads the plugin for the current session only. Use Option 1 for a persistent installation.

## Usage

Once installed, Claude will automatically use this skill when you ask to:

- "Create a diagram"
- "Draw a sequence diagram"
- "Show me the flow"
- "Visualize how X works"
- "Turn this into a diagram"
- "What's the architecture?"

### Example Prompts

```
Show me how the authentication flow works
```

```
Create a database diagram for the users and teams tables
```

```
Visualize the checkout process from cart to payment
```

## Supported Diagram Types

| Type | Use Case |
|------|----------|
| **Sequence Diagrams** | API flows, user journeys, webhook processes |
| **Flowcharts** | Decision trees, algorithms, process flows |
| **ER Diagrams** | Database schemas, table relationships |
| **Class Diagrams** | Component architecture, object relationships |
| **State Diagrams** | Status workflows, state machines |
| **Gantt Charts** | Project timelines, schedules |
| **Git Graphs** | Branch strategies, version history |
| **Mindmaps** | Feature planning, concept mapping |
| **Timelines** | User journeys, historical events |

## Output

The plugin generates standalone HTML files that:

- Work in any browser without setup
- Include interactive Mermaid.js diagrams
- Have responsive design for mobile/desktop
- Support dark mode automatically
- Include documentation and key points

## v1.1 Features

### Adaptive Context Interview

The skill now interviews you before generating diagrams using `AskUserQuestion`:
- **Purpose-first**: Asks whether the diagram is for academic papers, presentations, documentation, or a quick sketch
- **Adaptive follow-ups**: Only asks relevant questions based on your answers
- **Maximum 3-4 questions**: Never over-interviews; respects "just make it" requests

### Interactive Editor

When enabled, generated HTML files include a **sidebar editor** with:
- **Theme Switcher** - Toggle between Light, Dark, Neutral, and Forest themes
- **Global Color Palette** - Color pickers for primary, secondary, and accent colors
- **Per-Node Editing** - Click any node to change its individual colors
- **Inline Text Editing** - Double-click any node to edit its label
- **Node Resize** - Shift+click to cycle through size options
- **Font & Size Controls** - Choose font family and adjust size
- **Zoom Control** - Scale diagrams from 50% to 200%
- **Export** - Save as PNG or SVG
- **Auto-Save** - All customizations persist in localStorage

### Context Presets

- **Academic/Scientific** - Serif fonts, muted colors, print-optimized, publication-ready
- **Presentation** - Bold sans-serif, high-contrast vibrant colors, larger fonts and nodes

## Plugin Structure

```
mermaid-diagram-plugin/
├── .claude-plugin/
│   ├── plugin.json              # Plugin manifest
│   └── marketplace.json         # Marketplace catalog
├── skills/
│   └── mermaid-diagram-generator/
│       ├── SKILL.md                 # Main skill definition
│       ├── diagram-examples.md      # Templates for all diagram types
│       ├── mermaid-syntax-guide.md  # Complete syntax reference
│       ├── styling-guide.md         # HTML/CSS customization
│       ├── interactive-template.md  # Interactive editor HTML template
│       ├── context-presets.md       # Academic & Presentation presets
│       └── README.md               # Skill documentation
├── README.md                    # This file
└── LICENSE                      # MIT License
```

## Development

### Testing Locally

```bash
claude --plugin-dir /path/to/mermaid-diagram-plugin
```

### Adding New Diagram Templates

1. Add the template to `skills/mermaid-diagram-generator/diagram-examples.md`
2. Document the syntax in `mermaid-syntax-guide.md`
3. Update `SKILL.md` with the new use case

## License

MIT License - see [LICENSE](LICENSE) for details.

## Author

[Agentic Coding School](https://agenticcoding.school)
