# Evidence Card Research Workflow: Detailed Reference

This document provides comprehensive background and detailed methodology for evidence card research. For day-to-day operations, see the main [SKILL.md](SKILL.md) file.

## Historical Development Context

### Research Methodology Evolution
This workflow was developed through extensive iterative refinement, incorporating user feedback from multiple evidence card creation sessions. Key lessons learned:

1. **Tool Efficiency Discovery**: Initially used inefficient search tools, leading to prohibitive token costs. Developed strict hierarchy prioritizing Perplexity Ask over Perplexity Search.

2. **Quote Quality Standards**: User feedback emphasized avoiding "teeny tiny, disconnected, choppy random quotes" in favor of complete, impactful sentences.

3. **Source Verification Protocol**: Established requirement to always trace quotes back to original primary sources rather than accepting secondary summaries.

### Iterative Quality Control Process
The approval questionnaire format evolved from trial-and-error:

**Original Approach**: Direct card creation without structured feedback
**Problem**: Inconsistent quality, missed user preferences
**Solution**: Implemented multiple-choice approval system:
- A) Excellent - Rich, complete sentences with detailed explanations
- B) Good - Has some context but could be improved
- C) Poor - Short, choppy quotes that need significant revision
- D) Acceptable - Meets minimum standards for debate evidence

## Advanced Research Techniques

### Source Type Specialization

#### Constitutional Analysis
For constitutional arguments, use this progression:
1. **mcp__perplexity__perplexity_reason** - For complex constitutional interpretation
2. **Court Decision Access**: Use exa crawling for full opinions
3. **Quote Targeting**: Focus on holdings, reasoning, and precedential language
4. **Verification Priority**: Cross-reference with official court databases

#### Policy Analysis from Think Tanks
1. **Credential Verification**: Confirm author expertise and institutional authority
2. **Publication Context**: Understand think tank mission and potential bias
3. **Methodology Review**: Assess research quality and evidence backing
4. **Quote Extraction**: Prioritize policy analysis over opinion pieces

#### Government Source Research
1. **Official Position Identification**: Distinguish between official statements and individual opinions
2. **Document Hierarchy**: Prioritize primary documents over press releases
3. **Temporal Context**: Consider policy evolution and changing positions
4. **Cross-Agency Verification**: Confirm consistency across related departments

## Advanced Quality Assurance

### Source Reliability Matrix
```
Tier 1: Supreme Court opinions, Congressional Research Service
Tier 2: Federal agency official documents, peer-reviewed academic papers
Tier 3: Reputable think tanks (Cato, Heritage, Brookings), major newspapers
Tier 4: Trade publications, advocacy organizations
Tier 5: Secondary sources, encyclopedia entries (avoid)
```

### Quote Verification Protocol
1. **Original Source Access**: Use exa crawling with livecrawl: "preferred"
2. **Context Preservation**: Extract surrounding paragraphs for verification
3. **Attribution Accuracy**: Confirm speaker credentials and institutional affiliation
4. **Temporal Relevance**: Verify publication date and continuing validity

## Technical Implementation Details

### Windows-Specific Solutions
**File Path Handling**:
```bash
# Problem: Spaces in file names cause bash failures
# Solution: Use PowerShell for complex operations
powershell "Move-Item 'source with spaces.pdf' 'destination with spaces.pdf'"
```

**MCP Configuration**:
```json
{
  "mcpServers": {
    "perplexity": {
      "command": "cmd /c npx",  // Required for Windows compatibility
      "args": ["@anthropic-ai/mcp-server-perplexity"]
    }
  }
}
```

### PDF Generation Optimization
**Evolution from Print-to-PDF to Direct Conversion**:
- **Original Method**: Microsoft Print to PDF via print dialog
- **Limitations**: Required user interaction, inconsistent formatting
- **Current Method**: `mcp__Printer__markdown_to_pdf` direct conversion
- **Advantages**: Consistent formatting, automation capability, better quality

## Troubleshooting Advanced Issues

### Claude Skill Activation Problems
**Symptom**: Skill not triggering for relevant requests
**Diagnostic Process**:
1. Check description contains key trigger terms: "debate", "evidence", "research", "policy"
2. Verify YAML frontmatter validity (proper --- delimiters, no tabs)
3. Confirm file path: `.claude/skills/evidence-card-research/SKILL.md`
4. Test with explicit trigger: "I need to create debate evidence cards"

### Source Verification Challenges
**Problem**: Paywalled or inaccessible sources
**Solutions**:
1. **Alternative Source Search**: Look for same content in open-access venues
2. **Institutional Access**: Check if available through university databases
3. **Author Direct Contact**: Sometimes authors provide copies for research
4. **Alternative Platforms**: Search for pre-print versions or institutional repositories

### Quote Integration Issues
**Problem**: Quotes don't flow naturally when read aloud
**Resolution Techniques**:
1. **Context Expansion**: Include surrounding sentences for coherence
2. **Paraphrase Integration**: Combine partial quotes with paraphrased context
3. **Speaker Attribution**: Ensure clear who is speaking and their authority
4. **Logical Flow**: Arrange quotes to build coherent argument progression

## User Feedback Integration

### Common Pattern Recognition
**Recurring User Corrections**:
1. **Quote Fragmentation**: Users consistently rejected short, disconnected quotes
2. **Source Attribution**: Users demanded original sources, not encyclopedia excerpts
3. **Context Requirements**: Users wanted full attribution context, not just quotes
4. **Format Consistency**: Users preferred structured markdown table format

### Feedback Response Protocol
1. **Immediate Correction**: Revise specific issues without argument
2. **Pattern Recognition**: Identify recurring themes in user corrections
3. **Standard Updates**: Update methodology based on consistent feedback
4. **Documentation**: Record lessons learned in workflow documentation

## Methodology Validation

### Successful Outcomes Metrics
- **Quote Acceptance Rate**: Target >90% approval on first submission
- **Source Quality**: 100% original, verifiable sources
- **Format Compliance**: 100% adherence to markdown table structure
- **Timeliness**: Complete evidence sets within 2-3 hours

### Continuous Improvement Indicators
- **Reduced Revision Cycles**: Moving from 3-4 revisions to 1-2 revisions per card
- **User Satisfaction**: Higher approval ratings and fewer correction requests
- **Efficiency Gains**: Faster completion times through better tool usage
- **Quality Consistency**: Maintained standards across different research topics

## Future Development Areas

### Potential Enhancements
1. **Template Automation**: Create reusable templates for common source types
2. **Batch Processing**: Develop methods for processing multiple sources efficiently
3. **Quality Scoring**: Implement automated quality assessment metrics
4. **Cross-Reference Integration**: Build databases of quoted material for reuse

### Technology Integration Opportunities
1. **AI-Assisted Source Finding**: Enhanced algorithms for optimal source identification
2. **Automated Citation Formatting**: Direct integration with citation management systems
3. **Collaborative Review Platforms**: Team-based evidence card review and approval
4. **Performance Analytics**: Tracking research efficiency and quality metrics

---

*This workflow represents the culmination of extensive real-world testing and user feedback. For routine evidence card creation, refer to the main SKILL.md file. Use this document for complex cases, troubleshooting, or methodology enhancement.*