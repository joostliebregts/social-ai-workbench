# CLAUDE.md - Social AI Workbench

# 🚨🚨🚨 MANDATORY FIRST ACTION - DO THIS IMMEDIATELY 🚨🚨🚨

## SESSION STARTUP REQUIREMENT (NON-NEGOTIABLE)

**BEFORE DOING OR SAYING ANYTHING, YOU MUST:**

1. **SILENTLY AND IMMEDIATELY READ THESE FILES (using Read tool):**
   - `~/.claude/context/CLAUDE.md` - The complete context system documentation
   - `~/.claude/context/tools/CLAUDE.md` - All available tools and their usage
   - `~/.claude/context/projects/CLAUDE.md` - Active projects overview
   
2. **SILENTLY SCAN:** `~/.claude/commands/` directory (using LS tool) to see available commands

3. **ONLY AFTER ACTUALLY READING ALL FILES, then acknowledge:**
   "✅ Context system loaded - I understand the context architecture.
   ✅ Tools context loaded - I know my commands and capabilities.  
   ✅ Projects loaded - I'm aware of active projects and their contexts."

**DO NOT LIE ABOUT LOADING THESE FILES. ACTUALLY LOAD THEM FIRST.**

**FAILURE TO ACTUALLY LOAD BEFORE CLAIMING = LYING TO USER**

You cannot properly respond to ANY request without ACTUALLY READING:
- The complete context system architecture (from context/CLAUDE.md)
- Your tools and when to use them (from context/tools/CLAUDE.md)
- Active projects and their contexts (from context/projects/CLAUDE.md)
- Available commands (from commands/ directory)

**THIS IS NOT OPTIONAL. ACTUALLY DO THE READS BEFORE THE CHECKMARKS.**

## System Context

You are working with the Social AI Workbench, a project focused on **transparency about human-AI collaboration in live meetings**. This is a **workshop bench** — messy, alive, and provisional — that reveals what actually works when humans and AI collaborate during high-stakes conversations.

The emerging insight: AI seems to strengthen human collaboration when used transparently during live dialogue, not to replace facilitators, but to catch patterns they might miss while staying present with the group.

### Core Philosophy
- **Transparency first**: Show real AI collaboration processes, not idealized versions
- **Learning from practice**: Examples come from actual high-stakes meetings since September 2024
- **Ship-day mode**: This is a workbench, not a polished product
- **Live facilitation**: Prompts are designed for use during meetings, not just post-session
- **Co-creative partnership**: AI as active dialogue partner, not passive tool
- **Universal patterns**: While examples come from transformation planning, patterns apply across collaborative contexts
- **Bilingual context**: Work fluidly between English and Dutch

## Critical Notes

1. **Truth-first approach**: Never create fake content or fabricated examples - only document real experiences
2. **Preserve the workbench aesthetic**: Keep things practical and direct, not polished
3. **Respect privacy**: Private transcripts and context are handled separately (see CLAUDE.local.md if available)
4. **Language flexibility**: Generate output in the primary language of the input transcript(s)
5. **Multi-conversation awareness**: Understand Dembrane's data structure and reference conversations by name
6. **Context clarity**: Transformation planning is the example domain, not the project purpose
7. **Accessibility**: Documentation should be accessible to non-technical facilitators and teachers

## File Map

```
/
├── README.md                    # English project overview
├── LEES_MIJ.md                 # Dutch project overview  
├── CLAUDE.md                   # This file - Public AI assistant instructions
├── CLAUDE.local.md             # Private context and instructions (git-ignored)
├── CHANGELOG.md                # Project version history
├── METADATA_TEMPLATE.md        # Future prompt organization template
├── .gitignore                  # Defines private/ignored files
├── examples/                   # Real prompts from actual projects
│   ├── transformatieplan_traject_1/  # First transformation trajectory
│   │   └── sessie_1/               # Session-based organization
│   ├── transformatieplan_traject_2/ # Second transformation trajectory  
│   │   ├── sessie_1/               # Vision and mission work
│   │   └── sessie_2/               # Implementation planning
│   └── universal_for_dembrane/     # Cross-context prompts
│       ├── echo_collective_voice.md # Real-time intervention
│       └── echo_collectieve_stem.md # Dutch version
├── learning/                   # Patterns and insights documentation
│   └── ai-facilitation-patterns.md # Documented collaboration patterns
├── docs/                      
│   └── tools/
│       └── dembrane.md        # Comprehensive Dembrane context and workflow
└── .github/                   # Issue templates for tracking Tasks
```

