# CLAUDE.md - Sessie 1 (Trajectory A)

## Session Context

This directory contains prompts used during the first session of Transformation Planning Trajectory A. These are session-specific tools developed for and used during a live facilitation session.

## Session-Specific Files

- **`synthese_per_thema_universeel.md`**: Universal thematic synthesis tool
- **`tussentijdse_visie_terugkoppeling`**: Mid-session vision feedback processor  
- **`vraag_voor_volgende_groep.md`**: Question generator for next group/session

## Live Session Context

These prompts were designed for real-time use during Session 1, where:

1. **Near-real-time transcription** captured group dialogue via Dembrane
2. **Co-facilitator** monitored transcripts and applied these prompts
3. **Rapid synthesis** provided immediate feedback to participants
4. **Iterative refinement** based on group responses

## Prompt Characteristics

### Thematic Synthesis (`synthese_per_thema_universeel.md`)
- Processes multiple conversation blocks
- Clusters input by themes emerging from dialogue
- Provides structured output for group review
- Language: Dutch (matches session language)

### Vision Feedback (`tussentijdse_visie_terugkoppeling`) 
- Mid-session reflection tool
- Processes participant input on vision development
- Designed for course correction during the session
- Enables rapid iteration based on group feedback

### Next Group Questions (`vraag_voor_volgende_groep.md`)
- Bridges sessions and groups
- Synthesizes current session into actionable questions
- Maintains continuity in multi-group processes
- Forward-looking synthesis tool

## Technical Context

All prompts in this directory:

- **Work with Dembrane XML structure**: `<conversation><name><tags><transcript>`
- **Reference conversations by name**: Clear source attribution
- **Generate Dutch output**: Matches the session language
- **Include transparency blocks**: Show sources and reasoning
- **Handle multiple conversation blocks**: Multi-participant dialogue

## Session Workflow Integration

These prompts fit into the live facilitation flow:

1. **Real-time transcription** via Dembrane QR codes
2. **Continuous monitoring** by co-facilitator
3. **Strategic application** of prompts at key moments
4. **Live integration** of AI output into group dialogue
5. **Rapid feedback loops** for refinement

## For AI Assistants

When working with these session-specific prompts:

### Key Principles
- **Session context matters**: These were designed for specific moments in a group process
- **Language consistency**: Generate Dutch output to match the session
- **Multi-participant awareness**: Handle overlapping voices and perspectives
- **Real-time constraints**: Optimized for speed and clarity, not perfection

### Expected Input
- Multiple Dembrane conversation blocks from Session 1
- Dutch-language transcripts from transformation planning dialogue  
- Participant discussions about vision, themes, and next steps

### Quality Indicators
- Clear thematic clustering in synthesis output
- Actionable questions for next group/session
- Transparent sourcing from specific conversation blocks
- Appropriate Dutch professional language

## Privacy Notes

- Original transcripts with participant names are in `/context/conversations/` (git-ignored)
- These prompts have been sanitized but retain their functional structure
- They represent actual tools used in a real transformation planning process

## Session Legacy

These prompts capture the methodology of Session 1 in Trajectory A, showing how AI synthesis can be integrated into live group processes for immediate value delivery and continuity between sessions.