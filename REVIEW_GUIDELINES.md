# Review Guidelines for EWT2026

## Our Philosophy

EWT2026 exists to help junior and mid-level developers grow through real-world project experience and mentorship. As a reviewer, you're not just evaluating code—you're helping shape the next generation of engineers.

**Your review should:**

- Build confidence while encouraging growth
- Point to resources, not just solutions
- Celebrate what's done well
- Guide exploration rather than provide all answers
- Be kind, constructive, and respectful

---

## Core Principles

### 1. Respect Every Participant

- Remember: participants are learning and putting themselves out there
- Avoid condescending language ("obviously", "clearly", "just do X")
- Acknowledge the effort and courage it takes to submit code for review
- Treat every submission with the same care, regardless of skill level

### 2. Constructive Feedback Only

- Focus on improvement, not criticism
- Frame feedback as opportunities: "Consider using X because Y" instead of "This is wrong"
- No harmful, abusive, or discriminatory language—zero tolerance
- If you're frustrated, step away and come back later

### 3. Encourage Exploration

- **Don't give direct answers to everything**—help them learn to find answers
- Ask guiding questions: "Have you considered...?", "What would happen if...?"
- Point to documentation, articles, or concepts to explore
- Share your thinking process, not just the solution

### 4. Include Resources

- **Always include links** when discussing concepts, patterns, or tools
- Link to official documentation when possible
- Share blog posts, tutorials, or examples that helped you learn
- Create a "Further Reading" section if you have many resources

### 5. Prioritize Unreviewed Code

- Check for PRs that haven't received human review yet
- Our goal: review as many participants as possible, not perfect reviews on a few
- Breadth over depth—a good review for everyone beats perfect review for some

### 6. Collaborate with AI Reviews

- AI reviews happen first for DRAFT submissions
- Feel free to add context, corrections, or additional insights to AI reviews
- If AI missed something important, add it
- If AI was unclear or wrong, clarify

### 7. Tag and Communicate

- Use `@username` to ask participants for clarification
- Ask questions when the code or approach isn't clear
- Encourage dialogue—reviews are conversations, not lectures

---

## Review Checklist

When reviewing a submission, consider these areas:

### ✅ **Project Requirements**

- [ ] Does the solution meet the project brief requirements?
- [ ] Are all mandatory features implemented?
- [ ] Is the submission complete or are there missing pieces?

### ✅ **Code Quality**

- [ ] Is the code readable and well-organized?
- [ ] Are variable/function names clear and descriptive?
- [ ] Is there proper error handling?
- [ ] Are there any obvious bugs or issues?

### ✅ **Best Practices**

- [ ] Does the code follow language/framework conventions?
- [ ] Are there security concerns? (hardcoded secrets, SQL injection, etc.)
- [ ] Is the code maintainable?
- [ ] Are there opportunities to apply design patterns or principles?

### ✅ **Documentation**

- [ ] Is there a clear README explaining the approach?
- [ ] Are setup/run instructions included and clear?
- [ ] Are dependencies documented?
- [ ] Is the code commented where necessary (not over-commented)?

### ✅ **Tests (if applicable)**

- [ ] Are there tests for core functionality?
- [ ] Do tests actually run and pass?
- [ ] Is test coverage reasonable for a learning project?

### ✅ **Learning & Growth**

- [ ] What did the participant do well? (Always mention this!)
- [ ] What are 1-3 key areas for improvement?
- [ ] What concepts could they explore further?

---

## Review Structure Template

Here's a suggested structure for your reviews:

```markdown
## Review for @participant-username

### What You Did Well 🌟

[Always start with positives - what impressed you, what shows good understanding, what was well-executed]

### Core Feedback

#### Meets Requirements ✅ / ⚠️ / ❌

[Does this meet the project brief? If not, what's missing?]

#### Code Quality & Organization

[Feedback on structure, readability, naming, etc.]

- **Example:** Your function names are clear and descriptive, which makes the code easy to follow.
- **Suggestion:** Consider extracting this 50-line function into smaller, focused functions. Here's a good article on function composition: [link]

#### Best Practices & Patterns

[Language-specific conventions, design patterns, common pitfalls]

- **Issue:** Hardcoded database credentials in `config.js`
- **Why it matters:** Security risk if this code is ever shared or deployed
- **How to fix:** Use environment variables. See: [dotenv documentation](https://www.npmjs.com/package/dotenv)

#### Error Handling & Edge Cases

[How does the code handle failures, invalid input, etc.]

### Questions for You 🤔

[Ask clarifying questions about design decisions, approach, or anything unclear]

- Why did you choose approach X over Y?
- How does your code handle [specific edge case]?
- Have you considered [alternative approach]?

### Suggestions for Improvement 📚

#### High Priority

[Issues that should be addressed - security, major bugs, missing requirements]

#### Nice to Have

[Enhancements, optimizations, style improvements]

#### Explore Further (Optional)

[Concepts, patterns, or tools to learn more about]

- **Concept:** Dependency Injection - [link to article]
- **Pattern:** Repository Pattern for data access - [link]
- **Tool:** Consider trying [X] for [Y] - [link]

### Resources

[Curated list of documentation, articles, videos related to your feedback]

- [Official Docs - Topic X](link)
- [Great Tutorial - Topic Y](link)
- [Reference Implementation](link)

### Summary

[2-3 sentences: overall assessment, key takeaway, encouragement]

---

Great work putting this together! The effort you've put into [specific aspect] really shows. Focus on [1-2 key improvements] and keep building! 🚀
```