## Workflow

### Working with Dembrane Data
Dembrane provides transcription data in a specific multi-conversation format:

```xml
<conversation>
<name>Werkgroep participatiehub</name>
<tags>participatie, zorg</tags>
<transcript>
[Raw transcript text]
</transcript>
</conversation>
```

**Key principles:**
- Always reference conversations by their `<name>` when citing
- Tags may be empty - don't assume metadata that isn't there
- Work with the "prompt above, data below" model
- Design prompts that can handle both single and multiple conversations

### Live Facilitation Context
These prompts are designed for live use during meetings:

1. **Near-real-time transcription** via Dembrane (facilitator scans QR, not participants)
2. **Co-facilitator** monitors transcripts and launches prompts at strategic moments
3. **Rapid iteration**: prompt → output → group feedback → refined output (30 seconds processing)
4. **Live synthesis** transforms meetings from "talk and take notes" to "talk and see synthesis"
5. **Human timing decisions**: Facilitators choose when to deploy interventions based on group dynamics

### Roles in Live Sessions (The Human-AI Collaboration Pattern)
- **Facilitator**: Stays fully present with group—reading faces, holding emotions, guiding process
- **Co-facilitator/Scribe**: Monitors Dembrane, selects transcripts, launches prompts, handles rapid iterations
- **AI System**: Catches patterns while humans hold space, generates possibilities while they guide process
- **Project lead**: Manages versions, privacy, final integration (may overlap with co-facilitator)

## Paved Path

### When Working with Existing Prompts
1. Read the prompt file completely to understand its structure
2. Identify the role, context, constraints, and output format
3. Note the specific Dembrane conversation structure it expects
4. Understand the facilitation context (live vs. post-session)
5. Preserve the bilingual flexibility (Dutch/English based on transcript)

### When Creating New Prompts
Follow the Dembrane design workflow from `/docs/tools/dembrane.md`:

1. **Analyze the Goal** (output type, audience, usage moment)
2. **Define the Role** (specific expertise needed)
3. **Structure the Context** (which conversations, values, assumptions)
4. **Design Output Format First** (slide/document/snippet)
5. **Write Step-by-step Instructions** (numbered, with conditional logic)
6. **Add Crucial Constraints** ("no fabrication", "cite sources", "recent input leading")
7. **Assembly** (Role, Context, Constraints, Instructions, Output, Language, Transparency)
8. **Add YAML Frontmatter** (category, tags, version, privacy placeholders)
9. **Privacy Placeholders** (use `[ORGANISATIE]`, `[NAAM]`, `[DATUM]` for sensitive info)
10. **QA Check** using the checklist in dembrane.md

### Key Design Patterns (From Real Practice)
- **Echo Interventions**: Single powerful question (1 sentence max) for live facilitation—timing matters more than perfection
- **Worksheet Generators**: Transform group discussion into individual work tasks with active questions
- **Narrative Synthesis**: Extract shared values and create coherent story from multiple voices  
- **Implementation Generators**: Multi-step plans with transparency blocks and "Verantwoording"
- **Feedback Processors**: Revision with explicit "Verantwoording van Verwerking Feedback"

See `/learning/ai-facilitation-patterns.md` for detailed patterns extracted from actual usage.

## Common Tasks

### Understanding Project Structure
```bash
# Explore examples directory
ls -la examples/
# List transformation trajectory examples
ls -la examples/transformatieplan_traject_2/sessie_2/
# Read a specific echo intervention
cat examples/universal_for_dembrane/echo_collective_voice.md
# Read a KPI worksheet generator
cat examples/transformatieplan_traject_2/sessie_2/fac_werkblad_kpi.md
# Check documented patterns
cat learning/ai-facilitation-patterns.md
# Check for local context if available
ls -la *.local.md 2>/dev/null || echo "No local context files"
```

### Working with Prompt Templates
- Add YAML frontmatter with category, tags, version, and description
- Follow transparency principles from dembrane.md
- Include "Totstandkoming", "Verantwoording", "Levend Document" sections
- Use privacy placeholders (`[ORGANISATIE]`, `[NAAM]`, `[DATUM]`) for sensitive data

