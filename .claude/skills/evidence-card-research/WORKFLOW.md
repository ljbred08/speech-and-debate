# Evidence Card Research Workflow: Detailed Guide

This document provides the comprehensive workflow for creating high-quality evidence cards for policy debate.

## Table of Contents

- [Initial Setup and Configuration](#initial-setup-and-configuration)
- [Research Methodology](#research-methodology)
- [Source Quality Standards](#source-quality-standards)
- [Evidence Card Structure](#evidence-card-structure)
- [Iterative Review Process](#iterative-review-process)
- [Specific Research Techniques](#specific-research-techniques)
- [Technical Considerations](#technical-considerations)
- [Common Pitfalls and Solutions](#common-pitfalls-and-solutions)
- [Final Output Requirements](#final-output-requirements)

## Initial Setup and Configuration

### MCP Server Configuration
- Fixed Windows MCP configuration warning by changing perplexity server command from `"npx"` to `"cmd /c npx"` in `.claude.json`
- This resolved compatibility issues with Windows command execution

### File Organization
- Created dedicated `evidence-cards/` folder for all research outputs
- Maintained both markdown source files and printable PDF versions
- Used systematic naming convention for easy identification

## Research Methodology

### Tool Selection and Usage Hierarchy
1. **Perplexity Ask** - **PRIMARY search tool** for researching and answering questions about web content
2. **Perplexity Reason** - Excellent for in-depth analysis and comprehensive research when more detail is needed
3. **exa Web Search** - Preferred for controlled searches with live crawl capability
4. **exa Crawling** - Best for extracting full content from specific URLs with `livecrawl: "preferred"`
5. **Web Fetch** - Backup tool when exa tools are unavailable
6. **Perplexity Search** - **ALMOST NEVER USE** - Extremely high token count, avoid unless absolutely necessary

### Search Strategy Guidelines
- **Default to Perplexity Ask** as the primary research tool
- Use Perplexity Reason when deeper analysis is required
- Use `livecrawl: "preferred"` with exa tools to get fresh content rather than cached results
- Specify `numResults` parameter to limit search results and avoid overwhelming data
- **Avoid Perplexity Search** due to prohibitive token consumption
- Reserve Perplexity Search only for situations where other tools cannot provide needed information

## Source Quality Standards

### Primary Requirements
1. **Original Sources Only** - Never use encyclopedia excerpts or secondary summaries
2. **Single Source Per Card** - Each evidence card should feature ONE primary source
3. **Substantial Quotes** - Use complete, impactful sentences rather than short fragments
4. **Fresh Verification** - Always freshly fetch and verify each citation before finalizing

### Quote Quality Criteria
- Quotes must be complete sentences that flow naturally when read aloud
- Avoid "teeny tiny, disconnected, choppy random quotes"
- Each quote should stand alone as a coherent statement
- Verbal citations should include context and explanation
- Example format: "John Doe, in his article on example.com, says that 'Because such and such makes da da da da, we should not ban stock trading; it would create such and such an effect on la de dah and so on and so forth.'"

## Evidence Card Structure

### Required Elements
1. **Tag Line** - Concise summary of the main argument
2. **Verbal Citation** - Substantial quote(s) with proper attribution
3. **What the evidence says in context** - Explanation of the source's argument and relevance
4. **Impact** - Analysis of how the evidence supports the position
5. **Source Information** - Complete bibliographic details including:
   - Webpage or Book Title
   - URL or page number
   - Article Title if applicable
   - Author or Publisher
   - Date first published
   - Date updated (if applicable)
   - Date accessed

### Formatting Standards
- Use markdown table format for consistency
- Separate multiple quote sections with `<br><br>` for readability
- Maintain academic citation format throughout
- Ensure all source information is complete and verifiable

## Iterative Review Process

### Quality Control Steps
1. **Initial Research** - Find potential sources using Perplexity Ask or exa tools
2. **Source Verification** - Use exa crawling or Web Fetch to access full content
3. **Quote Selection** - Extract substantial, impactful quotes from original sources
4. **Draft Creation** - Create evidence card with proper structure and citations
5. **User Review** - Present cards for approval using multiple-choice questions
6. **Revision** - Refine based on feedback until quality standards are met
7. **Final Verification** - Double-check all quotes and source information
8. **PDF Generation** - Create printable versions using Microsoft Print to PDF

### Approval Questions Format
Present multiple-choice questions for each card:
- A) Excellent - Rich, complete sentences with detailed explanations
- B) Good - Has some context but could be improved
- C) Poor - Short, choppy quotes that need significant revision
- D) Acceptable - Meets minimum standards for debate evidence

## Specific Research Techniques

### Court Decisions
- Use exa crawling to access full court opinions
- Focus on constitutional analysis and holdings
- Quote key language about legal standards and reasoning
- Look for precedential value and binding authority

### Academic and Think Tank Sources
- Verify author credentials and institutional affiliations
- Extract policy analysis and constitutional arguments
- Look for experts with relevant academic or professional backgrounds
- Prioritize peer-reviewed or institutional publications

### Government Sources
- Access official statements and reports
- Focus on authoritative policy positions
- Verify publication dates and official attribution
- Cross-reference with primary source documents

## Technical Considerations

### Windows-Specific Issues
- Use `"cmd /c npx"` wrapper for npx commands in MCP configurations
- Handle file path quoting carefully when moving files with spaces
- Use PowerShell for complex file operations when bash fails
- Be aware of path escaping requirements in different shells

### PDF Generation
- Use Microsoft Print to PDF as default printer
- Create systematic file naming for easy identification
- Move PDFs to same location as source files for organization
- Test printer availability before starting large print jobs

### Backup and Preservation
- Commit work after major milestones to prevent loss
- Maintain both markdown and PDF versions
- Use descriptive file names for content identification
- Create organized folder structures for project management

## Common Pitfalls and Solutions

### Quote Quality Issues
- **Problem**: Short, fragmented quotes that lack context
- **Solution**: Always use complete sentences with clear attribution and context
- **Red Flag**: Quotes that don't make sense when read alone

### Source Reliability
- **Problem**: Using secondary sources or encyclopedia excerpts
- **Solution**: Always trace quotes back to original primary sources
- **Best Practice**: Verify every quote from the original document

### Verification Gaps
- **Problem**: Assuming quotes are accurate without verification
- **Solution**: Always fetch and verify each quote from the original source
- **Quality Check**: Cross-reference quote accuracy against source material

### File Organization
- **Problem**: Misplaced or disorganized research materials
- **Solution**: Use systematic naming and keep all related files in dedicated folders
- **Structure**: Create clear hierarchy with project-specific organization

### Tool Efficiency
- **Problem**: Wasting tokens on inefficient tools
- **Solution**: Use Perplexity Ask as primary tool, avoid Perplexity Search
- **Cost Management**: Monitor token usage and choose tools appropriately

## Final Output Requirements

Each evidence card must include:
- High-quality original source with verifiable credentials
- Substantial, complete-sentence quotes that flow naturally when read
- Complete bibliographic information for academic citation
- Clear impact analysis connecting evidence to policy position
- Both markdown source and printable PDF versions
- Proper formatting following debate evidence standards

## User Feedback Integration

### Key Learning Points
1. **Quote Quality Over Quantity**: Better to have fewer substantial quotes than many fragmented ones
2. **Original Source Verification**: Never trust secondary summaries without primary source verification
3. **Contextual Attribution**: Always provide full context for who is saying what and why it matters
4. **Iterative Refinement**: Be prepared to revise based on quality standards and user feedback
5. **Tool Efficiency**: Choose the most cost-effective tools for each research task

### Communication Standards
- Present work systematically with clear progress tracking
- Use multiple-choice questions for structured feedback
- Explain research decisions and source selection rationale
- Maintain transparency about verification processes

This workflow ensures production of debate evidence that meets the highest academic standards while maintaining practical utility for competitive policy debate.