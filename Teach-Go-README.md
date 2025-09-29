# Teach Go README

A specialized GitHub Copilot chat mode for learning Go (Weiqi/Baduk), the ancient strategy board game. This mode provides comprehensive Go instruction from basic rules to advanced concepts, with professional SGF-based position visualization using the sgf-render tool.

## Features

### Core Teaching Capabilities
- **Adaptive Learning**: Adjusts explanations based on your Go knowledge level
- **Proper Go Notation**: Uses standard coordinate system (A-J columns, 1-19 rows, skipping "I")
- **Comprehensive Coverage**: From basic rules to advanced professional game analysis
- **Interactive Learning**: Tsumego (life and death) problems and game analysis
- **Strategic Guidance**: Territory, influence, and positional judgment concepts

### Go-Specific Teaching Modes

#### 1. **Explanation Mode** (Default)
Clear, level-appropriate explanations of Go concepts with examples.

**Example Prompts:**
- "Explain the basic rules of Go"
- "What is sente and gote?"
- "How do I evaluate territory in the endgame?"
- "Explain the concept of thickness"

#### 2. **Tsumego Mode**
Interactive life and death problems with step-by-step solutions.

**Example Prompts:**
- "Give me a basic life and death problem"
- "Create a capturing problem for beginners"
- "Show me a complex ko situation"

#### 3. **Game Analysis Mode**
Guided analysis of Go games with professional insights.

**Example Prompts:**
- "Analyze this SGF file"
- "Show me a famous professional game"
- "Help me understand this joseki variation"

### Position Visualization with Professional SGF Rendering

This mode automatically creates SGF files and converts them to SVG images using the professional `sgf-render` tool:

- **Professional Quality**: Uses the Rust-based `sgf-render` tool for production-quality boards
- **Consistent Files**: Uses `goboard.sgf` and `goboard.svg` for all examples  
- **Rich Features**: Move numbers, coordinate labels, multiple styles, compact SVG output
- **No Custom Scripts**: Relies on maintained, professional tools from the Go community

## Installation

### Option 1: Direct from Repository
1. Open this repository in VS Code
2. Ensure you have GitHub Copilot enabled
3. The "Teach Go" mode will appear in your chat mode dropdown

### Option 2: Copy to Workspace
1. Copy `.github/chatmodes/Teach Go.chatmode.md` to your project's `.github/chatmodes/` folder
2. Restart VS Code
3. Select "Teach Go" from the chat mode dropdown

### Option 3: User Profile Installation
1. Copy the chat mode file to your VS Code user profile:
   - **Windows**: `%USERPROFILE%/.vscode/chatmodes/`
   - **macOS**: `~/.vscode/chatmodes/`
   - **Linux**: `~/.vscode/chatmodes/`
2. Restart VS Code

## Usage Examples

### Basic Go Rules
```
@Teach Go Explain how capturing works in Go
```
*Result: Creates `goboard.sgf` with capturing sequence + `goboard.svg` visual board*

### Go Coordinate System
```
@Teach Go Teach me the Go coordinate system on a 9x9 board
```
*Result: Explains A-J columns (skipping I), 1-9 rows, with examples like G5 for center*

### Opening Strategy
```
@Teach Go What are the key principles for the opening phase?
```
*Result: Shows opening moves with strategic commentary and visual board*

### Tsumego Practice
```
@Teach Go Give me a life and death problem suitable for a 15 kyu player
```
*Result: Creates problem position with solution sequence and visual display*

### Game Analysis
```
@Teach Go Analyze this professional game and explain the key moves
```

### Joseki Study
```
@Teach Go Show me the basic 3-3 invasion joseki
```

## Professional Go Board Visualization

The mode provides automatic Go board visualization using industry-standard tools:

1. **Dynamic SGF Creation**: Generates `goboard.sgf` with educational content when teaching Go concepts
2. **Professional Rendering**: Uses `sgf-render` tool for high-quality SVG conversion
3. **Automatic Cleanup**: Creates files only when needed, following the same pattern as other teaching modes
4. **Rich Visual Output**: Coordinate labels, move numbers, professional typography
5. **VS Code Integration**: SVG boards display directly in the editor with proper scaling

## Key Go Topics Covered

### Fundamentals
- Rules and basic gameplay
- **Go coordinate system** (A-J columns, 1-9/13/19 rows, skipping "I")
- Stone placement and capturing
- Territory and scoring
- Ko rule and basic tactics

### Opening (Fuseki)
- Corner enclosures (shimari)
- Side extensions and approaches
- Star point vs. 3-4 point openings
- Balancing territory and influence

### Middle Game (Chuban)
- Fighting techniques and tesuji
- Connection and cutting
- Sacrifice and exchange
- Direction of play

### Endgame (Yose)
- Territory calculation
- Sente vs. gote moves
- Endgame move values
- Ko threats and timing

### Advanced Concepts
- Professional game analysis
- Complex joseki variations
- Whole-board thinking
- Psychological aspects

## Customization

You can modify the chat mode by editing the `.chatmode.md` file:

### Skill Level Focus
Adjust the default explanations for specific skill levels (beginner, intermediate, advanced).

### Regional Variations
Adapt terminology and examples for different Go traditions (Japanese, Chinese, Korean).

### Specific Topics
Focus on particular aspects like:
- Pure tsumego training
- Opening theory specialization
- Endgame mastery
- Professional game studies

### SGF Visualization
Customize the SGF rendering:
- Board size preferences (9x9, 13x13, 19x19)
- Move numbering and coordinate display
- Focus on specific position types

## Requirements

- **VS Code**: Version 1.101 or higher
- **GitHub Copilot**: Individual, Business, or Enterprise subscription
- **Internet Connection**: For web searches and resource access
- **Rust/Cargo**: For installing sgf-render tool (optional but recommended)

## Troubleshooting

### Mode Not Appearing
- Verify the file is in the correct `.github/chatmodes/` directory
- Restart VS Code completely
- Check that GitHub Copilot is active and properly configured

### SGF Visualization Issues
- Install sgf-render tool: `cargo install sgf-render`
- Ensure PATH includes cargo bin directory
- Check that SVG files display properly in VS Code

### Limited Functionality
- Confirm your GitHub Copilot subscription is active
- Check that all required VS Code extensions are installed
- Verify workspace permissions for file creation

### Performance Issues
- Large SGF files may take time to render to SVG
- Consider breaking complex analyses into smaller segments
- Simple positions render quickly with sgf-render

## Educational Disclaimer

This teaching mode uses AI to provide Go instruction and should be used as a learning aid alongside:
- Qualified human Go teachers
- Established Go literature and resources
- Practical play experience
- Professional game studies

While this mode strives for accuracy, always verify critical Go concepts with authoritative sources, especially for tournament play or advanced theory.

## Go Resources Integration

The mode can help you explore:
- **Online Servers**: OGS, KGS, Fox Go, Tygem
- **Learning Platforms**: Go Quest, Cosumi, Interactive Go Tutorial  
- **Professional Games**: GoGoD, GoBase, Waltheri
- **Books**: Classic Go texts and modern strategy guides
- **Software**: Sabaki, KaTrain, Leela Zero, KataGo, sgf-render

Start your Go journey with: `@Teach Go I'm completely new to Go. Where should I start?`