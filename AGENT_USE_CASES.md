# Cursor Agent Use Cases Guide

This document explains the different types of agents available in Cursor and when to use each one.

## Agent Types Overview

Cursor provides several types of agents, each optimized for different scenarios:

### 1. **Background Agent** 🤖
**Current Agent Type**

**Best For:**
- Long-running, autonomous tasks that don't require immediate user interaction
- Tasks that can be completed independently without constant feedback
- Batch operations across multiple files
- Refactoring that requires systematic changes
- Code generation from specifications
- Automated fixes and improvements

**Characteristics:**
- Operates autonomously in the background
- Doesn't require user interaction during execution
- Can work on complex, multi-step tasks
- Ideal for tasks that might take time to complete
- Can make decisions independently based on instructions

**Example Scenarios:**
- "Refactor all API calls to use async/await"
- "Add error handling to all database queries"
- "Update all components to use the new design system"
- "Generate unit tests for all service classes"
- "Migrate from JavaScript to TypeScript across the project"

**Limitations:**
- Won't ask for clarifications (proceeds based on best judgment)
- May not be ideal for tasks requiring frequent user input
- Best for well-defined tasks with clear requirements

---

### 2. **Chat Agent** 💬
**Interactive Conversational Agent**

**Best For:**
- Questions and explanations about code
- Getting help understanding codebases
- Quick code reviews and suggestions
- Debugging assistance
- Learning and exploration
- Iterative problem-solving with back-and-forth discussion

**Characteristics:**
- Interactive, conversational interface
- Can ask clarifying questions
- Great for exploratory tasks
- Provides explanations and reasoning
- Can help with understanding complex code

**Example Scenarios:**
- "How does this authentication system work?"
- "Why is this function throwing an error?"
- "Can you explain this algorithm?"
- "What's the best way to implement feature X?"
- "Review this code and suggest improvements"

**Limitations:**
- Less efficient for large-scale automated changes
- Requires more back-and-forth for complex refactoring
- Better for guidance than execution of large tasks

---

### 3. **Composer Agent** 🎼
**Multi-File Editing Agent**

**Best For:**
- Complex features requiring changes across multiple files
- Coordinated updates that need to maintain consistency
- Feature implementations spanning frontend and backend
- Architecture changes affecting multiple components
- Large refactoring operations

**Characteristics:**
- Can edit multiple files simultaneously
- Maintains context across files
- Ensures consistency across related changes
- Can create new files as needed
- Handles dependencies between files

**Example Scenarios:**
- "Implement user authentication with login, registration, and password reset"
- "Add a new API endpoint with frontend integration"
- "Refactor the state management to use Redux"
- "Create a new feature module with all necessary components"
- "Migrate from REST to GraphQL"

**Limitations:**
- May be overkill for simple, single-file changes
- Requires clear specifications for best results

---

### 4. **Inline Edit Agent** ✏️
**Focused, Quick Edits**

**Best For:**
- Quick fixes in a single location
- Small, focused changes
- Immediate corrections
- Simple refactoring in one file
- Adding comments or documentation

**Characteristics:**
- Fast and focused
- Minimal context needed
- Quick turnaround
- Low overhead

**Example Scenarios:**
- "Fix the typo in this function name"
- "Add error handling to this specific function"
- "Update this variable name"
- "Add a comment explaining this logic"
- "Fix the syntax error on line 42"

**Limitations:**
- Not suitable for multi-file changes
- Limited scope per operation

---

## Decision Matrix: Which Agent to Use?

| Task Type | Recommended Agent | Why |
|-----------|------------------|-----|
| Large refactoring (10+ files) | Background Agent | Autonomous, systematic execution |
| Understanding code | Chat Agent | Interactive explanations |
| Multi-file feature | Composer Agent | Coordinated changes |
| Quick single-file fix | Inline Edit Agent | Fast and focused |
| Code generation | Background Agent | Can work independently |
| Debugging help | Chat Agent | Interactive problem-solving |
| Architecture changes | Composer Agent | Cross-file coordination |
| Batch operations | Background Agent | Autonomous execution |
| Learning/exploration | Chat Agent | Conversational guidance |
| Simple corrections | Inline Edit Agent | Quick turnaround |

---

## Best Practices

### For Background Agents:
- ✅ Provide clear, complete instructions
- ✅ Specify file patterns or locations
- ✅ Include examples of desired output
- ✅ Define success criteria
- ❌ Don't use for tasks requiring frequent decisions
- ❌ Avoid for exploratory tasks

### For Chat Agents:
- ✅ Ask specific questions
- ✅ Request explanations
- ✅ Use for code reviews
- ✅ Get recommendations
- ❌ Not ideal for large automated changes

### For Composer Agents:
- ✅ Describe the complete feature
- ✅ Mention all affected areas
- ✅ Specify requirements clearly
- ✅ Include acceptance criteria
- ❌ Overkill for single-file changes

### For Inline Edit Agents:
- ✅ Use for focused, specific changes
- ✅ Quick fixes and corrections
- ✅ Simple refactoring
- ❌ Not for multi-file operations

---

## Current Context

You are currently using a **Background Agent**, which is ideal for:
- The autonomous execution of well-defined tasks
- Systematic changes across your codebase
- Tasks that can be completed without constant interaction
- Long-running operations that benefit from background processing

This agent will proceed with tasks based on your instructions and make reasonable decisions when details aren't fully specified, ensuring efficient completion of your coding tasks.
