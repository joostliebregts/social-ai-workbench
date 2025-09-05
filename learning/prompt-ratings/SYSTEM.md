# Prompt Rating System

Framework for assessing prompt effectiveness in real collaborative contexts.

## Rating Dimensions

### 1. Output Quality (1-5)
- **5**: Exceptional - Output needs no editing, captures nuance perfectly
- **4**: High - Minor tweaks needed, good grasp of context  
- **3**: Good - Solid foundation, some refinement required
- **2**: Fair - Usable but needs significant improvement
- **1**: Poor - Major issues, requires complete rework

### 2. Context Sensitivity (1-5)
- **5**: Perfectly adapted to specific project/group dynamics
- **4**: Well-tuned to context with minor generic elements
- **3**: Generally appropriate, some context missed
- **2**: Some context awareness, mostly generic
- **1**: Context-blind, generic output

### 3. Live Facilitation Fit (1-5)
*How well does this work in near-real-time during meetings?*
- **5**: Perfect timing, enhances flow of conversation
- **4**: Good timing, minimal disruption to meeting flow
- **3**: Workable timing, some adjustment needed
- **2**: Slow enough to create awkward pauses
- **1**: Too slow for live use, post-session only

### 4. Iteration Friendliness (1-5)
*How well does this prompt handle feedback and refinement?*
- **5**: Excellent at incorporating feedback while maintaining structure
- **4**: Good at refinement with clear feedback
- **3**: Handles straightforward feedback well
- **2**: Requires careful feedback framing
- **1**: Difficult to refine, tends to lose coherence

## Overall Effectiveness Score
Average of all dimensions, plus subjective assessment:
- **A+**: Exceptional prompt, ready for wide reuse
- **A**: High quality, works reliably in context
- **B**: Good prompt, minor improvements needed  
- **C**: Functional but needs iteration
- **D**: Major issues, significant rework required

## Assessment Template

```markdown
# Prompt Assessment: [Prompt Name]

## Scores
- Output Quality: X/5
- Context Sensitivity: X/5  
- Live Facilitation Fit: X/5
- Iteration Friendliness: X/5

**Overall: [Letter Grade]**

## Notes
- What worked exceptionally well:
- Main areas for improvement:
- Specific contexts where this excels:
- Contexts where this struggles:

## Recommendation
- [Ready for reuse / Needs iteration / Retire prompt]
```