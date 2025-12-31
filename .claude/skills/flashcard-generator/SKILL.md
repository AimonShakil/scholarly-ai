---
name: flashcard-generator
description: Generates professional spaced-repetition flashcards from academic notes following evidence-based learning principles. Creates cards in Anki-compatible format with proper question-answer structure, tags, and metadata. Use when creating flashcards, study cards, making review materials, or when user mentions flashcards, Anki, spaced repetition, or active recall.
allowed-tools: Read, Write, Edit, Grep, Glob
---

# Flashcard Generator

## Overview

This skill generates professional-quality flashcards from academic notes using evidence-based learning principles. Flashcards follow the format used by spaced repetition systems (SRS) like Anki, with proper front/back structure, progressive difficulty, and organizational metadata. All flashcards maintain academic rigor and support effective long-term retention.

## Evidence-Based Flashcard Principles

Professional flashcards adhere to these cognitive science principles:

1. **Atomicity**: One concept per card (avoid complex, multi-part questions)
2. **Clarity**: Clear, unambiguous questions with precise answers
3. **Progressive Difficulty**: Range from basic recall to application and analysis
4. **Active Recall**: Questions that require retrieval, not recognition
5. **Elaborative Encoding**: Include context and connections to aid memory
6. **Mnemonics**: Use memory aids where appropriate
7. **Interleaving**: Mix different types of questions and topics
8. **Spaced Repetition Compatible**: Format supports SRS algorithms

## Flashcard Format Specification

Each flashcard file uses this structured markdown format:

```markdown
# [Topic Name] - Flashcards

**Source Note**: [Link to source note file]
**Created**: [YYYY-MM-DD]
**Total Cards**: [Number]
**Tags**: #subject-area #topic #difficulty-level

---

## Card 1
**Type**: Basic
**Difficulty**: Easy
**Tags**: #definition #remember

### Front
What is [term/concept]?

### Back
[Precise definition]

**Context**: [Brief explanation or example]
**Mnemonic**: [If applicable]

---

## Card 2
**Type**: Cloze
**Difficulty**: Medium
**Tags**: #understand #process

### Front
The process of {{c1::photosynthesis}} converts {{c2::light energy}} into {{c3::chemical energy}} in the form of {{c4::glucose}}.

### Back
*Auto-generated from cloze deletions*

**Context**: Occurs in chloroplasts of plant cells
**Related**: Cards 5, 12

---

## Card 3
**Type**: Application
**Difficulty**: Hard
**Tags**: #apply #problem-solving

### Front
Given a force of 50N applied to a 10kg mass, calculate the acceleration.

### Back
**Answer**: 5 m/s²

**Solution**:
Using Newton's Second Law: F = ma
50N = 10kg × a
a = 50N ÷ 10kg = 5 m/s²

**Key Concept**: F = ma relationship

---
```

## Card Types

### 1. Basic (Question → Answer)
- Simple recall questions
- Definitions, facts, terminology
- Who, what, when, where questions

### 2. Cloze Deletion (Fill-in-the-blank)
- Statements with key terms removed
- Supports multiple deletions ({{c1::}}, {{c2::}}, etc.)
- Excellent for processes, sequences, and relationships

### 3. Application (Problem → Solution)
- Requires applying knowledge
- Math problems, case studies
- Includes worked solutions

### 4. Comparison (Compare/Contrast)
- Similarities and differences
- Advantages and disadvantages
- Before and after scenarios

### 5. Image Occlusion (Visual → Labels)
- [Image description] with labeled components
- Diagrams, charts, anatomical structures
- Note: Actual images referenced, not embedded

### 6. List/Enumeration (Category → Items)
- "Name the X types of Y"
- Ordered sequences or unordered sets
- Mnemonics helpful here

## Instructions

### Step 1: Identify Source Material

Determine the input source:

**Option A: From Existing Note**
- User specifies a note file: "Create flashcards from quantum-mechanics.md"
- Read the specified note file
- Extract all relevant information

