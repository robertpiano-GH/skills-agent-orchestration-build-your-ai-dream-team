# Agent team

This project uses a custom four-agent team for building Mona's Project Pulse dashboard. The team is orchestrated through GitHub Copilot CLI running in a Codespace.

- **Orchestrator**
  - Target model: Claude Opus 4.7 (copilot)
  - Responsibility: Coordinate the overall project, break the dashboard work into phases, assign files and tasks to the specialist agents, and ensure the final solution integrates cleanly.
  - Definition: `.github/agents/orchestrator.agent.md`

- **Planner**
  - Target model: Claude Opus 4.7 (copilot)
  - Responsibility: Research the repository, create a practical implementation plan, identify dependencies and edge cases, and recommend a validated approach for building the dashboard.
  - Definition: `.github/agents/planner.agent.md`

- **Coder**
  - Target model: GPT-5.5 (copilot)
  - Responsibility: Implement code, fix bugs, add logic, and create or update dashboard support files with clear, testable, repository-consistent code.
  - Definition: `.github/agents/coder.agent.md`

- **Designer**
  - Target model: Gemini 3.1 Pro (copilot)
  - Responsibility: Design the dashboard UI/UX, visual styling, information hierarchy, and responsive behavior so the Project Pulse frontend looks polished and user friendly.
  - Definition: `.github/agents/designer.agent.md`

## How the team works together

The Orchestrator leads the Project Pulse effort by requesting a plan from the Planner, then delegating implementation and design tasks to the Coder and Designer. The Planner defines the work breakdown and dependencies, the Designer defines the dashboard look and interaction guidance, and the Coder implements the frontend and supporting files. This coordinated workflow ensures Project Pulse is built with a clear plan, polished UI, and working code under the GitHub Copilot CLI orchestration model.