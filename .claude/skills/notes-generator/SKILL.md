---
name: notes-generator
description: Generates comprehensive academic notes following Bloom's taxonomy methodology (Remember, Understand, Apply, Analyze, Evaluate, Create). Use when creating study notes, generating educational content, or when user mentions notes, study materials, Bloom's taxonomy, or learning objectives.
allowed-tools: Read, Write, Edit, Grep, Glob, WebFetch, WebSearch
---

# Notes Generator

## Overview

This skill generates comprehensive, pedagogically sound academic notes structured according to Bloom's taxonomy. Notes can be created from a topic title alone or enhanced with reference files. All generated content maintains scholarly rigor and formal academic tone as required by the project's educational standards.

## Bloom's Taxonomy Framework

The six levels of Bloom's taxonomy guide the structure of all generated notes:

1. **Remember**: Recall facts, terms, basic concepts, and foundational knowledge
2. **Understand**: Explain ideas, interpret information, summarize concepts
3. **Apply**: Use knowledge in new situations, implement solutions, execute procedures
4. **Analyze**: Break down information, examine relationships, distinguish between components
5. **Evaluate**: Make judgments, critique arguments, justify decisions
6. **Create**: Synthesize information, design solutions, formulate new perspectives

## Instructions

### Step 1: Gather Input Information

Determine the input mode:

**Mode A: Topic-Based Generation**
- User provides only a topic title
- Generate comprehensive notes through research and structured knowledge
- Example: "Generate notes on photosynthesis"

**Mode B: Reference-Based Generation**
- User provides topic title AND reference files (PDFs, articles, textbooks, etc.)
- Extract and synthesize information from provided sources
- Example: "Generate notes on machine learning using these research papers"

### Step 2: Research and Preparation

1. **Check existing content**: Search the `notes/` directory for related topics
   - Use Glob to find similar note files
   - Use Grep to identify related concepts
   - Identify opportunities for cross-referencing

2. **Gather information**:
   - **If topic-based**: Use knowledge base and WebSearch if needed for current information
   - **If reference-based**: Read all provided reference files thoroughly
   - Extract key concepts, definitions, theories, and examples
   - Identify the academic level and depth required

3. **Validate topic scope**: Ensure topic is well-defined and appropriately scoped
   - Too broad: Suggest breaking into multiple notes
   - Too narrow: Suggest combining with related topic

### Step 3: Structure Notes According to Bloom's Taxonomy

Create a hierarchical structure with the following mandatory sections:

```markdown
# [Topic Title]

## Metadata
- **Subject Area**: [Field/Discipline]
- **Academic Level**: [Introductory/Intermediate/Advanced]
- **Prerequisites**: [Required prior knowledge]
- **Related Topics**: [Cross-references to other notes]
- **Date Created**: [YYYY-MM-DD]

## I. Remember: Foundational Knowledge

### Key Terms and Definitions
- Term 1: Precise academic definition
- Term 2: Precise academic definition

### Fundamental Facts
- Core fact 1
- Core fact 2

### Basic Concepts
- Concept 1: Brief explanation
- Concept 2: Brief explanation

## II. Understand: Comprehension and Interpretation

### Conceptual Explanations
Detailed explanations of how concepts work, their mechanisms, and underlying principles.

### Visual Representations
[Describe diagrams, charts, or visual models that aid understanding]

### Comparative Analysis
Similarities and differences between related concepts or approaches.

### Summary of Main Ideas
Concise synthesis of core understandings.

## III. Apply: Practical Application

### Application Scenarios
Concrete situations where concepts can be applied.

### Procedural Steps
Step-by-step processes for implementing concepts.

### Worked Examples
Detailed examples demonstrating application of principles.

### Practice Problems
[If applicable] Problems for reinforcing application skills.

## IV. Analyze: Critical Examination

### Component Analysis
Breaking down complex systems into constituent parts.

### Relationships and Patterns
Identifying connections, dependencies, and organizational structures.

### Comparison and Contrast
Detailed analytical comparison of theories, methods, or approaches.

### Critical Examination
Strengths and limitations of various approaches or theories.

## V. Evaluate: Assessment and Critique

### Evidence and Support
Evaluation of empirical evidence and theoretical support.

### Critical Perspectives
Different viewpoints and scholarly debates.

### Limitations and Controversies
Acknowledged weaknesses, gaps, and ongoing debates.

### Criteria for Assessment
Standards for judging quality, validity, or effectiveness.

## VI. Create: Synthesis and Innovation

### Integration of Concepts
How ideas combine to form comprehensive understanding.

### Novel Applications
Creative ways to apply knowledge in new contexts.

### Research Questions
Open questions for further investigation.

### Future Directions
Emerging trends and potential developments in the field.

## References and Sources
[If reference files provided, cite them here]
[Include cross-references to related notes, flashcards, and quizzes]

## Notes for Review
- Key points requiring memorization
- Concepts requiring deeper study
- Connections to explore further
```

