# Changelog

All notable changes to the Social AI Workbench project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Planned
- Additional prompt templates for common facilitation scenarios
- Expanded documentation for Dembrane integration workflows
- Additional pattern documentation from emerging practice

## [0.3.0] - 2025-01-05

### Changed

#### Major Documentation Overhaul
- **Repositioned project purpose**: Now clearly focused on transparency about human-AI collaboration, with transformation planning as example context rather than primary focus
- **Complete README/LEES_MIJ rewrite**:
  - Truth-first approach eliminating all fictional content
  - Lead with core purpose rather than domain examples
  - Enhanced accessibility for non-technical audiences (facilitators, teachers)
  - Authentic Dutch version rather than translation
  - Direct links to real examples for immediate access

#### CLAUDE.md Updates
- Updated System Context to reflect repositioned purpose
- Enhanced Core Philosophy with transparency-first and learning-from-practice principles
- Clarified transformation planning as example domain, not project purpose
- Updated file map to reflect actual directory structure
- Enhanced workflow documentation with accurate technical details
- Improved Key Design Patterns section with references to documented patterns
- Updated Anti-Patterns with learnings from real experience
- Revised AI Assistant reminders emphasizing truth-first approach

### Added

#### Learning Documentation
- Created comprehensive `/learning/ai-facilitation-patterns.md`:
  - Documented patterns from actual Amsterdam transformation sessions
  - Technical infrastructure insights from Dembrane usage
  - Live facilitation patterns (Echo, Worksheet, Narrative)
  - AI-Human collaboration dynamics and role distribution
  - Timing insights and quality patterns
  - Common failure modes and effectiveness indicators

#### Enhanced Agent Capabilities
- Improved joost-writing-coach agent with stronger truth-first constraints
- Better handling of fabrication prevention
- Enhanced bilingual support

## [0.2.0] - 2025-01-05

### Added

#### Prompt Documentation System
- Implemented YAML frontmatter for 21+ prompt files with metadata
- Established 9-category classification system for prompts:
  - Analysis, Synthesis, Planning, Facilitation, Documentation
  - Feedback, Generation, Evaluation, Communication
- Added context blocks to all prompts explaining their purpose and usage
- Created universal/ folder with cross-project echo facilitation tools

#### Privacy Standardization
- Applied privacy placeholder system across all examples:
  - [ORGANISATIE] for client/organization names
  - [REGIO-NAAM] for geographic identifiers  
  - [SESSIE-DATUM] for meeting dates
  - [DEELNEMER] for participant names
- Standardized traject_1 and traject_2 directories with privacy-first approach
- Ensured no git-ignored content paths are referenced in documentation

### Changed

#### Documentation Updates
- Major overhaul of CLAUDE.md:
  - Fixed file map to reflect actual repository structure
  - Added comprehensive prompt documentation standards
  - Separated public/private context layers explicitly
  - Updated all example paths and references
  - Added detailed workflow for working with Dembrane data
- Updated README.md and LEES_MIJ.md with current project status
- Enhanced transparency about AI collaboration in documentation

#### Repository Structure
- Reorganized examples/ directory with clearer taxonomy
- Added transformatieplan_traject_1 and traject_2 alongside traject_B
- Created universal/ directory for cross-project facilitation tools
- Improved separation between workbench tools and polished outputs

### Technical
- Improved prompt consistency with standardized structure
- Enhanced citation requirements (conversations referenced by name)
- Strengthened anti-fabrication constraints in all prompts

### Notes
- This update represents collaborative work between human and AI (Claude) to standardize and improve the workbench
- Maintains ship-day aesthetic - functional over polished
- All changes preserve the core philosophy of transparency in AI collaboration

## [0.1.0] - 2025-01-05

### Added

#### Repository Structure
- Initial repository setup with modular directory structure
- Created `examples/` directory for real-world AI collaboration examples
- Created `learning/` directory for knowledge capture and improvement tracking
- Established structure for separating public and private project materials
- Added comprehensive `.gitignore` for privacy protection

#### Documentation
- Created bilingual README.md (English/Dutch) with near-real-time transcription context
- Added comprehensive CLAUDE.md main documentation file with:
  - System context and critical notes
  - Complete file map of repository structure
  - Workflow documentation for prompt sharing
  - Paved path guidelines for contributors
  - Common tasks and quick reference
- Created specialized CLAUDE.md files for subdirectories:
  - `examples/CLAUDE.md` - Example directory documentation
  - `learning/CLAUDE.md` - Learning framework documentation
  - Individual project CLAUDE.md files for trajectory examples
- Documented Dembrane integration approach and benefits
- Added GitHub issue template for task management

#### Learning Framework
- Established `learning/iterations/` for tracking prompt evolution
- Created `learning/lessons-learned/` for capturing insights
- Set up `learning/prompt-ratings/` for quality assessment
- Implemented structured approach for continuous improvement

#### Example Projects
- Added [PROJECT]_traject_B as reference implementation
- Renamed project files for clarity and consistency:
  - Removed "generator" suffix from all files
  - Converted to uppercase naming convention
  - Added [fac] prefix for facilitation-specific tools
- Created template structure for traject_1 and traject_2

### Changed

#### File Naming Conventions
- Standardized prompt file naming: `[category]_DESCRIPTIVE_NAME.md`
- Implemented prefix system:
  - `[fac]` for facilitation tools
  - `[doc]` for documentation generators
  - `[ana]` for analysis prompts
- Established uppercase convention for main descriptive names

#### Project Organization
- Restructured example directories for better navigation
- Improved separation between public prompts and project-specific materials
- Enhanced modularity for easy sharing and reuse

### Security & Privacy
- Implemented privacy-first approach with gitignored conversation contexts
- Planned anonymization strategy for sensitive information
- Established clear boundaries between shareable and private content

### Technical
- Configured repository for GitHub collaboration
- Set up issue tracking with custom templates
- Prepared for semantic versioning of prompt iterations

## Version History

### Versioning Strategy
This project uses semantic versioning:
- MAJOR version for incompatible prompt structure changes
- MINOR version for new functionality in backward-compatible manner
- PATCH version for backward-compatible improvements and fixes

### Release Notes
**v0.1.0** marks the initial public release of the Social AI Workbench, establishing the foundation for collaborative AI prompt sharing and learning within professional facilitation contexts.

---

*This changelog is maintained as part of the Social AI Workbench project, documenting the evolution of collaborative AI practices in professional settings.*