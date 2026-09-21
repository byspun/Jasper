# Jasper

> A mobile development workstation and AI development agent for Android.

Jasper brings a full development environment to your phone, giving developers the tools to build, run, test, debug, secure, and deploy software without needing a traditional PC.

Jasper is built around a simple idea:

**Your phone should be able to do more.**



## Table of Contents

- [What Jasper Is](#what-jasper-is)
- [What Jasper Is Not](#what-jasper-is-not)
- [Core Features](#core-features)
- [AI](#ai)
- [Agents](#agents)
- [Skills](#skills)
- [MCP and Integrations](#mcp-and-integrations)
- [Development Lifecycle](#development-lifecycle)
- [Discuss and Build Modes](#discuss-and-build-modes)
- [Security](#security)
- [Memory](#memory)
- [Efficiency](#efficiency)
- [Models and Routing](#models-and-routing)
- [Backup](#backup)
- [Open Source Foundations](#open-source-foundations)
- [Design Principles](#design-principles)
- [Project Status](#project-status)
- [License](#license)



## What Jasper Is

| Jasper is | Description |
|---|---|
| 📱 A mobile development workstation | A full development environment designed to run on Android |
| 🤖 An AI development agent | Jasper can work alongside the developer throughout the development process |
| 💻 A PC-like development environment | Terminal, editor, files, Git, preview, AI and other development tools in one place |
| 🧠 An intelligent development system | Jasper can decide how a task should be handled and select the right tools, agents, skills and models |
| 🔐 Privacy-first | Designed around local control, offline use and minimal data collection |
| 🧩 Customizable | Users can add their own models, providers, agents, skills, MCPs and tools |
| 🛠️ Open | Built by adapting useful open-source projects instead of rebuilding everything from scratch |



## What Jasper Is Not

| Jasper is not | Why |
|---|---|
| ❌ Just an AI chatbot | Jasper is a development workstation first |
| ❌ Just a mobile code editor | It includes a terminal, runtime, Git, preview, AI, agents and more |
| ❌ A cloud IDE | The goal is to run the development environment directly on the device |
| ❌ Locked to one AI model | Users can configure different local and online models |
| ❌ Limited to one provider | Users can choose from supported providers or add their own |
| ❌ A giant collection of AI features | Features exist to make development easier, not to add complexity |
| ❌ Dependent on AI for every action | Normal development tools remain available without AI |



## Core Features

### Development Environment

- Native Android application
- Linux environment through PRoot
- ARM64 support
- Integrated terminal
- PTY support
- xterm.js terminal interface
- Code editor powered by CodeMirror
- File manager
- File editor
- Git support
- Browser based project preview
- Project templates
- Blank projects
- Mobile-first interface
- Long-running process support
- Foreground service
- Wake lock support

### Privacy

- No mandatory account
- No telemetry
- Offline capable
- Local model support
- Local development environment
- User controlled network access
- User controlled AI providers and integrations



## AI

Jasper is the AI agent that works alongside the developer.

It can help with the full development process instead of only generating code.

### Local Models

Jasper supports local models through:

- llama.cpp
- GGUF models
- User-selected local models

### Online Models

Jasper will support multiple online AI providers, including providers such as:

- Anthropic
- OpenAI
- DeepSeek
- OpenRouter
- Other supported providers

If a preferred provider is not supported directly, users can add it as a custom provider.

### Model Support

- Native model registry
- OpenAI-compatible endpoints
- Anthropic-compatible endpoints
- Custom endpoints
- Multiple models
- Model combinations
- Fallback chains
- Intelligent model routing
- Dynamic intelligence scaling
- Automatic vision routing
- Provider failure handling

Jasper should work properly with only one configured model. Multiple models are there for users who want more flexibility, speed, cost control or specialization.



## Agents

Jasper can use specialist sub-agents for different parts of a development task.

Examples include:

- Architect
- Backend
- Frontend
- Database
- Security
- QA
- DevOps

Jasper decides which specialists are actually needed instead of running every available agent.

Sub-agents do not require separate AI models. The same model can handle different specialist roles using different instructions, tools, permissions and context.



## Skills

Skills define **how** an agent should perform a task.

Jasper includes built-in skills and allows users to manage their own.

Users can:

- Add skills
- Create skills
- Edit skills
- Disable skills
- Delete skills

Useful skills from existing open-source projects can also be adapted and included where they make sense.



## MCP and Integrations

Jasper supports MCP so users can connect external tools and services.

Users can:

- Add custom MCPs
- Manage connected MCPs
- Remove MCPs
- Configure MCP connections

### Composio

Jasper uses the Composio SDK to make connecting everyday apps and tools easier.

When Jasper needs access to something that requires a connection, it can ask the user and show a **Connect** action.

After authorization, the connected tool becomes available through Jasper and can be managed from the MCP section.

Power users can also connect their own Composio MCP directly.

Custom MCP support remains available for tools and services that are not covered by Composio.



## Development Lifecycle

Jasper is designed to support the whole development loop:

```text
Idea
  ↓
Discuss
  ↓
Architect
  ↓
Build
  ↓
Run
  ↓
Observe
  ↓
Diagnose
  ↓
Fix
  ↓
Test
  ↓
Secure
  ↓
Deploy
  ↓
Remember
```

The goal is not simply to generate code.

Jasper should be able to help create something, run it, inspect what happened, find problems, fix them, test the result, check security, and deploy when the developer is ready.



## Discuss and Build Modes

Jasper has two simple modes.

### Discuss

Used for:

- Conversation
- Brainstorming
- Planning
- Architecture
- Questions

Discuss mode should not accidentally modify the user's project.

### Build

Used when the developer is ready to work on the project.

Build mode can:

- Create code
- Edit code
- Modify files
- Run commands
- Test
- Debug
- Secure
- Deploy
- Perform other development actions allowed by the runtime



## Security

Security is part of Jasper's development process.

Jasper can:

- Check applications for security issues
- Find vulnerabilities and loopholes
- Understand discovered problems
- Create patches
- Apply patches
- Test patches
- Verify fixes

Jasper also has a permission and policy layer that controls what agents and tools are allowed to do.

Sensitive actions can require user confirmation.



## Memory

Jasper has one unified memory system built around a memory graph.

It can store and connect things such as:

- User preferences
- Projects
- Project knowledge
- Architecture decisions
- Development history
- Skills
- Relationships between pieces of information

The memory system is designed to retrieve relevant context instead of constantly sending entire project and conversation histories to the model.

Jasper's memory can improve over time by learning what information matters, what is temporary, and what should be remembered.

### Project Knowledge

Projects can optionally include their own knowledge file containing things such as:

- Architecture
- Conventions
- Requirements
- Constraints
- Important decisions
- Project rules
- Things that should never be used

Project knowledge supplements Jasper's memory when needed.



## Efficiency

Jasper should avoid wasting code, tokens, context and resources.

### Code Efficiency

Jasper uses ideas from [Ponytail](https://github.com/DietrichGebert/ponytail) to:

- Avoid unnecessary code
- Avoid needless abstractions
- Reduce unnecessary dependencies
- Prefer existing platform features
- Keep implementations smaller when possible

### AI Efficiency

Jasper uses ideas from [Caveman](https://github.com/JuliusBrussee/caveman) to:

- Reduce unnecessary AI output
- Reduce unnecessary context
- Keep important technical details intact
- Preserve commands, code, paths, errors and warnings
- Adjust output based on the task

Efficiency should never come at the cost of correctness.



## Models and Routing

Jasper separates task decisions from model selection.

The first step is figuring out what needs to happen.

A lightweight local decision system can handle simple and obvious cases without requiring another AI model.

For unclear cases, Jasper can use the configured AI model to help make the decision.

The routing system can then consider:

- Task type
- Task complexity
- Required capabilities
- Required agents
- Required skills
- Required tools
- Model capabilities
- Context requirements
- Vision requirements
- Cost
- Token usage
- Latency
- Provider availability
- Local or remote execution
- Privacy requirements
- Device resources
- User preferences

The result is not simply:

> "Which model should answer?"

It is:

> "How should this task be executed?"

Model selection is only one part of that decision.



## Backup

Jasper uses an encrypted `.jasp` backup format.

A backup can contain:

- Memory
- Memory graph
- Preferences
- Settings
- Skills
- MCP configuration
- Agent configuration
- Provider configuration
- Model configuration
- Encrypted credentials and API keys
- Project metadata
- Optionally selected project source code

Regenerable and heavy data is excluded, including:

- node_modules
- .git
- dist
- Caches
- Model binaries
- Runtime binaries

When restoring on another device, missing dependencies, models and runtime components can be downloaded or regenerated as needed.

The `.jasp` payload is encrypted as a whole using authenticated encryption so that opening the file as plain text does not expose its internal contents.



## Open Source Foundations

Jasper does not need to reinvent every part of its system.

Useful open-source projects can be adapted and changed to fit Jasper's architecture.

| Project | Jasper use |
|---|---|
| [Strix](https://github.com/usestrix/strix) | Security testing, vulnerability discovery, patching and verification |
| [Agency Agents](https://github.com/msitarzewski/agency-agents) | Specialist agent system |
| Open-source skill projects | Built-in and reusable skills |
| [Ponytail](https://github.com/DietrichGebert/ponytail) | Code efficiency |
| [Caveman](https://github.com/JuliusBrussee/caveman) | AI output and context efficiency |
| [Graphify](https://github.com/Graphify-Labs/graphify) | Memory graph foundation |

These projects are building blocks. Jasper can modify them where necessary instead of depending on their original structure forever.



## Design Principles

### Mobile First

Jasper is designed around phones from the start.

The goal is not to shrink a desktop IDE onto a phone. The interface and workflow should make sense on a small touchscreen.

### User Control

Users should be able to choose:

- Models
- Providers
- Agents
- Skills
- MCPs
- Tools
- Permissions
- Project settings

### Local First

Jasper should make as much use of the device as possible.

Cloud services are options, not requirements for the core development environment.

### Simple by Default

Jasper should expose useful controls without forcing users to understand every internal system.

Power users should still have access to deeper controls when they want them.

### Open

Jasper should make use of good existing open-source work and contribute improvements where possible.

### No Unnecessary Complexity

If something can be solved with a small, reliable solution, Jasper should not turn it into a large system just because it can.



## Project Status

Jasper is currently in the planning and research stage.

The core architecture and feature set are being defined before implementation begins.

The project will be built incrementally, with existing open-source projects being evaluated and adapted where they can save development time and provide proven solutions.



## License

License information will be added when the project is ready for release.
