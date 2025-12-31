---
name: quiz-generator
description: Generates rigorous professional-level quizzes with 10-15 multiple-choice questions (4-5 options each) based on academic notes. Creates comprehensive assessments with detailed explanations, answer keys, and scoring rubrics. Use when creating quizzes, assessments, exams, tests, or when user mentions quiz generation, assessment creation, or testing materials.
allowed-tools: Read, Write, Edit, Grep, Glob
---

# Quiz Generator

## Overview

This skill generates comprehensive, professional-level quizzes designed to rigorously assess deep understanding of academic content. Each quiz contains 10-15 carefully crafted multiple-choice questions with 4-5 options, complete with detailed explanations, answer keys, and alignment to Bloom's taxonomy. Quizzes are suitable for senior professionals, graduate students, and advanced learners seeking rigorous assessment.

## Professional Quiz Standards

Professional-level quizzes adhere to these assessment principles:

1. **Rigorous Difficulty**: Questions test deep understanding, application, and analysis (not just recall)
2. **Quality Distractors**: Wrong answers are plausible and test common misconceptions
3. **Comprehensive Coverage**: Questions span all major topics in source material
4. **Clear Language**: Unambiguous questions with precisely worded options
5. **Explanation-Rich**: Detailed rationale for correct answers and why others are incorrect
6. **Bloom's Alignment**: Questions target higher-order thinking (Understand, Apply, Analyze, Evaluate)
7. **Professional Context**: Scenarios and applications relevant to professional practice
8. **Fair Assessment**: Questions assess learning objectives fairly and validly

## Quiz Format Specification

Each quiz file uses this structured format:

