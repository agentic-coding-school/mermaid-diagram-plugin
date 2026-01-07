# Mermaid Diagram Plugin for Claude Code

A Claude Code plugin that generates interactive HTML diagrams with Mermaid.js for visualizing flows, sequences, architectures, and processes.

## Installation

### Option 1: Install from GitHub (Recommended)

```bash
claude /plugin install https://github.com/agentic-coding-school/mermaid-diagram-plugin
```

### Option 2: Install Locally

Clone this repository and load it with the `--plugin-dir` flag:

```bash
git clone https://github.com/agentic-coding-school/mermaid-diagram-plugin.git
claude --plugin-dir ./mermaid-diagram-plugin
```

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

## Plugin Structure

```
mermaid-diagram-plugin/
├── .claude-plugin/
│   └── plugin.json          # Plugin manifest
├── skills/
│   └── mermaid-diagram-generator/
│       ├── SKILL.md              # Main skill definition
│       ├── diagram-examples.md   # Templates for all diagram types
│       ├── mermaid-syntax-guide.md  # Complete syntax reference
│       ├── styling-guide.md      # HTML/CSS customization
│       └── README.md             # Skill documentation
├── README.md                 # This file
└── LICENSE                   # MIT License
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
