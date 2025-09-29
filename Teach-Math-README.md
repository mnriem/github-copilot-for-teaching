# Teach Math Chat Mode

The **Teach Math** chat mode turns GitHub Copilot into a mathematics teacher bot. It helps users learn mathematical concepts, solve math problems, and connect math to programming through clear explanations, examples, and step-by-step guidance.

## Key Features
- **Adaptive Explanations**: Adjusts to your math knowledge level
- **Worked Examples**: Step-by-step solutions and explanations
- **Quiz Mode**: Interactive questions to test your understanding
- **Problem-Solving Mode**: Guided solutions to math problems
- **Project Mode**: Build programming projects that apply math concepts
- **Multi-Tool Integration**: Web search, code execution, file reading

## How It Works
- Ask about mathematical concepts, notation, or problem-solving strategies
- Request worked examples or visualizations
- Try quiz mode to test your math skills
- Use project mode for hands-on computational math projects

## Example Prompts
- "Can you explain the chain rule in calculus with an example?"
- "Quiz me on probability basics."
- "Help me build a Python simulation for rolling dice."
- "Walk me through solving this equation step by step."

## Customization
You can customize this mode by editing `.github/chatmodes/Teach Math.chatmode.md`:

1. **Modify the Description**: Change the teaching style or focus areas (e.g., focus on statistics, calculus, or applied math)
2. **Adjust Tools**: Add or remove available tools (e.g., enable more visualization or computation tools)
3. **Update Instructions**: Modify the teaching approach, quiz style, or add specific math topics

Example customization for statistics focus:
```markdown
---
description: 'A statistics-focused math teacher that specializes in probability, data analysis, and visualization.'
tools: [
	"web-search",
	"code-execution",
	"file-reader"
]
---
```

## Troubleshooting

### Chat Mode Not Appearing
- Ensure you're using VS Code version 1.101 or later
- Check the chat mode dropdown in the Chat view - custom modes appear there
- For workspace modes: ensure the `.github/chatmodes/` directory exists with the `.chatmode.md` file
- For user profile modes: use "Chat: Configure Chat Modes" to verify installation
- Restart VS Code if you just added the chat mode file

### Limited Functionality
- Verify your GitHub Copilot subscription includes chat features
- Check that all required tools are enabled in your Copilot settings

### Performance Issues
- Some features require internet connectivity for web search
- Code execution depends on your local development environment
