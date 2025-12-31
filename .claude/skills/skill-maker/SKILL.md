---
name: skill-maker
description: Generates new Claude Code skills with proper structure, YAML metadata, and documentation following official standards. Use when creating new skills, generating skill templates, or when the user requests to create/build/make a skill.
---

# Skill Maker

## Overview

This skill creates properly formatted Claude Code skills that follow official Claude Code documentation standards and best practices. It ensures consistency, quality, and compliance with skill development guidelines.

## Instructions

When a user requests to create a new skill, follow this comprehensive process:

### Step 1: Gather Requirements

**IMPORTANT**: Before generating any skill, you MUST gather complete information. If the user's prompt is missing any of the following, use the AskUserQuestion tool to clarify:

#### Required Information:
1. **Skill Purpose**: What should the skill do? What problem does it solve?
2. **Skill Name**: What should it be called? (If not provided, suggest based on purpose)
3. **When to Use**: When should Claude automatically invoke this skill? What keywords/scenarios trigger it?
4. **Tool Requirements**: Does this skill need specific tools? Should tool access be restricted?
5. **Complexity**: Is this a simple single-file skill or does it need multiple files (reference docs, examples, scripts)?

#### Optional Information (Ask if relevant):
- **Model Preference**: Should this skill use a specific model (e.g., haiku for speed, opus for quality)?
- **Dependencies**: Does this skill require external packages, libraries, or tools?
- **Examples**: Can the user provide examples of how they want to use the skill?
- **Scope**: Should this be personal (~/.claude/skills/), project (.claude/skills/), or plugin-based?

### Step 2: Validate Requirements

Before creating the skill, validate:

1. **Name Validation**:
   - Lowercase letters, numbers, and hyphens only
   - Maximum 64 characters
   - Must match directory name
   - Format: `kebab-case` (e.g., `skill-maker`, `pdf-processor`)

2. **Description Validation**:
   - Maximum 1024 characters
   - Must answer TWO questions:
     - **What**: What does this skill do?
     - **When**: When should Claude use it?
   - Include trigger keywords users might say

3. **Tool Restrictions** (if applicable):
   - Valid tools: Read, Write, Edit, Bash, Grep, Glob, WebFetch, WebSearch, LSP, Task, etc.
   - Use `Bash(command:*)` for command-specific restrictions
   - Only restrict if security/safety requires it

### Step 3: Determine Skill Structure

Choose the appropriate structure:

#### Simple Single-File Skill (< 500 lines):
```
skill-name/
└── SKILL.md
```

Use when:
- Instructions are straightforward
- No extensive reference material needed
- Fits comfortably in one file

#### Multi-File Skill (Progressive Disclosure):
```
skill-name/
├── SKILL.md           # Overview and essential instructions (< 500 lines)
├── reference.md       # Detailed API docs, specifications
├── examples.md        # Comprehensive usage examples
└── scripts/           # Utility scripts (not loaded into context)
    ├── helper.py
    └── validate.sh
```

Use when:
- Extensive documentation needed
- Multiple examples required
- Utility scripts enhance functionality
- SKILL.md would exceed 500 lines

### Step 4: Generate SKILL.md

Create the SKILL.md file with proper structure:

```yaml
---
name: skill-name
description: Clear description of what it does. Use when [trigger scenarios/keywords].
allowed-tools: Tool1, Tool2  # Optional - only if restricting access
model: model-name             # Optional - only if specific model needed
---

# Skill Name (Title Case)

## Overview

Brief introduction to the skill's purpose and capabilities.

## Instructions

Step-by-step guidance for Claude on how to use this skill:

1. **First step**: Clear action with context
2. **Second step**: What to do next
3. **Third step**: How to complete the task

### Subsection if needed

Additional detailed instructions organized logically.

## Examples

Provide concrete, realistic examples:

### Example 1: [Scenario Name]

**User request**: "Example user input"

**Process**:
1. Action taken
2. Next action
3. Result

### Example 2: [Another Scenario]

Show different use cases to clarify scope.

## Best Practices

- Key guideline 1
- Key guideline 2
- Important pattern or principle

## Error Handling

Common issues and how to resolve them:

- **Issue**: Description
  **Solution**: How to fix

## Additional Resources

(For multi-file skills only)

- For detailed API documentation, see [reference.md](reference.md)
- For more examples, see [examples.md](examples.md)
- To use helper script: `bash scripts/helper.sh <args>`

## Requirements

(If applicable)

List any dependencies:
```bash
pip install package-name
npm install package-name
```

## Validation Checklist

Before completing, verify:
- [ ] Task accomplished successfully
- [ ] Output meets requirements
- [ ] Best practices followed
- [ ] Errors handled appropriately
```