```markdown
# [Topic Name] - Professional Assessment Quiz

## Quiz Metadata
- **Source Note**: [Link to source note file]
- **Created**: [YYYY-MM-DD]
- **Difficulty Level**: Professional/Advanced
- **Total Questions**: [10-15]
- **Estimated Time**: [20-30 minutes]
- **Passing Score**: 70% (7-11 correct)
- **Recommended For**: Senior professionals, graduate students, advanced learners

## Instructions for Test-Takers

1. Read each question carefully and consider all options before selecting your answer
2. Each question has exactly ONE correct answer
3. Questions are designed to test deep understanding and application, not just memorization
4. Time yourself: Aim to complete the quiz within the estimated time
5. Review the explanations after completing to reinforce learning
6. Passing score: 70% or higher indicates mastery of the material

---

## Questions

### Question 1
**Difficulty**: Medium
**Bloom's Level**: Understand
**Topic**: [Specific concept being tested]

A research team observes that cellular respiration rates decrease significantly when mitochondrial membranes are damaged. Which of the following best explains this observation?

**A)** Mitochondrial DNA becomes inaccessible, preventing enzyme synthesis

**B)** The electron transport chain cannot maintain the proton gradient necessary for ATP synthesis

**C)** Glycolysis is inhibited due to lack of oxygen availability

**D)** The Calvin cycle cannot proceed without intact mitochondrial membranes

**E)** Cellular respiration shifts entirely to anaerobic pathways

**Correct Answer**: B

---

### Question 2
**Difficulty**: Hard
**Bloom's Level**: Apply
**Topic**: [Specific concept being tested]

[Question text with professional context or scenario...]

**A)** [First plausible option]

**B)** [Second plausible option]

**C)** [Third plausible option - CORRECT]

**D)** [Fourth plausible option]

**E)** [Fifth plausible option - if applicable]

**Correct Answer**: C

---

[Continue for all 10-15 questions...]

---

## Answer Key

1. **B** - The electron transport chain cannot maintain the proton gradient necessary for ATP synthesis
2. **C** - [Correct answer text]
3. **A** - [Correct answer text]
[Continue for all questions...]

**Score Calculation**:
- Your Score: _____ / [Total Questions]
- Percentage: _____ %
- Result: [ ] Pass (≥70%) [ ] Review Needed (<70%)

---

## Detailed Explanations

### Question 1: Explanation

**Correct Answer: B** - The electron transport chain cannot maintain the proton gradient necessary for ATP synthesis

**Why this is correct**:
The mitochondrial membrane integrity is essential for maintaining the electrochemical proton gradient across the inner mitochondrial membrane. The electron transport chain pumps protons from the matrix to the intermembrane space, creating a gradient that drives ATP synthase. When membranes are damaged, this gradient cannot be maintained, severely reducing ATP production through oxidative phosphorylation.

**Why other options are incorrect**:

- **A** (Mitochondrial DNA becomes inaccessible): While mitochondrial DNA encodes some proteins, damage to membranes doesn't make DNA inaccessible. Additionally, most proteins are encoded by nuclear DNA. This doesn't directly explain the immediate decrease in respiration rates.

- **C** (Glycolysis is inhibited): Glycolysis occurs in the cytoplasm, not in mitochondria, and doesn't require intact mitochondrial membranes. This option confuses different cellular processes.

- **D** (Calvin cycle cannot proceed): The Calvin cycle is part of photosynthesis in plants, not cellular respiration. This option tests whether you confuse these fundamental processes.

- **E** (Shifts to anaerobic pathways): While some anaerobic respiration might occur, this doesn't explain why respiration rates *decrease*. Anaerobic pathways are less efficient but would still produce some ATP.

**Key Concept**: Mitochondrial membrane integrity and the chemiosmotic theory of ATP synthesis.

**Related Material**: See notes on oxidative phosphorylation and electron transport chain; Flashcard #23.

---

### Question 2: Explanation

**Correct Answer: [Letter]** - [Answer text]

**Why this is correct**:
[Detailed explanation of the correct answer, including supporting concepts, principles, or calculations]

**Why other options are incorrect**:
- **[Letter]**: [Explanation of why this distractor is wrong and what misconception it represents]
- **[Letter]**: [Explanation]
[Continue for all distractors...]

**Key Concept**: [Main concept being assessed]
**Related Material**: [Cross-references to notes/flashcards]

---

[Continue explanations for all questions...]

---

## Performance Analysis

### Score Interpretation

**90-100% (Exceptional Mastery)**:
- Demonstrates comprehensive understanding of all major concepts
- Ready for advanced applications and research-level work
- Consider moving to more advanced topics

**80-89% (Strong Competency)**:
- Solid grasp of core concepts with minor gaps
- Review explanations for missed questions
- Ready for most professional applications

**70-79% (Adequate Understanding)**:
- Meets minimum competency requirements
- Review notes and flashcards for reinforcement
- Focus on areas where questions were missed

**Below 70% (Further Study Needed)**:
- Significant gaps in understanding remain
- Thoroughly review source notes
- Practice with flashcards before retaking quiz
- Consider seeking additional resources or instruction

### Topic Coverage

This quiz assesses understanding across the following areas:
- [Topic 1]: Questions 1, 4, 7, 10
- [Topic 2]: Questions 2, 5, 8, 12
- [Topic 3]: Questions 3, 6, 9, 11, 13
- [Topic 4]: Questions 14, 15

**If you missed questions in a particular topic area, focus your review on those sections of the notes.**

### Bloom's Taxonomy Distribution

- **Remember**: [0-1 questions] - Basic recall
- **Understand**: [3-4 questions] - Comprehension and interpretation
- **Apply**: [4-5 questions] - Application to new situations
- **Analyze**: [3-4 questions] - Breaking down and examining relationships
- **Evaluate**: [2-3 questions] - Critical assessment and judgment

**Professional-level assessment emphasizes higher-order thinking (Apply, Analyze, Evaluate).**

---

## Study Recommendations

### If You Scored Below 70%
1. **Review source notes** thoroughly, especially sections corresponding to missed questions
2. **Practice with flashcards** to reinforce key concepts and definitions
3. **Focus on understanding**, not just memorization
4. **Retake quiz** after 2-3 days of focused review

### If You Scored 70-89%
1. **Review explanations** for all missed questions carefully
2. **Identify patterns** in types of questions missed
3. **Strengthen weak areas** using targeted flashcard review
4. **Consider advanced applications** of concepts you've mastered

### If You Scored 90%+
1. **Review any missed questions** to eliminate remaining gaps
2. **Explore advanced topics** building on this foundation
3. **Apply knowledge** to real-world professional scenarios
4. **Consider teaching** or explaining concepts to others

---

## Related Materials
- **Source Notes**: [../notes/topic-name.md](../notes/topic-name.md)
- **Flashcard Set**: [../flashcards/topic-name.md](../flashcards/topic-name.md)
- **Related Quizzes**: [Links to related assessment quizzes]
- **Further Reading**: [Additional resources if applicable]

---

## Quiz Statistics
- Total Questions: [Number]
- Multiple Choice (4 options): [Number]
- Multiple Choice (5 options): [Number]
- Difficulty Distribution: Easy: [N], Medium: [N], Hard: [N]
- Average Completion Time: [X] minutes
- Recommended Retake Interval: 1 week (for scores <90%)
```

