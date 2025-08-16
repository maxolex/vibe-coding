# Ultimate Vibe Coding Guide for Full-Stack Applications V1.0
**Author:** Maxolex  
**Creation Date:** August 2025  
**Last Update:** August 2025  

---

## 🎯 Introduction: Vibe Coding for Full-Stack Applications

Vibe Coding transforms how you develop complete applications by intelligently orchestrating AI to create modular, maintainable, and professional code. This approach enables you to build complex full-stack applications while maintaining control over the architecture.

### Essential Tools
- **Gemini 2.5 Pro Thinking**: For architecture and planning (1M token context)
- **Cursor with Claude Opus 4.1 Thinking**: For implementation and deep reasoning
- **Framework Documentation**: Official documentation for your tech stack

**⚠️ Fundamental Principle:** *Architectural planning is EVERYTHING.* Never let AI plan autonomously - you must direct every architectural decision.

---

## 🌍 Phase 0: Language and Internationalization Configuration

### Setting AI Response Language

#### 🔥 **PROMPT #0 - AI Language Configuration**
```markdown
<think>
I need to configure the AI's response language and consider internationalization needs:
1. Determine the primary development language for code/comments
2. Set the natural language for AI responses
3. Define documentation language standards
4. Consider team's language preferences
5. Plan for user-facing content languages
6. Establish naming conventions (English vs local)
7. Set up translation workflow if needed
8. Define language fallback strategies

[Continue reasoning for 500+ words about language choices and their implications...]
</think>

Configure your AI assistant's language preferences:

1. **AI Response Language**: [English/French/Spanish/German/etc.]
   - All explanations and documentation in: [LANGUAGE]
   - Error messages and logs in: [LANGUAGE]
   - Comments in code in: [LANGUAGE]

2. **Code Standards**:
   - Variable/function names: [English/Local Language]
   - Database field names: [English/Local Language]
   - API endpoint naming: [English/Local Language]

3. **Documentation Language**:
   - Technical docs: [LANGUAGE]
   - User docs: [LANGUAGE]
   - Code comments: [LANGUAGE]

Please confirm these settings and maintain them throughout our session.
```

### Application Language Configuration

#### 🔥 **PROMPT #0.1 - Internationalization Planning**
```markdown
<think>
For implementing internationalization (i18n), I must consider:
1. Target markets and their languages
2. Right-to-left (RTL) language support needs
3. Date, time, and number formatting by locale
4. Currency and unit conversions
5. Translation management system
6. Dynamic content translation strategy
7. SEO implications for multiple languages
8. Performance impact of loading translations

[Detailed analysis of i18n requirements - 500+ words...]
</think>

Define the application's language requirements:

1. **Default Application Language**: [e.g., English]

2. **Supported Languages** (if multi-language):
   - Primary: [e.g., English - en]
   - Secondary: [e.g., French - fr, Spanish - es, German - de]
   - Future planned: [List languages]

3. **Internationalization Strategy**:
   - Frontend i18n library: [e.g., react-i18next, vue-i18n]
   - Backend i18n approach: [e.g., accept-language header]
   - Translation management: [e.g., JSON files, CMS, translation service]
   - Dynamic content handling: [Database fields per language]

4. **Localization Requirements**:
   - Date/Time formats: [ISO 8601 / locale-specific]
   - Number formats: [Decimal separators by locale]
   - Currency display: [Symbol position and format]
   - RTL support needed: [Yes/No]

Create `i18n-config.md` in memory-bank/ with these specifications.
```

---

## 📋 Phase 1: Setup and Planning

### 1. Product Requirements Document (PRD)

#### 🔥 **PROMPT #1 - PRD Creation with Reasoning**
```markdown
<think>
I need to create a comprehensive requirements document for a [YOUR APP TYPE] application.
Let me analyze the needs step by step:

1. Define the problem the application solves
2. Identify target users and their needs
3. List essential features (MVP)
4. Define technical and business constraints
5. Establish measurable success criteria
6. Anticipate main technical challenges
7. Propose base architecture
8. Define development phases

[Continue reasoning for at least 500 words...]
</think>

Create a detailed Product Requirements Document (PRD) in Markdown for my application [DESCRIPTION].
The application must [MAIN OBJECTIVES].

Structure the document with:
- Executive Summary
- Objectives and KPIs
- Detailed User Stories
- MVP vs. Future Features
- Technical Constraints
- Acceptance Criteria
- Risks and Mitigations
- Internationalization Requirements (if applicable)

Name the file: product-requirements.md
```

