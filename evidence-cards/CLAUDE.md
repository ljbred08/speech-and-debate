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

### Source Documentation (-source.md files)

- **Purpose**: Complete source content markdown files for verification and research
- **Requirement**: Each evidence card (.md file) must have a corresponding -source.md file
- **Creation**: Use percollate, Chrome PDF + Parse, or direct PDF download + Parse methods
- **Content**: Full original source content with consistent formatting including:
  - Title, author, publication date
  - Source URL for verification
  - Complete text of original article/document
- **Location**: Same folder as corresponding evidence card (e.g., `01-card-source.md`)

### Printable Versions (.pdf files)

- **Purpose**: Formatted PDF versions ready for debate competition use
- **Generation**: Should be created using `mcp__Printer__markdown_to_pdf` for consistent formatting
- **Usage**: Intended for printing and evidence exchange in debate rounds
- **Naming**: Should use clear, descriptive naming (e.g., "01-topic-source.pdf")
- **Content**: Should be identical to the corresponding .md files; if not, notify the user and help figure out how to merge the differences and which version is accurate.

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

## File Organization

- **Naming Convention**: Use systematic numbering (01-, 02-, etc.) for easy organization
- **Consistent Structure**: All files follow the standard evidence card template
- **Paired Files**: Each markdown file has a corresponding PDF version
- **Version Control**: Changes should be committed to preserve research progress
- **Archive Management**: Orphaned markdown files (without corresponding PDFs) should be moved to archive subfolder
- **PDF Naming**: PDF files must use underscores instead of spaces for Parse tool compatibility (e.g., `Ban_Stock_Trading_1.pdf`)

## Usage Guidelines

### For Debate Competition

- **PDF Files**: Use printed PDFs for debate rounds and evidence exchange
- **Verbal Citations**: All evidence includes complete verbal citations for rounds
- **Strategic Use**: Cards support comprehensive argument construction
- **Citation Accuracy**: All bibliographic information is complete and verifiable

### For Research and Verification

- **Markdown Files**: Use as source for further research; however DO NOT treat the md files as infallible as they are still very likely to have mistakes. For definitive fact-checking, always use the original sources linked.
- **Source Links**: Include URLs for accessing original documents
- **Content Sync**: PDF files should be identical to corresponding .md files (format differences only: PDFs use headers, markdown uses table format)

## File Management Workflow

### PDF Processing and Organization

When working with new PDF documents or verifying existing collections:

1. **Parse PDFs**: Use `parse` tool to convert PDFs to markdown for analysis
2. **Verify Mappings**: Compare parsed content with existing markdown files to identify correct matches
3. **Archive Orphans**: Move any markdown files without corresponding PDFs to archive subfolder
4. **Create Missing Files**: For PDFs without corresponding markdown files, create new markdown files using table schema
5. **Content Verification**: Ensure PDF and markdown content matches exactly (format differences only)

### Schema Standards

All evidence card markdown files must use structured table format with these columns:

- **Tag Line**: Concise summary of main argument
- **Verbal Citation**: Complete quotes with source attribution for debate rounds
- **What the evidence says in context**: Full explanation of source arguments
- **Impact**: Analysis connecting evidence to debate positions
- **Bibliographic Information**: Complete citation details (title, URL, author, dates)

## Creating New Evidence Cards

##### To create new evidence cards, use the **Evidence Card Research skill.**

The skill provides:

- Complete research workflow and tool guidance
- Quality standards and approval criteria
- Step-by-step instructions for card creation
- Troubleshooting and best practices

See the skill documentation for comprehensive guidance on evidence card research methodology.

This folder should serve as a comprehensive resource for high-quality debate evidence research, with all cards meeting rigorous academic and competitive debate standards.

##### To fact-check anything, use the fact-check skill.