### Step 4: Content Generation Guidelines

**Academic Tone Requirements** (from CLAUDE.md):
- Use formal, scholarly language appropriate for academic contexts
- Employ precise terminology and well-structured explanations
- Maintain objectivity and evidence-based reasoning
- Avoid colloquialisms, informal expressions, and casual language
- Present information in a clear, pedagogical manner suitable for learning

**Quality Standards**:
- **Accuracy**: Ensure all information is factually correct and current
- **Depth**: Provide comprehensive coverage appropriate to academic level
- **Clarity**: Use clear, well-structured explanations
- **Evidence**: Support claims with evidence, examples, or reasoning
- **Organization**: Maintain logical flow and hierarchical structure
- **Completeness**: Address all six levels of Bloom's taxonomy

**Integration with Reference Files**:
- Extract relevant information from each provided file
- Synthesize information across multiple sources
- Cite sources appropriately in References section
- Highlight conflicting viewpoints if sources disagree
- Note which Bloom level each piece of information addresses

### Step 5: Cross-Reference Integration

1. **Link to related notes**: Identify connections to existing notes
   - Format: `See also: [Topic Name](../notes/topic-name.md)`

2. **Suggest flashcard topics**: Identify key facts for flashcard creation
   - Format: `Flashcard recommended: [Concept/Term]`

3. **Propose quiz questions**: Note areas suitable for assessment
   - Format: `Quiz topic: [Assessment area]`

### Step 6: File Management

1. **Generate filename**: Convert topic to kebab-case
   - Example: "Cellular Respiration" → `cellular-respiration.md`

2. **Save to notes/ directory**: Use Write tool to create file
   - Path: `notes/[topic-name].md`

3. **Create directory if needed**: Ensure notes/ directory exists
   - Command: `mkdir -p notes/`

4. **Verify output**: Confirm file was created successfully

### Step 7: User Confirmation

Provide summary to user:
1. **File created**: Full path to generated note
2. **Structure overview**: Brief description of sections included
3. **Cross-references**: Related materials identified
4. **Next steps**: Suggest creating companion flashcards/quizzes
5. **Review recommendation**: Encourage user to review and refine

## Examples

### Example 1: Topic-Based Generation

**User request**: "Generate notes on Newton's Laws of Motion"

**Process**:
1. Search `notes/` directory for related physics topics
2. Gather comprehensive information on Newton's three laws
3. Structure according to Bloom's taxonomy:
   - **Remember**: Define three laws, key terms (inertia, force, momentum)
   - **Understand**: Explain how each law works, provide interpretations
   - **Apply**: Show worked examples (calculating forces, motion scenarios)
   - **Analyze**: Examine relationships between laws, compare with other theories
   - **Evaluate**: Discuss limitations, when laws don't apply (quantum scale)
   - **Create**: Propose experimental designs, novel applications
4. Create file: `notes/newtons-laws-of-motion.md`
5. Add cross-references to classical-mechanics.md (if exists)
6. Suggest flashcards for three laws and key equations

**Output**: Comprehensive note file with academic rigor, mathematical formulations, and practical examples.

### Example 2: Reference-Based Generation

**User request**: "Generate notes on machine learning from these papers: paper1.pdf, paper2.pdf"

**Process**:
1. Read both provided PDF files using Read tool
2. Extract key concepts, methodologies, and findings from each
3. Synthesize information across sources:
   - **Remember**: Definitions from papers, key algorithms mentioned
   - **Understand**: Explain methodologies used by authors
   - **Apply**: Include code examples or procedures from papers
   - **Analyze**: Compare approaches in paper1 vs paper2
   - **Evaluate**: Critique methodologies, note limitations authors mention
   - **Create**: Identify research gaps, propose extensions
4. Create file: `notes/machine-learning-synthesis.md`
5. Cite both papers in References section
6. Cross-reference existing AI or statistics notes

**Output**: Synthesized note integrating multiple sources with proper citations and critical analysis.

### Example 3: Updating Existing Notes

**User request**: "Add application examples to the quantum-mechanics.md notes"

**Process**:
1. Read existing `notes/quantum-mechanics.md`
2. Identify "III. Apply: Practical Application" section
3. Generate relevant application examples:
   - Quantum computing applications
   - Semiconductor technology
   - Laser physics
4. Edit file to insert new content maintaining academic tone
5. Ensure consistency with existing structure
6. Update metadata (Date Modified)

**Output**: Enhanced note with expanded application section.

## Best Practices

### Content Quality
- **Precision**: Use exact terminology; define specialized terms on first use
- **Evidence-based**: Support assertions with reasoning or citations
- **Pedagogical structure**: Build from simple to complex concepts
- **Balanced coverage**: Ensure all six Bloom levels receive appropriate attention
- **Consistency**: Maintain uniform formatting and style throughout

