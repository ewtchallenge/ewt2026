# EWT2026 Project Context for LLMs

**Purpose:** This document provides comprehensive context about the EWT2026 (Engineering With Temi 2026) project for Large Language Models to understand the project structure, goals, processes, and guidelines.

**Last Updated:** January 2026

---

## Project Overview

### What is EWT2026?

EWT2026 is a free, open-source, year-long global coding challenge designed to help junior and mid-level developers build real-world project experience through:

- **Monthly Projects:** 12 guided projects (January - December 2026), one per month
- **Expert Code Reviews:** Human reviewers provide constructive feedback on submissions
- **AI-Assisted Reviews:** AI agents provide initial feedback on draft submissions
- **Community Collaboration:** Participants help each other through GitHub Discussions

### Core Philosophy

1. **Learning through doing:** Build real projects, not tutorials
2. **Mentorship through code review:** Expert feedback accelerates growth
3. **Community-driven:** Collaborative, supportive environment
4. **Free and open:** No costs, all code is open source
5. **Human in the loop:** AI assists, but human reviewers provide final feedback

### Key Stakeholders

1. **Participants:** Developers building the monthly projects
2. **Reviewers:** Experienced engineers (2+ years) volunteering to review code
3. **Maintainers:** @engineeringwithtemi (Temiloluwa Ojo) and approved collaborators
4. **Community:** Everyone helping in Discussions, sharing resources, supporting others

---

## Repository Structure

```
ewt2026/
├── .github/
│   ├── CODEOWNERS                    # Auto-assigns reviewers by file/language
│   ├── ISSUE_TEMPLATE/
│   │   ├── reviewer-application.yml  # Reviewer volunteer form
│   │   ├── project-question.yml      # Project clarification questions
│   │   ├── bug-report.yml           # Bug reports
│   │   ├── feature-request.yml      # Feature suggestions
│   │   ├── general-question.yml     # General questions
│   │   └── config.yml               # Issue template configuration
│   ├── PULL_REQUEST_TEMPLATE/
│   │   └── submission.md            # PR template for submissions
│   └── workflows/
│       └── validate-submission.yml  # Validates PR structure (optional)
├── docs/
│   ├── how-to-participate.md        # Complete participation guide
│   ├── faq.md                       # Frequently asked questions
│   └── llm.md                       # This file
├── january-2026/
│   ├── README.md                    # January project requirements
│   ├── RESOURCES.md                 # Helpful links and tutorials
│   └── submissions/
│       ├── .gitkeep
│       ├── participant1-username/   # Each participant's folder
│       │   ├── README.md
│       │   ├── src/
│       │   └── ...
│       └── participant2-username/
├── february-2026/
│   └── (same structure as january-2026)
├── march-2026/
├── ... (through december-2026)
├── README.md                        # Main project overview
├── CODE_OF_CONDUCT.md              # Community standards
├── CONTRIBUTING.md                  # Contribution guidelines
└── REVIEW_GUIDELINES.md            # Comprehensive reviewer guide
```

### Critical Folder Structure Rule

**Participants MUST place their code in:**

```
/[month]-2026/submissions/[their-exact-github-username]/
```

**Why:** This prevents merge conflicts. Since each participant has a unique GitHub username, they can't modify the same files, ensuring zero conflicts.

**Example:**

- User `johndoe` submits to: `/january-2026/submissions/johndoe/`
- User `janedoe` submits to: `/january-2026/submissions/janedoe/`
- No conflicts possible!

**Validation:**

- GitHub Actions can validate this structure
- PRs modifying files outside this pattern should be flagged

---

## Monthly Project Cycle

### Timeline (Each Month)

```
Week 1:
├── Day 1: Project brief published in /[month]-2026/README.md
├── Day 1-7: Announcement video released
├── Day 1-7: Participants ask clarification questions
└── Day 1-7: Participants begin development

Weeks 1-4:
├── Participants develop solutions
├── DRAFT PRs submitted anytime (AI + optional human review)
├── Participants iterate based on feedback
└── Community discusses approaches in monthly Discussion category

End of Week 4:
└── FINAL submission deadline

Week 5+:
├── Human reviewers provide comprehensive feedback
├── Participants respond to reviews
└── Next month's project begins (cycle repeats)
```

### Monthly Folder Contents

Each month folder (e.g., `/january-2026/`) contains:

1. **README.md** - Project requirements including:

   - Problem description
   - Technical requirements
   - Constraints and rules
   - Success criteria
   - Suggested tech stacks (optional)
   - Example use cases

2. **RESOURCES.md** - Helpful materials:

   - Documentation links
   - Tutorial recommendations
   - Relevant articles
   - Example projects (non-spoiler)

3. **submissions/** - Participant code:
   - One subfolder per participant
   - Named exactly as participant's GitHub username

---

## Submission Process

### Participant Workflow

1. **Fork** the `engineeringwithtemi/ewt2026` repository
2. **Clone** their fork locally
3. **Create branch** (e.g., `january-submission`)
4. **Create folder:** `/january-2026/submissions/their-username/`
5. **Develop solution** with required README.md
6. **Commit and push** to their fork
7. **Create PR** to original repo's `main` branch
8. **Fill PR template** completely
9. **Submit** as [DRAFT] or [FINAL]

### Submission Types

**[DRAFT] Submission:**

- Purpose: Early feedback, direction validation
- Review: AI-first, optional human review
- Timeline: Anytime during the month
- Updates: Freely allowed
- Priority: Lower priority for human review

**[FINAL] Submission:**

- Purpose: Comprehensive human review
- Review: Human reviewers prioritized
- Timeline: Before end-of-month deadline
- Updates: Allowed but may not be re-reviewed
- Priority: High priority for human review

**Converting DRAFT to FINAL:**

- Change PR title: Remove `[DRAFT]` or add `[FINAL]`
- Comment: "Ready for final review!"

### Required Submission Contents

**Every submission MUST include:**

1. **README.md** with:

   - Project overview
   - Tech stack used
   - How to run the code
   - Design approach and decisions
   - Challenges faced and solutions
   - What was learned
   - Questions for reviewers (optional)

2. **Source code** in any structure they prefer

3. **Dependency files** (package.json, requirements.txt, Cargo.toml, etc.)

**Optional but encouraged:**

- Tests
- Additional documentation
- Setup scripts
- Docker configuration

---

## Review Process

### Reviewer Assignment

**Automatic (via CODEOWNERS):**

```plaintext
# CODEOWNERS example
/january-2026/** @maintainer @january-lead-reviewer
/january-2026/**/*.rs @rust-reviewer1 @rust-reviewer2
/january-2026/**/*.js @javascript-reviewer1
/january-2026/**/*.py @python-reviewer1 @python-reviewer2
```

When a PR is created:

1. GitHub automatically requests review from matching CODEOWNERS
2. Reviewers get notified
3. Reviewers can self-assign from open PRs

**Manual:**

- Reviewers browse open PRs
- Filter by language/expertise
- Prioritize FINAL submissions without human review

### Review Prioritization

**Priority order:**

1. FINAL submissions without any human review
2. FINAL submissions in reviewer's expertise area
3. Older submissions (submitted earlier)
4. DRAFT submissions (if time permits)

### Review Quality Standards

Reviews must include:

1. **Positives (ALWAYS start with this):**

   - What the participant did well
   - Specific code/decisions to celebrate
   - Recognition of effort

2. **Core Feedback:**

   - Code quality and organization
   - Adherence to requirements
   - Best practices
   - Security issues
   - Error handling

3. **Categorized Issues:**

   - 🎯 **Critical:** Security, major bugs, missing requirements
   - ⚠️ **Important:** Best practices, maintainability
   - 💡 **Suggestions:** Improvements, optimizations
   - 📚 **Learning:** Concepts to explore further

4. **Resources (REQUIRED):**

   - Link to documentation when mentioning concepts
   - Share articles, tutorials, examples
   - Provide learning paths

5. **Questions:**

   - Ask about design decisions
   - Promote thinking: "Have you considered...?"
   - Request clarification when needed

6. **Encouragement:**
   - End with positive, encouraging note
   - Acknowledge progress and effort

### Review Anti-Patterns (AVOID)

❌ **Don't:**

- Give complete solutions (guide instead)
- Only list negatives (always start with positives)
- Be vague ("this could be better")
- Use condescending language ("obviously", "clearly")
- Overwhelm with 50+ comments
- Assume knowledge without explanation
- Review outside your expertise without caveats

✅ **Do:**

- Guide exploration with questions
- Provide specific, actionable feedback
- Include links to resources
- Explain why suggestions matter
- Focus on 3-5 key improvements
- Be kind and encouraging
- Frame as opportunities, not failures

---

## Code of Conduct Principles

**Core Values:**

1. **Respect:** Treat everyone with dignity and kindness
2. **Inclusivity:** Welcome people of all backgrounds and skill levels
3. **Constructive:** Focus on helping people grow, not tearing down
4. **Collaboration:** Support each other's learning
5. **Safety:** Zero tolerance for harassment, discrimination, abuse

**Specific Rules:**

- ✅ Be respectful and professional
- ✅ Give constructive, helpful feedback
- ✅ Encourage and celebrate others
- ✅ Help others learn through guidance, not answers
- ❌ No harassment, discrimination, or hate speech
- ❌ No spam or excessive self-promotion
- ❌ No plagiarism or copying others' work
- ❌ No sharing complete solutions during active month

**Enforcement:**

- Violations reported to @engineeringwithtemi
- Action taken based on severity
- Range: warning → temporary ban → permanent ban

---

## Technology and Language Guidelines

### Allowed Technologies

**Participants can use ANY:**

- Programming languages
- Frameworks and libraries
- Tools and platforms
- Databases
- APIs
- Cloud services
- AI assistants (ChatGPT, Copilot, Claude, etc.)

**With requirements:**

- Must document in README
- Must provide setup instructions
- Must be runnable by reviewers (or provide demos/screenshots)
- Must handle secrets properly (environment variables, not hardcoded)

### Common Tech Stacks

**Backend:**

- Python: Django, Flask, FastAPI
- JavaScript/TypeScript: Node.js, Express, Nest.js
- Rust: Actix, Rocket, Axum
- Go: Gin, Echo, Chi
- Java: Spring Boot
- C#: .NET

**Frontend:**

- React, Vue, Angular, Svelte
- Next.js, Nuxt.js, SvelteKit
- Vanilla JavaScript/HTML/CSS

**Full-stack:**

- MERN/MEAN stack
- Django + React
- Rails
- Laravel

**Other:**

- CLI tools (Rust, Go, Python)
- Mobile (React Native, Flutter, Swift, Kotlin)
- Desktop (Electron, Tauri)
- Data science (Python, R, Julia)

### Security Requirements

**CRITICAL - Participants MUST:**

- ❌ Never commit API keys, passwords, secrets
- ✅ Use environment variables for secrets
- ✅ Include `.gitignore` for sensitive files
- ✅ Provide `.env.example` with dummy values
- ❌ No SQL injection vulnerabilities
- ❌ No XSS vulnerabilities in web apps
- ✅ Validate and sanitize user input

**Reviewers MUST flag security issues as 🎯 Critical**

---

## GitHub Features Used

### Issues

**Issue Templates (`.github/ISSUE_TEMPLATE/`):**

1. **reviewer-application.yml** - Reviewer volunteer applications
2. **project-question.yml** - Questions about project requirements
3. **bug-report.yml** - Report bugs in infrastructure/process
4. **feature-request.yml** - Suggest improvements
5. **general-question.yml** - Other questions

**Usage:**

- Official clarifications and tracking
- Reviewer onboarding
- Bug/feature tracking
- Not for general discussion (use Discussions instead)

### Pull Requests

**PR Template (`.github/PULL_REQUEST_TEMPLATE/submission.md`):**

Required fields:

- Submission type: [DRAFT] or [FINAL]
- Month/project
- GitHub username (must match folder)
- Tech stack
- Solution overview
- Challenges faced
- Questions for reviewers
- Checklist confirmation

**PR Workflow:**

1. Participant creates PR from their fork
2. GitHub Actions validate structure (optional)
3. CODEOWNERS auto-assigns reviewers
4. Review process begins
5. Participant responds to feedback
6. PR is merged (not closed) after review complete

**Why merge instead of close:**

- Preserves all submissions in main branch
- Creates browsable archive of solutions
- Allows participants to reference others (after deadline)
- Maintains clean history

### Discussions

**Categories:**

- 📢 **Announcements** - Monthly projects, updates (maintainers only)
- 💬 **General** - Community chat, introductions
- ❓ **Q&A** - Technical questions, help
- 🗓️ **[Month] 2026** - Monthly project discussions (12 categories)
- 💡 **Ideas & Suggestions** - Improvement ideas
- 🎨 **Show & Tell** - Share completed solutions (post-deadline)
- 🤝 **Collaboration** - Find partners, study groups
- 🎓 **Resources & Learning** - Share helpful resources
- 🏆 **Wins & Milestones** - Celebrate achievements
- 🐛 **Debugging Help** - Get unstuck

**Usage Guidelines:**

- Use for community interaction and support
- Not for tracking (use Issues for that)
- Encourage participation and collaboration
- Async, conversational format

### GitHub Actions (Optional)

**Validation workflow (`.github/workflows/validate-submission.yml`):**

Checks:

- ✅ PR only modifies files in `/[month]-2026/submissions/[pr-author-username]/`
- ✅ README.md exists in submission folder
- ❌ Fails if files modified outside allowed folder
- ❌ Fails if README.md missing

**Benefits:**

- Prevents accidental mistakes
- Catches structural issues early
- Maintains repository integrity

---

## Common Scenarios and Responses

### Scenario 1: Participant asks "Can I use Python instead of JavaScript?"

**Response:**
"Yes! You can use any programming language or technology you prefer. The project requirements specify _what_ to build, not _how_ to build it. Python is perfectly fine. Just make sure to document your approach in your README and include setup instructions."

### Scenario 2: Participant's code has hardcoded API key

**Review Feedback:**
"🎯 **Critical - Security Issue:** I noticed your API key is hardcoded on line 23. This is a security risk if this code is shared or accidentally made public.

**How to fix:**

```python
# Instead of:
API_KEY = "sk-1234567890"