### 2. Technical Architecture and Stack

#### 🔥 **PROMPT #2 - Tech Stack Selection with Analysis**
```markdown
<think>
To choose the best technical stack, I must analyze:

1. Application nature (real-time, CRUD, analytics, etc.)
2. Required scalability (user count, data volume)
3. Team skills and learning curve
4. Ecosystem and community support
5. Performance and optimization needs
6. Infrastructure and maintenance costs
7. Security and compliance requirements
8. Required third-party integrations
9. Internationalization support in frameworks

[In-depth analysis of at least 500 words...]
</think>

Based on the PRD (product-requirements.md), recommend the optimal technical stack.

Analyze and justify your choices for:
- Frontend: Framework, state management, UI library, i18n support
- Backend: Framework, architecture (REST/GraphQL/gRPC)
- Database: SQL vs NoSQL, specific choice
- Authentication: Solution and strategy
- Infrastructure: Cloud provider, containerization
- Testing: Frameworks and strategy
- CI/CD: Pipeline and tools
- Monitoring: Logs, metrics, alerting
- Internationalization: Libraries and services

For each choice, provide:
1. Why this technology
2. Alternatives considered
3. Trade-offs accepted
4. Official documentation URL
5. I18n/L10n capabilities

Save as: tech-stack-analysis.md
```

### 3. Cursor Rules Configuration

#### 🔥 **PROMPT #3 - Rules Generation with Best Practices**
```markdown
In Cursor, use /Generate Cursor Rules command with files:
- product-requirements.md
- tech-stack-analysis.md
- i18n-config.md

Then modify rules to include these MANDATORY rules marked as "Always":

# CRITICAL RULES (Always)
- Always read memory-bank/@architecture.md before writing code
- Always read memory-bank/@database-schema.md for any DB operation
- Always read memory-bank/@api-contracts.md for endpoints
- Always read memory-bank/@i18n-config.md for language settings
- Always use <think></think> methodology for complex decisions
- Always write tests before implementation (TDD)
- Always document changes in progress.md
- Always use configured language for comments and documentation: [LANGUAGE]

# ARCHITECTURE RULES (Always)
- Strictly separate concerns (MVC/MVVM/Clean Architecture)
- One file per component/service/controller
- Name files following convention: [feature].[type].[ext]
- Use dependency injection
- Implement Repository pattern for data access
- Implement i18n from the start if multi-language

# QUALITY RULES (Conditional)
- TypeScript strict mode mandatory
- ESLint + Prettier configuration
- Minimum 80% code coverage
- Document all public functions in [CONFIGURED LANGUAGE]
- Handle all errors explicitly
- Externalize all user-facing strings for i18n
```

### 4. Detailed Implementation Plan

#### 🔥 **PROMPT #4 - Plan with Testing Methodology**
```markdown
<think>
To create an effective implementation plan, I must:

1. Decompose the application into independent modules
2. Identify dependencies between modules
3. Define optimal development order
4. Create tests validating each step
5. Plan user validation points
6. Anticipate technical difficulties
7. Establish measurable milestones
8. Define "done" criteria for each step
9. Plan i18n implementation strategy

[Detailed reasoning of 500+ words...]
</think>

Create a detailed implementation plan based on:
- product-requirements.md
- tech-stack-analysis.md
- i18n-config.md
- Configured Cursor rules

Structure each step as:

## Step X: [Descriptive Name]
**Objective:** [What will be accomplished]
**Prerequisites:** [Required previous steps]
**Instructions:**
1. [Specific action]
2. [Specific action]
**Validation Tests:**
- [ ] Unit test: [Description]
- [ ] Integration test: [Description]
- [ ] E2E test: [Description]
- [ ] I18n test: [All strings externalized]
**Success Criteria:** [Measurable and observable]
**Documentation to Update:** [Affected files]

Organize in phases:
1. Base Infrastructure (DB, Auth, Config, I18n setup)
2. Core API (CRUD, Validation, Errors)
3. Frontend Foundation (Routing, State, UI, Language Switcher)
4. MVP Features (by priority)
5. Optimizations and Polish

Save: implementation-plan.md
```