**Option B: From Topic (Auto-find Note)**
- User mentions topic: "Create flashcards for photosynthesis"
- Search `notes/` directory for matching note
- If not found, inform user and ask if they want note generated first

**Option C: From Multiple Notes**
- User wants flashcards covering multiple topics
- Read all specified note files
- Create integrated flashcard set with cross-topic connections

### Step 2: Analyze Source Content

1. **Read the source note(s)** completely using Read tool

2. **Identify flashcard-worthy content**:
   - **Definitions**: All key terms and concepts
   - **Facts**: Important dates, names, figures, formulas
   - **Processes**: Step-by-step procedures or sequences
   - **Relationships**: Cause-effect, comparisons, hierarchies
   - **Applications**: Problem-solving scenarios and examples
   - **Critical points**: Core principles and theories

3. **Map to Bloom's taxonomy** (if source note uses it):
   - Remember level → Basic flashcards
   - Understand level → Cloze and comparison flashcards
   - Apply level → Application flashcards
   - Analyze level → Complex comparison and reasoning flashcards
   - Evaluate/Create → Advanced application scenarios

4. **Determine difficulty distribution**:
   - 40% Easy (basic recall, definitions)
   - 40% Medium (understanding, simple application)
   - 20% Hard (complex application, analysis)

### Step 3: Generate Flashcards

For each identified concept, create appropriate flashcard(s):

#### A. Basic Flashcards (Definitions and Facts)

**Question design**:
- Start with: "What is...", "Define...", "Who was...", "When did..."
- Be specific and unambiguous
- Include context if term has multiple meanings

**Answer design**:
- Concise but complete
- Include context or example
- Add mnemonic if helpful

**Example**:
```markdown
## Card 12
**Type**: Basic
**Difficulty**: Easy
**Tags**: #definition #biology #remember

### Front
What is osmosis?

### Back
The movement of water molecules across a selectively permeable membrane from an area of higher water concentration to an area of lower water concentration.

**Context**: A type of passive transport; does not require energy
**Mnemonic**: "Water goes with the flow" (high to low concentration)
```

#### B. Cloze Deletion Flashcards (Processes and Relationships)

**Cloze design**:
- Use {{c1::text}} format for deletions
- Number deletions logically ({{c1::}}, {{c2::}}, etc.)
- Each deletion becomes a separate card automatically
- Keep sentences focused (one concept)

**Example**:
```markdown
## Card 15
**Type**: Cloze
**Difficulty**: Medium
**Tags**: #process #biology #understand

### Front
During cellular respiration, {{c1::glucose}} is broken down in the presence of {{c2::oxygen}} to produce {{c3::ATP}}, {{c4::carbon dioxide}}, and {{c5::water}}.

### Back
*Auto-generated from cloze deletions*

**Context**: Occurs in mitochondria; equation: C₆H₁₂O₆ + 6O₂ → 6CO₂ + 6H₂O + ATP
**Related**: Cards 14 (aerobic vs anaerobic), 16 (glycolysis)
```

#### C. Application Flashcards (Problem-Solving)

**Problem design**:
- Present realistic scenario or problem
- Provide necessary information
- Ask specific question

**Solution design**:
- Show complete worked solution
- Explain reasoning at each step
- Highlight key concepts or formulas used

**Example**:
```markdown
## Card 23
**Type**: Application
**Difficulty**: Hard
**Tags**: #apply #physics #calculation

### Front
A 2kg object is moving at 10 m/s. How much kinetic energy does it possess?

### Back
**Answer**: 100 Joules

**Solution**:
1. Use kinetic energy formula: KE = ½mv²
2. Substitute values: KE = ½(2kg)(10m/s)²
3. Calculate: KE = ½(2)(100) = 100J

**Key Concept**: Kinetic energy is proportional to mass and velocity squared
**Common Error**: Forgetting to square the velocity
```

#### D. Comparison Flashcards

**Design**:
- Ask for similarities or differences
- Request advantages/disadvantages
- Compare theories, methods, or concepts