# Use environment variables:
import os
API_KEY = os.getenv("API_KEY")
```

**Resources:**

- [Python Environment Variables Guide](link)
- [python-dotenv Documentation](link)

Please update this before your final submission."

### Scenario 3: Participant asks if they can use ChatGPT

**Response:**
"Yes, you can use ChatGPT, GitHub Copilot, Claude, or any AI assistants! They're great learning tools. However:

1. Make sure you **understand** the code you submit
2. Be able to **explain** your design decisions
3. **Learn from** the AI rather than just copying

Your README should explain **your** approach and thinking. Reviewers may ask questions to ensure you understand your submission."

### Scenario 4: Participant asks "What if I don't finish?"

**Response:**
"Submit what you have! Even incomplete submissions are valuable:

- You'll get feedback on what you built
- It shows your thinking process
- You'll learn from the review
- It's better than not submitting

Late submissions are still accepted (though not prioritized for review). The goal is learning, not perfection!"

### Scenario 5: Reviewer asks "Should I reject this PR?"

**Guidance:**
"Don't use 'Request changes' or 'Reject' harshly. Remember:

- These are learning submissions, not production code
- Focus on education, not gatekeeping
- Use 'Comment' for most reviews
- Use 'Request changes' only for critical security issues or completely missing requirements
- Use 'Approve' when it's solid work, even if there are suggestions

Frame everything as learning opportunities, not failures."

### Scenario 6: Participant submitted to wrong folder

**Response (in PR):**
"Thanks for your submission! I noticed your code is in `/january-2026/[wrong-folder]/` instead of `/january-2026/submissions/your-username/`.

This is important because our system prevents merge conflicts by requiring each participant to use their own folder.

**To fix:**

1. Close this PR
2. Move your code locally to `/january-2026/submissions/your-username/`
3. Commit the changes
4. Create a new PR

Let me know if you need help with this!"

### Scenario 7: Someone asks "Is there a certificate?"

**Response:**
"There's currently no certificate, but you gain something more valuable:

- **Portfolio:** 12 reviewed projects to showcase
- **GitHub history:** Public evidence of your work
- **Real feedback:** Expert code reviews you can learn from
- **Interview material:** Projects and learnings to discuss
- **Community:** Network of developers and reviewers

These are more valuable to employers than a certificate!"

---

## Best Practices for LLMs Assisting Users

### When Helping Participants

**Do:**

1. ✅ **Guide, don't solve:** Ask questions that promote thinking
2. ✅ **Explain concepts:** Help them understand, not just copy code
3. ✅ **Suggest resources:** Point to documentation and tutorials
4. ✅ **Encourage best practices:** Security, testing, clean code
5. ✅ **Remind about README:** Their README must explain their approach
6. ✅ **Check folder structure:** Ensure they're in correct folder
7. ✅ **Promote understanding:** "Can you explain why this works?"

**Don't:**

1. ❌ **Give complete solutions:** They need to build it themselves
2. ❌ **Write their README:** It should reflect their thinking
3. ❌ **Ignore security:** Always highlight security issues
4. ❌ **Skip explanations:** Always explain _why_, not just _what_
5. ❌ **Encourage shortcuts:** Learning matters more than completion

**Example Good Assistance:**
User: "How do I parse JSON in Python?"
LLM: "Python has a built-in json module that's perfect for this!
Here's the basic pattern:

import json

# From a string

data = json.loads(json_string)

# From a file

with open('data.json') as f:
data = json.load(f)

```