## Instructions

### Step 1: Identify Source Material

Determine the source for quiz generation:

**Option A: From Specific Note**
- User specifies: "Create a quiz from quantum-mechanics.md"
- Read the specified note file
- Extract all assessable content

**Option B: From Topic (Auto-find Note)**
- User mentions: "Generate a quiz on photosynthesis"
- Search `notes/` directory for matching note
- If not found, inform user note must be created first

**Option C: From Multiple Notes (Comprehensive Assessment)**
- User wants: "Quiz covering all biology notes"
- Read multiple related note files
- Create integrated assessment across topics

### Step 2: Analyze Source Content and Plan Quiz

1. **Read source note(s) completely** using Read tool

2. **Identify assessable concepts** across Bloom's taxonomy:
   - **Understand**: Explanations, interpretations, conceptual understanding
   - **Apply**: Problem-solving, calculations, practical applications
   - **Analyze**: Relationships, comparisons, component analysis
   - **Evaluate**: Critical assessment, evidence evaluation, judgment

3. **Map content to question targets**:
   - Extract 15-20 potential question topics
   - Ensure comprehensive coverage of note content
   - Prioritize higher-order thinking (Apply, Analyze, Evaluate)
   - Include professional/practical scenarios where relevant

4. **Determine question distribution**:
   - **Total**: 10-15 questions (adjust based on content depth)
   - **Difficulty**: 20% Medium, 50% Hard, 30% Very Hard
   - **Bloom's**: Minimal Remember (0-1), Heavy Apply/Analyze (70%), Some Evaluate (30%)
   - **Options**: Mix of 4-option (simpler) and 5-option (complex) questions

5. **Identify common misconceptions**:
   - Review content for typical errors or confusions
   - These become high-quality distractors (wrong answers)

### Step 3: Generate Questions

For each identified concept, craft a professional-level question:

#### Question Construction Guidelines

