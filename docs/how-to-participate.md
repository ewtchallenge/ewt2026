# How to Participate in EWT2026

## Overview

EWT2026 is a year-long coding challenge where you build 12 real-world projects (one per month) and receive expert code reviews. This guide walks you through everything you need to participate successfully.

---

## Before You Start

### Prerequisites

- **GitHub account** (free)
- **Git installed** on your computer
- **Basic programming knowledge** in at least one language
- **Development environment** set up for your chosen language
- **Time commitment**: 10-20 hours per month (varies by project and experience level)

### Recommended Skills

- Basic Git/GitHub workflow (fork, clone, commit, push, PR)
- Ability to read technical documentation
- Willingness to learn and receive feedback
- Comfort with command line basics

**New to Git/GitHub?** Check out these resources:

- [GitHub's Git Handbook](https://guides.github.com/introduction/git-handbook/)
- [Git Tutorial for Beginners](https://www.youtube.com/watch?v=8JJ101D3knE)
- [GitHub's Hello World Guide](https://guides.github.com/activities/hello-world/)

---

## Step-by-Step Participation Guide

### Phase 1: Project Announcement (Week 1 of Each Month)

#### 1. Watch the Announcement Video

- Check the Announcements discussion category for the monthly project video
- Subscribe to the repository to get notifications
- Video includes project walkthrough, requirements clarification, and Q&A
- Take notes on requirements and constraints

#### 2. Read the Project Brief

- Navigate to the current month's folder (e.g., `/january-2026/`)
- Read `README.md` thoroughly - this contains:
  - Project description and goals
  - Technical requirements
  - Submission guidelines
  - Success criteria
  - Suggested resources

#### 3. Ask Clarifying Questions

- **For official requirement clarifications**: Open an [Issue using the Project Question template](/../../issues/new/choose)
- **For general discussion**: Use the monthly Discussion category (e.g., January 2026)
- **For community help**: Use the Q&A or General discussion categories
- **Check existing questions first** to avoid duplicates

---

### Phase 2: Development (Weeks 1-4)

#### 1. Fork the Repository

```bash
# On GitHub, click "Fork" button at top right of the repository
# This creates your personal copy
```

#### 2. Clone Your Fork

```bash
# Clone to your local machine
git clone https://github.com/YOUR-USERNAME/ewt2026.git
cd ewt2026
```

#### 3. Create Your Submission Folder

**CRITICAL:** Your folder MUST be named exactly after your GitHub username.

```bash
# Create your folder structure
mkdir -p january-2026/submissions/YOUR-GITHUB-USERNAME
cd january-2026/submissions/YOUR-GITHUB-USERNAME
```

**Example:**

```bash
# If your GitHub username is "johndoe"
mkdir -p january-2026/submissions/johndoe
cd january-2026/submissions/johndoe
```

#### 4. Set Up Your Project

Create the following structure in your folder:

```
january-2026/submissions/your-username/
├── README.md              # Required - explains your solution
├── src/                   # Your source code
│   └── (your code files)
├── tests/                 # Optional but encouraged
│   └── (test files)
├── docs/                  # Optional - additional documentation
├── .gitignore            # Recommended
└── (dependency files)     # package.json, Cargo.toml, requirements.txt, etc.
```

#### 5. Create Your README.md

Your submission **must** include a README.md. Here's a template:

````markdown
# [Project Name] - [Your Name]

## Overview

Brief description of what you built (2-3 sentences).

## Tech Stack

- **Language:** [e.g., Python 3.11, Rust 1.75, JavaScript ES6]
- **Frameworks/Libraries:** [e.g., React 18, Flask 3.0, Tokio]
- **Tools:** [e.g., Docker, PostgreSQL, Redis]

## Features

- Feature 1
- Feature 2
- Feature 3

## How to Run

### Prerequisites

- [List what's needed to run your project]
- [e.g., Node.js 18+, Python 3.11+, Docker]

### Installation

```bash
# Step-by-step installation commands
git clone [your-fork-url]
cd january-2026/submissions/your-username
npm install  # or pip install -r requirements.txt, cargo build, etc.
```

### Running the Application

```bash
# Commands to run your project
npm start
# or
python main.py
# or
cargo run
```

### Running Tests (if applicable)

```bash
npm test
# or
pytest
# or
cargo test
```

## My Approach

### Problem Understanding

How I understood the requirements and what I set out to build.

### Design Decisions

Key architectural or design choices I made and why:

- Decision 1: [Why I chose X over Y]
- Decision 2: [How I structured the code]
- Decision 3: [Trade-offs I considered]

### Implementation Details

Interesting aspects of the implementation:

- How I handled [specific challenge]
- Algorithm/pattern used for [specific feature]
- Performance considerations

## Challenges & Solutions

### Challenge 1: [Description]

**Problem:** What went wrong or was difficult
**Solution:** How I solved it
**Learning:** What I learned from this

### Challenge 2: [Description]

**Problem:** ...
**Solution:** ...
**Learning:** ...

## What I Learned

- Key takeaway 1
- Key takeaway 2
- Key takeaway 3
- New skills/concepts acquired

## Future Improvements

If I had more time or were to refactor, I would:

- Improvement 1
- Improvement 2
- Improvement 3

## Resources Used

- [Documentation/Tutorial 1](url)
- [Article/Blog 2](url)
- [Video/Course 3](url)

## Questions for Reviewers

Specific areas where I'd like feedback:

1. [Question/area 1]
2. [Question/area 2]
3. [Question/area 3]

---

**Project:** EWT2026 - January 2026
**Submission Date:** [Date]
**Time Spent:** [Approximate hours] (optional)
````

#### 6. Develop Your Solution

**Best Practices:**

- ✅ Commit regularly with clear commit messages
- ✅ Write clean, readable code
- ✅ Add comments for complex logic
- ✅ Handle errors appropriately
- ✅ Test your code (even if informal testing)
- ✅ Follow language/framework conventions
- ✅ Keep security in mind (no hardcoded secrets!)

**Git Workflow:**

```bash
# Create a branch for your work
git checkout -b january-submission

# Make changes, then commit
git add .
git commit -m "Add initial project structure"

# Continue working
git add .
git commit -m "Implement core feature X"

# Push to your fork regularly
git push origin january-submission
```

---

### Phase 3: Submission

#### Draft Submission (Optional but Recommended)

Submit early for AI review and optional human feedback:

1. **Ensure your code is committed and pushed to your fork**
2. **Go to the original repository** (not your fork)
3. **Click "Pull requests" → "New pull request"**
4. **Click "compare across forks"**
5. **Select:**
   - Base repository: `engineeringwithtemi/ewt2026`
   - Base branch: `main`
   - Head repository: `YOUR-USERNAME/ewt2026`
   - Compare branch: `january-submission` (or whatever you named it)
6. **Click the dropdown arrow next to "Create pull request"**
7. **Select "Create draft pull request"**
8. **Click "Draft pull request"**
9. **Title:** `January 2026 - Your Name` (No tags needed)
10. **Fill out the PR template completely**
11. **Submit**

**Draft Benefits:**

- Get AI feedback early
- Identify issues before final submission
- Optional human review if reviewers have time
- Can update freely

#### Final Submission

When you're ready for comprehensive human review:

**Option 1: Convert Draft to Final**

1. Go to your PR page
2. Click the "Ready for review" button (usually near the bottom or in the merge box)
3. Add a comment:
   ```markdown
   @engineeringwithtemi Ready for final review!
   ```

**Option 2: New Final Submission**

- Follow the same PR process but select "Create pull request" (not draft)
- Title: `January 2026 - Your Name`
- Fill out PR template

**Final Submission Checklist:**

- [ ] Code is complete and tested
- [ ] README.md is thorough and clear
- [ ] All project requirements met
- [ ] Code is clean and well-organized
- [ ] No sensitive information (API keys, passwords)
- [ ] All files in correct folder: `/month-2026/submissions/your-username/`
- [ ] PR template completely filled out
- [ ] PR is marked as "Ready for review" (not Draft)

---

### Phase 4: Review & Iteration

#### Receiving Your Review

Reviews typically arrive within:

- **Draft submissions:** 1-3 days (AI) or 3-7 days (human, if available)
- **Final submissions:** 5-10 days after month deadline

#### Understanding Your Review

Reviewers will provide feedback on:

- ✅ **Code quality** - Organization, readability, naming
- ✅ **Best practices** - Language conventions, patterns
- ✅ **Requirements** - Does it meet the project brief?
- ✅ **Learning opportunities** - Concepts to explore further
- ✅ **Security & errors** - Potential issues
- ✅ **What you did well** - Celebrate your wins!

Reviews are categorized:

- 🎯 **Critical** - Must address (security, functionality)
- ⚠️ **Important** - Should address (best practices)
- 💡 **Suggestion** - Nice to have (improvements)
- 📚 **Learning** - Explore further (optional)

#### Responding to Reviews

**Do:**

- ✅ Thank the reviewer for their time
- ✅ Ask clarifying questions if unclear
- ✅ Engage in constructive dialogue
- ✅ Share your reasoning for decisions
- ✅ Mark conversations as resolved when addressed

**Don't:**

- ❌ Take feedback personally
- ❌ Argue defensively
- ❌ Ignore critical feedback
- ❌ Demand more reviews

**Example Response:**

```markdown
Thanks @reviewer for the detailed feedback!

Regarding the error handling suggestion - that makes sense. I hadn't considered
the edge case you mentioned. I've updated the code to handle that scenario.

Quick question: You mentioned using the repository pattern. I'm not familiar
with it - could you point me to a good resource to learn more?

I'll address the critical security issue today and update the PR.
```

#### Making Updates (Optional)

You can update your PR after review:

```bash
# Make changes locally
git add .
git commit -m "Address reviewer feedback: improve error handling"
git push origin january-submission
```

**Note:** Updates after final review submission may not receive additional priority review.

---

## Important Rules & Guidelines

### Folder Structure Rule (CRITICAL)

**Your submission MUST be in:**

```
/[month]-2026/submissions/[your-exact-github-username]/
```

**You may ONLY modify files inside your own folder.**

❌ **Do NOT:**

- Modify other participants' folders
- Modify project requirements or READMEs outside your folder
- Modify any `.github/` files
- Create folders outside `submissions/your-username/`

✅ **Do:**

- Create any structure you want inside your personal folder
- Add as many files as needed in your folder
- Organize your code however makes sense

**Why?** This prevents merge conflicts and keeps everyone's work separate.

### Timeline & Deadlines

- **Week 1:** Project announced
- **Weeks 1-4:** Work on your solution
- **End of Week 4:** Deadline for final submissions
- **After deadline:** Late submissions accepted but not prioritized

**Example Timeline:**

- January 1: January project announced
- January 1-31: Development period
- January 31: Final submission deadline
- February 1: February project announced (cycle continues)

### What You Can Use

**Allowed:**

- ✅ Any programming language
- ✅ Any frameworks, libraries, tools
- ✅ AI assistants (ChatGPT, Copilot, Claude, etc.)
- ✅ Online resources, tutorials, documentation
- ✅ Asking for help in Discussions
- ✅ Collaboration with other participants

**Must Do:**

- ✅ Write your own README explaining your approach
- ✅ Understand the code you submit
- ✅ Credit significant help or code sources
- ✅ Follow the Code of Conduct

**Not Allowed:**

- ❌ Copying another participant's solution
- ❌ Submitting someone else's work as your own
- ❌ Plagiarizing without attribution

### Code of Conduct

All participants must follow our [Code of Conduct](../CODE_OF_CONDUCT.md):

- Be respectful and kind
- No harassment or discrimination
- Help others learn, don't just give answers
- Create an inclusive environment
- Report violations to maintainers

---

## Tips for Success

### Project Planning

1. **Read requirements carefully** - Don't skip details
2. **Break down the problem** - Create a task list
3. **Start simple** - Get basic version working first
4. **Iterate and improve** - Add features incrementally
5. **Test as you go** - Don't wait until the end

### Writing Good Code

1. **Make it work first** - Then make it better
2. **Use meaningful names** - Variables, functions, files
3. **Keep functions small** - One responsibility per function
4. **Comment complex logic** - But don't over-comment obvious code
5. **Handle errors** - Don't let your program crash silently
6. **Follow conventions** - Language/framework best practices

### Getting Great Reviews

1. **Write a thorough README** - Reviewers appreciate context
2. **Ask specific questions** - What do you want feedback on?
3. **Show your thinking** - Explain design decisions
4. **Be honest about challenges** - What did you struggle with?
5. **Submit on time** - Final submissions after deadline aren't prioritized

### Learning Effectively

1. **Don't just copy code** - Understand what it does and why
2. **Experiment** - Try different approaches
3. **Read others' code** - After deadline, see different solutions
4. **Take notes** - Document what you learn
5. **Apply feedback** - Use review insights in future projects

### Time Management

1. **Start early** - Don't wait until week 4
2. **Set milestones** - Week 1: planning, Week 2: core features, etc.
3. **Submit a draft** - Get early feedback
4. **Leave buffer time** - For unexpected issues
5. **It's okay to submit imperfect** - Learning matters more than perfection

---

## Getting Help

### Before Asking

1. **Search existing resources:**
   - Project README
   - [FAQ](faq.md)
   - GitHub Discussions
   - Existing Issues
2. **Try debugging yourself:**
   - Read error messages carefully
   - Use print/console.log debugging
   - Search the error message online
3. **Reduce to minimal example:**
   - Isolate the problem
   - Create smallest code that reproduces it

### Where to Ask

**For Project Questions:**

- Official clarifications: [Create a Project Question Issue](/../../issues/new/choose)
- General discussion: Monthly Discussion category
- Technical help: Q&A Discussion category

**For Coding Help:**

- Debugging Help Discussion category
- Q&A Discussion category
- Your monthly project Discussion category

**For Process Questions:**

- General Discussion category
- [FAQ](faq.md)

### How to Ask Good Questions

**Include:**

1. What you're trying to do
2. What you expected to happen
3. What actually happened
4. What you've already tried
5. Relevant code snippets or error messages
6. Your environment (language version, OS, etc.)

**Example:**

````markdown
## Problem

I'm trying to parse JSON from an API in my January project, but I'm getting an error.

## Expected

The JSON should parse into a dictionary/object.

## Actual

Error: `JSONDecodeError: Expecting value: line 1 column 1 (char 0)`

## What I've Tried

- Checked the API response with curl - it returns JSON
- Tried different parsing methods
- Googled the error message

## Code

```python
import requests
import json

response = requests.get("https://api.example.com/data")
data = json.loads(response)  # Error happens here
```

## Environment

- Python 3.11
- requests library 2.31.0
- macOS 14.1
````

---

## After Submission

### Review Period

- Wait patiently for your review
- Check your PR for comments
- Respond to questions from reviewers
- Engage constructively with feedback

### Learning from Reviews

- Read feedback carefully
- Click on resource links
- Try implementing suggestions in a new branch
- Apply learnings to next month's project

### Sharing Your Work

After the month's deadline:

- Share in the Show & Tell Discussion category
- Write a blog post about what you learned
- Help others by reviewing their approach
- Use the hashtag #EWT2026 on social media

### Next Month

- Reflect on what you learned
- Note what to improve
- Apply feedback to next project
- Keep building momentum!

---

## Frequently Encountered Issues

### "My PR isn't showing up"

- Make sure you're creating a PR to `engineeringwithtemi/ewt2026`, not your own fork
- Check that you selected the correct base branch (`main`)

### "I can't push to the repository"

- You shouldn't push directly - use a Pull Request from your fork
- Review the Git workflow section above

### "I made changes to wrong folder"

- Close your PR
- Fix your local repository
- Create new PR with correct structure

### "I submitted to wrong month"

- Comment on your PR explaining the mistake
- We can help you sort it out

### "I missed the deadline"

- Submit anyway! Late submissions are accepted but not prioritized
- You'll still get a review, just maybe not as quickly

### "I need to change my submission after review"

- Just push more commits to your branch
- Comment on the PR explaining changes
- Updates after final review may not get re-reviewed

---

## Community & Support

### Connect with Others

- General Discussion category - Introduce yourself
- Collaboration Discussion category - Find partners
- Monthly project Discussion categories - Discuss current challenge
- Discord/Skool (links in main README)

### Stay Updated

- Watch the repository for notifications
- Follow #EWT2026 on social media
- Check the Announcements discussion category regularly
- Subscribe to discussion categories you're interested in

### Give Back

- Help answer questions in Discussions
- Share resources you found helpful
- Encourage other participants
- Consider becoming a reviewer after gaining experience

---

## Quick Reference Checklist

**Before Starting:**

- [ ] Forked the repository
- [ ] Read the project README
- [ ] Understood the requirements

**During Development:**

- [ ] Created folder: `/month-2026/submissions/my-username/`
- [ ] Wrote comprehensive README.md
- [ ] Committed code regularly
- [ ] Tested my solution

**Before Submitting:**

- [ ] All requirements met
- [ ] Code is clean and documented
- [ ] README explains my approach
- [ ] No sensitive information
- [ ] Everything in correct folder

**Submission:**

- [ ] Created PR to main repository
- [ ] Filled out PR template
- [ ] PR is Open (Draft or Ready for Review)
- [ ] Double-checked everything

**After Submission:**

- [ ] Responded to reviewer questions
- [ ] Engaged constructively with feedback
- [ ] Marked conversations as resolved
- [ ] Thanked my reviewer

---

## You've Got This! 🚀

Remember:

- **It's about learning, not perfection**
- **Everyone starts somewhere**
- **The community is here to help**
- **Every project makes you better**
- **Asking questions is encouraged**
- **Your unique approach is valuable**

Happy coding, and welcome to EWT2026!

---

**Questions?** Check the [FAQ](faq.md) or ask in the Discussions tab

**Need help?** The community is here for you!

**Found a typo or improvement?** Submit a PR or open an Issue!
