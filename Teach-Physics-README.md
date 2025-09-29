# Teach Physics Chat Mode

The **Teach Physics** chat mode turns GitHub Copilot into an interactive physics teacher. It helps users learn physics concepts, solve problems, and connect theory to computation through clear explanations, examples, and step-by-step guidance.

## Key Features
- **Adaptive Explanations**: Adjusts to your physics knowledge level
- **Worked Examples**: Step-by-step solutions and explanations
- **Quiz Mode**: Interactive questions to test your understanding
- **Problem-Solving Mode**: Guided solutions to physics problems
- **Project Mode**: Build computational projects that apply physics concepts
- **Multi-Tool Integration**: Web search, code execution, file reading

## How It Works
- Ask about physics concepts, laws, or problem-solving strategies
- Request worked examples, visualizations, or simulations
- Try quiz mode to test your physics skills
- Use project mode for hands-on computational physics projects

## Example Prompts
- "Can you explain Newton's second law with an example?"
- "Quiz me on basic kinematics."
- "Help me build a Python simulation for projectile motion."
- "Walk me through solving this circuit problem step by step."

## Customization
You can customize this mode by editing `.github/chatmodes/Teach Physics.chatmode.md`:

1. **Modify the Description**: Change the teaching style or focus areas (e.g., focus on mechanics, electromagnetism, or modern physics)
2. **Adjust Tools**: Add or remove available tools (e.g., enable more visualization or computation tools)
3. **Update Instructions**: Modify the teaching approach, quiz style, or add specific physics topics

Example customization for mechanics focus:
```markdown
---
description: 'A mechanics-focused physics teacher that specializes in motion, forces, and energy.'
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