---

## Review Examples

### ❌ Bad Review:

> "This code is messy and hard to read. You should refactor it. Also you're not handling errors properly. The naming is bad too."

**Problems:**

- Vague and discouraging
- No specific guidance
- No resources
- No positives mentioned
- Unhelpful tone

### ✅ Good Review:

> **What You Did Well:** Your algorithm is efficient and the core logic is sound! I also appreciate that you included comments explaining the tricky parts.
>
> **Suggestion on Readability:** The `processData()` function is doing a lot (parsing, validation, transformation, and saving). Consider breaking it into smaller functions:
>
> ```javascript
> function processData(data) {
>   const parsed = parseInput(data);
>   const validated = validateData(parsed);
>   const transformed = transformData(validated);
>   return saveToDatabase(transformed);
> }
> ```
>
> This makes each step testable and easier to understand. Here's a great article on the Single Responsibility Principle: [link]
>
> **Error Handling:** I noticed that if the database connection fails, the app crashes. Have you considered using try-catch blocks? Check out [error handling best practices in Node.js](link).
>
> Keep up the great work! 🎉

**Why it's good:**

- Starts with genuine praise
- Specific, actionable feedback
- Includes code example
- Links to resources
- Encouraging tone
- Asks questions to promote thinking

---

## Types of Feedback

### 🎯 **Critical (Must Address)**

Issues that:

- Break core functionality
- Create security vulnerabilities
- Violate project requirements
- Could cause data loss or system failures

**Example:**

> **Critical:** SQL query is vulnerable to injection attacks. Never concatenate user input directly into queries. Use parameterized queries instead: [link to docs]

### ⚠️ **Important (Should Address)**

Issues that:

- Violate best practices
- Make code hard to maintain
- Could cause bugs in edge cases
- Impact performance significantly

**Example:**

> **Important:** Loading the entire dataset into memory could cause issues with large files. Consider streaming or pagination: [link to solution]

### 💡 **Suggestion (Nice to Have)**

Ideas that:

- Improve code quality
- Introduce helpful patterns
- Optimize performance
- Enhance user experience

**Example:**

> **Suggestion:** You might enjoy trying the builder pattern here to make object creation more fluent: [link to pattern]

### 📚 **Learning Opportunity**

Concepts to explore:

- Related technologies
- Advanced patterns
- Industry practices
- Alternative approaches

**Example:**

> **For Further Learning:** Your caching implementation works well! If you want to dive deeper, check out Redis for production-grade caching: [link]

---

## What to Look For (By Language/Technology)

### General (All Languages)

- Clear variable/function naming
- Proper error handling
- No hardcoded secrets or credentials
- Code organization and structure
- Comments where necessary (complex logic, not obvious code)
- README with setup instructions

### JavaScript/TypeScript

- Proper use of `const`/`let` (no `var`)
- Async/await vs callbacks vs promises
- Error handling in async code
- Package.json with dependencies
- Modern ES6+ features used appropriately
- TypeScript: proper typing, avoiding `any`

### Python

- PEP 8 style compliance (or mention if not)
- Virtual environment usage
- requirements.txt or pyproject.toml present
- Proper exception handling
- Use of context managers (`with` statement)
- Type hints (Python 3.5+)

### Rust

- Ownership and borrowing used correctly
- Error handling with Result/Option
- No unnecessary `.clone()` or `.unwrap()`
- Cargo.toml present and correct
- Idiomatic Rust patterns
- No unsafe code without justification

### Go

- Go fmt compliance
- Error handling (not ignoring errors)
- go.mod present
- Proper use of goroutines and channels
- Context usage for cancellation
- Idiomatic Go patterns

### General Web Development

- Responsive design considerations
- Accessibility basics (semantic HTML, alt text)
- No inline styles (use CSS)
- Security: XSS prevention, CSRF tokens, etc.
- Performance: minimize bundle size, lazy loading

