# Contributing to EWT2026

## For Participants

### Folder Structure Rules (CRITICAL - Prevents Merge Conflicts)

**You MUST create your submission in a folder named exactly after your GitHub username:**

```
/[month]-2026/submissions/[your-exact-github-username]/
```

**Example:** If your GitHub username is `johndoe`, your folder MUST be:

```
/january-2026/submissions/johndoe/
```

⚠️ **Important:**

- Use your exact GitHub username (case-sensitive)
- Do NOT modify any files outside your personal folder
- Do NOT modify other participants' folders
- Do NOT modify the project README or requirements

This ensures zero merge conflicts!

### Submission Process

1. **Fork** the repository to your GitHub account
2. **Clone** your fork locally
3. **Create a branch** (recommended naming: `january-submission`)
4. **Create your folder:**

```bash
   mkdir -p january-2026/submissions/your-username
   cd january-2026/submissions/your-username
```

5. **Add your files:**

   - `README.md` (required - explain your approach)
   - Your source code
   - Tests (optional but encouraged)
   - Any documentation

6. **Commit your changes:**

```bash
   git add .
   git commit -m "January 2026 submission - [brief description]"
```

7. **Push to your fork:**

```bash
   git push origin january-submission
```

8. **Create Pull Request:**
   - Go to the original repository
   - Click "New Pull Request"
   - Select your branch
   - Fill out the PR template completely
   - Add `[DRAFT]` or `[FINAL]` to the title

## Issues vs Discussions: When to Use What

We use both GitHub Issues and Discussions to organize different types of communication. Here's when to use each:

### Use **Issues** for:

- ✅ **Reviewer applications** - Apply to become a code reviewer
- ✅ **Bug reports** - Report problems with the repository, workflows, or documentation
- ✅ **Feature requests** - Suggest improvements that need tracking and implementation
- ✅ **Official project clarifications** - Questions about requirements that need definitive answers from maintainers

### Use **Discussions** for:

- 💬 **General questions** - Ask the community for help or advice
- 💬 **Approach discussions** - Discuss different ways to solve the monthly challenge
- 💬 **Show & Tell** - Share your completed solution and what you learned
- 💬 **Community chat** - Introduce yourself, network with other participants
- 💬 **Monthly project threads** - Discuss the current month's challenge with peers
- 💬 **Ideas and feedback** - Share suggestions in a conversational format

**Quick Guide:**

- Need official action or tracking? → **Issue**
- Want community conversation? → **Discussion**
- Not sure? → Start with **Discussion**, we can convert to Issue if needed

**Discussion Categories:**

- 📢 **Announcements** - Monthly project releases and important updates (maintainers only)
- 💬 **General** - Community chat and introductions
- ❓ **Q&A** - General programming questions and setup help
- 🗓️ **[Month] 2026** - Discussion for each month's project (e.g., January 2026, February 2026)
- 💡 **Ideas & Suggestions** - Casual suggestions and brainstorming
- 🎨 **Show & Tell** - Share your solutions and learnings
- 🤝 **Collaboration** - Find study partners and form review groups

### Draft vs Final Submissions

**[DRAFT] Submissions:**

- For early feedback
- Primarily reviewed by AI
- Optional human review
- Can be updated freely
- Remove `[DRAFT]` tag when ready for final review

**[FINAL] Submissions:**

- Ready for human reviewer feedback
- Should be complete and tested
- Updates after review will not be prioritized
- Must be submitted before month deadline

### Timeline

- **Week 1:** Project announced, requirements published
- **Weeks 1-4:** Work on your solution, submit drafts anytime
- **End of Week 4:** Deadline for FINAL submissions
- **After Deadline:** Late submissions accepted but not prioritized

### Required Files in Your Submission

#### README.md (Required)

Your submission folder MUST include a README.md with:

- Project overview
- How to run your code
- Technologies/dependencies used
- Your approach and design decisions
- Challenges you faced
- What you learned

#### Example Structure:

```
january-2026/submissions/your-username/
├── README.md              # Required
├── src/                   # Your code structure
│   ├── main.rs           # (or main.js, main.py, etc.)
│   └── ...
├── tests/                 # Optional but encouraged
├── docs/                  # Optional
├── Cargo.toml            # Or package.json, requirements.txt, etc.
└── ...
```

### What NOT to Do

❌ Create folders outside `/[month]/submissions/[your-username]/`
❌ Modify other participants' code
❌ Modify project requirements or READMEs
❌ Use offensive or inappropriate folder/file names
❌ Submit the same solution to multiple months
❌ Use a different username than your GitHub account

### Code of Conduct

Please read our [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md) before participating.

### Questions?

- Check the [FAQ](docs/faq.md)
- Check project-specific README in `/[month]-2026/README.md`
- Open a GitHub Discussion
- Ask in Discord/Skool community

## For Reviewers

See [REVIEW_GUIDELINES.md](./REVIEW_GUIDELINES.md) for reviewer-specific instructions.