For your project, you'll want to:
1. Import the json module
2. Read your data source
3. Handle potential errors (the JSON might be invalid)

Have you considered what happens if the JSON is malformed? You might want to wrap it in a try-except block.

The official docs are really helpful: https://docs.python.org/3/library/json.html

Try implementing it and let me know if you run into specific errors!"
```

### When Helping Reviewers

**Do:**

1. ✅ **Support constructive feedback:** Help frame criticism positively
2. ✅ **Suggest resources to share:** Find good documentation links
3. ✅ **Identify patterns:** Help spot common issues or good practices
4. ✅ **Draft review structure:** Offer template following guidelines
5. ✅ **Balance:** Remind to include positives AND improvements
6. ✅ **Check tone:** Ensure feedback is kind and encouraging

**Example:**

```
Reviewer: "This code is messy and has bad naming. How do I say this?"

LLM: "Let's frame this constructively! Here's a suggested approach:

**What They Did Well:**
'Your logic for [specific feature] is solid! The algorithm works correctly.'

**Suggestion on Code Organization:**
'The code would be more maintainable with some refactoring. For example, breaking the 80-line function into smaller, focused functions would make it easier to understand and test.

Here's a pattern you might find helpful: [link to Single Responsibility Principle]'

**Naming:**
'Using more descriptive variable names would make the code self-documenting. For instance:
- Instead of `data`, consider `user_records` or `api_response`
- Instead of `process()`, maybe `validate_and_save_user()`