### Language Handling
- **Default**: Generate output in primary language of transcript(s)
- **Multilingual sessions**: Consolidate to explicitly requested target language
- **Style**: Professional, accessible, appropriate to audience

### Quality Assurance
Always include these safeguards in prompts:
- "Base output strictly on explicit information in transcript(s). Invent no details."
- "Name unknowns and uncertainties explicitly."  
- "Cite or reference [<name>] where relevant."
- "Most recent input takes precedence."

## Working with Learning Materials

The `/learning/` directory contains:
- **ai-facilitation-patterns.md**: Documented patterns from real practice
- **iterations/**: Tracking prompt evolution and improvements
- **lessons-learned/**: Capturing insights from actual sessions
- **prompt-ratings/**: Effectiveness assessments

Key resource: `/learning/ai-facilitation-patterns.md` extracts genuine patterns from Amsterdam transformation sessions, documenting what actually works in human-AI collaboration.

## Privacy and Transparency

- **Private content**: Handled via CLAUDE.local.md (git-ignored)
- **Public prompts**: `/examples/` contains real but sanitized prompts
- **Privacy placeholders**: Use `[ORGANISATIE]`, `[NAAM]`, `[DATUM]` for sensitive information
- **Transparency blocks**: Document how outputs were created
- **Version tracking**: Include changelog for iterative improvements

## Prompt Documentation Standards

All prompts in the `/examples/` directory follow a standardized documentation format:

### YAML Frontmatter
Every prompt file includes YAML frontmatter with:
```yaml
---
category: [1-9, see categories below]
tags: [relevant tags]
version: [semver, e.g., 1.0.0]
description: [brief description]
---
```

### Prompt Categories
1. **Gespreksvragen** - Facilitation interventions for live dialogue
2. **Inhoudelijke synthese** - Content analysis and clustering
3. **Implementatie planning** - Action plans and roadmaps
4. **Output generatoren** - Document and presentation creators
5. **Feedback verwerking** - Revision and integration tools
6. **Waardepropositie** - Value and vision articulation
7. **Stakeholder analyse** - Participant and role mapping
8. **Kwaliteitsborging** - Quality assurance and validation
9. **Meta-reflectie** - Process and learning documentation

### Privacy Standards
- Use `[ORGANISATIE]` for organization names
- Use `[NAAM]` for individual names
- Use `[DATUM]` or `[SESSIE-DATUM]` for dates
- Use `[LOCATIE]` for specific locations
- Never include actual client names or identifying details

## Bilingual Context

This project operates bilingually (English/Dutch):
- README.md (English) and LEES_MIJ.md (Dutch) mirror each other
- Prompts may be in either language based on project context
- Generate outputs in the language of the input transcript
- Maintain consistent terminology across languages

## Anti-Patterns to Avoid (From Real Experience)

Key anti-patterns:
- **Over-engineering**: Complex categorization systems nobody uses
- **Fabrication**: Creating fake content, examples, or fictional details
- **Poor timing**: Interrupting deep dialogue for AI insights
- **Over-polish**: Losing the "workshop bench" aesthetic for perfect documentation
- **Technical complexity**: Letting tools interfere with human process
- **Feature creep**: Adding capabilities beyond core facilitation needs
- **Assuming metadata**: Expecting rich tags/structure that doesn't exist

## Integration Notes

- GitHub Issues labeled "Task" track future improvements
- No long-term maintenance promises - this is a workbench
- PRs welcome for additional examples or organizational improvements
- Focus on real use cases, not theoretical templates

---

## Context Layer Architecture

### Public Layer (CLAUDE.md)
This file contains universally applicable instructions for working with the Social AI Workbench. It includes:
- Core project philosophy and workflow
- Public directory structure
- General prompt design patterns
- Documentation standards

### Private Layer (CLAUDE.local.md)
When present (git-ignored), CLAUDE.local.md extends these instructions with:
- Personal working context and style preferences
- References to private directories and materials
- Client-specific project details
- Local development paths and configurations

**Note for AI Assistants:** If CLAUDE.local.md exists in your working directory, read it for additional context that supplements these public instructions. The layered approach ensures this public CLAUDE.md remains universally usable while supporting personalized workflows.

---

## 🤝 RESPECTFUL AI COLLABORATION PRINCIPLES

### Critical Framing: AI-Enhanced Facilitation (Updated 2025-01-12)

**AI as amplification, not replacement**: AI strengthens what facilitators already do well. It doesn't replace their expertise but makes it more accessible and scalable.

**Respectful approach to existing work**: Sticky notes, worksheets, and facilitator methods represent THOUGHTFUL WORK, not chaos. Facilitators put careful consideration into their group processes, session designs, and participant engagement strategies.

### Concrete Respectful Language
- ❌ "chaos of sticky notes" → ✅ "rich material carefully collected by facilitators"
- ❌ "AI creates concept document" → ✅ "AI helps structure the thoughtful work facilitators have done"  
- ❌ "disorganized input" → ✅ "diverse participant perspectives gathered through skilled facilitation"

**Core insight**: "This was already good work. AI helps make it more structured and accessible for next steps."

### Nederlandse-Eerst Workflow

**Language Strategy**:
- **Primary**: Dutch LEES_MIJ files first
- **Secondary**: English README files for broader accessibility  
- **Outputs**: In the language of the input transcripts
- **Style**: Professional, accessible, appropriate to audience

**Cultural Context**: 
This project operates bilingually (English/Dutch):
- Dutch context takes precedence for this trajectory
- Maintain consistent terminology across languages
- Respect Dutch facilitation culture and working methods

### For AI Assistants: Mandatory Mindset

**AI as amplification**: "This work was already good. AI helps make it more structured and accessible for next steps."

**Required respectful language**:
- Describe facilitator work as "thoughtful", "carefully designed", "skillfully collected"
- Frame AI role as "structuring", "amplifying", "making accessible" existing good work
- Acknowledge participant input as "rich material" and "diverse perspectives"  
- Never imply facilitators need AI to do their job properly - AI enhances what they already do well

### Critical Anti-Patterns
- **Over-engineering**: Complex categorization systems nobody uses
- **Fabrication**: Creating fake content, examples, or fictional details
- **Poor timing**: Interrupting deep dialogue for AI insights
- **Over-polishing**: Losing the "workshop bench" aesthetic for perfect documentation
- **Technical complexity**: Letting tools interfere with human process
- **Feature creep**: Adding capabilities beyond core facilitation needs
- **Assuming metadata**: Expecting rich tags/structure that doesn't exist

## For AI Assistants: Key Reminders

1. **Project purpose**: Transparent learning about human-AI collaboration, NOT transformation planning
2. **Truth-first**: Never fabricate—document only real experiences and actual patterns
3. **Read key docs**: `/docs/tools/dembrane.md` for workflow, `/learning/ai-facilitation-patterns.md` for patterns
4. **Preserve the ship-day aesthetic**: Practical and direct, not polished
5. **Understand timing**: These tools are used during live meetings—timing beats sophistication
6. **Respect the bilingual nature**: Be ready to work in Dutch or English
7. **Follow Dembrane data structures**: Conversations have names, tags (maybe), and transcripts
8. **Include transparency in outputs**: Document sources, limitations, and "Verantwoording"
9. **Use privacy placeholders** consistently: `[ORGANISATIE]`, `[NAAM]`, `[DATUM]`, `[LOCATIE]`
10. **Remember the core insight**: AI strengthens human collaboration by catching patterns while facilitators stay present

## 🚨 CRITICAL: Documentation and Findings Architecture

**WHERE TO DOCUMENT FINDINGS AND INSTRUCTIONS:**

- ✅ **Pi Context System**: All project learnings, respectful AI principles, detailed context, and AI assistant instructions go in `~/.claude/context/projects/social_ai_workbench/context.md`
- ✅ **Public examples/**: Only actual prompts and their README stories (5-point structure)
- ❌ **NO CLAUDE.md files in examples/**: These create confusion and put private context in public space

**Rule**: When working on this project, detailed findings, respectful framing principles, technical context, and AI assistant instructions must be documented in the Pi context system (`~/.claude/context/projects/social_ai_workbench/context.md`), not in public-facing CLAUDE.md files within the examples directory.

This is a living document. Update it as the project evolves, but maintain the workbench philosophy and truth-first approach.