---

## Handling Different Skill Levels

### Beginner Submissions

- **Be extra encouraging** - this might be their first code review ever
- Focus on 2-3 key improvements, not everything
- Explain concepts more thoroughly
- Suggest beginner-friendly resources
- Celebrate working code, even if imperfect

**Example:**

> Getting this working is a great achievement! The logic is solid. To take it further, let's focus on two things: error handling and code organization. Here are some beginner-friendly guides: [links]

### Intermediate Submissions

- Point out best practices and patterns
- Discuss trade-offs in design decisions
- Suggest refactoring opportunities
- Introduce intermediate/advanced concepts
- Challenge them with "what if" scenarios

**Example:**

> Your implementation works well! Have you considered what happens when [edge case]? Also, the repository pattern might clean up your data access layer—worth exploring: [link]

### Advanced Submissions

- Discuss architectural decisions
- Performance and scalability considerations
- Advanced patterns and practices
- Industry standards and production concerns
- Ask for their reasoning on complex decisions

**Example:**

> Solid implementation of the CQRS pattern. I'm curious about your choice of [X] for event sourcing—have you compared it with [Y]? Also consider the CAP theorem implications here: [link]

---

## Common Pitfalls to Avoid

### ❌ **Don't Do This:**

1. **Give the complete solution**

   - Bad: "Here's the full code you should use: [paste solution]"
   - Good: "Consider this approach: [hint], and check out [pattern] here: [link]"

2. **Be vague**

   - Bad: "This could be better"
   - Good: "This function could be more maintainable if split into smaller pieces. See Single Responsibility Principle: [link]"

3. **Focus only on negatives**

   - Bad: Only listing problems
   - Good: Start with what they did well, then constructive feedback

4. **Overwhelm with feedback**

   - Bad: 50 comments on every single line
   - Good: Focus on 3-5 key areas for improvement

5. **Use jargon without explanation**

   - Bad: "This violates LSP and needs DI with IoC"
   - Good: "The Liskov Substitution Principle suggests [explanation]. Here's a clear guide: [link]"

6. **Forget to encourage**

   - Bad: Pure technical critique with no human touch
   - Good: End with encouragement and acknowledgment of effort

7. **Make assumptions about knowledge**
   - Bad: "Obviously you should use a factory pattern here"
   - Good: "A factory pattern might help here—it's a way to [brief explanation]. Learn more: [link]"

---

## Special Cases

### DRAFT Submissions

- Expect incomplete or work-in-progress code
- Focus on direction and approach
- Ask questions about their plan
- Lighter, quicker feedback
- Encourage them to keep going

### Late Submissions

- Still provide quality feedback
- Note they may not be prioritized
- Same respect and care as on-time submissions
- Acknowledge their effort

### Incomplete Submissions

- Note what's missing
- Assess what IS there
- Encourage completion
- Provide feedback on implemented parts

### Exceptional Submissions

- Celebrate excellence!
- Share as an example (with permission)
- Provide advanced challenges
- Still give constructive feedback on small improvements

---

## Communication Guidelines

### Tone

- **Professional but friendly** - like mentoring a colleague
- **Encouraging and supportive** - people are nervous about reviews
- **Honest but kind** - truth with compassion
- **Curious, not judgmental** - ask questions, don't assume

### Language

- Use "we" and "our" sometimes to build collaboration
  - "We could improve this by..."
  - "Our error handling could be more robust"
- Use questions to promote thinking
  - "What would happen if the API is down?"
  - "How might we handle very large files?"
- Avoid absolutes unless truly absolute
  - Instead of "Never use X", try "X is generally avoided because Y"

### Emoji Usage (Optional)

- Use sparingly and professionally
- Appropriate: ✅ ❌ 🎯 💡 📚 🚀 🌟 ⚠️
- Avoid: 😂 🤣 💩 (can seem mocking)

---

## Reviewing AI-Generated Code

Participants may use AI assistance (ChatGPT, Copilot, Claude, etc.). This is okay! Our focus is on learning, not the source.

**What to look for:**

- Do they understand the code they've submitted?
- Can they explain design decisions?
- Have they customized it for the requirements?
- Did they just copy-paste or did they learn from it?

**How to address it:**

- Ask questions about design choices
- Request explanation of complex parts
- Suggest improvements that require understanding
- Focus on learning outcomes, not code origin

**Example:**

> I see you're using [pattern/approach]. Can you explain why this approach works well for this problem? Also, how would you modify this if [requirement changed]?

---

## Time Management

### Per Review Time Budget

