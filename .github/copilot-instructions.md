# GitHub Copilot Instructions

## Project Overview

This repository provides custom GitHub Copilot chat modes for educational purposes. Each chat mode acts as a specialized teacher for different subjects (Programming, Math, Physics, Chemistry, Biology, Chess, and Music).

## Architecture

### Core Structure
- **Chat Mode Files**: `.github/chatmodes/*.chatmode.md` - Define custom Copilot teaching personalities
- **Documentation Files**: `Teach-{Subject}-README.md` - Individual documentation for each teaching mode
- **Main README**: `README.md` - Project overview, installation, and usage instructions

### Chat Mode Pattern
All chat modes follow a consistent structure with three key sections:

1. **YAML Frontmatter**: Defines description and available tools
2. **Core Teaching Instructions**: Subject-specific teaching behavior and methodology
3. **Mode-Specific Features**: Special capabilities (quiz mode, project mode, visualizations)

Example frontmatter pattern:
```yaml
---
description: 'You are a [subject] teacher bot that helps users learn [subject] concepts...'
tools: [
    "web-search",
    "code-execution", 
    "file-reader"
]
---
```

## Key Conventions

### Teaching Mode Behaviors
- **Adaptive Learning**: All modes assess user knowledge level and adapt explanations
- **Multi-Modal Support**: Three consistent modes across all subjects:
  - **Explanation Mode** (default): Clear, level-appropriate explanations
  - **Quiz Mode**: Interactive testing with immediate feedback
  - **Project Mode**: Step-by-step guided project building

### Specialized Features
- **Chess Mode**: Requires `eronnen.vscode-markdown-chess` extension, creates `game.md` files with chess notation
- **Math/Physics**: Supports LaTeX formatting and computational visualizations
- **Programming**: Emphasizes code execution, file analysis, and hands-on projects

### Tool Integration
All modes use standardized tools:
- `web-search`: Current information and tutorials
- `code-execution`: Live demonstrations and calculations
- `file-reader`: Analyzing user-provided content

## Development Workflow

### Adding New Teaching Modes
1. Create `.github/chatmodes/Teach {Subject}.chatmode.md` following the established pattern
2. Create corresponding `Teach-{Subject}-README.md` documentation
3. Update main `README.md` with new mode in the chat modes list
4. Follow the three-section structure: frontmatter, core instructions, special features

### File Naming Conventions
- Chat modes: `Teach {Subject}.chatmode.md` (with space, exact casing)
- Documentation: `Teach-{Subject}-README.md` (hyphenated, title case)
- Subjects: Biology, Chemistry, Chess, Math, Music, Physics, Programming

### Documentation Standards
- Include disclaimer about AI-generated content accuracy
- Provide installation instructions (3 options: repository direct, workspace copy, user profile)
- List key features, example prompts, customization guide, and troubleshooting
- Maintain consistent structure across all subject README files

## Extension Dependencies

- **Chess Mode**: Requires `eronnen.vscode-markdown-chess` for board visualization
- **VS Code Version**: 1.101+ for custom chat mode support
- **Copilot Subscription**: Individual, Business, or Enterprise required

## Common Patterns

### Error Handling
- All teaching modes include troubleshooting sections
- Common issues: mode not appearing, limited functionality, performance issues
- Standard solution: restart VS Code, check version requirements, verify subscription

### User Experience
- Modes auto-discover when repository is open in VS Code
- Accessible via chat mode dropdown or Command Palette
- Focus on educational disclaimers and safety (especially for lab-based subjects)

When working with this codebase, maintain consistency with existing patterns, ensure educational safety disclaimers, and test chat mode functionality in VS Code with GitHub Copilot enabled.