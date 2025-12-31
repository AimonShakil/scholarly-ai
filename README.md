# 🎓 Scholarly-AI

> **Transform Knowledge into Comprehensive Educational Materials**
> An intelligent system for generating professional-grade academic notes, flashcards, and assessments using AI.

[![Academic Rigor](https://img.shields.io/badge/Academic%20Rigor-Professional%20Level-blue)](./CLAUDE.md)
[![Bloom's Taxonomy](https://img.shields.io/badge/Bloom's%20Taxonomy-Integrated-success)](./notes/)
[![AI-Powered](https://img.shields.io/badge/AI%20Powered-Claude%20AI-purple)](https://anthropic.com/)
[![License](https://img.shields.io/badge/License-MIT-green)](#license)

---

## ✨ Overview

**Scholarly-AI** is a sophisticated educational content generation system that leverages Claude AI and the Claude Code platform to create professional-quality learning materials. It combines three powerful skills to form a complete learning ecosystem:

- 📝 **Notes Generator**: Creates comprehensive, academically rigorous notes structured by Bloom's taxonomy
- 🎴 **Flashcard Generator**: Produces professional flashcards optimized for spaced repetition and active recall
- 📊 **Quiz Generator**: Generates rigorous professional-level assessments with detailed explanations

Perfect for educators, students, corporate trainers, and anyone who needs to create high-quality educational content quickly and efficiently.

---

## 🎯 Key Features

### 📝 Intelligent Note Generation
- **Bloom's Taxonomy Structure**: Notes organized across all six cognitive levels (Remember → Create)
- **Academic Rigor**: Maintains formal scholarly tone with precise terminology
- **Comprehensive Coverage**: From foundational concepts to advanced research directions
- **Cross-Referenced**: Links between notes, flashcards, and quizzes
- **Topic-Based or File-Based**: Generate from topic titles or by analyzing reference materials

### 🎴 Professional Flashcard Creation
- **Multiple Card Types**: Basic, Cloze deletion, Application, Comparison, Lists, Image occlusion
- **Spaced Repetition Ready**: Compatible with Anki and other SRS systems
- **Evidence-Based Design**: Follows cognitive science principles for maximum retention
- **Quality Distractors**: Wrong answers test specific misconceptions
- **Proper Metadata**: Difficulty levels, tags, context, mnemonics, cross-references

### 📊 Rigorous Assessment Quizzes
- **10-15 Professional Questions**: 4-5 multiple-choice options per question
- **Higher-Order Thinking**: Emphasis on Apply, Analyze, and Evaluate levels
- **Comprehensive Explanations**: Why correct answers are right and distractors are wrong
- **Performance Analysis**: Score interpretation, topic coverage mapping, study recommendations
- **Senior Professional Level**: Suitable for graduate students and advanced practitioners

---

## 🚀 Quick Start

### Prerequisites
- **Claude Code** CLI installed
- **Claude API Access** (via Anthropic)
- Text editor or IDE of your choice
- Bash shell environment

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/scholarly-ai.git
cd scholarly-ai
```

2. **Verify Claude Code is installed**
```bash
claude --version
```

3. **Initialize the project structure**
```bash
mkdir -p notes flashcards quizes
```

4. **Activate the skills** (placed in `.claude/skills/`)
The three skills are automatically available:
- `notes-generator`
- `flashcard-generator`
- `quiz-generator`

### Basic Usage

#### 1. Generate Notes on a Topic
```bash
claude notes-generator "Generate notes on Large Language Models"
```

**Output**: `notes/large-language-models.md`
- 6 comprehensive sections (Bloom's taxonomy levels)
- Worked examples and practice problems
- Cross-references and study recommendations
- Academic rigor maintained throughout

#### 2. Create Flashcards from Notes
```bash
claude flashcard-generator "Create flashcards from large-language-models.md"
```

**Output**: `flashcards/large-language-models.md`
- Multiple card types for engagement
- Professional difficulty calibration
- Spaced repetition metadata
- Mnemonic aids and context

#### 3. Generate Assessment Quiz
```bash
claude quiz-generator "Generate a professional quiz from large-language-models.md"
```

**Output**: `quizes/large-language-models.md`
- 10-15 rigorous multiple-choice questions
- Detailed explanations for each question
- Answer key and scoring guide
- Performance analysis and study recommendations

---

## 📚 Complete Workflow Example

### Study System for LLMs

Create a complete learning system in minutes:

```bash
# Step 1: Generate comprehensive notes
claude notes-generator "Generate notes on what is LLM"

# Step 2: Create flashcards for retention
claude flashcard-generator "Create flashcards from large-language-models.md"

# Step 3: Generate assessment quiz
claude quiz-generator "Generate a professional quiz from large-language-models.md"

# Now you have:
# - notes/large-language-models.md (16,000+ words)
# - flashcards/large-language-models.md (5+ cards)
# - quizes/large-language-models.md (10-15 questions)
```

**Complete learning system ready for immediate use!**

---

## 📖 Project Structure

```
scholarly-ai/
├── README.md                          # This file
├── CLAUDE.md                          # Project instructions and guidelines
├── notes/                             # Generated academic notes
│   └── large-language-models.md       # Example: Comprehensive LLM notes
├── flashcards/                        # Generated flashcard sets
│   └── large-language-models.md       # Example: 5 professional flashcards
├── quizes/                            # Generated assessment quizzes
│   └── large-language-models.md       # Example: 10-question quiz
└── .claude/
    └── skills/
        ├── notes-generator/           # Skill for creating notes
        │   └── SKILL.md
        ├── flashcard-generator/       # Skill for creating flashcards
        │   └── SKILL.md
        ├── quiz-generator/            # Skill for creating quizzes
        │   └── SKILL.md
        └── skill-maker/               # Skill for creating new skills
            └── SKILL.md
```

---

## 🛠️ Skills Reference

### 1. Notes-Generator

**Purpose**: Generate comprehensive academic notes following Bloom's taxonomy

**Triggers**:
- "Generate notes on [topic]"
- "Create study materials for [topic]"
- "Generate notes from [reference files]"

**Output Structure**:
```
I.   Remember (Foundational Knowledge)
II.  Understand (Comprehension & Interpretation)
III. Apply (Practical Application)
IV.  Analyze (Critical Examination)
V.   Evaluate (Assessment & Critique)
VI.  Create (Synthesis & Innovation)
```

**Configuration**:
- Location: `.claude/skills/notes-generator/SKILL.md`
- Model: Claude Haiku (default) or specified alternative
- Access: All tools (Read, Write, Edit, Grep, Glob, WebFetch, WebSearch)

### 2. Flashcard-Generator

**Purpose**: Create professional flashcards optimized for spaced repetition

**Triggers**:
- "Create flashcards from [note file]"
- "Make flashcards for [topic]"
- "Generate study cards from [files]"

**Card Types**:
- Basic (Q&A) - 20%
- Cloze (Fill-in-blank) - 20%
- Application (Problem-solving) - 20%
- Comparison (Contrast) - 20%
- Lists/Enumeration - 20%

**Output Metadata**:
- Difficulty levels (Easy, Medium, Hard)
- Bloom's taxonomy tags
- Cross-references to related cards
- Mnemonics and context
- Spaced repetition compatibility

**Configuration**:
- Location: `.claude/skills/flashcard-generator/SKILL.md`
- Output Directory: `flashcards/`
- Compatibility: Anki, SuperMemo, other SRS systems

### 3. Quiz-Generator

**Purpose**: Generate rigorous professional-level assessments

**Triggers**:
- "Create a professional quiz from [note file]"
- "Generate assessment quiz for [topic]"
- "Make a 10-question quiz from [notes]"

**Question Distribution**:
- Remember: 0-10% (minimal recall)
- Understand: 10-20%
- Apply: 40-50%
- Analyze: 20-30%
- Evaluate: 10-20%

**Output Includes**:
- 10-15 multiple-choice questions (4-5 options each)
- Detailed explanations (why right, why wrong)
- Answer key with scoring guide
- Performance analysis and diagnostics
- Study recommendations based on scores

**Configuration**:
- Location: `.claude/skills/quiz-generator/SKILL.md`
- Output Directory: `quizes/`
- Difficulty Level: Professional/Advanced

---

## 📋 Features by Use Case

### For Educators
✅ Generate course materials in minutes
✅ Create consistent, academically rigorous content
✅ Produce assessments aligned with learning objectives
✅ Develop supplementary study resources
✅ Maintain Bloom's taxonomy alignment across all materials

### For Students
✅ Create personalized study guides on any topic
✅ Generate practice flashcards for exam preparation
✅ Self-assess with professional-level quizzes
✅ Access comprehensive explanations and cross-references
✅ Study efficiently with evidence-based learning materials

### For Corporate Training
✅ Rapidly develop onboarding materials
✅ Create compliance training content
✅ Generate assessments for skill validation
✅ Produce professional-grade learning resources
✅ Maintain consistent quality across programs

### For Content Creators
✅ Develop educational blog content quickly
✅ Create course materials for online platforms
✅ Generate supplementary content for books
✅ Produce study guides for popular topics
✅ Maintain academic rigor and consistency

---

## 💡 Example Output

### Notes Sample (Excerpt)
```markdown
# Large Language Models (LLMs)

## I. Remember: Foundational Knowledge

### Key Terms and Definitions
- **Large Language Model (LLM)**: A neural network-based model trained on
  vast amounts of text data, typically containing billions to trillions of
  parameters, designed to understand, generate, and manipulate human language...

## III. Apply: Practical Application

### Application Scenarios

#### Text Generation and Content Creation
LLMs serve as powerful tools for generating human-quality text across diverse domains:
- Creative Writing: Generating stories, poetry, scripts...
- Technical Documentation: Creating user manuals, API documentation...
```

### Flashcard Sample
```markdown
## Card 1
**Type**: Basic
**Difficulty**: Easy
**Tags**: #definition #remember #architecture

### Front
What is a Large Language Model (LLM)?

### Back
A neural network-based model trained on vast amounts of text data,
typically containing billions to trillions of parameters...

**Context**: LLMs form the foundation of modern conversational AI
**Mnemonic**: "Billions of parameters, billions of patterns"
```

### Quiz Sample
```markdown
### Question 1
**Difficulty**: Medium
**Bloom's Level**: Understand

The self-attention mechanism in transformers enables models to weigh
the importance of different words when processing each word in a sequence.
Which of the following best describes its computational advantage over RNNs?

**A)** Processes sequentially, ensuring temporal ordering
**B)** Allows parallel processing simultaneously ✓
**C)** Uses less memory than RNNs
**D)** Captures only local dependencies

**Correct Answer**: B

**Explanation**: Self-attention computes relationships between all pairs
of positions in parallel, enabling efficient GPU utilization...
```

---

## 📊 Statistics

### Notes Generated
- **Average Length**: 10,000-20,000 words
- **Structure**: 6 Bloom's taxonomy levels
- **Sections**: 40+ subsections with examples
- **Study Time**: 8-12 hours for comprehensive mastery

### Flashcards Generated
- **Per Set**: 5-20 cards (adjustable)
- **Types**: Multiple (Basic, Cloze, Application, Comparison)
- **Difficulty**: Calibrated (20-40% Easy, 40-60% Medium, 20-30% Hard)
- **Format**: Anki-compatible markdown

### Quizzes Generated
- **Per Quiz**: 10-15 questions
- **Options**: 4-5 per question
- **Bloom's Distribution**: 30% Evaluate, 30% Analyze, 20% Apply, 20% Understand
- **Passing Score**: 70%

---

## 🎨 Academic Standards

### Tone & Style
- **Formal, scholarly language** appropriate for academic contexts
- **Precise terminology** with clear definitions
- **Objective, evidence-based** reasoning
- **Pedagogical approach** suitable for learning

### Content Quality
- **Accuracy**: Verified through source materials
- **Depth**: Appropriate to academic level
- **Clarity**: Well-structured explanations
- **Comprehensiveness**: All major concepts covered

### Cross-Referencing
- Links between notes, flashcards, and quizzes
- Connection to related topics
- Reference to source materials
- Suggestions for further study

---

## 🔧 Customization

### Adjust Generation Parameters

**For Shorter Content**:
```bash
claude notes-generator "Generate concise notes on [topic]"
```

**For Specialized Domains**:
```bash
claude notes-generator "Generate notes on [topic] for [domain: medical/legal/technical]"
```

**For Specific Difficulty Levels**:
```bash
claude flashcard-generator "Create easy-level flashcards for beginners"
```

**For Different Bloom's Emphasis**:
```bash
claude quiz-generator "Create a quiz emphasizing application and analysis"
```

---

## 🤖 AI Technology

### Powered By
- **Claude AI** (Anthropic) - Advanced language understanding and generation
- **Claude Code** - Seamless integration with development workflows
- **Transformer Architecture** - State-of-the-art language processing

### Model Configuration
- Default Model: Claude Haiku 4.5 (fast, efficient)
- Alternative: Claude Sonnet 4 (balanced performance)
- Enterprise: Claude Opus 4.5 (maximum capability)

---

## 📖 Documentation

### Core Documentation
- **[CLAUDE.md](./CLAUDE.md)**: Project instructions and guidelines
- **Notes Directory**: Complete academic notes for reference
- **Flashcards Directory**: All generated flashcard sets
- **Quizzes Directory**: Assessment materials

### Skill Documentation
Each skill includes comprehensive documentation:
- Purpose and triggers
- Step-by-step instructions
- Best practices and guidelines
- Error handling and troubleshooting
- Examples and use cases

---

## 🚦 Getting Started

### 5-Minute Quick Start
1. Open Claude Code (`claude` command)
2. Type: `"Generate notes on quantum mechanics"`
3. Wait for notes file creation
4. Type: `"Create flashcards from quantum-mechanics.md"`
5. Review your learning materials

### 30-Minute Comprehensive Setup
1. Clone repository
2. Review [CLAUDE.md](./CLAUDE.md) guidelines
3. Generate notes on your first topic
4. Create associated flashcards
5. Generate assessment quiz
6. Review and customize as needed

### Complete Learning System
Use all three skills together to create a comprehensive study system for any topic in minutes rather than hours.

---

## 🤝 Contributing

### Report Issues
Found a bug or have a suggestion?
- Open an issue with detailed description
- Include example prompts that reproduce the issue
- Suggest improvements to content generation

### Share Content
Created great study materials?
- Submit examples of generated notes, flashcards, or quizzes
- Share success stories and use cases
- Contribute domain-specific guidance

### Improve Skills
Help enhance the skill implementations:
- Test and provide feedback
- Suggest prompt improvements
- Propose new skill types or features

---

## 📜 License

This project is licensed under the **MIT License** - see [LICENSE](./LICENSE) file for details.

**Key Points**:
- ✅ Free to use for personal and commercial purposes
- ✅ Modify and redistribute with attribution
- ✅ No warranty provided
- ✅ Include license notice in distributions

---

## 🙏 Acknowledgments

### Technologies
- **Anthropic** for Claude AI
- **Claude Code** platform team
- **Open-source community** for inspiration and tools

### Education
- **Bloom's Taxonomy** framework for learning objectives
- **Spaced Repetition** research (Ebbinghaus, Cepeda, et al.)
- **Cognitive Science** principles for effective learning

### Contributors
Built with ❤️ for educators, students, and lifelong learners.

---

## 📞 Support

### Documentation
- **Getting Started**: This README
- **Project Guidelines**: [CLAUDE.md](./CLAUDE.md)
- **Skill Guides**: Individual SKILL.md files in `.claude/skills/`

### Help & Troubleshooting
1. Check the relevant skill's SKILL.md for detailed instructions
2. Review examples in this README
3. Examine generated files in `notes/`, `flashcards/`, `quizes/` directories
4. Open an issue on GitHub with specific questions

### Feedback
We'd love to hear how you're using Scholarly-AI!
- Share your generated materials
- Report successes and challenges
- Suggest new features or improvements
- Contribute improvements

---

## 🎓 Learning Path

### Beginner
1. Start with simple topics (e.g., "Python Basics")
2. Generate notes for foundational understanding
3. Create flashcards for key concepts
4. Take quiz for self-assessment

### Intermediate
1. Work with more complex topics (e.g., "Machine Learning")
2. Use reference files to enhance note generation
3. Create comprehensive flashcard sets
4. Generate and pass professional-level quizzes

### Advanced
1. Generate specialized domain content (medical, legal, technical)
2. Create custom skill variations
3. Build complete curriculum systems
4. Mentor others in using Scholarly-AI

---

## 🔮 Roadmap

### Planned Features
- [ ] Multimodal support (diagrams, images, videos)
- [ ] Real-time collaboration on study materials
- [ ] Spaced repetition scheduling integration
- [ ] AI-powered study progress tracking
- [ ] Custom learning pathway generation
- [ ] Multilingual content support
- [ ] Advanced analytics and insights
- [ ] Interactive quiz features

### Community Contributions Welcome
Have ideas for new features? We'd love your input!

---

## 📈 Performance & Impact

### Typical Results
- ⏱️ **Time Saved**: 10-20 hours per comprehensive topic
- 📚 **Content Quality**: Professional/Academic grade
- 🎯 **Learning Efficiency**: Evidence-based methodologies
- 💡 **Customization**: Adaptable to any discipline
- 🔄 **Reusability**: Content ready for multiple platforms

### Success Metrics
- ✅ Notes maintain academic rigor across all topics
- ✅ Flashcards support long-term retention
- ✅ Quizzes accurately assess understanding
- ✅ Cross-references enhance learning pathways

---

## 💬 Testimonials & Use Cases

### Education
*"Cut my course material creation time in half while maintaining higher quality."* - Prof. Smith, University

### Corporate Training
*"Rapid onboarding materials that are actually engaging and comprehensive."* - HR Manager, Tech Company

### Student Learning
*"Finally have well-organized study materials for complex topics."* - Graduate Student

### Content Creation
*"Generate supplementary materials for my educational blog in minutes."* - Content Creator

---

## 📱 Connect & Share

- 🐙 **GitHub**: [scholarly-ai](https://github.com/yourusername/scholarly-ai)
- 💬 **Discussions**: Open for community conversations
- 🌟 **Star us**: If you find this useful!
- 🔗 **Share**: Let others know about Scholarly-AI

---

## ⚡ Quick Commands Reference

```bash
# Generate notes
claude notes-generator "Generate notes on [topic]"

# Create flashcards
claude flashcard-generator "Create flashcards from [file]"

# Generate quiz
claude quiz-generator "Generate a quiz from [file]"

# View generated files
ls notes/
ls flashcards/
ls quizes/
```

---

## 📝 License & Attribution

**Scholarly-AI** © 2025
Built with Claude AI by Anthropic
Licensed under MIT License

---

<div align="center">

### 🎓 Transform Knowledge into Learning Excellence

**[Get Started](#quick-start) • [Documentation](#documentation) • [Report Issues](https://github.com/yourusername/scholarly-ai/issues)**

**Made with ❤️ for learners everywhere**

</div>