### Bloom's Taxonomy Application
- **Remember**: Focus on facts that must be memorized (definitions, dates, formulas)
- **Understand**: Provide explanations, not just definitions
- **Apply**: Always include concrete, worked examples
- **Analyze**: Show relationships, patterns, and component structures
- **Evaluate**: Present multiple perspectives and critical assessments
- **Create**: Encourage synthesis and original thinking

### Academic Standards
- **Formal language**: Avoid contractions, slang, and casual expressions
- **Objectivity**: Present information neutrally; note when presenting opinions
- **Clarity**: Use clear, direct sentences; avoid unnecessarily complex prose
- **Organization**: Use headings, subheadings, and lists for readability
- **Citations**: Credit sources appropriately when using reference materials

### File Organization
- **Naming conventions**: Use kebab-case for all filenames
- **Directory structure**: Always save to `notes/` directory
- **Cross-references**: Use relative paths for internal links
- **Metadata**: Always include complete metadata section
- **Versioning**: Update date modified when editing existing notes

## Error Handling

### Common Issues and Solutions

**Issue**: Topic too broad to cover comprehensively
- **Solution**: Ask user if they want to narrow scope or create multiple notes
- **Example**: "Introduction to Biology" → Break into cellular biology, genetics, ecology

**Issue**: Insufficient information from reference files
- **Solution**: Inform user that additional sources may be needed
- **Action**: Supplement with general knowledge where appropriate, note limitations

**Issue**: Notes directory doesn't exist
- **Solution**: Create directory automatically before writing file
- **Command**: `mkdir -p notes/`

**Issue**: Conflicting information across reference sources
- **Solution**: Present both perspectives in "Evaluate" section
- **Format**: "Source A argues X, while Source B contends Y. The evidence suggests..."

**Issue**: Topic requires specialized notation (mathematical, chemical, etc.)
- **Solution**: Use appropriate markdown syntax or Unicode symbols
- **Examples**: LaTeX for math, chemical formulas, musical notation

**Issue**: Existing note file with same name
- **Solution**: Ask user if they want to:
  1. Overwrite existing note
  2. Merge new content with existing
  3. Create with different filename

## Integration with Project Structure

This skill integrates seamlessly with the scholarly-ai project:

### Directory Alignment
- **Output location**: `notes/` directory as specified in CLAUDE.md
- **Related materials**: Cross-reference `flashcards/` and `quizzes/` directories
- **Consistency**: Follow project's academic tone requirements

### Workflow Integration
1. **Notes generation** (this skill) → Comprehensive study materials
2. **Flashcard generation** → Extract key facts from notes
3. **Quiz generation** → Create assessments based on notes

### Academic Tone Compliance
All generated notes automatically adhere to CLAUDE.md requirements:
- Formal, scholarly language
- Precise terminology
- Well-structured explanations
- Objectivity and evidence-based reasoning
- Clear, pedagogical presentation

## Validation Checklist

Before completing note generation, verify:

- [ ] All six Bloom's taxonomy levels are addressed comprehensively
- [ ] Academic tone is maintained throughout (formal, scholarly, precise)
- [ ] Metadata section is complete and accurate
- [ ] Content is factually accurate and up-to-date
- [ ] File saved to `notes/` directory with kebab-case filename
- [ ] Cross-references to related materials are included
- [ ] Reference files (if provided) are properly cited
- [ ] Structure follows the prescribed template
- [ ] Examples are concrete and illustrative
- [ ] Content is appropriate for specified academic level
- [ ] Markdown formatting is correct and consistent
- [ ] User informed of file location and next steps

## Advanced Features

### Adaptive Depth
Adjust content depth based on:
- Academic level specified (introductory/intermediate/advanced)
- Topic complexity
- Reference material depth
- User's indicated background knowledge

### Multi-Source Synthesis
When provided multiple reference files:
- Compare and contrast different perspectives
- Identify common themes across sources
- Note contradictions or disagreements
- Synthesize into coherent narrative
- Properly attribute ideas to sources

### Progressive Enhancement
For existing notes:
- Add missing Bloom levels
- Expand thin sections
- Update outdated information
- Add new examples or applications
- Improve cross-referencing

## Requirements

No external dependencies required. All functionality uses built-in tools:
- Read: For processing reference files
- Write: For creating new note files
- Edit: For updating existing notes
- Grep/Glob: For finding related content
- WebFetch/WebSearch: For research (when needed)

## Testing and Quality Assurance

To ensure quality, each generated note should:
1. **Read naturally**: Flow logically from foundational to advanced concepts
2. **Be comprehensive**: Cover topic thoroughly at appropriate depth
3. **Maintain standards**: Adhere to academic tone and formatting requirements
4. **Provide value**: Offer clear learning pathway through Bloom's levels
5. **Enable assessment**: Support flashcard and quiz generation

## Conclusion

This skill transforms topics and reference materials into pedagogically sound, academically rigorous study notes. By consistently applying Bloom's taxonomy, it ensures comprehensive coverage from basic recall to creative synthesis, supporting effective learning and retention.
