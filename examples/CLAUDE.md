# CLAUDE.md - Examples Directory

## Purpose

This directory contains raw prompts from real projects in the Social AI Workbench. These are not polished templates — they are working artifacts from live facilitation sessions, showing how AI prompts actually get used during collaborative meetings.

## What You'll Find Here

- **Real prompts**: Actual prompts used in transformation planning and other collaborative processes
- **Context-dependent content**: These prompts reference specific Dembrane conversation structures
- **Bilingual materials**: Dutch and English content based on the original project language
- **Live facilitation tools**: Designed for use during meetings, not just post-session analysis

## Directory Structure

```
examples/
├── transformatieplan_traject_B/     # Amsterdam transformation planning - trajectory B
│   ├── concept_deelplan_generator_universeel.md
│   ├── facilitatorTool_dynamische_echo.md
│   ├── FacilitatieTool_flipover_generator.md
│   ├── missie_visie_generator.md
│   └── [other transformation tools]
└── transformatieplan_traject_a/     # Transformation planning - trajectory A
    └── sessie_1/                    # Session-specific prompts
        ├── synthese_per_thema_universeel.md
        ├── tussentijdse_visie_terugkoppeling
        └── vraag_voor_volgende_groep.md
```

## How These Prompts Work

All prompts in this directory are designed for the Dembrane workflow:

1. **Multi-conversation data**: Handle XML blocks with `<name>`, `<tags>`, and `<transcript>` elements
2. **Live application**: Used during meetings with near-real-time transcription
3. **Rapid iteration**: Applied → output → group feedback → refined output
4. **Language flexibility**: Generate output in the primary language of the transcript(s)

## Key Patterns

### Echo Interventions
Single powerful questions for live facilitation (e.g., `facilitatorTool_dynamische_echo.md`)

### Implementation Generators
Multi-step plans with transparency blocks showing sources and reasoning

### Synthesis Tools
Thematic clustering and analysis across multiple conversation blocks

### Feedback Processors
Revision tools with "Verantwoording van Verwerking" (reasoning documentation)

## Working with These Prompts

### Before Use
1. Read the entire prompt to understand its structure
2. Check the expected Dembrane conversation format
3. Understand whether it's designed for single or multiple conversations
4. Note any session-specific context or constraints

### During Application
- Always reference conversations by their `<name>` when citing sources
- Base output strictly on explicit information in transcripts
- Include transparency blocks showing sources and limitations
- Follow the language of the input transcript(s)

## Privacy and Context

- These prompts have been sanitized of client-specific details
- They represent real usage patterns from actual facilitation sessions
- The original transcripts they worked with are in `/context/conversations/` (git-ignored)
- Each prompt captures a specific moment in a collaborative process

## Anti-Patterns

These examples intentionally avoid:
- Over-engineered categorization systems
- Fake or theoretical examples
- Universal templates that ignore context
- Polished product presentation

## For AI Assistants

When working with these prompts:

1. **Understand the live context**: These were used during active meetings
2. **Preserve the workbench aesthetic**: Keep practical, not polished
3. **Respect the Dembrane structure**: Always work with the XML conversation format
4. **Include transparency**: Document sources and limitations in outputs
5. **Language awareness**: Generate in Dutch or English based on transcript language
6. **No fabrication**: Base all output on explicit transcript content

Remember: These are workshop tools, not documentation. They show how AI actually gets integrated into collaborative human processes.