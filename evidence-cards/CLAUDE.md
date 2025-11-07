# Evidence Cards Collection

This folder contains debate evidence cards with both markdown source files and corresponding PDF versions for competitive policy debate research and competition.

## Folder Structure

### Evidence Cards (.md files)
- **Purpose**: Markdown source files containing structured evidence for debate
- **Structure**: Each file should follow the standard evidence card format with:
  - Tag lines summarizing main arguments
  - Verbal citations with substantial quotes
  - Context explaining source arguments
  - Impact analysis connecting evidence to positions
  - Complete bibliographic information for academic citation

### Printable Versions (.pdf files)
- **Purpose**: Formatted PDF versions ready for debate competition use
- **Generation**: Should be created using `mcp__Printer__markdown_to_pdf` for consistent formatting
- **Usage**: Intended for printing and evidence exchange in debate rounds
- **Naming**: Should use clear, descriptive naming (e.g., "01-topic-source.pdf")

## Quality Standards

### Source Requirements
All evidence cards should contain:
- **Original Sources Only**: No encyclopedia excerpts or secondary summaries
- **Authoritative Sources**: Court decisions, government documents, academic papers, reputable think tanks
- **Complete Verification**: All quotes must be verified from original source documents
- **Proper Attribution**: Full context including speaker credentials and institutional authority

### Quote Quality Standards
Quotes should be:
- **Complete Sentences**: Full sentences that flow naturally when read aloud
- **Substantial Content**: Meaningful quotes that support arguments, not fragments
- **Contextual**: Include enough surrounding information to understand the quote's significance
- **Accurate**: Exact wording from original sources with proper citation

## File Management

### Organization
- **Naming Convention**: Use systematic numbering (01-, 02-, etc.) for easy organization
- **Consistent Structure**: All files should follow the same evidence card template
- **Paired Files**: Each markdown file should have a corresponding PDF version
- **Version Control**: Commit changes to preserve research progress

### Creation Workflow
When creating new evidence cards:
1. **Research Phase**: Use Perplexity Ask as primary research tool
2. **Source Verification**: Use exa crawling to access and verify original sources
3. **Quote Selection**: Extract substantial, complete-sentence quotes
4. **Card Creation**: Format using standard evidence card structure
5. **Quality Review**: Apply approval criteria for quote quality and source reliability
6. **PDF Generation**: Create printable version using markdown_to_pdf tool

## Usage Guidelines

### For Debate Competition
- **PDF Files**: Use printed PDFs for debate rounds and evidence exchange
- **Verbal Citations**: All evidence should include complete verbal citations for rounds
- **Strategic Use**: Cards should support comprehensive argument construction
- **Citation Accuracy**: All bibliographic information should be complete and verifiable

### For Research and Development
- **Markdown Files**: Use as source for further research and verification
- **Source Links**: Include URLs for accessing original documents
- **Quality Assurance**: Apply consistent standards to all new evidence cards
- **Methodology**: Follow evidence card research workflow for new research

## Research Best Practices

### Source Verification
- Always trace quotes back to original primary sources
- Use exa crawling with livecrawl: "preferred" for fresh content
- Cross-reference author credentials and institutional authority
- Verify publication dates and continuing relevance

### Quality Control
- Apply multiple-choice approval criteria:
  - A) Excellent: Rich, complete sentences with detailed explanations
  - B) Good: Has some context but could be improved
  - C) Poor: Short, choppy quotes that need significant revision
  - D) Acceptable: Meets minimum standards for debate evidence
- Iterate based on feedback until quality standards are met
- Maintain both markdown and PDF versions for flexibility

## Technical Notes

### Tool Usage
- **Research Tools**: Prioritize Perplexity Ask over search tools for efficiency
- **Content Extraction**: Use exa crawling as primary method for source verification
- **PDF Generation**: Use markdown_to_pdf for consistent, automated conversion
- **File Operations**: Use PowerShell for complex operations when bash fails

### Platform Considerations
- **Windows Compatibility**: Use cmd /c npx wrapper for MCP configurations
- **Path Handling**: Handle spaces in file names carefully
- **Printer Access**: Use list_printers and print_file only when physical printing is requested

This folder should serve as a comprehensive resource for high-quality debate evidence research, with all cards meeting rigorous academic and competitive debate standards.