### 5. Memory Bank Configuration

```bash
project-root/
├── memory-bank/
│   ├── @architecture.md          # Global architecture (Always rule)
│   ├── @database-schema.md       # Complete DB schema (Always rule)
│   ├── @api-contracts.md         # API contracts (Always rule)
│   ├── @i18n-config.md          # I18n configuration (Always rule)
│   ├── product-requirements.md   # PRD
│   ├── tech-stack-analysis.md    # Technical analysis
│   ├── implementation-plan.md    # Detailed plan
│   ├── progress.md               # Step tracking
│   ├── decisions.md              # ADR (Architecture Decision Records)
│   ├── translations/             # Translation files
│   │   ├── en.json              # English translations
│   │   ├── fr.json              # French translations
│   │   └── [locale].json        # Other languages
│   └── framework-docs/           # Framework documentation
│       ├── frontend-framework.md
│       ├── backend-framework.md
│       ├── database-orm.md
│       └── i18n-library.md
└── .cursor/
    └── rules                      # Configured Cursor rules
```

---

## 🚀 Phase 2: Implementation with Vibe Coding

### Plan Validation and Clarification

#### 🔥 **PROMPT #5 - Validation with Deep Questions**
```markdown
<think>
Before starting implementation, I must ensure perfect understanding of:
1. Overall architecture and chosen patterns
2. Naming conventions and file structure
3. State management strategy
4. Security patterns to implement
5. Error handling strategy
6. Performance requirements
7. Deployment constraints
8. External dependencies
9. I18n implementation approach

[500+ word analysis of the plan...]
</think>

Carefully read all documents in /memory-bank.

Analyze implementation-plan.md and ask me up to 10 critical questions to clarify:
- Technical ambiguities
- Non-explicit architecture decisions
- Preferred code patterns
- Undocumented conventions
- Edge cases to handle
- I18n/L10n specific requirements

After my answers, update implementation-plan.md with these clarifications.
```

### First Implementation Prompt

#### 🔥 **PROMPT #6 - Implementation with TDD and Documentation**
```markdown
<think>
To implement Step 1, I must:
1. Understand the exact objective of this step
2. Identify all files to create/modify
3. Define interfaces and contracts
4. Write tests first (TDD)
5. Implement minimal code to pass tests
6. Refactor for quality
7. Document architecture
8. Validate success criteria
9. Ensure i18n compliance

[Detailed implementation reasoning...]
</think>

Read all documents in /memory-bank, especially @architecture.md, @database-schema.md, and @i18n-config.md.

Proceed with Step 1 of the implementation plan following this methodology:

1. **Write tests first** (TDD):
   - Unit tests for business logic
   - Integration tests for interactions
   - E2E tests if applicable
   - I18n tests for string externalization

2. **Implement code**:
   - Minimal code to pass tests
   - Strict adherence to defined patterns
   - Complete error handling
   - All strings externalized for i18n

3. **Document**:
   - Update @architecture.md with new components
   - Add new endpoints in @api-contracts.md
   - Document schema in @database-schema.md if modified
   - Update translation keys in translations/

4. **Validate**:
   - Run all tests and display results
   - Verify step success criteria
   - Confirm i18n compliance

Do NOT proceed to Step 2 before my complete validation.
```

### Continuous Implementation Workflow

#### 🔥 **PROMPT #7 - Incremental Progress with Context**
```markdown
<think>
Before continuing, I must:
1. Review progress.md to understand completed work
2. Verify current architecture state
3. Identify next step dependencies
4. Anticipate impacts on existing code
5. Plan necessary regression tests
6. Consider possible optimizations
7. Verify consistency with established patterns
8. Document decisions made
9. Check i18n consistency

[500+ word contextual analysis...]
</think>

Browse all files in memory-bank/, especially:
- progress.md to understand completed work
- @architecture.md for current system state
- @database-schema.md for data structures
- @api-contracts.md for interfaces
- @i18n-config.md for language settings

Proceed with Step [N] by:
1. Respecting patterns established in previous steps
2. Writing tests first
3. Verifying non-regression of existing features
4. Documenting all architectural changes
5. Ensuring i18n compliance for new features
6. Updating progress.md with:
   - What was implemented
   - Technical decisions made
   - Challenges encountered and solutions
   - Suggested future improvements

Display test results before completing.
```