**Example**:
```markdown
## Card 18
**Type**: Comparison
**Difficulty**: Medium
**Tags**: #compare #biology #analyze

### Front
Compare and contrast mitosis and meiosis.

### Back
**Similarities**:
- Both involve cell division
- Both include DNA replication
- Both use spindle fibers

**Differences**:
- Mitosis: 2 identical diploid cells; meiosis: 4 unique haploid cells
- Mitosis: 1 division; meiosis: 2 divisions
- Mitosis: somatic cells; meiosis: gametes

**Context**: Mitosis for growth/repair, meiosis for reproduction
```

#### E. List/Enumeration Flashcards

**Design**:
- Ask for complete list or sequence
- Provide count if helpful ("Name the 3...")
- Order matters for sequences

**Example**:
```markdown
## Card 9
**Type**: List
**Difficulty**: Medium
**Tags**: #list #remember #sequence

### Front
List the steps of the scientific method in order.

### Back
1. Observation
2. Question
3. Hypothesis
4. Experiment
5. Analysis
6. Conclusion
7. Communication

**Mnemonic**: "Only Quiet Hippos Eat Apples Carefully, Chewing"
**Note**: Some variations include "Replication" after conclusion
```

### Step 4: Add Metadata and Organization

For each flashcard, include:

1. **Card number**: Sequential numbering
2. **Type**: Basic, Cloze, Application, Comparison, List, Image
3. **Difficulty**: Easy, Medium, Hard
4. **Tags**: Minimum 2-3 relevant tags
   - Subject area (e.g., #biology, #physics, #history)
   - Topic (e.g., #photosynthesis, #newton-laws)
   - Cognitive level (e.g., #remember, #understand, #apply)
   - Card type (e.g., #definition, #calculation, #process)

5. **Context**: Additional explanatory information
6. **Mnemonics**: Memory aids where applicable
7. **Related cards**: Cross-references to connected concepts

### Step 5: File Management and Organization

1. **Generate filename**: Match source note name
   - Source: `notes/cellular-respiration.md`
   - Output: `flashcards/cellular-respiration.md`

2. **Ensure directory exists**:
   ```bash
   mkdir -p flashcards/
   ```

3. **Create flashcard file** with complete header:
   ```markdown
   # [Topic Name] - Flashcards

   **Source Note**: [../notes/topic-name.md](../notes/topic-name.md)
   **Created**: YYYY-MM-DD
   **Last Modified**: YYYY-MM-DD
   **Total Cards**: [Number]
   **Difficulty Distribution**: Easy: X, Medium: Y, Hard: Z
   **Tags**: #subject #topic #difficulty

   ## Study Recommendations
   - Review new cards: [Number] cards/day
   - Estimated time: [X] minutes for initial review
   - Best for: [Academic level/background]

   ---
   ```

4. **Write all cards** following the format specification

5. **Add summary section** at end:
   ```markdown
   ---

   ## Summary Statistics
   - Total Cards: [Number]
   - Basic: [Number]
   - Cloze: [Number]
   - Application: [Number]
   - Comparison: [Number]
   - List: [Number]
   - Image: [Number]

   ## Tags Index
   - #remember: Cards [list]
   - #understand: Cards [list]
   - #apply: Cards [list]
   - #analyze: Cards [list]

   ## Related Materials
   - Source Notes: [Links]
   - Related Flashcard Sets: [Links]
   - Recommended Quizzes: [Links]
   ```

### Step 6: Quality Assurance

Verify each flashcard meets quality standards:

**Clarity Check**:
- [ ] Question is unambiguous
- [ ] Answer is precise and complete
- [ ] No unnecessary complexity

**Atomicity Check**:
- [ ] One concept per card
- [ ] Can be answered in <30 seconds
- [ ] Doesn't require multiple mental steps

**Academic Rigor Check**:
- [ ] Terminology is accurate
- [ ] Information is factually correct
- [ ] Academic tone maintained
- [ ] Sources are acknowledged

**Usability Check**:
- [ ] Appropriate difficulty level
- [ ] Proper tags assigned
- [ ] Metadata complete
- [ ] Format is consistent

### Step 7: User Confirmation

Provide comprehensive summary:

1. **File created**: Path to flashcard file
2. **Statistics**: Number of cards by type and difficulty
3. **Coverage**: What topics/concepts are covered
4. **Import instructions**: How to import into Anki or other SRS
5. **Study recommendations**: Suggested review schedule
6. **Next steps**: Create related quiz or generate more flashcards

## Examples

### Example 1: Generate from Existing Note

**User request**: "Create flashcards from the quantum-mechanics.md notes"

**Process**:
1. Read `notes/quantum-mechanics.md`
2. Identify key concepts:
   - Wave-particle duality (definition)
   - Heisenberg uncertainty principle (formula and meaning)
   - Schrödinger equation (application)
   - Quantum superposition (concept)
   - Observables and operators (relationship)
3. Generate 25 flashcards:
   - 10 Basic (definitions, key terms)
   - 8 Cloze (processes, equations)
   - 4 Application (calculations, problem-solving)
   - 2 Comparison (classical vs quantum)
   - 1 List (postulates of quantum mechanics)
4. Create file: `flashcards/quantum-mechanics.md`
5. Distribution: 10 Easy, 10 Medium, 5 Hard

**Output**:
```
Created: flashcards/quantum-mechanics.md
- 25 flashcards generated
- Difficulty: 40% Easy, 40% Medium, 20% Hard
- Coverage: All major concepts from source note
- Estimated study time: 15 minutes initial review
```

### Example 2: Generate from Topic (Auto-find)

**User request**: "Make flashcards for photosynthesis"

**Process**:
1. Search `notes/` directory: Find `notes/photosynthesis.md`
2. Read note and extract concepts
3. Generate 30 flashcards covering:
   - Light-dependent reactions
   - Calvin cycle
   - Chloroplast structure
   - Key molecules (chlorophyll, ATP, NADPH)
   - Overall equation
4. Include mnemonics for complex processes
5. Create file: `flashcards/photosynthesis.md`

**Output**: Comprehensive flashcard set with process diagrams described

### Example 3: Generate from Multiple Notes

**User request**: "Create a flashcard set covering all chemistry notes"

**Process**:
1. Use Glob to find all notes: `notes/*chemistry*.md`
2. Read all matching files:
   - `notes/organic-chemistry.md`
   - `notes/inorganic-chemistry.md`
   - `notes/chemical-bonding.md`
3. Generate integrated set (60 cards):
   - Organize by topic area
   - Create cross-topic comparison cards
   - Tag by specific chemistry sub-field
4. Create file: `flashcards/chemistry-comprehensive.md`

**Output**: Master flashcard set with cross-references between chemistry topics

### Example 4: Update Existing Flashcard Set

**User request**: "Add more application problems to the physics flashcards"

**Process**:
1. Read existing `flashcards/physics.md`
2. Identify current application cards
3. Review source note for additional problems
4. Generate 5 new application flashcards
5. Edit file to insert new cards with sequential numbering
6. Update summary statistics

**Output**: Enhanced flashcard set with additional practice problems

## Best Practices

### Question Design
- **Be specific**: Avoid vague questions like "Explain X" (too broad)
- **Use precise language**: Match terminology from source notes
- **Provide context**: Include necessary background information
- **Avoid tricks**: Questions should test knowledge, not reading comprehension
- **Test understanding**: Go beyond simple recall when appropriate

### Answer Design
- **Be complete**: Answer the question fully
- **Be concise**: Avoid unnecessary information
- **Add value**: Include context, mnemonics, or examples
- **Maintain accuracy**: Double-check facts and formulas
- **Show work**: For calculations, include solution steps

### Mnemonic Integration
Use mnemonics strategically:
- **Acronyms**: First letters of list items (e.g., ROY G. BIV for colors)
- **Rhymes**: Memory verses for sequences
- **Vivid imagery**: Unusual mental pictures
- **Method of loci**: Spatial memory techniques
- **Chunking**: Group related items

### Tag Strategy
Create consistent, hierarchical tag system:
- **Subject hierarchy**: #biology > #cellular-biology > #cell-division
- **Cognitive level**: #remember, #understand, #apply, #analyze
- **Content type**: #definition, #formula, #process, #problem
- **Difficulty**: #easy, #medium, #hard
- **Source**: #from-notes, #from-lecture, #from-textbook

### Difficulty Calibration
- **Easy**: Simple recall, direct from notes, one-step thinking
- **Medium**: Requires understanding, connecting concepts, simple application
- **Hard**: Complex application, multi-step reasoning, synthesis

### Spaced Repetition Optimization
- **Initial interval**: Easy cards can be reviewed after longer intervals
- **Leeches**: Identify consistently difficult cards for revision
- **Suspend criteria**: Very easy cards can be suspended after mastery
- **Related cards**: Schedule related cards to appear together

## Integration with Anki

### Export Format
Flashcards can be converted to Anki format:

1. **Basic cards** → Anki "Basic" note type
2. **Cloze cards** → Anki "Cloze" note type
3. **Application cards** → Anki "Basic (and reversed)" or custom note type
4. **Tags** → Anki tag system (hierarchical)

### Import Instructions
To import into Anki:
1. Convert markdown to Anki-compatible format (CSV or APKG)
2. Use tags to organize into decks
3. Configure custom fields (Context, Mnemonic, Related)
4. Set up filtered decks by difficulty or topic

### Conversion Script
*If needed, a conversion script can be created*:
```bash
# Future enhancement: markdown to Anki converter
python scripts/md_to_anki.py flashcards/topic.md -o output.apkg
```

## Error Handling

### Common Issues and Solutions

**Issue**: Source note file not found
- **Solution**: Use Glob to search for similar filenames
- **Action**: Ask user to specify correct filename or create note first
- **Example**: "Note 'quantam-mechanics.md' not found. Did you mean 'quantum-mechanics.md'?"

**Issue**: Source note lacks sufficient content
- **Solution**: Inform user that note may need expansion
- **Action**: Generate flashcards from available content, note limitations
- **Example**: "Only 8 flashcards generated due to limited source content. Consider expanding the note."

**Issue**: Too many flashcards generated (>100)
- **Solution**: Ask if user wants to:
  1. Keep all cards (comprehensive review)
  2. Filter by difficulty (essential cards only)
  3. Split into multiple sets (by sub-topic)

**Issue**: Flashcards directory doesn't exist
- **Solution**: Create directory automatically
- **Command**: `mkdir -p flashcards/`

**Issue**: Duplicate or very similar cards
- **Solution**: Review and consolidate before finalizing
- **Action**: Combine similar cards or differentiate questions

**Issue**: Formula or notation complexity
- **Solution**: Use Unicode or LaTeX notation
- **Note**: Inform user that proper rendering requires LaTeX support
- **Example**: E = mc² vs E = mc^2 vs $E = mc^2$

## Advanced Features

### Progressive Card Generation
For large notes, generate cards in phases:
1. **Phase 1**: Essential definitions and core concepts (Easy/Medium)
2. **Phase 2**: Applications and relationships (Medium/Hard)
3. **Phase 3**: Advanced synthesis and analysis (Hard)

### Cross-Reference Cards
Create cards that connect multiple topics:
```markdown
## Card 45
**Type**: Comparison
**Difficulty**: Hard
**Tags**: #cross-topic #synthesis #analyze

### Front
How does the concept of entropy in thermodynamics relate to information entropy in computer science?

### Back
Both measure disorder or uncertainty:
- **Thermodynamics**: Entropy measures energy dispersal and system disorder
- **Information Theory**: Entropy measures information uncertainty and surprise

**Connection**: Both use similar mathematical formulations and represent irreversibility of processes

**Related**: See flashcards/thermodynamics.md Card 12, flashcards/information-theory.md Card 7
```

### Image Occlusion Cards
For visual content:
```markdown
## Card 28
**Type**: Image Occlusion
**Difficulty**: Medium
**Tags**: #visual #anatomy #remember

### Front
[IMAGE: Diagram of human heart with chambers labeled A, B, C, D]
Identify structure A.

### Back
**Answer**: Right Atrium

**Image**: See notes/cardiovascular-system.md Figure 2
**Context**: Receives deoxygenated blood from the body via superior and inferior vena cava
**Related**: Cards 29 (Right Ventricle), 30 (Left Atrium), 31 (Left Ventricle)
```

### Reverse Cards
Some cards benefit from bidirectional testing:
```markdown
## Card 33a
**Type**: Basic
**Difficulty**: Easy
**Tags**: #definition #bidirectional

### Front
What is mitochondria?

### Back
The "powerhouse of the cell"; organelle responsible for cellular respiration and ATP production.

---

## Card 33b (Reverse)
**Type**: Basic
**Difficulty**: Easy
**Tags**: #definition #bidirectional

### Front
What organelle is known as the "powerhouse of the cell"?

### Back
Mitochondria

**Context**: Produces ATP through cellular respiration
**Note**: Reverse card of #33a
```

## Validation Checklist

Before completing flashcard generation, verify:

- [ ] All key concepts from source note(s) are covered
- [ ] Appropriate distribution of card types (varied, not just one type)
- [ ] Difficulty distribution roughly follows 40-40-20 guideline
- [ ] All cards have complete metadata (type, difficulty, tags)
- [ ] Questions are clear and unambiguous
- [ ] Answers are accurate and complete
- [ ] Academic tone maintained throughout
- [ ] Mnemonics included where helpful
- [ ] Tags are consistent and hierarchical
- [ ] File saved to `flashcards/` directory
- [ ] Filename matches source note (kebab-case)
- [ ] Header includes all required metadata
- [ ] Summary statistics are accurate
- [ ] Cross-references to related materials included
- [ ] Format is compatible with SRS systems
- [ ] User informed of file location and usage instructions

## Integration with Project Structure

This skill integrates seamlessly with the scholarly-ai project:

### Directory Alignment
- **Output location**: `flashcards/` directory (per CLAUDE.md)
- **Source material**: Reads from `notes/` directory
- **Related materials**: Cross-reference `quizzes/` directory

### Workflow Integration
1. **Notes generation** → Comprehensive study materials
2. **Flashcard generation** (this skill) → Active recall practice
3. **Quiz generation** → Formal assessment

### Cross-Skill Coordination
- **From notes-generator**: Use notes as primary source
- **To quiz-generator**: Flashcards inform quiz question generation
- **Bidirectional**: Notes ↔ Flashcards (continuous enhancement)

## Requirements

No external dependencies required for basic functionality.

**Optional enhancements**:
- LaTeX rendering for mathematical notation
- Image processing for occlusion cards
- Anki export script (Python-based)

```bash
# Optional: For Anki export functionality
pip install genanki markdown
```

## Quality Metrics

Excellent flashcard sets demonstrate:

1. **Coverage**: All major concepts addressed (>90% of note content)
2. **Variety**: Multiple card types used appropriately
3. **Clarity**: Questions are unambiguous (<5% confusion rate)
4. **Difficulty**: Appropriate calibration for target audience
5. **Retention**: Cards support long-term memory (SRS compatible)
6. **Engagement**: Questions are interesting and relevant
7. **Efficiency**: No redundant or trivial cards

## Conclusion

This skill transforms academic notes into professional, evidence-based flashcards that maximize learning efficiency. By following cognitive science principles and maintaining consistency with spaced repetition systems, these flashcards support effective long-term retention and mastery of academic material.

The flashcard-generator works in perfect harmony with the notes-generator skill, creating a complete study system: comprehensive notes for deep understanding, and targeted flashcards for active recall and retention.
