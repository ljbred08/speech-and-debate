---
name: fact-checking
description: Fact-check evidence. Verify accuracy of all info in evidence that has already been found.
allowed-tools: mcp__perplexity__perplexity_ask, mcp__exa__web_search_exa, mcp__exa__crawling_exa, Read, TodoWrite
---

# Fact Checking Workflow

#### Tool Usage Hierarchy

Use tools in this order for efficiency:

1. **mcp__exa__crawling_exa** - Extract full content from specific URLs; primary fact-checking tool as we can get verbatim content of linked website.
2. **mcp__perplexity__perplexity_ask** - PRIMARY research tool (most efficient)
3. **mcp__exa__web_search_exa** - Controlled searches with livecrawl: "preferred", used to find up-to-date raw web page info and links. Only use after first trying Perplexity because Perplexity normally gives better results.
4. **AVOID mcp__perplexity__perplexity_search** - Extremely high token cost

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

There should be ONE and ONE ONLY source (webpage link) per card.

## Quote Quality Standards

### Requirements

- Quotes must be complete sentences that flow naturally when read aloud
- Each quote should stand alone as a coherent statement
- Avoid "teeny tiny, disconnected, choppy random quotes"
- Include context and explanation in verbal citations
- Quotes must be word-for-word accurate

### Good Example Format

- 'Jim Harper, director of information policy studies at the Cato Institute, in his March 16, 2008 blog post "Sunlight Is the Best Disinfectant" on techliberation.com, argues that H.R. 2341, the Stop Trading on Congressional Knowledge Act, would be problematic because "enforcement would either be ineffective, lead to endless investigations, or cause employees to withdraw from investing as a precaution," warning that such a ban would "cause endless (perhaps politically motivated) investigations of our representatives and their staffs" and "force many or most congressional employees to withdraw from investing as a prophylactic," which would deprive "congressional staff of normal sources of income and of participation in investment that keeps their experience and thinking in line with other Americans."'

- "Failing to increase the debt limit would have catastrophic economic consequences. It would cause the government to default on its legal obligations – an unprecedented event in American history. That would precipitate another financial crisis and threaten the jobs and savings of everyday Americans – putting the United States right back in a deep economic hole, just as the country is recovering from the recent recession." - U.S. Department of the Treasury, "Debt Limit", 2025

### Bad Examples

- "Rather than broaden the ban, Congress should repeal it entirely" (too short)
- "no charges ever brought" (fragmented)
- Multiple short quotes without context

## Workflow

1. List all .md evidence card files available for checking. Make a todo list of all the files you need to cover.

2. Start checking process:
   
   1. Use crawl tool to fetch content from linked URL in document
   
   2. Verify citations against website content
   
   3. If citations do not match WORD-FOR-WORD:
      
      1. STOP and notify the user; suggest replacement accurate quotes from the website that meet quality criteria. (make use of questions tool.) Make sure to provide the user with the weblink so that they can view the website. (When I say suggest replacement quotes, research (fetch article) and suggest them BEFORE asking the question. Example question answers: 1. a quote 2. a quote 3. a quote 4. a quote 5. all quotes 6. only some (specify which) 7. find new source entirely)
      
      2. After you have worked out the disrepancy with the user, mark that file complete and start process for next file.
   
   4. If citations do match WORD-FOR-WORD:
      
      1. Quickly pass the citation by the user to make sure quality is good (use questions tool). If they say it's bad, suggest replacement accurate quotes from the website that meet quality criteria.
      
      2. If they say it's good, check it off and move on to next file.

3. After you have done the process for all the files, report to user; for any files that were changed, regenerate the PDF versions with markdown_to_pdf.

## Source File Usage During Fact-Checking

### Using Existing Source Documentation

When fact-checking evidence cards, first check if corresponding source markdown files already exist:

```bash
# Look for existing source files
find evidence-cards/ -name "*-source.md"
```

**If source file exists (e.g., `01-topic-source.md`):**
- Use Read tool to access the source content directly
- Verify quotes against the existing source markdown file
- No need to create new source documentation

**If source file doesn't exist:**
- Create source documentation using percollate or Chrome PDF + Parse methods
- Use the source URL from the evidence card to generate the source file
- Follow the source creation workflow in the evidence-card-research skill

### Source File Verification

When using existing source files:
1. Verify the source file contains the complete original content
2. Check that the source URL matches the evidence card citation
3. Ensure content is complete and not truncated
4. Use the source file for all quote verification instead of web crawling

PLEASE OBEY the instructions about user interaction. Do not just blaze on through the entire thing and only interact with the user after you're done.