---

## 🔧 Phase 3: Framework Documentation Integration

### Documentation Setup

#### 🔥 **PROMPT #8 - Extracting Relevant Documentation**
```markdown
For each framework/library in our stack, create a condensed documentation file:

1. Visit [FRAMEWORK]'s official documentation
2. Use RepoPrompt or similar tool to extract:
   - Recommended patterns
   - Core APIs we'll use
   - Best practices
   - Common pitfalls to avoid
   - Relevant code examples
   - I18n/L10n features and setup

3. Save in memory-bank/framework-docs/[framework]-essentials.md

Structure:
```markdown
# [Framework] Essentials for Our Project

## Core Concepts
[Key concepts needed]

## Patterns We Use
[Specific patterns to implement]

## API Reference
[APIs we'll use]

## I18n/L10n Support
[Framework's internationalization features]

## Best Practices
[Rules to follow]

## Common Pitfalls
[Errors to avoid]

## Code Examples
[Relevant examples for our case]
```
```

### Documentation Usage

Add this Cursor rule (Always):
```
# Before implementing a feature using [Framework]:
- Consult memory-bank/framework-docs/[framework]-essentials.md
- Verify recommended patterns
- Use examples as reference
- Check i18n best practices for the framework
```

---

## 🐛 Phase 4: Debugging and Optimization

### Structured Debugging

#### 🔥 **PROMPT #9 - Bug Analysis and Resolution**
```markdown
<think>
To resolve this bug, I must:
1. Understand expected vs. observed behavior
2. Identify stack trace and context
3. Form hypotheses about the cause
4. Trace data flow
5. Identify failure point
6. Propose possible solutions
7. Evaluate each solution's impact
8. Choose the best approach
9. Consider i18n-related issues

[Detailed bug analysis of 500+ words...]
</think>

I encountered this error:
[PASTE ERROR OR SCREENSHOT]
Context:
- Action performed: [DESCRIPTION]
- Expected result: [DESCRIPTION]
- Actual result: [DESCRIPTION]
- UI Language when error occurred: [LANGUAGE]

Analyze the problem by:
1. Explaining the probable cause
2. Proposing 2-3 solutions with trade-offs
3. Implementing the optimal solution
4. Adding tests to prevent regression
5. Documenting the fix in decisions.md
```

### Progressive Optimization

#### 🔥 **PROMPT #10 - Optimization with Metrics**
```markdown
<think>
To optimize this part of the application:
1. Identify current bottlenecks
2. Measure baseline performance
3. Analyze usage patterns
4. Propose specific optimizations
5. Evaluate ROI of each optimization
6. Implement by priority
7. Measure improvement
8. Document changes
9. Consider i18n impact on performance

[500+ word optimization analysis...]
</think>

Analyze performance of [FEATURE/COMPONENT] and propose optimizations.

Consider:
- Frontend performance (bundle size, rendering, lazy loading, translation loading)
- Backend performance (queries, caching, indexing)
- Network performance (compression, CDN, pagination)
- I18n performance (lazy load translations, optimize bundles per locale)
- Perceived UX (skeleton screens, optimistic updates)

For each optimization:
1. Current metric
2. Target goal
3. Optimization technique
4. Estimated impact
5. Implementation complexity

Implement top 3 optimizations with best ROI.
```

---

## 🎨 Phase 5: Advanced Features

### Adding Complex Features

#### 🔥 **PROMPT #11 - Feature Planning with Impact Analysis**
```markdown
<think>
To add this new feature:
1. Analyze impact on existing architecture
2. Identify necessary modifications
3. Evaluate regression risks
4. Plan progressive integration
5. Define necessary tests
6. Estimate required effort
7. Propose implementation plan
8. Anticipate edge cases
9. Plan i18n for new UI strings

[500+ word impact analysis...]
</think>

I want to add [FEATURE DESCRIPTION].

Create a feature-implementation-plan.md that:
1. Analyzes impact on current architecture
2. Lists components to create/modify
3. Defines implementation steps
4. Specifies required tests
5. Identifies risks and mitigations
6. Proposes feature flag strategy if needed
7. Plans i18n for new content
8. Estimates development time

Use the same structured format as implementation-plan.md.
```

---

## 💡 Advanced Tips and Best Practices

### State and Data Management
```markdown
# For complex applications, maintain:
memory-bank/
├── @state-diagram.md      # Application state diagram
├── @data-flow.md          # Data flow between components
├── @event-catalog.md      # System events catalog
├── @error-codes.md        # Error codes reference
└── @translation-keys.md   # All i18n keys catalog
```

### Testing Strategy
- **Unit Tests**: For all business logic
- **Integration Tests**: For module interactions
- **E2E Tests**: For critical user journeys
- **Performance Tests**: For critical endpoints
- **Security Tests**: For authentication and authorization
- **I18n Tests**: For proper string externalization and locale switching

### Recommended Git Workflow
```bash
# Before each new step
git add . && git commit -m "feat: Complete Step [N] - [Description]"

# Create branch for complex features
git checkout -b feature/[feature-name]

# In case of issues
git stash  # Save temporarily
git reset --hard HEAD~1  # Revert to previous commit
```

### Complementary Tools
- **Frontend Design**: v0, Lovable, or Bolt.new for prototyping
- **API Testing**: Postman or Insomnia with shared collections
- **Database Design**: dbdiagram.io for schema visualization
- **Architecture Diagrams**: draw.io or Mermaid
- **API Documentation**: Swagger/OpenAPI
- **Monitoring**: Sentry for errors, DataDog for metrics
- **Translation Management**: Lokalise, Crowdin, or POEditor
- **I18n Testing**: Pseudolocalization tools

---

## ❓ Advanced FAQ

**Q: How to manage database migrations?**
**A:** Maintain a `migrations/` folder with numbered scripts. Document each migration in `memory-bank/@database-schema.md` with the reason for change.

**Q: How to implement microservices architecture?**
**A:** Create an `implementation-plan.md` per service. Use a shared `memory-bank/` folder for inter-service contracts and a specific one per service for internal details.

**Q: How to manage environments (dev/staging/prod)?**
**A:** Use `.env.[environment]` files and document differences in `memory-bank/environments.md`. Implement feature flags for progressive deployments.

**Q: How to optimize for SEO and Core Web Vitals?**
**A:** Create an `seo-implementation.md` with specific steps for SSR/SSG, dynamic meta tags, structured data, and performance optimizations. Include hreflang tags for multi-language. Measure with Lighthouse at each step.

**Q: How to implement CI/CD pipeline?**
**A:** Start with `cicd-implementation.md` defining steps: linting → tests → build → deploy. Use GitHub Actions or GitLab CI with progressive workflows. Include i18n validation in the pipeline.

**Q: How to handle multi-language content in database?**
**A:** Choose between: 1) Separate columns per language, 2) Translation tables with foreign keys, or 3) JSON columns with language keys. Document choice in `@database-schema.md`.

---

## 🚀 Quick Reference Commands

```markdown
# Starting a new project
"Create a PRD for [APP TYPE] with <think> reasoning of 500+ words"

# Language configuration
"Set AI responses in [LANGUAGE] and configure i18n for [LANGUAGES]"

# Technical analysis
"Analyze and recommend optimal stack with <think> detailed justification"

# Implementation
"Implement Step [N] with TDD, update all memory-bank/ docs"

# Debugging
"<think> Analyze this error [ERROR] and propose 3 solutions with trade-offs"

# Optimization
"Profile and optimize [COMPONENT] with before/after metrics"

# Documentation
"Update @architecture.md with this session's changes"

# I18n
"Extract all hardcoded strings and create translation keys"
```

---

**Final Note:** The success of Vibe Coding relies on your ability to direct AI with precise and structured prompts. Always use the `<think>` methodology for important decisions and maintain rigorous documentation in your memory-bank. The quality of your application will be directly proportional to the quality of your planning and prompts.

🎯 **Reminder:** Every complex prompt must contain at least 500 words of reflection within `<think></think>` tags to ensure thorough analysis and thoughtful decisions.

🌍 **Language Tip:** Configure your preferred language settings at the start of each session to ensure consistent communication and documentation throughout your development process.