**Question Stem Design**:
- Present realistic professional scenarios or problems
- Use precise, unambiguous language
- Avoid negative phrasing ("Which is NOT...") unless necessary
- Include all necessary context and information
- Make question independent (doesn't rely on previous questions)

**Examples of Professional Question Stems**:

✅ **Good** (Professional, scenario-based):
```
A pharmaceutical company is developing a drug that targets mitochondrial
function. During clinical trials, researchers observe increased lactate
production in muscle tissue. Which mechanism most likely explains this finding?
```

❌ **Poor** (Too simple, recall-only):
```
What is the powerhouse of the cell?
```

✅ **Good** (Application-focused):
```
An engineer must select a material for high-temperature applications
(>800°C). Given that the material must also resist oxidation and maintain
structural integrity, which property should be prioritized?
```

❌ **Poor** (Vague):
```
Which material is best for high temperatures?
```

#### Distractor (Wrong Answer) Design

**Quality Distractor Principles**:

1. **Plausible**: Seems correct without deep understanding
2. **Tests Misconceptions**: Addresses common errors in reasoning
3. **Grammatically Parallel**: Same structure as correct answer
4. **Similar Length**: Avoid "correct answer is longest" pattern
5. **Mutually Exclusive**: No overlap between options
6. **Diagnostic**: Reveals specific gaps in understanding

**Distractor Types**:

**Type 1: Common Misconception**
- Represents a typical error in student thinking
- Example: Confusing correlation with causation

**Type 2: Partial Understanding**
- Contains some truth but misses key component
- Example: Identifies mechanism but wrong location or timing

**Type 3: Related Concept Confusion**
- Correct for a different but related question
- Example: Answer that would be right if question asked about photosynthesis instead of respiration

**Type 4: Calculation Error**
- Correct process but common arithmetic mistake
- Example: Forgot to square a value, used wrong units

**Type 5: Overgeneralization**
- Takes a rule beyond its valid domain
- Example: Applies Newton's laws at quantum scale

#### Answer Option Format

**Structure each question**:

```markdown
### Question [N]
**Difficulty**: [Medium/Hard/Very Hard]
**Bloom's Level**: [Understand/Apply/Analyze/Evaluate]
**Topic**: [Specific concept from notes]

[Question stem with professional context, 2-4 sentences]

**A)** [Distractor 1 - Common misconception]

**B)** [Distractor 2 - Partial understanding]

**C)** [Correct answer - Complete and accurate]

**D)** [Distractor 3 - Related concept confusion]

**E)** [Distractor 4 - Optional fifth distractor for very complex questions]

**Correct Answer**: C
```

### Step 4: Write Comprehensive Explanations

For each question, create detailed explanation:

**Explanation Structure**:

1. **State correct answer** with label
2. **Explain why correct**:
   - Provide underlying principle or theory
   - Show reasoning or calculation steps
   - Connect to broader concepts
3. **Explain why each distractor is wrong**:
   - Identify the misconception it represents
   - Clarify the correct understanding
   - Note what would make it correct (if applicable)
4. **Provide key concept** being tested
5. **Add cross-references** to related materials

**Example Explanation**:

```markdown
### Question 5: Explanation

**Correct Answer: D** - Increase the substrate concentration while maintaining constant enzyme concentration

**Why this is correct**:
According to Michaelis-Menten kinetics, reaction velocity increases with substrate concentration until reaching Vmax. At substrate concentrations well below Km, the reaction rate is approximately first-order with respect to substrate. Therefore, doubling substrate concentration would approximately double the initial reaction rate, provided enzyme is not saturated. This is the most direct method to increase throughput in an industrial enzyme reactor operating below saturation.

**Why other options are incorrect**:

- **A** (Increase temperature by 50°C): While higher temperatures generally increase reaction rates, a 50°C increase would likely denature most enzymes, causing complete loss of activity. Enzyme-catalyzed reactions have optimal temperature ranges, typically 25-45°C for mesophilic enzymes. This option tests whether you understand protein stability versus kinetic temperature dependence.

- **B** (Add competitive inhibitor): Competitive inhibitors bind to the active site and *decrease* reaction velocity by competing with substrate. This would reduce, not increase, the production rate. This tests understanding of enzyme inhibition mechanisms.

- **C** (Decrease pH to 3.0): Most enzymes have narrow optimal pH ranges. A pH of 3.0 is highly acidic and would denature most enzymes or drastically reduce activity. This extreme pH would likely halt production entirely. This tests knowledge of enzyme pH dependence.

- **E** (Reduce substrate concentration): Reducing substrate concentration would decrease reaction velocity according to Michaelis-Menten kinetics. This is the opposite of the desired effect and tests basic understanding of the relationship between substrate concentration and reaction rate.

**Key Concept**: Michaelis-Menten enzyme kinetics and factors affecting reaction velocity in industrial bioreactors.

**Calculation** (for deeper understanding):
If V₀ = Vmax[S]/(Km + [S]), and [S] << Km:
V₀ ≈ (Vmax/Km)[S]
Doubling [S] approximately doubles V₀

**Related Material**:
- Notes: See enzyme-kinetics.md section on Michaelis-Menten equation
- Flashcards: Cards 15-18 on enzyme kinetics
- Professional Context: Industrial enzyme optimization, bioreactor design

**Further Consideration**:
In practice, substrate cost and solubility limits must be considered. At very high [S], product inhibition may also become significant.
```

### Step 5: Create Answer Key and Scoring Guide

**Answer Key Section**:
```markdown
## Answer Key

1. **B** - [Brief answer text]
2. **D** - [Brief answer text]
3. **A** - [Brief answer text]
[... continue for all questions]

**Score Calculation**:
Count the number of correct answers and calculate percentage.

- 14-15 correct (93-100%): Exceptional mastery
- 12-13 correct (80-92%): Strong competency
- 11 correct (73-79%): Adequate understanding
- 10 correct (67-72%): Borderline - review recommended
- Below 10 (<67%): Further study required

**Passing Score**: 11/15 (73%) for professional competency certification
```

### Step 6: Add Performance Analysis

**Topic Coverage Analysis**:
```markdown
### Topic Coverage

Map questions to topics for diagnostic feedback:

**[Major Topic 1]**: Questions 1, 4, 7, 11, 14
**[Major Topic 2]**: Questions 2, 5, 9, 13
**[Major Topic 3]**: Questions 3, 6, 10, 15
**[Major Topic 4]**: Questions 8, 12

**Diagnostic Use**: If you missed multiple questions from the same topic, focus your review on that specific section of the notes.
```

**Bloom's Distribution**:
```markdown
### Bloom's Taxonomy Distribution

- **Understand** (Comprehension): Questions 1, 4, 8
- **Apply** (Application): Questions 2, 5, 7, 10, 12
- **Analyze** (Analysis): Questions 3, 6, 9, 13, 15
- **Evaluate** (Evaluation): Questions 11, 14

**Note**: Professional-level assessment emphasizes application and analysis over mere recall.
```

### Step 7: File Management

1. **Generate filename**: Match source note name
   - Source: `notes/molecular-biology.md`
   - Output: `quizes/molecular-biology.md`
   - Note: Directory is "quizes" per CLAUDE.md (not "quizzes")

2. **Ensure directory exists**:
   ```bash
   mkdir -p quizes/
   ```

3. **Create quiz file** with complete structure:
   - Metadata header
   - Instructions for test-takers
   - All questions (10-15)
   - Answer key
   - Detailed explanations
   - Performance analysis
   - Study recommendations
   - Related materials

4. **Verify completeness**: Ensure all sections are present

### Step 8: User Confirmation

Provide comprehensive summary:

1. **File created**: Path to quiz file
2. **Question count**: Total questions and distribution
3. **Difficulty level**: Confirmation of professional/advanced level
4. **Coverage**: Topics and concepts assessed
5. **Usage instructions**: How to take the quiz
6. **Scoring**: How to interpret results
7. **Next steps**: Recommendations based on performance

## Examples

### Example 1: Generate from Existing Note

**User request**: "Create a professional quiz from the thermodynamics.md notes"

**Process**:
1. Read `notes/thermodynamics.md`
2. Identify key concepts across Bloom's levels:
   - Laws of thermodynamics (Understanding)
   - Entropy calculations (Application)
   - Heat engine efficiency analysis (Analysis)
   - Comparing thermodynamic processes (Evaluation)
3. Generate 12 questions:
   - 1 Understanding (15%)
   - 5 Application (42%)
   - 4 Analysis (33%)
   - 2 Evaluation (10%)
4. Create high-quality distractors testing misconceptions:
   - Confusion between heat and temperature
   - Misapplication of laws
   - Calculation errors in entropy
5. Write detailed explanations with derivations
6. Create file: `quizes/thermodynamics.md`
7. Difficulty: 2 Medium, 6 Hard, 4 Very Hard

**Output**:
```
Created: quizes/thermodynamics.md
- 12 professional-level questions
- Difficulty: 17% Medium, 50% Hard, 33% Very Hard
- Bloom's: 8% Understand, 42% Apply, 33% Analyze, 17% Evaluate
- Estimated completion time: 25 minutes
- Passing score: 9/12 (75%)
```

### Example 2: Generate from Topic

**User request**: "Generate a quiz on quantum mechanics"

**Process**:
1. Search `notes/` directory: Find `notes/quantum-mechanics.md`
2. Read note and extract assessable content
3. Focus on professional applications:
   - Wave-particle duality in experimental design
   - Uncertainty principle applications
   - Quantum state calculations
   - Interpretation of quantum phenomena
4. Generate 15 questions with realistic scenarios:
   - Research laboratory contexts
   - Engineering applications
   - Theoretical problem-solving
5. Create 5-option questions for most complex topics
6. Include detailed mathematical explanations
7. Create file: `quizes/quantum-mechanics.md`

**Output**: Rigorous assessment suitable for graduate-level physics

### Example 3: Comprehensive Assessment Across Multiple Notes

**User request**: "Create a comprehensive quiz covering all organic chemistry notes"

**Process**:
1. Use Glob to find: `notes/*organic-chemistry*.md`
2. Read multiple files:
   - `notes/organic-chemistry-basics.md`
   - `notes/organic-reaction-mechanisms.md`
   - `notes/organic-synthesis.md`
3. Generate integrated quiz (15 questions):
   - Span all major topics proportionally
   - Include cross-topic synthesis questions
   - Test ability to compare different mechanisms
   - Apply knowledge to novel synthesis problems
4. Create comprehensive coverage map
5. Create file: `quizes/organic-chemistry-comprehensive.md`

**Output**: Master assessment covering entire organic chemistry curriculum

### Example 4: Update Existing Quiz

**User request**: "Add more application questions to the biochemistry quiz"

**Process**:
1. Read existing `quizes/biochemistry.md`
2. Identify current question distribution
3. Review source notes for additional application scenarios
4. Generate 3 new application-level questions:
   - Clinical biochemistry scenarios
   - Industrial enzyme applications
   - Metabolic pathway analysis
5. Edit file to integrate new questions
6. Update answer key and explanations
7. Adjust question numbering and cross-references

**Output**: Enhanced quiz with strengthened application assessment

## Best Practices

### Question Writing Excellence

**Clarity**:
- Use precise, professional terminology
- Avoid ambiguous wording
- Provide all necessary context
- Remove extraneous information

**Fairness**:
- Test content covered in notes
- Avoid "trick" questions
- Don't test trivial details
- Ensure questions are answerable with provided knowledge

**Discrimination**:
- Questions should differentiate between strong and weak understanding
- Avoid questions everyone gets right or wrong
- Target 50-70% difficulty for discrimination

**Professional Relevance**:
- Frame questions in professional contexts
- Use realistic scenarios from practice
- Test applicable knowledge, not just theory

### Distractor Quality

**Effective Distractors**:
✅ Test specific misconceptions
✅ Require careful reasoning to eliminate
✅ Could seem correct with partial understanding
✅ Grammatically parallel to correct answer

**Ineffective Distractors**:
❌ Obviously wrong to anyone
❌ Absurd or humorous options
❌ Grammatically inconsistent
❌ Significantly different length/detail from correct answer

### Explanation Quality

**Excellent Explanations Include**:
- Clear statement of why answer is correct
- Underlying principles and theories
- Calculations or derivations where applicable
- Specific explanation for each distractor
- Identification of misconceptions being tested
- Cross-references to study materials
- Professional context and applications

**Poor Explanations**:
- Simply restate the correct answer
- Don't explain why distractors are wrong
- Use circular reasoning
- Lack depth or detail

### Difficulty Calibration

**Professional Level Calibration**:

**Medium (20% of questions)**:
- Straightforward application of concepts
- Direct use of formulas or principles
- One-step reasoning
- Example: Calculate pH of a buffer solution with given concentrations

**Hard (50% of questions)**:
- Multi-step reasoning required
- Integration of multiple concepts
- Analysis of complex scenarios
- Example: Predict outcome of metabolic pathway disruption with compensatory mechanisms

**Very Hard (30% of questions)**:
- Synthesis of multiple concepts
- Evaluation of complex situations
- Novel application to unfamiliar contexts
- Professional judgment required
- Example: Design experimental approach to test hypothesis with consideration of confounding variables

### Coverage Balance

Ensure comprehensive assessment:
- ✅ All major topics from notes represented
- ✅ Proportional representation (more content = more questions)
- ✅ Mix of concept types (definitions, processes, applications, evaluations)
- ✅ Integration questions spanning multiple topics
- ❌ Avoid over-sampling favorite topics
- ❌ Don't ignore difficult-to-assess concepts

### Professional Scenarios

**Strong Professional Contexts**:
- Research laboratory decision-making
- Clinical application of knowledge
- Engineering design challenges
- Industrial process optimization
- Policy and regulatory considerations
- Ethical dilemmas in practice

**Examples**:

```markdown
A biotech company is scaling up production of a therapeutic protein. During
pilot testing, they observe that 15% of the protein product is misfolded.
Which intervention would most likely reduce misfolding without significantly
decreasing yield?
```

```markdown
An environmental engineer must select a remediation strategy for soil
contaminated with heavy metals. Site constraints include proximity to
groundwater (5m depth), residential area (200m), and budget limitations
($500K). Which approach best balances effectiveness, safety, and cost?
```

## Error Handling

### Common Issues and Solutions

**Issue**: Source note file not found
- **Solution**: Use Glob to search for similar filenames
- **Action**: Ask user to specify correct filename or create note first
- **Example**: "Note 'quantum-mechaniks.md' not found. Did you mean 'quantum-mechanics.md'?"

**Issue**: Note content insufficient for 10-15 questions
- **Solution**: Generate fewer questions with warning
- **Action**: Inform user that note may need expansion for comprehensive assessment
- **Example**: "Only 7 questions possible from current content. Expand notes or create shorter quiz?"

**Issue**: Note content only supports recall-level questions
- **Solution**: Inform user that professional-level quiz requires application/analysis content
- **Action**: Suggest adding examples, applications, and analysis to notes
- **Example**: "Source notes contain mostly definitions. Add applications and examples for professional-level assessment."

**Issue**: Quizes directory doesn't exist
- **Solution**: Create directory automatically
- **Command**: `mkdir -p quizes/`
- **Note**: Use "quizes" per CLAUDE.md (not "quizzes")

**Issue**: Multiple possible correct answers
- **Solution**: Revise question or options to ensure only one correct answer
- **Action**: Add qualifiers like "most likely," "primary," "best"
- **Example**: Change "Which is correct?" to "Which is the PRIMARY mechanism?"

**Issue**: Distractors too easy to eliminate
- **Solution**: Revise to create more plausible distractors
- **Action**: Base distractors on actual misconceptions from teaching experience

## Advanced Features

### Adaptive Question Pools

For comprehensive topics, create question banks:

```markdown
# Molecular Biology - Question Pool

## Pool A: DNA Structure and Replication (20 questions)
[Questions 1-20 covering DNA topics]

## Pool B: Transcription and Translation (20 questions)
[Questions 21-40 covering protein synthesis]

## Pool C: Gene Regulation (15 questions)
[Questions 41-55 covering regulation]

---

## Generated Quizzes

### Quiz 1 (Standard)
Selected questions: 1, 5, 12, 21, 27, 33, 41, 44, 48, 52, 3, 19, 28, 39, 50

### Quiz 2 (Alternative Form)
Selected questions: 2, 7, 15, 22, 29, 35, 42, 46, 49, 54, 6, 18, 25, 37, 51
```

### Case-Based Questions

For advanced professional assessment:

```markdown
### Questions 8-11: Case Study

**Background**:
A 45-year-old patient presents with persistent fatigue, weight loss, and
muscle weakness. Laboratory tests reveal elevated blood glucose (180 mg/dL),
low cortisol (3 μg/dL), and elevated ACTH (120 pg/mL). Imaging shows bilateral
adrenal atrophy.

---

### Question 8
**Based on the presentation, what is the most likely diagnosis?**
[Options...]

### Question 9
**Which pathophysiological mechanism best explains the laboratory findings?**
[Options...]

### Question 10
**What additional test would best confirm the diagnosis?**
[Options...]

### Question 11
**Which treatment approach is most appropriate for this patient?**
[Options...]
```

### Calculation-Heavy Questions

For quantitative subjects:

```markdown
### Question 12
**Difficulty**: Very Hard
**Bloom's Level**: Apply
**Topic**: Thermodynamics - Entropy Calculations

A reversible heat engine operates between a hot reservoir at 600K and a cold
reservoir at 300K. The engine absorbs 2000J of heat from the hot reservoir
during each cycle.

Calculate the maximum work output per cycle and the heat rejected to the cold
reservoir.

**A)** Work: 500J, Heat rejected: 1500J
**B)** Work: 1000J, Heat rejected: 1000J ✓
**C)** Work: 1200J, Heat rejected: 800J
**D)** Work: 800J, Heat rejected: 1200J
**E)** Work: 1500J, Heat rejected: 500J

**Correct Answer**: B

---

**Explanation includes full derivation**:
1. Maximum efficiency: η = 1 - Tc/Th = 1 - 300/600 = 0.5 (50%)
2. Work output: W = η × Qh = 0.5 × 2000J = 1000J
3. Heat rejected: Qc = Qh - W = 2000J - 1000J = 1000J
[...]
```

### Visual/Diagram-Based Questions

Reference figures from notes:

```markdown
### Question 7
**Difficulty**: Hard
**Bloom's Level**: Analyze
**Topic**: Organic Mechanisms

**Refer to Figure 3.2 in notes/organic-reaction-mechanisms.md**

The reaction mechanism shown depicts the formation of a carbocation intermediate
in step 2. Which structural feature of the starting material makes this
carbocation particularly stable?

**A)** Adjacent electron-withdrawing group
**B)** Resonance stabilization from neighboring π-system ✓
**C)** Hyperconjugation from β-hydrogens
**D)** Inductive effect from nearby alkyl groups
**E)** Aromatic stabilization

**Correct Answer**: B
```

### Comparative Analysis Questions

Test ability to discriminate:

```markdown
### Question 14
**Difficulty**: Very Hard
**Bloom's Level**: Evaluate
**Topic**: Research Methodology

Three research teams investigated the same hypothesis using different approaches:

- **Team A**: Randomized controlled trial (n=500, 2-year duration)
- **Team B**: Meta-analysis of 15 existing studies (combined n=3,200)
- **Team C**: Longitudinal observational study (n=10,000, 5-year duration)

All three studies reached different conclusions. When advising policymakers,
which study's findings should carry the most weight for establishing causation,
and why?

**A)** Team A - Randomization eliminates confounding despite smaller sample ✓
**B)** Team B - Largest combined sample size increases statistical power
**C)** Team C - Longest duration captures long-term effects best
**D)** All equally - Different methodologies provide complementary evidence
**E)** None - Contradictory findings indicate insufficient evidence

**Correct Answer**: A

[Detailed explanation of research methodology hierarchy, internal validity vs
external validity trade-offs, causal inference criteria...]
```

## Integration with Project Structure

This skill integrates seamlessly with the scholarly-ai project:

### Directory Alignment
- **Output location**: `quizes/` directory (per CLAUDE.md spelling)
- **Source material**: Reads from `notes/` directory
- **Related materials**: Cross-references `flashcards/` directory

### Workflow Integration
1. **Notes generation** → Comprehensive study materials
2. **Flashcard generation** → Active recall practice
3. **Quiz generation** (this skill) → Formal assessment and validation

### Complete Learning System
- **Study**: Use notes for deep learning (Bloom's taxonomy)
- **Practice**: Use flashcards for retention (spaced repetition)
- **Assess**: Use quizzes for validation (professional competency)

### Cross-Skill Coordination

**From notes-generator**:
- Extract content structured by Bloom's taxonomy
- Use "Apply," "Analyze," and "Evaluate" sections for questions
- Reference examples and applications from notes

**From flashcard-generator**:
- Flashcards test recall; quizzes test application and analysis
- Complementary assessment tools
- Cross-reference in study recommendations

## Validation Checklist

Before completing quiz generation, verify:

- [ ] 10-15 questions generated (appropriate for content depth)
- [ ] Each question has 4-5 plausible options
- [ ] Only ONE correct answer per question
- [ ] Professional-level difficulty maintained (not simple recall)
- [ ] Comprehensive coverage of source note content
- [ ] All major topics represented proportionally
- [ ] Bloom's taxonomy emphasis on Apply/Analyze/Evaluate (70%+)
- [ ] Difficulty distribution: ~20% Medium, ~50% Hard, ~30% Very Hard
- [ ] Each question has complete metadata (difficulty, Bloom's, topic)
- [ ] All distractors are plausible and test specific misconceptions
- [ ] Detailed explanation provided for every question
- [ ] Explanation addresses why correct answer is right AND why each distractor is wrong
- [ ] Answer key is accurate and complete
- [ ] Performance analysis includes topic coverage mapping
- [ ] Study recommendations based on score ranges
- [ ] Cross-references to notes and flashcards included
- [ ] File saved to `quizes/` directory (note spelling)
- [ ] Filename matches source note (kebab-case)
- [ ] Academic tone maintained throughout
- [ ] User informed of file location and usage instructions

## Requirements

No external dependencies required for basic functionality.

**Optional enhancements**:
- LaTeX rendering for mathematical equations
- Automatic quiz grading script
- Statistical analysis of question difficulty

```bash
# Optional: For automated grading
python scripts/grade_quiz.py quizes/topic.md --answers user_answers.txt
```

## Quality Metrics

Excellent professional quizzes demonstrate:

1. **Validity**: Questions accurately assess intended learning outcomes
2. **Reliability**: Consistent assessment across different test-takers
3. **Discrimination**: Differentiates between strong and weak understanding
4. **Fairness**: All questions answerable with provided study materials
5. **Comprehensiveness**: Covers all major topics adequately
6. **Rigor**: Appropriate difficulty for professional/advanced level
7. **Clarity**: Unambiguous questions and options
8. **Utility**: Provides meaningful diagnostic feedback

### Statistical Targets

Well-designed questions typically show:
- **Difficulty Index** (P): 0.40-0.70 (40-70% answer correctly)
- **Discrimination Index** (D): >0.30 (top performers 30% more likely to answer correctly)
- **Distractor Efficiency**: Each distractor chosen by at least 5% of test-takers

## Conclusion

This skill transforms academic notes into rigorous, professional-level assessment instruments. By emphasizing higher-order thinking, providing comprehensive explanations, and maintaining high standards for question quality, these quizzes serve as effective tools for validating deep understanding and professional competency.

The quiz-generator completes the scholarly-ai learning ecosystem: notes for learning, flashcards for retention, and quizzes for assessment—a comprehensive system for mastering academic and professional content.
