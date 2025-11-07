---
name: evidence-card-research
description: Create high-quality debate evidence cards with proper source verification, substantial quotes, and academic rigor. Use when researching policy debate topics, finding constitutional arguments, or creating evidence cards for competitive debate.
allowed-tools: mcp__perplexity__perplexity_ask, mcp__perplexity__perplexity_reason, mcp__exa__web_search_exa, mcp__exa__crawling_exa, WebFetch, Read, Write, Edit, TodoWrite, mcp__Printer__print_file, mcp__Printer__markdown_to_pdf, mcp__Printer__list_printers
---

# Evidence Card Research Assistant

This skill provides a comprehensive workflow for creating debate evidence cards that meet the highest academic standards while maintaining practical utility for competitive policy debate.

## Quick Start

When you need to create evidence cards for debate, I will:

1. **Research Phase**: Use Perplexity Ask as primary tool, exa tools for verification
2. **Source Verification**: Extract full content from original sources
3. **Quote Selection**: Find substantial, complete-sentence quotes
4. **Card Creation**: Format with proper structure and attribution
5. **Quality Review**: Present for approval with structured feedback
6. **Final Output**: Generate both markdown and PDF versions

## Tool Usage Hierarchy (CRITICAL)

Use tools in this order for efficiency:

1. **mcp__perplexity__perplexity_ask** - PRIMARY research tool (most efficient)
2. **mcp__perplexity__perplexity_reason** - For complex constitutional analysis
3. **mcp__exa__web_search_exa** - Controlled searches with livecrawl: "preferred"
4. **mcp__exa__crawling_exa** - Extract full content from specific URLs
5. **WebFetch** - Backup when exa tools unavailable
6. **AVOID mcp__perplexity__perplexity_search** - Extremely high token cost

## Evidence Card Structure

Each card must include:

```markdown
| **Tag Line** | Concise summary of main argument |
|--------------|----------------------------------|
| **Verbal Citation** | Substantial quote(s) with proper attribution |
| **What the evidence says in context** | Explanation of source's argument |
| **Impact** | Analysis of how evidence supports position |
| **Webpage or Book Title** | Complete source title |
| **URL or page number** | Full URL or page reference |
| **Article Title if Applicable** | Specific article or chapter title |
| **Author or Publisher** | Author credentials and publisher |
| **Date first published** | Original publication date |
| **Date updated** | Last update date if applicable |
| **Date accessed** | Research access date |
```

## Quote Quality Standards

### Requirements
- Quotes must be complete sentences that flow naturally when read aloud
- Each quote should stand alone as a coherent statement
- Avoid "teeny tiny, disconnected, choppy random quotes"
- Include context and explanation in verbal citations

### Good Example Format
"John Doe, in his article on example.com, says that 'Because such and such makes da da da da, we should not ban stock trading; it would create such and such an effect on la de dah and so on and so forth.'"

### Bad Examples
- "Rather than broaden the ban, Congress should repeal it entirely" (too short)
- "no charges ever brought" (fragmented)
- Multiple short quotes without context

## Research Process

### 1. Initial Research
- Use Perplexity Ask with specific, targeted queries
- Focus on finding original sources, not encyclopedia excerpts
- Look for court decisions, academic papers, think tank analysis

### 2. Source Verification
- Use exa crawling with `livecrawl: "preferred"` for fresh content
- Always verify quotes from original source documents
- Cross-reference author credentials and institutional authority

### 3. Quality Control
- Present cards for approval using multiple-choice questions:
  - A) Excellent - Rich, complete sentences with detailed explanations
  - B) Good - Has some context but could be improved
  - C) Poor - Short, choppy quotes that need significant revision
  - D) Acceptable - Meets minimum standards for debate evidence

## Common Research Scenarios

### Court Decisions
- Use exa crawling to access full opinions
- Focus on constitutional analysis and holdings
- Quote key language about legal standards and reasoning

### Academic/Think Tank Sources
- Verify author credentials and institutional affiliations
- Extract policy analysis and constitutional arguments
- Prioritize peer-reviewed or institutional publications

### Government Sources
- Access official statements and reports
- Focus on authoritative policy positions
- Cross-reference with primary source documents

## Technical Considerations

### File Organization
- Create dedicated `evidence-cards/` folder
- Maintain both markdown and PDF versions
- Use systematic naming (01-topic-source.md)

### PDF Generation
- **Default**: Use `mcp__Printer__markdown_to_pdf` to convert markdown evidence cards directly to PDF files
- Create clear file naming for identification (01-topic-source.pdf)
- Save PDFs to same location as source files
- **Physical Printouts**: Only use `mcp__Printer__list_printers` and `mcp__Printer__print_file` when user specifically requests physical printing

### Windows-Specific Issues
- Use PowerShell for complex file operations when bash fails
- Handle file path quoting carefully with spaces in names

## Output Examples

### Final Evidence Card Set
Each project should include:
- 8+ evidence cards with different sources
- Both markdown source files and printable PDFs
- Complete verification of all quotes and sources
- Proper academic citation format

### Quality Checklist
Before finalizing each card:
- [ ] Source is original and verifiable
- [ ] Quotes are complete and impactful sentences
- [ ] Attribution includes full context
- [ ] Impact analysis connects evidence to position
- [ ] Source information is complete and accurate
- [ ] Card follows proper formatting structure

## Troubleshooting

### If Claude Doesn't Use This Skill
- Check that description includes key terms: "debate", "evidence", "research", "policy"
- Ensure YAML frontmatter is valid (--- opening/closing, proper indentation)
- Verify skill is in correct location: `.claude/skills/evidence-card-research/SKILL.md`

### Common Issues
- **Poor quote quality**: Re-read "Quote Quality Standards" section
- **Source verification gaps**: Always use exa crawling to verify original sources
- **Inefficient tool usage**: Follow tool hierarchy strictly, avoid Perplexity Search

## Continuous Improvement
If the user tells you a new tweak that is not already covered in this skill file, ask the user if they'd like you to add it to this skill file.

## Version History

- v1.0.0 (2025-11-07): Initial release with complete workflow and quality standards