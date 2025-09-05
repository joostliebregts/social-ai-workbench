# CLAUDE.md - Social AI Workbench

## System Context

You are working with the Social AI Workbench, a living collection of real prompts used in collaborative AI projects. This is a **workshop bench** — messy, alive, and provisional. The core insight behind this project is transparency about how AI actually works in co-creative human processes, specifically during live meetings using near-real-time transcription.

### Core Philosophy
- **Ship-day mode**: This is a workbench, not a polished product
- **Transparency**: Show real AI collaboration processes, not idealized versions  
- **Live facilitation**: Prompts are designed for use during meetings, not just post-session
- **Co-creative partnership**: AI as active dialogue partner, not passive tool
- **Bilingual context**: Work fluidly between English and Dutch

## Critical Notes

1. **Never create fake content**: Wait for real prompts from actual projects
2. **Preserve the workbench aesthetic**: Keep things practical and direct, not polished
3. **Respect privacy**: Any private transcripts in `/context/conversations/` are git-ignored
4. **Language flexibility**: Generate output in the primary language of the input transcript(s)
5. **Multi-conversation awareness**: Understand Dembrane's data structure and reference conversations by name

## File Map

```
/
├── README.md                    # English project overview
├── LEES_MIJ.md                 # Dutch project overview  
├── CLAUDE.md                   # This file - AI assistant instructions
├── METADATA_TEMPLATE.md        # Future prompt organization template
├── .constraints.md             # Ship-day constraints and anti-patterns
├── .gitignore                  # Excludes private conversations
├── examples/                   # Real prompts from actual projects
│   └── Transformatieplan/      # Amsterdam transformation planning prompts
│       ├── facilitatorTool_dynamische_echo.md
│       ├── FacilitatieTool_flipover_generator.md
│       ├── werkblad_generator_KPI.md
│       ├── missie_visie_generator.md
│       └── [other transformation tools]
├── learning/                   # Future: public learning materials
├── context/
│   ├── documentation_guidelines.md  # Writing guidance for repository docs
│   ├── audience_facing/       # Working context and writing guides (git-tracked)
│   └── conversations/         # Private transcripts (git-ignored)
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

1. **Near-real-time transcription** via Dembrane QR codes
2. **Co-facilitator** monitors transcripts and launches prompts
3. **Rapid iteration**: prompt → output → group feedback → refined output
4. **Live synthesis** transforms meetings from "talk and take notes" to "talk and see synthesis"

### Roles in Live Sessions
- **Facilitator**: Focuses on dialogue, introduces AI output to group
- **Co-facilitator/Scribe**: Manages Dembrane, selects transcripts, launches prompts
- **Project lead**: Manages versions, privacy, final integration

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
8. **QA Check** using the checklist in dembrane.md

### Key Design Patterns
- **Echo Interventions**: Single powerful question for live facilitation
- **Implementation Generators**: Multi-step plans with transparency blocks  
- **Synthesis Tools**: Thematic clustering across conversations
- **Feedback Processors**: Revision with "Verantwoording van Verwerking"

## Common Tasks

### Understanding Project Structure
```bash
# Explore examples directory
ls -la examples/
# Read a specific prompt
cat examples/Transformatieplan/facilitatorTool_dynamische_echo.md
# Check constraints and philosophy
cat .constraints.md
```

### Working with Prompt Templates
- Use `METADATA_TEMPLATE.md` structure for future documentation
- Follow transparency principles from dembrane.md
- Include "Totstandkoming", "Verantwoording", "Levend Document" sections

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

The `/learning/` directory is planned for:
- Public learning materials and iterations
- Lessons-learned documentation
- Prompt effectiveness ratings
- Workshop methodologies

Current status: Not yet populated (ship-day constraints)

## Privacy and Transparency

- **Private transcripts**: `/context/conversations/` is git-ignored
- **Public prompts**: `/examples/` contains real but sanitized prompts
- **Transparency blocks**: Document how outputs were created
- **Version tracking**: Include changelog for iterative improvements

## Repository Documentation Standards

When working on public-facing repository documentation (README's, CHANGELOG's, etc.):

**See `/context/documentation_guidelines.md` for comprehensive guidance on:**
- Writing style and tone for external documentation
- Language policy (English/Dutch usage)
- Content principles and privacy boundaries
- Repository-specific formatting standards
- Quality checklist for public-facing content

**Quick reference:**
- Keep the workbench aesthetic - practical over polished
- Start with concrete observations, not corporate speak
- Use sentence case for headers
- Evidence-link decisions and credit sources
- Respect privacy boundaries (`[ORGANISATIE]` for client names)

## Bilingual Context

This project operates bilingually (English/Dutch):
- README.md (English) and LEES_MIJ.md (Dutch) mirror each other
- Prompts may be in either language based on project context
- Generate outputs in the language of the input transcript
- Maintain consistent terminology across languages

## Anti-Patterns to Avoid

From `.constraints.md`:
- Over-engineering or complex organization systems
- Creating fake content or examples
- Premature categorization/metadata
- Polished product mindset
- Losing the "workshop bench" aesthetic
- Feature creep beyond core purpose

## Integration Notes

- GitHub Issues labeled "Task" track future improvements
- No long-term maintenance promises - this is a workbench
- PRs welcome for additional examples or organizational improvements
- Focus on real use cases, not theoretical templates

---

## For AI Assistants: Key Reminders

1. **Read `/docs/tools/dembrane.md` first** for comprehensive workflow understanding
2. **Preserve the ship-day aesthetic** - practical and direct, not polished
3. **Work with real content only** - never fabricate examples
4. **Understand the live facilitation context** - these tools are used during meetings
5. **Respect the bilingual nature** - be ready to work in Dutch or English
6. **Follow Dembrane data structures** - conversations have names, tags, and transcripts
7. **Include transparency in outputs** - document sources and limitations
8. **Remember the core insight**: AI as co-creative partner during live dialogue

This is a living document. Update it as the project evolves, but maintain the workbench philosophy.