This makes the code readable without needing as many comments.'

Notice how this:
1. Starts positive
2. Explains WHY it matters
3. Gives specific examples
4. Provides resources
5. Stays encouraging"
```

### When Answering Process Questions

**Always:**

1. ✅ **Check the docs:** Reference specific documentation
2. ✅ **Provide links:** Point to relevant guides
3. ✅ **Be accurate:** Don't make up processes
4. ✅ **Explain rationale:** Help them understand the "why"
5. ✅ **Encourage community:** Suggest Discussions for some questions

**Example:**

```
User: "When's the deadline for January?"

LLM: "The January 2026 project deadline is January 31, 2026 (end of Week 4).

However, don't worry too much about the deadline:
- You can submit late (it's just not prioritized for review)
- It's better to submit something incomplete than nothing
- The goal is learning, not racing to finish

The complete timeline for each month is:
- Week 1: Project announced
- Weeks 1-4: Development
- End Week 4: Deadline
- Week 5+: Reviews

See the [FAQ](docs/faq.md#timeline--deadlines) for more details!"
```

---

## Project Evolution and Maintenance

### Monthly Project Creation

**Each month, maintainers create:**

1. New folder: `/[month]-2026/`
2. Project README with requirements
3. RESOURCES.md with helpful links
4. Announcement video
5. GitHub Discussion in monthly category
6. Update CODEOWNERS for month-specific reviewers (optional)

### Review Cycles

**Expected timeline:**

- Projects run concurrently (January review happens during February development)
- Reviewers aim for 5-10 day turnaround after deadline
- Some reviews may be faster/slower based on volume

### Continuous Improvement

**Project welcomes:**

- Documentation improvements
- Process suggestions
- Tooling enhancements
- Community ideas

**Via:**

- Feature request Issues
- Ideas & Suggestions Discussions
- PRs to documentation
- Feedback from participants and reviewers

---

## Key Success Metrics

### For Participants

**Success means:**

- ✅ Built a working project (even if imperfect)
- ✅ Learned new concepts or technologies
- ✅ Received and understood code review feedback
- ✅ Can explain their design decisions
- ✅ Improved from previous months
- ✅ Engaged with the community

**NOT measured by:**

- ❌ Perfect code on first try
- ❌ Completing all 12 months
- ❌ Using most advanced tech
- ❌ Getting "approved" reviews
- ❌ Comparison with others

### For Reviewers

**Success means:**

- ✅ Provided constructive, helpful feedback
- ✅ Participant understands suggestions
- ✅ Encouraged continued learning
- ✅ Balanced positives with improvements
- ✅ Included useful resources
- ✅ Maintained kind, professional tone

**NOT measured by:**

- ❌ Number of comments left
- ❌ Finding every possible issue
- ❌ Getting participant to implement all suggestions
- ❌ Speed of review
- ❌ Strictness or perfectionism

### For the Project

**Success means:**

- ✅ Active participation each month
- ✅ Positive community culture
- ✅ Participants report learning and growth
- ✅ Reviewers feel appreciated and supported
- ✅ Diverse submissions (languages, approaches)
- ✅ Sustainable volunteer reviewer pool
- ✅ Clear, helpful documentation

---

## Common Edge Cases

### What if someone submits the same solution twice?

**Context:** Participant might submit to multiple months with same/similar code

**Response:**

- Allow it if they're applying the solution to different project requirements
- Discourage if it's just resubmitting identical code for no reason
- Focus on learning—did they learn from the first review?

### What if a participant's code doesn't run?

**Review approach:**

- Note it in review: "I wasn't able to run this locally because..."
- Review the code itself for logic, structure, practices
- Ask participant for clarification: "Can you provide updated setup instructions?"
- Still provide value: feedback on readable code, approach, etc.

### What if someone plagiarizes?

**If reviewer suspects plagiarism:**

1. Check if it's properly attributed (is the source cited?)
2. If no attribution and clearly copied: report to maintainers
3. Don't accuse publicly in review
4. Let maintainers handle investigation and action

**Maintainer action:**

- Investigate claim
- Ask participant to explain code
- If confirmed plagiarism: close PR, warning, potential ban
- Document incident

### What if a participant is rude to a reviewer?

**Reviewer should:**

- Not engage in argument
- Stay professional
- Report to maintainers (mention @engineeringwithtemi)

**Maintainer action:**

- Review the exchange
- Reach out to participant privately
- Warning or action based on severity
- Support the reviewer

### What if there are too many submissions to review?

**Options:**

1. **Request more reviewers:** Post in community asking for volunteers
2. **Prioritize:** Focus on FINAL submissions, older submissions first
3. **Communicate:** Set expectations about review timeline
4. **AI assistance:** Use AI for DRAFT reviews to lighten load
5. **Accept delays:** Better late quality reviews than rushed bad ones

### What if project requirements are ambiguous?

**Participant should:**

- Create Issue with "Project Question" template
- Ask specific clarification questions
- Wait for maintainer response

**Maintainer should:**

- Respond publicly in Issue (so all see answer)
- Update project README if needed
- Consider announcement if it affects many participants

---

## Technical Implementation Notes

### CODEOWNERS Strategy

**By month:**

```plaintext
/january-2026/** @maintainer @january-lead
```

**By language:**

```plaintext
/january-2026/**/*.rs @rust-expert1 @rust-expert2
/january-2026/**/*.py @python-expert1 @python-expert2
```

**By both:**

```plaintext
/january-2026/** @maintainer
/january-2026/**/*.js @js-expert1
/february-2026/** @maintainer
/february-2026/**/*.py @python-expert1
```

**Considerations:**

- More specific patterns override general ones
- Last matching pattern wins (be careful with order)
- All listed reviewers get requested
- Can use GitHub teams: `@org/team-name` (requires Organization)

### GitHub Actions for Validation

**Example validation (optional):**

```yaml
# Validates PR structure
name: Validate Submission

on:
  pull_request:
    types: [opened, synchronize]

jobs:
  validate:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
        with:
          fetch-depth: 0

      - name: Validate folder structure
        run: |
          PR_AUTHOR="${{ github.event.pull_request.user.login }}"
          CHANGED_FILES=$(git diff --name-only origin/main...HEAD)

          # Check files are in correct folder
          for file in $CHANGED_FILES; do
            if [[ ! "$file" =~ ^[a-z]+-2026/submissions/${PR_AUTHOR}/ ]]; then
              echo "Error: $file is outside allowed folder"
              exit 1
            fi
          done

      - name: Check for README
        run: |
          PR_AUTHOR="${{ github.event.pull_request.user.login }}"
          MONTH_FOLDER=$(git diff --name-only origin/main...HEAD | grep -o '^[a-z]*-2026' | head -1)

          if [ ! -f "${MONTH_FOLDER}/submissions/${PR_AUTHOR}/README.md" ]; then
            echo "Error: Missing required README.md"
            exit 1
          fi
```

**Benefits:**

- Catches structural errors early
- Prevents merge conflicts
- Enforces README requirement
- Reduces maintainer burden

**Caution:**

- Don't over-validate (allow flexibility)
- Clear error messages
- Don't block learning (warnings OK)

### Merge Strategy

**After review:**

- PRs are **merged**, not closed
- This preserves submissions in main branch
- Creates browsable archive
- Allows post-deadline learning from others

**Merge settings:**

- Allow squash merges (cleaner history)
- Or allow regular merges (preserves commit history)
- Disable rebase merges (can lose context)

**Branch cleanup:**

- Participant's fork branches remain
- No need to clean up (their repo)

---

## LLM Usage in EWT2026

### AI-Assisted Reviews (DRAFT submissions)

**AI can:**

- Provide quick initial feedback on DRAFT submissions
- Identify common issues (security, bugs, structure)
- Suggest improvements and resources
- Free up human reviewers for FINAL submissions

**AI should:**

- Follow review guidelines (positives first, resources, encouragement)
- Mark feedback as AI-generated
- Be cautious about complex/nuanced issues
- Defer to human reviewers when uncertain

**AI limitations:**

- May miss context or intent
- Can't provide mentorship like humans
- May not understand all project requirements
- Shouldn't replace human review for FINAL submissions

### Participant Use of AI

**Encouraged:**

- Learning concepts with AI assistance
- Getting unstuck on specific issues
- Understanding error messages
- Exploring different approaches

**Guidelines:**

- Must understand generated code
- Should learn, not just copy
- README reflects their thinking, not AI's
- Be prepared to explain decisions

### This Document's Purpose

**For LLMs helping users:**

- Understand project structure and goals
- Provide accurate process guidance
- Support participants constructively
- Help reviewers write better feedback
- Answer questions based on actual documentation
- Direct users to appropriate resources

**For maintaining consistency:**

- Ensures LLMs give consistent advice
- Reduces confusion from contradictory information
- Provides single source of truth
- Helps onboard new LLM interactions

---

## Quick Reference

### Key URLs and Paths

```
Repository: https://github.com/engineeringwithtemi/ewt2026

Documentation:
- Main README: /README.md
- Participation Guide: /docs/how-to-participate.md
- FAQ: /docs/faq.md
- Review Guidelines: /REVIEW_GUIDELINES.md
- Code of Conduct: /CODE_OF_CONDUCT.md
- Contributing: /CONTRIBUTING.md

Issue Templates: /.github/ISSUE_TEMPLATE/
PR Template: /.github/PULL_REQUEST_TEMPLATE/submission.md
CODEOWNERS: /.github/CODEOWNERS

Monthly Projects: /[month]-2026/
Submissions: /[month]-2026/submissions/[username]/
```

### Key Contacts

```
Primary Maintainer: @engineeringwithtemi (Temiloluwa Ojo)
Community: GitHub Discussions, Discord/Skool (links in README)
Social: #EWT2026 hashtag
```

### Important Dates (2026)

```
January 1: January project launch
February 1: February project launch
... (1st of each month)
December 31: Final project deadline of the year
```

---

## Version History

**v1.0 (January 2026):**

- Initial version
- Documents project structure and processes
- Provides LLM context for assisting users

**Future updates:**

- Will reflect process changes
- Incorporate learnings from first months
- Add new scenarios as they emerge

---

## Contributing to This Document

**This document should be updated when:**

- Project structure changes
- New processes are added
- Common scenarios emerge
- Documentation evolves

**How to update:**

- Submit PR with changes
- Explain what changed and why
- Maintainers review and merge
- Keep version history updated

---

**End of LLM Context Document**

_This document provides comprehensive context for LLMs to understand and assist with EWT2026. For human-readable guides, see /docs/ folder._