- **Quick review:** 10-15 minutes (scan, high-level feedback)
- **Standard review:** 20-30 minutes (thorough, multiple comments)
- **Deep review:** 45-60 minutes (detailed, complex projects)

Most reviews should be standard. Don't feel pressure to write novels!

### Prioritization

1. **FINAL** submissions without human review
2. **DRAFT** submissions that need guidance
3. Additional context on AI reviews
4. **FINAL** submissions that already have one review

### When to Step Back

- If you're too busy, it's okay to skip a review cycle
- Quality over quantity—don't rush reviews
- If you're not familiar with the tech stack, let someone else review
- Communicate with other reviewers to avoid duplicate effort

---

## How to Become a Reviewer

Thank you for considering volunteering your time and expertise to help other engineers grow! Here's how to join:

### Requirements

- **2+ years of relevant experience** (professional or significant personal projects)
- **Demonstrated expertise** in at least one technology stack
- Experience with code reviews or mentoring (preferred but not required)
- Commitment to our Code of Conduct and these guidelines
- Availability to review at least 2-3 submissions per month

### Application Process

1. **Create an Issue**

   - Title: `Reviewer Volunteer - [Your Name]`
   - Assign: `@engineeringwithtemi` (Temiloluwa Ojo) + any existing reviewer

2. **In the Issue Description, Include:**

```markdown
## Reviewer Application

### About Me

**Name:** [Your Name]
**GitHub:** @your-username
**Location/Timezone:** [Optional, helps with coordination]

### Experience

**Years of Experience:** [Number]
**Primary Expertise:** [Languages/Technologies you're strongest in]
**Secondary Skills:** [Other areas you're comfortable reviewing]

**Professional Background:**
[Brief overview - current role, relevant experience, notable projects]

### Why I Want to Review

[Your motivation - give back to community, practice mentoring, stay sharp, etc.]

### Availability

**Estimated time commitment:** [e.g., "3-5 hours per month", "2-3 reviews per month"]
**Preferred review types:** [DRAFT, FINAL, both, specific months/projects]
**Technologies I'm excited to review:** [Languages/frameworks you want to focus on]

### Code Review Experience

[Any prior review/mentoring experience - work, open source, teaching, etc.]

### Additional Info

[Anything else we should know]

### Acknowledgment

- [ ] I have read the CODE_OF_CONDUCT.md
- [ ] I have read the REVIEW_GUIDELINES.md
- [ ] I commit to respectful, constructive, and helpful reviews
- [ ] I understand this is a volunteer position
```

3. **Wait for Approval**

   - We'll review your application
   - May ask follow-up questions
   - Typically respond within 3-5 days

4. **Once Approved:**
   - Added as repository collaborator with **write** access
   - Added to CODEOWNERS for your areas of expertise
   - Invited to reviewer Discord/Skool channel
   - Can start reviewing submissions!

### Reviewer Onboarding

When approved, you'll receive:

- Access to reviewer-only channels
- Introduction to other reviewers
- Guidance on using GitHub review features
- Template for your first review (optional)
- Assignment to upcoming month based on your expertise

---

## Recognition & Appreciation

We deeply appreciate our reviewers! Here's how we recognize your contributions:

- **Public acknowledgment** in monthly project wraps
- **Reviewer spotlight** featuring outstanding reviewers
- **Contributor badge** on your profile (coming soon)
- **LinkedIn recommendation** available upon request (after 3+ months)
- **Reference for future opportunities** if needed
- **Community reputation** as a trusted mentor

---

## Questions or Concerns?

- **Technical questions about a submission:** Ask in the PR thread
- **Guideline questions:** Create a GitHub Discussion or ask in reviewer channel
- **Conflicts or issues:** Contact @engineeringwithtemi privately
- **Suggestions for improvement:** We're always learning! Share your ideas

---

## Quick Reference

### Before You Review

- [ ] Read the project brief for this month
- [ ] Check if submission has existing reviews
- [ ] Review the Code of Conduct
- [ ] Allocate 20-30 minutes

### During Review

- [ ] Start with positives
- [ ] Focus on 3-5 key areas
- [ ] Include links to resources
- [ ] Ask clarifying questions
- [ ] Use clear, kind language
- [ ] Provide specific, actionable feedback

### After Review

- [ ] Submit your review
- [ ] Mark yourself as having reviewed (if tracking)
- [ ] Follow up on participant questions
- [ ] Celebrate their effort!

---

## Thank You!

Your time, expertise, and kindness make EWT2026 possible. Every review you provide helps someone become a better engineer. That's powerful. Thank you for being part of this journey! 🚀

---

**Questions? Feedback on these guidelines?**
Open a Discussion or reach out to @engineeringwithtemi