### Step 5: Create Supporting Files (if multi-file skill)

#### reference.md Template:
```markdown
# [Skill Name] Reference

## Detailed Documentation

### API Reference

Comprehensive technical details...

### Configuration Options

All available settings...

### Advanced Usage

Complex scenarios and edge cases...
```

#### examples.md Template:
```markdown
# [Skill Name] Examples

## Basic Examples

### Example 1: [Name]
[Detailed example with code]

### Example 2: [Name]
[Another detailed example]

## Advanced Examples

### Example 3: [Complex Scenario]
[Advanced usage pattern]

## Real-World Use Cases

### Use Case 1: [Scenario]
[Complete workflow example]
```

### Step 6: Create Directory and Files

1. Determine scope and create in appropriate location:
   - **Project-specific**: `.claude/skills/skill-name/`
   - **Personal**: `~/.claude/skills/skill-name/`

2. Create directory: `mkdir -p [location]/skill-name`

3. Write SKILL.md with proper YAML frontmatter

4. Create supporting files if multi-file structure

5. Create scripts directory if needed (ensure scripts are executable)

### Step 7: Validate Generated Skill

Perform quality checks:

1. **YAML Syntax**:
   - Starts with `---`
   - Ends with `---`
   - No tabs (spaces only for indentation)
   - Valid field names and values

2. **Content Quality**:
   - Clear, actionable instructions
   - Concrete examples provided
   - Best practices documented
   - Proper markdown formatting

3. **File Structure**:
   - Directory name matches skill name
   - All referenced files exist
   - Relative paths use forward slashes
   - SKILL.md under 500 lines

4. **Functional Requirements**:
   - Description triggers appropriately
   - Tool restrictions work as intended
   - Instructions are complete and unambiguous

### Step 8: Inform User

After creating the skill, provide:

1. **Summary**: What was created and where
2. **File locations**: Full paths to all created files
3. **How to use**: Example invocation
4. **Testing suggestion**: How to test the skill
5. **Next steps**: Any additional configuration needed

## Common Skill Patterns

### Pattern 1: Read-Only Analysis Skills

```yaml
---
name: code-analyzer
description: Analyzes code for patterns, issues, or metrics. Use when analyzing, reviewing, or auditing code.
allowed-tools: Read, Grep, Glob
---
```

Use when skill should NOT modify files.

### Pattern 2: Code Generation Skills

```yaml
---
name: test-generator
description: Generates unit tests for existing code. Use when creating tests or when user mentions testing, test coverage, or unit tests.
allowed-tools: Read, Write, Edit, Grep, Glob
---
```

Use when skill needs to create/modify code.

### Pattern 3: External Tool Integration

```yaml
---
name: api-tester
description: Tests REST APIs using curl. Use when testing APIs, endpoints, or making HTTP requests.
allowed-tools: Bash(curl:*), Read, Write
---
```

Use when skill wraps external command-line tools.

### Pattern 4: Research and Documentation Skills

```yaml
---
name: doc-researcher
description: Researches documentation and provides summaries. Use when looking up documentation, APIs, or library references.
allowed-tools: WebFetch, WebSearch, Read, Write
---
```

Use when skill needs to fetch external information.

### Pattern 5: Fast Processing Skills

```yaml
---
name: quick-formatter
description: Formats code quickly using standard tools. Use when formatting code or fixing style issues.
allowed-tools: Read, Edit, Bash
model: claude-sonnet-4-20250514
---
```

Use when speed is important (haiku model) but ensure task is simple enough.

## Quality Standards Checklist

Before finalizing any skill, ensure:

- [ ] **Naming**: Kebab-case, max 64 chars, meaningful
- [ ] **Description**: Answers "what" and "when", max 1024 chars
- [ ] **YAML**: Valid syntax, required fields present
- [ ] **Instructions**: Clear, step-by-step, actionable
- [ ] **Examples**: At least 2 concrete examples provided
- [ ] **Best Practices**: Key patterns documented
- [ ] **Structure**: Appropriate for complexity (single vs multi-file)
- [ ] **Length**: SKILL.md under 500 lines (use progressive disclosure if longer)
- [ ] **References**: All file references valid and exist
- [ ] **Tools**: Restrictions appropriate for security/safety
- [ ] **Model**: Specified only if needed (e.g., haiku for speed)
- [ ] **Dependencies**: Documented if required
- [ ] **Testing**: Testable and verifiable

## Error Prevention

### Common Mistakes to Avoid:

