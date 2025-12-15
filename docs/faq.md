# Frequently Asked Questions (FAQ)

## Table of Contents

- [General Questions](#general-questions)
- [Participation Questions](#participation-questions)
- [Technical Questions](#technical-questions)
- [Submission Questions](#submission-questions)
- [Review Questions](#review-questions)
- [Reviewer Questions](#reviewer-questions)
- [Timeline & Deadlines](#timeline--deadlines)
- [Community & Support](#community--support)

---

## General Questions

### What is EWT2026?

EWT2026 (Engineering With Temi 2026) is a free, year-long coding challenge where developers build 12 real-world projects (one per month) and receive expert code reviews. It's designed to help junior and mid-level developers gain practical experience and improve their skills through mentorship and community collaboration.

### Is EWT2026 really free?

Yes! Participation is completely free. There are no hidden costs, premium tiers, or paid features. Code reviews are provided by volunteer reviewers who donate their time and expertise.

### Who is EWT2026 for?

EWT2026 is designed for:

- Junior developers (0-2 years experience) looking to build real-world projects
- Mid-level developers (2-5 years) wanting to expand their skills
- Self-taught developers needing portfolio projects
- Career switchers building practical experience
- Anyone wanting to improve through code reviews and mentorship

Advanced developers are welcome too, but projects are calibrated for junior-to-mid skill levels.

### Do I need to participate every month?

No! You can participate in as many or as few months as you like. Each project is standalone—you don't need to complete previous months to join a new one. However, consistent participation will maximize your learning.

### What if I'm a complete beginner?

You should have basic programming knowledge in at least one language. If you can:

- Write simple programs (loops, conditionals, functions)
- Understand basic data structures (arrays, objects/dictionaries)
- Read and understand code documentation

Then you're ready! The projects vary in difficulty, and early months tend to be more beginner-friendly.

### Can I participate if I'm already working as a developer?

Absolutely! Many working developers participate to:

- Learn new technologies
- Get feedback from senior engineers
- Build portfolio projects
- Practice skills outside their daily work
- Give back by helping others in discussions

### What languages/technologies can I use?

Any language or technology you want! Common choices include:

- **Languages:** JavaScript, Python, Rust, Go, Java, C#, Ruby, PHP, TypeScript
- **Frameworks:** React, Vue, Angular, Django, Flask, Spring Boot, .NET, Rails
- **Tools:** Docker, databases, APIs, cloud services

Each monthly project specifies requirements (e.g., "build a web scraper"), but you choose how to implement it.

---

## Participation Questions

### How do I get started?

1. **Fork the repository** at [github.com/engineeringwithtemi/ewt2026](https://github.com/engineeringwithtemi/ewt2026)
2. **Read the current month's project** in `/[month]-2026/README.md`
3. **Create your submission folder** at `/[month]-2026/submissions/your-username/`
4. **Build your solution**
5. **Submit a Pull Request**

See the full guide: [How to Participate](how-to-participate.md)

### Do I need to know Git/GitHub?

Basic Git/GitHub knowledge is required:

- Forking a repository
- Cloning to your computer
- Committing changes
- Creating pull requests

New to Git? Check these resources:

- [GitHub's Git Handbook](https://guides.github.com/introduction/git-handbook/)
- [Git Tutorial for Beginners](https://www.youtube.com/watch?v=8JJ101D3knE)

### Can I use AI tools like ChatGPT, Copilot, or Claude?

Yes! AI assistants are allowed and encouraged as learning tools. However:

- ✅ You must **understand** the code you submit
- ✅ You must be able to **explain** your design decisions
- ✅ You should **learn from** the AI, not just copy-paste
- ✅ Your README should explain **your approach** and thinking

Reviewers may ask questions to ensure you understand your submission.

### Can I work with others or get help?

Yes! Collaboration is encouraged:

- ✅ Discuss approaches in the monthly Discussion categories
- ✅ Ask for help when stuck (in Discussions or Q&A)
- ✅ Form study groups
- ✅ Pair program with other participants

However:

- ❌ Don't copy another participant's solution
- ❌ Don't submit someone else's work as your own
- ✅ Do credit significant help in your README

### What if I don't finish in time?

Submit what you have! Benefits of submitting incomplete work:

- You still get feedback on what you built
- Partial solutions show your thinking process
- You learn from the review
- It's better than not submitting at all

Late submissions are accepted but not prioritized for review.

### Can I submit multiple solutions?

One submission per person per month. However, you can:

- Update your submission before final review
- Try different approaches in your own fork
- Share alternative approaches in Discussions (after deadline)

### What if I want to change my approach mid-month?

That's fine! You can:

- Update your code before final submission
- Explain in your README why you pivoted
- Submit a DRAFT first, get feedback, then change direction

Learning and iteration are encouraged.

---

## Technical Questions

### Where should my code go?

**Your code MUST be in:**

```
/[month]-2026/submissions/[your-exact-github-username]/
```

Example:

```
/january-2026/submissions/johndoe/
```

You can create any structure inside your folder:

```
january-2026/submissions/johndoe/
├── README.md
├── src/
├── tests/
├── docs/
└── (dependency files)
```

### What files are required?

**Required:**

- `README.md` - Explains your solution, approach, and learnings

**Recommended:**

- Source code files
- Dependency files (package.json, requirements.txt, Cargo.toml, etc.)
- `.gitignore`

**Optional but encouraged:**

- Tests
- Additional documentation
- Setup scripts

### Can I use external libraries and frameworks?

Yes! Use any libraries, frameworks, or tools you want. Just:

- ✅ Document them in your README
- ✅ Include dependency files
- ✅ Provide setup instructions
- ✅ Make sure reviewers can run your code

### How do I handle API keys and secrets?

**Never commit secrets to the repository!**

❌ **Don't:**

```python
API_KEY = "sk-1234567890abcdef"  # DON'T DO THIS
```

✅ **Do:**

```python
import os
API_KEY = os.getenv("API_KEY")
```

**In your README, include:**

- Where to get API keys
- How to set environment variables
- Example `.env.example` file

### Can I include a database in my project?

Yes! Options:

- **Local database:** SQLite, file-based storage
- **Dockerized database:** Provide docker-compose.yml
- **Cloud database:** Document how to set it up
- **Mock data:** Provide sample data for testing

Make sure reviewers can run your project without complex setup.

### What if my project needs paid services?

Try to use free tiers or alternatives:

- Free API tiers (many services offer free plans)
- Local alternatives (SQLite instead of PostgreSQL)
- Mock/demo modes
- Docker for local services

If paid services are necessary:

- Document the costs
- Provide alternatives or mocks
- Make the paid parts optional

### My project is really large. Can I submit it?

Yes, but consider:

- Not every file needs to be in the repo (node_modules, build artifacts)
- Use `.gitignore` appropriately
- Focus on quality over quantity
- Reviewers may not review every single file in depth

If it's extremely large (100+ files), consider:

- Highlighting key files in your README
- Pointing reviewers to the most important parts

---

## Submission Questions

### What's the difference between DRAFT and FINAL submissions?

**Draft Pull Request:**

- Early submission for feedback
- Primarily AI-reviewed
- Optional human review if reviewers have time
- Can be updated freely
- Good for getting direction early

**Final Submission (Ready for Review):**

- Marked as "Ready for review"
- Should be complete and tested
- Updates after review may not be re-reviewed
- Prioritized for human reviewers

**Timeline:**

```
Week 1: Submit DRAFT → Get AI feedback → Iterate
Week 3: Submit DRAFT → Get feedback → Refine
Week 4: Submit FINAL → Get human review
```

### How do I submit a DRAFT vs FINAL?

**To submit a Draft:**

- Click the arrow next to "Create pull request"
- Select "Create draft pull request"

**To submit as Final:**

- Click "Create pull request" directly
- Or convert your Draft PR by clicking "Ready for review"

**Converting to Final:**

- Go to your PR page
- Click "Ready for review" button
- Add a comment: `Ready for final review!`

### What should I write in the PR description?

Fill out the PR template completely. Include:

- Which month/project
- Submission type (DRAFT/FINAL)
- Brief overview of your solution
- Tech stack used
- Challenges you faced
- Questions for reviewers

See the template when you create a PR.

### Can I update my submission after creating the PR?

Yes! Just push more commits to your branch:

```bash
# Make changes locally
git add .
git commit -m "Address feedback: improve error handling"
git push origin your-branch-name
```

The PR automatically updates. However, updates after final review may not be re-reviewed.

### I made a mistake in my submission. What do I do?

**Small mistake (typo, minor bug):**

- Push a fix commit
- Comment on the PR explaining the change

**Wrong folder or major structural issue:**

- Close the PR
- Fix your local repository
- Create a new PR

**Need help:**

- Comment on your PR asking for guidance
- Ask in the General Discussion category

### Can I delete my submission and start over?

You can:

- Close your PR
- Delete your branch locally and on your fork
- Start fresh with a new branch and PR

However, consider just updating your existing PR instead—showing iteration is valuable!

---

## Review Questions

### When will I get my review?

**DRAFT submissions:**

- AI review: Usually within 1-3 days
- Human review: If reviewers have time (not guaranteed)

**FINAL submissions:**

- Target: Within 5-10 days after the month's deadline
- May be faster or slower depending on reviewer availability
- Earlier submissions generally reviewed faster

### What if I don't get a review?

Possible reasons:

- Submitted very late (deprioritized)
- Month had many submissions (reviewers overwhelmed)
- Technical issues

What to do:

- Wait at least 10 days after deadline
- Comment on your PR: "Checking on review status"
- Ask in General Discussion
- Be patient—reviewers are volunteers

### Can I request a specific reviewer?

Not directly, but:

- CODEOWNERS automatically assigns reviewers based on language/folder
- You can mention expertise you'd like: "Would appreciate feedback from someone experienced with React"
- Maintainers may assign based on availability

Don't tag specific reviewers unless invited to do so.

### What if I disagree with the review feedback?

Reviews are learning opportunities, but dialogue is welcome:

**✅ Do:**

- Ask clarifying questions politely
- Explain your reasoning for decisions
- Engage in constructive discussion
- Research the suggested approach

**❌ Don't:**

- Argue defensively
- Dismiss feedback without consideration
- Demand the reviewer is wrong
- Take it personally

**Example response:**

```markdown
Thanks for the feedback! I chose approach X because [reasoning].
I see your point about approach Y. Could you explain more about
why it's preferred in this case? I'd like to understand the
trade-offs better.
```

### Can I get a second review or opinion?

For different perspectives:

- Ask in Discussions (after deadline)
- Request another reviewer's input (politely)
- Share your submission in Show & Tell

Don't demand multiple reviews—reviewers are volunteers.

### How do I know if my review is complete?

Reviewers will typically:

- Leave inline comments on code
- Provide an overall summary review
- Mark the review as "Approve," "Request changes," or "Comment"

If unclear, ask: "Is this review complete, or should I wait for more feedback?"

---

## Reviewer Questions

### How do I become a reviewer?

1. **Meet the requirements:**

   - 2+ years of relevant experience
   - Demonstrated expertise in at least one tech stack
   - Commitment to Code of Conduct

2. **Apply:**

   - Create an Issue using the "Reviewer Volunteer Application" template
   - Fill out your background, expertise, and motivation
   - Wait for approval (typically 3-5 days)

3. **Once approved:**
   - Added as repository collaborator
   - Invited to reviewer channels
   - Can start reviewing!

See: [REVIEW_GUIDELINES.md](../REVIEW_GUIDELINES.md)

### Do I get paid to review?

No, this is a volunteer position. Benefits include:

- Giving back to the community
- Improving your own skills
- Building reputation
- Networking with other engineers
- LinkedIn recommendations available
- Recognition in the community

### How much time do I need to commit?

Flexible! Suggested minimum:

- 2-3 hours per month
- 2-3 reviews per month

Review when you have time. No pressure to review every submission.

### What if I'm not sure about something in a review?

**It's okay to:**

- Say "I'm not familiar with this approach"
- Research before responding
- Ask other reviewers for input
- Focus on what you do know

**Don't:**

- Pretend to know something you don't
- Give incorrect information
- Review outside your expertise without caveats

### Can I stop being a reviewer?

Yes, anytime! Just:

- Let maintainers know
- We'll remove you from CODEOWNERS
- You can rejoin later if you want

No hard feelings—life happens!

---

## Timeline & Deadlines

### When are projects announced?

**First week of each month:**

- January 1: January project announced
- February 1: February project announced
- And so on...

Announcements include:

- Project requirements (README)
- Announcement video
- Discussion thread

### What are the deadlines?

**Monthly cycle:**

- Week 1: Project announced
- Weeks 1-4: Development period
- End of Week 4: Final submission deadline

**Example:**

- January 1: Project announced
- January 31: Final submission deadline
- February 1: Next project begins

### What happens if I miss the deadline?

**You can still submit!**

Late submissions are:

- ✅ Accepted
- ✅ Reviewed (when reviewers have time)
- ❌ Not prioritized

**Better late than never**—you'll still learn from the feedback.

### Can I work on multiple months simultaneously?

Yes! If you want to catch up or work ahead:

- Each month's project stays available
- You can submit to any month anytime
- Focus on learning, not just completing all 12

### Is there a final deadline for the entire year?

No hard cutoff. The 2026 projects run January-December 2026, but:

- Projects remain available after 2026
- You can complete them at your own pace
- Reviews may slow down after the active year

---

## Community & Support

### Where can I ask questions?

**GitHub Discussions (various categories):**

- General - Community chat
- Q&A - Technical questions
- Monthly project categories - Project-specific discussion
- Debugging Help - When you're stuck

**GitHub Issues:**

- Project clarifications - Official requirement questions
- Bug reports - Repository/process issues

**External:**

- Discord/Skool community (links in README)
- Use #EWT2026 on social media

### How do I report a Code of Conduct violation?

**If you experience or witness:**

- Harassment
- Discrimination
- Disrespectful behavior
- Spam or trolling

**Report it:**

1. Contact @engineeringwithtemi directly (GitHub or email)
2. Provide details of what happened
3. Include links/screenshots if possible

All reports are confidential and taken seriously.

### Can I promote my work or services?

**Allowed:**

- Sharing your completed projects
- Mentioning tools/libraries you used
- Linking to your portfolio/GitHub in your README
- Celebrating wins and milestones

**Not allowed:**

- Spam or excessive self-promotion
- Advertising paid services
- Recruiting without permission
- Off-topic promotion

### Is there a certificate or credential?

Not currently, but you gain:

- 12 reviewed projects for your portfolio
- GitHub contribution history
- Real code review feedback
- Community recognition
- Experience you can discuss in interviews

These are more valuable than a certificate!

### Can I write about EWT2026 or share my experience?

Absolutely! Please do:

- Blog about your journey
- Create YouTube videos
- Share on social media (#EWT2026)
- Write case studies
- Give talks about what you learned

Just:

- ✅ Be honest about your experience
- ✅ Credit EWT2026 and reviewers
- ❌ Don't misrepresent the program

### How can I support EWT2026?

**As a participant:**

- Help others in Discussions
- Share resources you found helpful
- Encourage fellow participants
- Spread the word about the challenge

**As a developer:**

- Become a reviewer
- Contribute to documentation
- Suggest improvements
- Share on social media

**As anyone:**

- Star the repository
- Share with others who'd benefit
- Provide feedback to improve the program

---

## Troubleshooting

### I can't create a Pull Request

**Common issues:**

1. **Pushing to wrong repo:**

   - Make sure you're creating PR from your fork to the original repo
   - Not from your fork to your fork

2. **Wrong branch:**

   - PR should target `main` branch of original repo

3. **No changes:**
   - Make sure you've committed and pushed changes

**Solution:**

- Review [How to Participate](how-to-participate.md) Git workflow section
- Ask in Q&A Discussion

### My PR isn't showing my changes

**Check:**

- Did you push to your fork? `git push origin your-branch`
- Are you looking at the right branch?
- Did commits actually happen? `git log`

### I accidentally modified files outside my folder

**Fix it:**

1. Close your PR
2. Locally, undo changes to files outside your folder
3. Create new PR with only your folder changes

**Or:**

- Ask for help in your PR comments
- A maintainer can guide you

### GitHub Actions are failing on my PR

**Check the error message:**

- Did you modify files outside your folder?
- Is your README.md present?
- Do you have the right folder structure?

**Fix:**

- Address the specific issue mentioned
- Push the fix
- Actions will re-run automatically

### I'm stuck on my project

**Before asking:**

1. Re-read the project requirements
2. Search for the error message online
3. Try debugging step-by-step
4. Check if others asked similar questions

**Then ask in:**

- Debugging Help Discussion (with specific details)
- Monthly project Discussion
- Q&A Discussion

**Provide:**

- What you're trying to do
- What's happening
- What you've tried
- Relevant code/error messages

---

## Still Have Questions?

**Documentation:**

- [How to Participate](./how-to-participate.md)
- [Review Guidelines](../REVIEW_GUIDELINES.md)
- [Contributing Guidelines](../CONTRIBUTING.md)
- [Code of Conduct](../CODE_OF_CONDUCT.md)

**Ask the Community:**

- General Discussion category
- Q&A Discussion category
- Monthly project Discussion categories

**Contact:**

- Create an Issue (for official questions)
- Tag @engineeringwithtemi in Discussions

---

**Last Updated:** January 2026

**Found an issue with this FAQ?** Submit a PR or create an Issue!
