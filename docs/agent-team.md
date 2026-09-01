# Agent team

Mona's Project Pulse dashboard is built using a specialized team of four custom agents, orchestrated through GitHub Copilot CLI running in a Codespace. Each agent is designed with specific capabilities and responsibilities to ensure high-quality implementation.

## Agent Roles

### 1. Orchestrator
- **Model**: Claude Opus 4.7 (copilot)
- **Responsibility**: Coordinates the Planner, Coder, and Designer agents to break down complex requests into tasks and delegate work to specialists. Verifies that the integrated result is cohesive and reports final outcomes.
- **Location**: `.github/agents/orchestrator.agent.md`

### 2. Planner
- **Model**: Claude Opus 4.7 (copilot)
- **Responsibility**: Creates detailed implementation strategies and technical plans by researching the codebase, documentation, dependencies, and edge cases. Produces ordered implementation steps, file assignments, and identifies parallel vs. sequential work.
- **Location**: `.github/agents/planner.agent.md`

### 3. Coder
- **Model**: GPT-5.5 (copilot)
- **Responsibility**: Implements code-oriented tasks with clear structure, explicit errors, and testable behavior. Creates support configuration files as needed and validates changes before reporting completion.
- **Location**: `.github/agents/coder.agent.md`

### 4. Designer
- **Model**: Gemini 3.1 Pro (copilot)
- **Responsibility**: Handles UI/UX design, accessibility, information architecture, and visual design. Creates a polished dashboard with visible project cards, status badges, and responsive layout that exceeds bare HTML pages.
- **Location**: `.github/agents/designer.agent.md`

## Orchestration Approach

This agent team operates through GitHub Copilot CLI in a Codespace, allowing for structured collaboration where the Orchestrator coordinates specialized tasks. Work is executed in parallel when file scopes do not overlap and dependencies permit, and sequentially when integration or approval is required.