1. **Vague descriptions**: Always include trigger keywords
2. **Missing examples**: Always provide at least 2 examples
3. **Overly long SKILL.md**: Use progressive disclosure for complex skills
4. **Invalid YAML**: Use spaces, not tabs; validate syntax
5. **Wrong naming**: Ensure kebab-case, no uppercase, no underscores
6. **Incomplete instructions**: Make sure steps are actionable and complete
7. **No best practices**: Always include key patterns and guidelines
8. **Missing dependencies**: Document all required packages/tools
9. **Unrestricted tools**: Consider if tool access should be limited
10. **No validation**: Always verify skill structure and content

## Examples of Well-Structured Skills

### Example 1: Simple Academic Note Generator

```yaml
---
name: academic-note-generator
description: Creates structured academic notes in markdown format. Use when creating study notes, lecture summaries, or academic documentation.
allowed-tools: Read, Write, Edit, Grep, Glob
---

# Academic Note Generator

## Overview

Generates comprehensive, well-structured academic notes following scholarly standards with proper citations and organization.

## Instructions

1. **Gather topic information**: Ask user for subject, topic, and key concepts
2. **Research existing notes**: Check notes/ directory for related content
3. **Create structured outline**: Organize into sections (Introduction, Main Concepts, Examples, Summary)
4. **Write content**: Use formal academic tone, precise terminology
5. **Add cross-references**: Link to related notes and flashcards
6. **Save to notes/ directory**: Use descriptive kebab-case filename

## Examples

### Example 1: Creating a Physics Note

**User request**: "Create notes on Newton's Laws of Motion"

**Process**:
1. Create `notes/newtons-laws-of-motion.md`
2. Structure: Introduction → Three Laws → Applications → Summary
3. Use formal academic language
4. Include mathematical formulations
5. Cross-reference related topics

### Example 2: Updating Existing Note

**User request**: "Add examples to quantum mechanics notes"

**Process**:
1. Read existing `notes/quantum-mechanics.md`
2. Identify appropriate section
3. Add examples maintaining academic tone
4. Update cross-references if needed

## Best Practices

- Use formal, scholarly language
- Include proper citations and references
- Organize content hierarchically
- Cross-reference related materials
- Maintain consistent formatting
```

### Example 2: Multi-File Skill with Scripts

```yaml
---
name: pdf-extractor
description: Extracts text, tables, and images from PDF files for academic use. Use when working with PDF documents, research papers, or document extraction.
allowed-tools: Bash(python:*), Read, Write
---

# PDF Extractor

## Overview

Comprehensive PDF processing for academic research, including text extraction, table parsing, and image extraction.

## Quick Start

For basic text extraction:
```python
python scripts/extract_text.py input.pdf output.txt
```

For detailed usage patterns, see [examples.md](examples.md).
For complete API reference, see [reference.md](reference.md).

## Requirements

```bash
pip install pypdf pdfplumber pillow
```

## Common Tasks

### Extract Text
1. Run extraction script: `python scripts/extract_text.py <pdf_file>`
2. Review output in specified location
3. Post-process if needed

### Extract Tables
1. Use table extractor: `python scripts/extract_tables.py <pdf_file>`
2. Tables saved as CSV files
3. Verify data accuracy

## Scripts

- `scripts/extract_text.py`: Text extraction utility
- `scripts/extract_tables.py`: Table parsing tool
- `scripts/extract_images.py`: Image extraction helper

## Additional Resources

- [examples.md](examples.md): Comprehensive usage examples
- [reference.md](reference.md): Detailed API documentation
```

## Usage Workflow

When user requests: "Create a skill that [does X]"

1. **Analyze request**: Identify what X requires
2. **Ask questions**: Use AskUserQuestion for missing details:
   - What should the skill be named?
   - When should it be automatically triggered?
   - Does it need specific tools?
   - Should it be simple or comprehensive?
3. **Design skill**: Determine structure and components
4. **Generate files**: Create SKILL.md and supporting files
5. **Validate**: Run through quality checklist
6. **Deliver**: Inform user of what was created and how to use it

## Testing Recommendations

After creating a skill, suggest to user:

1. **Test invocation**: Try using trigger keywords from description
2. **Debug mode**: Run `claude --debug` to see skill loading
3. **Validate YAML**: Ensure no syntax errors
4. **Test functionality**: Verify skill works as intended
5. **Iterate**: Refine based on actual usage

## Best Practices for Skill-Maker

- **Always ask questions**: Better to clarify than assume
- **Follow standards**: Consistency is key for quality
- **Provide examples**: Show, don't just tell
- **Think about triggers**: Description should match user language
- **Consider scope**: Right level of complexity for the task
- **Document dependencies**: Don't leave users guessing
- **Validate output**: Check generated files before confirming
- **Test mentally**: Would this skill work as written?
