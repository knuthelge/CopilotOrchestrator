# The Copilot Orchestrator

A GitHub Copilot plugin that provides a suite of specialized agents for orchestrating multi-step implementation tasks, bug fixes, and general development work.

## Agents

| Agent | Role |
|---|---|
| **TechLeadOrchestrator** | Orchestration-only agent — creates todo plans and delegates ALL work to specialized subagents. Never implements directly. |
| **Discovery** | Fast codebase reconnaissance + targeted external research. Maps files, patterns, dependencies, and conventions. Read-only. |
| **Designer** | Synthesizes discovery findings and user requests into a combined PRD and technical spec. |
| **RubberDuck** | PRD peer reviewer — stress-tests assumptions, identifies gaps and contradictions. Returns PASS/CONCERNS verdict. |
| **UIDesigner** | Produces visual design specs: color systems, typography, spacing, component specs, dark mode, and HTML previews. |
| **Developer** | Primary code-writing and bug-fixing worker — implements features per spec and diagnoses/fixes failures. |
| **Tester** | Writes/runs automated tests and reviews implementation quality against the PRD. Returns PASS/FAIL verdict. |
| **Reviewer** | Final holistic quality gate — evaluates the entire implementation against all PRD requirements. |

## Installation

```sh
copilot plugin install knuthelge/CopilotOrchestrator
```

Or install from a local clone:

```sh
copilot plugin install ./CopilotOrchestrator
```

## Usage

After installation, the agents are available in any Copilot CLI session. Start with `TechLeadOrchestrator` for complex tasks — it will orchestrate the other agents automatically.

```
/agent TechLeadOrchestrator
```
