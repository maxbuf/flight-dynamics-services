# How to onboard

- **Rule of thumb:** Expect to be a solid contributor after 3 months
- Prioritize up-to-date docs, async Q&A channels, and low-risk tasks
- Build trust with 1-2 small, dependable PRs daily
- Adopt "cautious curiosity": Learn via small, observable changes
- PR Rules: Atomic changes, tests/migrations, feature flags, clear descriptions (trade-offs, issue links)

## Table of contents

- []()

## First 5 days

_Goal: Get the environment running and land your first "hello world" change._

## First 30 days
## First 90 days

For each, goals and high-level targets

---

## Contribute fast
## Understand the codebase
## Understand the system design

---

## Tech stack

**Python**

- [ ] [https://docs.python-guide.org](https://docs.python-guide.org)
- [ ] 

**Django**

- [ ] [https://roadmap.sh/django](https://roadmap.sh/django)
- [ ] [https://docs.djangoproject.com/en/6.0/](https://docs.djangoproject.com/en/6.0/)
- [ ] [https://docs.djangoproject.com/en/6.0/topics/](https://docs.djangoproject.com/en/6.0/topics/)
- [ ] [https://docs.djangoproject.com/en/6.0/ref/applications/](https://docs.djangoproject.com/en/6.0/ref/applications/)
- [ ] [https://docs.djangoproject.com/en/6.0/howto/](https://docs.djangoproject.com/en/6.0/howto/)
- [ ] [https://docs.djangoproject.com/en/6.0/ref/](https://docs.djangoproject.com/en/6.0/ref/)

**asyncio**

- [] []()

**graphene**

- [] []()

**pytest**

- [ ] [https://docs.pytest.org/en/stable/explanation/index.html](https://docs.pytest.org/en/stable/explanation/index.html)
- [ ] [https://docs.pytest.org/en/stable/how-to/index.html](https://docs.pytest.org/en/stable/how-to/index.html)
- [ ] [https://programmingmylife.com/2025-02-07-pytest-a-practical-guide.html](https://programmingmylife.com/2025-02-07-pytest-a-practical-guide.html)
- [ ] [https://realpython.com/pytest-python-testing/](https://realpython.com/pytest-python-testing/)
- [ ] [https://realpython.com/pytest-python-testing/](https://realpython.com/pytest-python-testing/)
- [ ] [https://github.com/noahgift/pytest-tips-tricks](https://github.com/noahgift/pytest-tips-tricks)
- [ ] 

**mypy**

- [ ] [https://mypy.readthedocs.io/en/stable/getting_started.html](https://mypy.readthedocs.io/en/stable/getting_started.html)

**C++**

- [] []()

**NATS**

- [] []()

**InfluxDB**

- [] []()

---

## First 5 days

_Goal: Get the environment running and land your first "hello world" change._

- [ ] **Access & setup:**
  - [ ] Provision all tools and their access
  - [ ] Set up recurring 1:1s with your manager (day 1)
  - [ ] Identify your onboarding buddy/mentor and schedule an intro 1:1
- [ ] **Environment validation:**
  - [ ] Can I run the service and its tests locally in under _x_ minutes?
  - [ ] Document any "tribal knowledge" or missing steps in the documentation
- [ ] **First commit:**
  - [ ] Fix a small bug, doc typo, or linting issue
  - [ ] Run the full test suite
  - [ ] Open a PR and request review
  - [ ] Update the related ticket in the bug tracking system
  - [ ] Follow the change through to deployment/production

## First 30 days

_Goal: Understand how the team moves from idea to production_

- [ ] **Team & domain:**
  - [ ] "30-Minute intro" circuit: Ask your manager for a list of names
  - [ ] For each person:
    - 25 mins: Let them talk. Ask: _"What is the motivation behind our work? Where does this fit in the bigger goals? Who knows the most about X?"_
    - 3 mins: Ask: _"What are the biggest challenges the team has right now?"_
    - 2 mins: Ask: _"Who else should I talk to?"_ (Repeat until no new names appear)
  - [ ] Read documentation/quick start guides for the specific versions of the tech stack (e.g., Django, GraphQL, NATS, InfluxDB docs)
  - [ ] Focus on the business value: What is the customer actually trying to achieve?
- [ ] **Codebase:**
  - [ ] Map the project:
    - Run `cloc . --by-file` to find the largest, most complex files
    - Run `git log --since='1 week ago' --name-only --pretty="" | sort | uniq` to find the most updated files in the last 7 days
  - [ ] Trace the flow:
    - Pick one API call/request and trace it end-to-end through every layer
    - Identify core abstractions and design patterns used
- [ ] **Infrastructure:**
  - [ ] Review the CI config file (this is the "source of truth" for deployment)
  - [ ] Identify where runtime errors and alerts are concentrated
  - [ ] Which modules have the fewest tests or most bugs?

## First 60 days

_Goal: Increase independence and start contributing to team culture_

- [ ] **Get involved:**
  - [ ] Shadowing: Pair program; don't just watch the code, note their debugging strategies and which files they keep open
  - [ ] Incident response: Stay active in incident channels and pay attention to how the team responds to production alerts
- [ ] The "weekly musing":
  - Every Monday, take 1 hour to review your personal notes
  - Organize personal notes
  - Identify "Chesterton’s Fences" (ugly code that exists for a historical reason)
- [ ] **Contribute:**
  - [ ] Stabilize (60% of time): Fix small bugs, improve flaky tests, and ship 1–2 low-risk PRs daily
  - [ ] Improve (30% of time): Address recurrent pain points. Add logs/telemetry to dark areas of the code
  - [ ] 

---

## Example "30/60/90"

### First week

### First 30/60 days

- Goal: Working local setup, several small PRs merged, basic end-to-end understanding
- Pair program: Ask questions about their workflow, note which files they frequently access, get to know their debugging strategies
- Understand the "why": Dig deep into the motivation behind tasks; understand the business context and technical reasoning; ask (seemingly basic questions)
- Monitor team communications: Stay active in ncident response discussions, pay special attention to production alerts and how the team responds to them
- Create personal documentation: Maintain a living document of your discoveries, questions, and insights; document important code paths, architectural decisions, and system interfaces as you encounter them
- Build technical maps: Create diagrams of system architecture, data flows, and entity relationships; start with high-level “black boxes” and gradually fill in the details as your understanding grows
- Maintain a command cheat sheet: Keep track of useful commands, scripts, and workflows you discover; include context about when and why to use them
- Gather information on the domain: Important for understanding of a codebase is to have a deep understanding of the domain
- Write internal guides: Once you learn something new, document it for the next person
- Contribute to official documentation: When you find gaps in the existing documentation, take the initiative to improve it
- Regularly reflect on your learnings:
  - Can you describe the system in a few concise sentences?
  - How does it interact with adjacent systems?
  - What surprised you most during the learning process?
  - What aspects remain unclear?
 - Code base discovery template: [https://gist.github.com/brittanyellich/262d8d94d8b80cfd9ec5dad677d2fef8](https://gist.github.com/brittanyellich/262d8d94d8b80cfd9ec5dad677d2fef8)
 - Documatic code search engine: [https://marketplace.visualstudio.com/items?itemName=Documatic.documatic](https://marketplace.visualstudio.com/items?itemName=Documatic.documatic)
 - GitLens code authorship visualization: [https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)

### First 90 days

- Goal: Ownership of a service or subsystem, contributions to reducing debt, credible proposals for larger improvements
- Learn and stabilize (60%): Run, trace code, fix small bugs, improve tests, ship small PRs
- Improve (30%): Address recurrent pain points, add monitoring, incrementally refactor with tests
- Lead (10%): Propose larger changes, design documents, or process/tooling improvements backed by data and prototypes

## Credits

- [https://www.developing.dev/p/how-to-onboard](https://www.developing.dev/p/how-to-onboard)
- [https://boz.com/articles/career-cold-start](https://boz.com/articles/career-cold-start)
- [https://github.blog/developer-skills/application-development/how-github-engineers-learn-new-codebases/](https://github.blog/developer-skills/application-development/how-github-engineers-learn-new-codebases/)
- [https://stackoverflow.com/beta/discussions/77469060/how-do-you-quickly-learn-a-new-projects-large-codebase](https://stackoverflow.com/beta/discussions/77469060/how-do-you-quickly-learn-a-new-projects-large-codebase)
- [https://www.quora.com/How-do-you-deal-with-a-big-existing-code-base-when-you-are-new-to-the-team](https://www.quora.com/How-do-you-deal-with-a-big-existing-code-base-when-you-are-new-to-the-team)
- [https://news.ycombinator.com/item?id=19924100](https://news.ycombinator.com/item?id=19924100)
- [https://stackoverflow.com/questions/215076/whats-the-best-way-to-become-familiar-with-a-large-codebase](https://stackoverflow.com/questions/215076/whats-the-best-way-to-become-familiar-with-a-large-codebase)
- [https://stackoverflow.com/questions/214605/the-best-way-to-familiarize-yourself-with-an-inherited-codebase](https://stackoverflow.com/questions/214605/the-best-way-to-familiarize-yourself-with-an-inherited-codebase)

---

**Checklist**

- [ ] Can I run the app and tests locally in under _x_ minutes?
- [ ] Where are the runtime errors and alerts concentrated?
- [ ] Which modules have the fewest tests and most bugs?
- [ ] Who approves changes for each area?
- [ ] What are the deployment and rollback steps?

---

**Effective learning**

- Read from public APIs inward, not file-by-file
- Identify core abstractions and variant implementations
- Use IDE + structure map: call hierarchy, find usages, and type hints
- Use tests as documentation (tests often reveal intended behavior)
- Add tests when behavior is ambiguous
- Read relevant commits and PR discussions to learn why things were implemented a certain way

**Contributing**

- Make atomic, well-scoped changes
- One logical change per PR, clear description, and link to related issues or design docs
- Include tests and migration steps
- Use feature flags and canary releases
- Reduce blast radius and enable gradual rollouts
- Respect the review process
- Incorporate feedback promptly and explain trade-offs in PR descriptions
- Make improvements as you go:
  - Run a code prettifier to format the code nicely
  - Change variable names to make them clearer (using a refactoring tool)
  - Reducing clutter in the code: Commented out code, meaningless comments, pointless variable initializations and so on
  - Change the code to use current code conventions
  - Start to extract functionality into meaningful routines
  - Start to add tests where possible
  - Get rid of magic numbers
  - Reduce duplication where possible

**Refactoring**

- Add tests around the area
- Write benchmarks for performance-sensitive code, measure before/after
- Break work into incremental, reversible steps
- Replace modules piecewise, keep compatibility layers, and avoid cross-cutting changes in one PR
- Define success criteria (performance, test coverage, clarity, and maintainability metrics)

**Common pitfalls**

- Don’t refactor blindly: large cosmetic changes make review and blame hard
- Don’t assume intentions: historical constraints often explain ugly designs
- Don’t shortcut tests or CI: they’re the safety net for a complex system
- Don’t push big changes without stakeholder alignment and rollout plan

---

# How to onboard

- Set expectations with your new manager from the start
- Setup 1:1s day one

## Table of contents

- [Contribute fast](#contribute-fast)
- [Learn about the team](#learn-about-the-team)
- [Learn about the codebase](#learn-about-the-codebase)
- [Learn about the systems](#learn-about-the-systems)
- [Example "5/30/90" plan](#example-53090-plan)
  - [First 5 days](#first-5-days)
  - [First 30 days](#first-30-days)
  - [First 90 days](#first-90-days)
- [Open questions](#open-questions)

## Learn about the team

Find someone on the team: Ask for 30 minutes with them (ask manager for initial list of names)
- For the first 25 minutes: Ask them to tell you everything they think you should know
  - _Learning team direction: "What is the motivation behind your work?," "How does this fit into the team's plan?," "What wins are we expecting from this?"_
  - _Learning system design: "Where does your work fit into the overall system?," "What pieces does our team own?"_
  - _Learning who knows what: "Who knows the most about <area>?," "If <area> breaks, who knows how to fix it?"_
- Take notes, stop to ask about things you don't understand
- For the next 3 minutes: Ask about the biggest challenges the team has right now
- For the final 2 minutes: Ask who else you should talk to; write down every name they give you
- Repeat until you aren't given any new names

## Contribute fast

- **Goal: Get comfortable making changes**
- Immediate priority: Start landing code, get a high-level understanding of the codebase
- Add or improve onboarding docs, diagrams, and runbooks as you learn
- Cautious curiosity: Learn the system by using and changing it in small, observable increments
  - Get a general overview of how everything works together
  - Focus on small sections of code at a time, fully understanding how they work
  - Pick a feature to develop and learn as you go along
- Make notes as you go and take an hour (e.g., every Monday) to read through and arrange the notes from previous weeks
- Build trust through dependable contributions
- Scale improvements only after understanding the risks and adding safety nets
- Example approach: Land lots of low-risk changes (~1-2 per day) that improve the codebase

## Learn about the codebase

- Gain context fast:
  - Read available documentation carefully (for any documentation related to the team's stack [e.g., Django], make sure to read the documentation for the correct version)
  - Read `README`, `CONTRIBUTING`, design docs, architecture diagrams, recent PRs
  - Identify the tech stack and at least the major "quick start" quides or basic documentation (dive deeper as you work on the codebase)
  - Identify maintainers and owners: Code ownership files, PR authors, recent commit history
- Run the code:
  - Set up the local environment (git workflow, local storage, feature flags/configs)
  - Run the tests (note failing tests if any)
  - Write down pain points
  - Identify errors and alerts
  - Identify low-test/buggy modules
  - Understand how to deploy/rollback
- Understand the high-level areas:
  - Start with the different components
  - Then the subdirectories
  - Then the classes and their relations and so on
  - _Build an intuition for how everything works_
- Understand the functionality:
  - "What will this function return if I give it \<input\>?"
  - "How can I summarize what this method is made to do?"
  - "What are some potential gaps in the existing tests for this method?"
- Understand design patterns:
  - Identify the name of the design pattern that was implemented
  - Understand the intention and the meaning of abstractions
- Trace a single (API) call path end-to-end:
  - Follow the code through layers
  - Understand integration points
  - Add comments to explain what you think it might do
- Test and instrument:
  - Use logs, metrics, debuggers to observe runtime behavior
  - Add temporary log statements or breakpoints
- Analyize telemetry and metrics:
  - Study metrics to understand how the system behaves in production
  - What patterns emerge during peak usage
  - Which components require the most attention
- Explore through testing:
  - Make deliberate modifications to the code
  - Observe their effects
  - Write new tests to verify understanding
  - Intentionally break things (in development) to see how the system fails
  - _Build an intuitive understanding of the application’s boundaries and failure modes_

- Understand overall structure:
  - `cloc . --by-file` for big files/ratios
  - `git grep` key classes; review tests/CI for intent/deployment
  - Visualize the system

## Learn about the systems

- Understand the high-level: System boundaries, data model, deployment pipeline, configs
- "Which services work together?"
- "What goal are they trying to achieve?"
- "How are each of the services deployed/run/accessed?"
- "What's the development workflow for each?

## Example "5/30/90" plan

- 

### First 5 days

- **By day 5, learn to commit:** Basics of compiling, running, modifying, debugging, and committing changes
- Once code is up and running, push a small fix (go through every part of the process of committing that change):
  - Run the tests
  - Commit to the right branch
  - Request a PR
  - Update the bug tracking system
- Get your hands dirty:
  - Tackle small, well-defined tasks (e.g., fix docs or small bugs, flaky tests, linting issues, non-critical improvements)
  - Create small PRs to learn the review cycle
- Map technical debt and hotspots: Modules with high churn, most bugs, sparse tests, or ad-hoc patterns
- Document all the tribal knowledge you can


- High-level trace:
  - Services: Interactions, boundaries, goals, deploy/workflow
  - End-to-end API call: Logs/debugger/breakpoints; production metrics/telemetry
  - Break things in dev: Explore failure modes, add new tests
- Ship stuff: Docs, linting, flaky fixes

- [ ] Orientation meetings with manager, team, and HR
- [ ] Setup tools for your stack and access provisioning
- [ ] Documentation basics
- [ ] Schedule recurring 1:1s with manager (weekly 30 min check-ins): "What are my top 3 priorities for first 30 days?," "What are my role expectations?"
- [ ] Schedule intro 1:1 with buddy/mentor
- [ ] Contribute fast: Fix a small bug or doc tweak if access allows
- [ ] Create personal onboarding documentation tracking progress, questions
- [ ] Questions: "What are my day 1 priorities?," "Who is my onboarding buddy/mentor?"

### First 30 days
### First 90 days

## Open questions

- [ ] 

## First 30 days (Learn the process)

- [ ] Confirm learning, role clarity, and early progress
- [ ] 30 day review: 1:1 discussing role-level expectations vs. next-level goals (e.g., autonomy by day 90)
- [ ] Review documentation:
  - [ ] Company culture/values
  - [ ] Processes
  - [ ] Tools
- [ ] Shadow team members
- [ ] Complete initial training modules
- [ ] Small contributions: Low-stakes tasks with feedback
- [ ] "Am I on track for success metrics?," "Any blockers for ramp-up?"

- **By day 30, learn the process:** Go through one or two development cycles / sprints / units of development time
- Understand how different meetings are run, how estimates work, how completed work is reviewed, etc.
- Get a sense of the shipping process as well
- Know your repos
- Know your pipelines
- Know your process to take in work
- Know your backlog: Understand what decisions have already been discussed and why

## First 60 days (Learn to collaborate)

- [ ] Bi-weekly 1:1s: Feedback on early work, cross-team intros
- [ ] Lead small projects
- [ ] Deeper process documentation review
- [ ] Meet key stakeholders (ceremonial or functional)
- [ ] Questions: "How can I contribute more independently?," "Feedback on collaboration style?"

- Show your personality:
  - How do you approach work?
  - How can you make the team process better?
  - Do you document your "Today I learned"?
  - What's in your toolbelt?
  - What is your definition of done?

## First 90 days (Learn the code)

- [ ] Formal 90-day review 1:1: Full expectations recap, performance goals, next steps
- [ ] Present contributions (e.g., project recap)
- [ ] Update personal documentation/wiki
- [ ] Plan ongoing 1:1 cadence and development goals
- [ ] Questions: "What defines success at my level/next level?," "Opportunities for growth/impact?"

- **By dat 90, learn the code:** Learn enough of the code to be comfortable taking on larger tasks, and have a general idea of the strengths and weaknesses of the architecture
- "Know where to look"
- Do you follow through to get your ideas past the finish line?
- Do you leave work unfinished?
- Have you identified and proposed in a compelling way ways to improve our process/business?
- Do your day to day work and exceed expectations

---

- Rule of thumb: Expect solid contributions after 3 months
- Prioritize up-to-date docs, async Q&A channels, and low-risk tasks
- Adopt "cautious curiosity": Learn via small, observable changes
- Build trust with 1-2 dependable PRs daily

## Principles

- Mindset: Fresh eyes spot issues; note everything (mannerism, debt hotspots)
- Habits: Weekly 1hr note review (e.g., Mondays); living doc for rewrites/ideas
- PR Rules: Atomic changes, tests/migrations, feature flags, clear descriptions (trade-offs, issue links)
- Avoid Pitfalls: No blind refactors (mind Chesterton's Fence); always test/CI; no big changes without rollout plans

## First 30 days

### Team and process
### Codebase

- Goal: Deepen understanding; 5+ merged PRs; end-to-end intuition; team map
- Team:
  - 30min chats (manager list): 25min their world (direction/wins, system/owners, experts); 3min challenges; 2min next names. Repeat to exhaustion.
  - Pair: Workflows/files/debug; "why" on tasks/business.
  - Monitor: Chats, incidents/alerts.
- Codebase:
  - Summarize sections: Functions (input/output/gaps), patterns/abstractions.
  - Build: Diagrams (flows/relations); command cheatsheet; domain notes.
  - Explore: Tests/IDE (hierarchy/usages/hints); commits/PRs for "why".

Reflect: System desc? Interactions? Surprises/gaps?

Contribute: Templated issues (logs/fixes); docs/runbooks.
- 

## First 60 days

### Team and process
### Codebase

- Goal: Consistent PRs; basic ownership
- 

## First 90 days

### Team and process
### Codebase

- Goal: Own sub-system, advocate for improvements
- 

## Ongoing

- 

## Credits

- [https://medium.com/runkeeper-everyone-every-run/better-short-term-goals-for-new-engineering-hires-9a180f1ebc0f](https://medium.com/runkeeper-everyone-every-run/better-short-term-goals-for-new-engineering-hires-9a180f1ebc0f)
- [https://www.reddit.com/r/devops/comments/zdlrwk/whats_generally_in_your_306090_day_plan/](https://www.reddit.com/r/devops/comments/zdlrwk/whats_generally_in_your_306090_day_plan/)

---

0. Understanding a codebase:

0.0. Get to know the codebase:

0.0.0. Code distribution:

You can get an overall "idea" of the code distribution, or where the meat is, by using `cloc . --by-file`. This shows you a listing of files and their respective number of lines of code and comments. You instantly get an idea of the "big" files of the project you probably should get to know.

You also see the ratio comment/code and can start documenting and writing tests as you go. It will help you understand the project, and will be useful for everyone and in refactoring.

0.0.1. Structure:

0.0.1.0: Visualization

Drawing helps me. Conceptual blocks of the project. It can start as block names and boxes "Codec", "Streaming", "Persistence", "Dispatcher", etc.

Drawing on paper, whiteboard, etc. You can also use something like "Gliffy" to diagram for yourself and with someone when communicating. You can both change and make sure you're talking about the same thing.

And do it going down the abstraction scale. Higher abstractions to lower abstractions.

I also found a quick automatically generated "UML" diagram helps. I don't write them necessarily, but I use a tool that tells me about the structure of a project.

pyreverse for Python, scaladiagrams for Scala, are just a few examples that generate an image you can save and glance over after the `cloc` stuff.

0.0.1.1: Grep

I use `git grep` on the classes found in the biggest files I found with `cloc`. I can see how they "disseminate" through the project and how they get around and are used

0.0.1.2: Tests

I look at unit tests (if any) to get a sense on what the different parts do and how they're used. You learn a lot about "intent" from the tests if you're lucky to have them. I add tests as I get acquainted with the project.

If there's a CI config file, I'll check it out and it tells me how to deploy the project. It's often more accurate than the readme or else the builds would fail.

0.0.2: Musing

I maintain a separate "musing" file, sometimes called "refactoring" where I'll put a comment with the path to a file and the part it's about (say a function, or a class), and rewrite it. It is separate in the beginning as I don't know if the refactoring is relevant or if there's any Chesterton's Fence and I don't want to pollute the repo. It is my way of grappling with the code. Several rewrites. Often when I'm in a quiet place and my juices are flowing.

0.1. Taking notes for project:

One of my habits from the beginning was taking notes. I can now pull my notebooks at my current job and see the chronology (dated by month) and ordered. I can walk through the different difficulties, conceptualizations, drawings and schematics, sequence diagrams, re-architectures, refactorings, etc.

As you embark on your journey in a project, your fresh eyes are valuable. You're seeing a lot of what has become "normal" for other developers. Note  _everything_. The idiosyncratic build or deployment. Out of date documentation. Everything.

You can create well written issues that follow a template with expected and actual behaviors, screenshots, logs, stack traces, possible fixes, likely culprits, etc.. If your repo does not have a template for issue, propose one.

Write issues in a way to make them easier to fix for everyone. Your group can use your notes to rework an API or the user experience. You're also working to streamline future contributions for newcomers.

0.2. Knowledge Base

As your understanding of the project increases and you touch more and more parts, you can maintain a sort of knowledge base. It is highly likely that this knowledge base will serve as the project documentation if it has none.

1. Attention

1.1 Taking meeting notes:

Many meetings. Few actions. Everybody ends up talking about the same things and issues drag on forever. You can take notes and review them later. Write them up and send them to everyone. Check out minutes of meetings.

You can write the gist of what's said, and the  _action_  that must be taken, by whom, and when.

Taking these notes will help mitigate your distraction during the meeting as you can review them at your rythm.

```
  # Minutes of Meeting
  --------------------
  
  ## Date: 2019-03-25
  ## Place: BIGCorp HQ. City, State.
  
  ## Participants:
  
  ### BIGCorp:
  
    - John Doe (jd)
    - MeMyself I (mmi)
  
  ### OtherCorp:
    - Dilbert (db@othercorp.com)
    - Dogbert (dg@othercorp.com)
  
  
  ## Topics:
  
    - Scheduled information sending
    - Information flow
    - Architecture for Project X
  
  ## Details:
  
  OtherCorp has raised some issues for the timeline of Project X...
  Blah blah blah.
  
  ## Actions:
  
  ### BIGCorp:
  
  - [ ] @bc: Send project X estimates by 2019-03-28
  - [x] @bc: Send invoice and cheque for offices remodeling
  - [ ] @mmi: Add different schemes for user authentication
  - [ ] @mmi: Finalize migrations so we take into account user's timezone
  
  ### OtherCorp:
  
  - [ ] @oc: Expose API end points for user's identity verification
  - [ ] @oc: Cache the results of the most common queries


```

2. Skills

Understand the business value for the customer (what value is your code bringing to the customer, what are they trying to achieve).

Daily improvements. Reading good books and implementing what they contain. Writing the best code you can write. Reading the best code you can find. Consistent, continuous, relentless, improvement.

If you can be better than you were when the day started, and do that daily, good things may happen.

Constantly transfer the quality gains to the projects you're involved in (better documentation techniques, better patterns, less complexity, etc.)

Help others write better code by setting the example. Mentor newcomers to the project. Help write tools for everyone to use.


--- 



- Set expectations with your new manager from the start
- Setup 1:1s day one

## Table of contents

- [Contribute fast](#contribute-fast)
- [Learn about the team](#learn-about-the-team)
- [Learn about the codebase](#learn-about-the-codebase)
- [Learn about the systems](#learn-about-the-systems)
- [Example "5/30/90" plan](#example-53090-plan)
  - [First 5 days](#first-5-days)
  - [First 30 days](#first-30-days)
  - [First 90 days](#first-90-days)
- [Open questions](#open-questions)

## Learn about the team

Find someone on the team: Ask for 30 minutes with them (ask manager for initial list of names)
- For the first 25 minutes: Ask them to tell you everything they think you should know
  - _Learning team direction: "What is the motivation behind your work?," "How does this fit into the team's plan?," "What wins are we expecting from this?"_
  - _Learning system design: "Where does your work fit into the overall system?," "What pieces does our team own?"_
  - _Learning who knows what: "Who knows the most about <area>?," "If <area> breaks, who knows how to fix it?"_
- Take notes, stop to ask about things you don't understand
- For the next 3 minutes: Ask about the biggest challenges the team has right now
- For the final 2 minutes: Ask who else you should talk to; write down every name they give you
- Repeat until you aren't given any new names

## Contribute fast

- **Goal: Get comfortable making changes**
- Immediate priority: Start landing code, get a high-level understanding of the codebase
- Add or improve onboarding docs, diagrams, and runbooks as you learn
- Cautious curiosity: Learn the system by using and changing it in small, observable increments
  - Get a general overview of how everything works together
  - Focus on small sections of code at a time, fully understanding how they work
  - Pick a feature to develop and learn as you go along
- Make notes as you go and take an hour (e.g., every Monday) to read through and arrange the notes from previous weeks
- Build trust through dependable contributions
- Scale improvements only after understanding the risks and adding safety nets
- Example approach: Land lots of low-risk changes (~1-2 per day) that improve the codebase

## Learn about the codebase

- Gain context fast:
  - Read available documentation carefully (for any documentation related to the team's stack [e.g., Django], make sure to read the documentation for the correct version)
  - Read `README`, `CONTRIBUTING`, design docs, architecture diagrams, recent PRs
  - Identify the tech stack and at least the major "quick start" quides or basic documentation (dive deeper as you work on the codebase)
  - Identify maintainers and owners: Code ownership files, PR authors, recent commit history
- Run the code:
  - Set up the local environment (git workflow, local storage, feature flags/configs)
  - Run the tests (note failing tests if any)
  - Write down pain points
  - Identify errors and alerts
  - Identify low-test/buggy modules
  - Understand how to deploy/rollback
- Understand the high-level areas:
  - Start with the different components
  - Then the subdirectories
  - Then the classes and their relations and so on
  - _Build an intuition for how everything works_
- Understand the functionality:
  - "What will this function return if I give it \<input\>?"
  - "How can I summarize what this method is made to do?"
  - "What are some potential gaps in the existing tests for this method?"
- Understand design patterns:
  - Identify the name of the design pattern that was implemented
  - Understand the intention and the meaning of abstractions
- Trace a single (API) call path end-to-end:
  - Follow the code through layers
  - Understand integration points
  - Add comments to explain what you think it might do
- Test and instrument:
  - Use logs, metrics, debuggers to observe runtime behavior
  - Add temporary log statements or breakpoints
- Analyize telemetry and metrics:
  - Study metrics to understand how the system behaves in production
  - What patterns emerge during peak usage
  - Which components require the most attention
- Explore through testing:
  - Make deliberate modifications to the code
  - Observe their effects
  - Write new tests to verify understanding
  - Intentionally break things (in development) to see how the system fails
  - _Build an intuitive understanding of the application’s boundaries and failure modes_

- Understand overall structure:
  - `cloc . --by-file` for big files/ratios
  - `git grep` key classes; review tests/CI for intent/deployment
  - Visualize the system

## Learn about the systems

- Understand the high-level: System boundaries, data model, deployment pipeline, configs
- "Which services work together?"
- "What goal are they trying to achieve?"
- "How are each of the services deployed/run/accessed?"
- "What's the development workflow for each?

## Example "5/30/90" plan

- 

### First 5 days

- **By day 5, learn to commit:** Basics of compiling, running, modifying, debugging, and committing changes
- Once code is up and running, push a small fix (go through every part of the process of committing that change):
  - Run the tests
  - Commit to the right branch
  - Request a PR
  - Update the bug tracking system
- Get your hands dirty:
  - Tackle small, well-defined tasks (e.g., fix docs or small bugs, flaky tests, linting issues, non-critical improvements)
  - Create small PRs to learn the review cycle
- Map technical debt and hotspots: Modules with high churn, most bugs, sparse tests, or ad-hoc patterns
- Document all the tribal knowledge you can


- High-level trace:
  - Services: Interactions, boundaries, goals, deploy/workflow
  - End-to-end API call: Logs/debugger/breakpoints; production metrics/telemetry
  - Break things in dev: Explore failure modes, add new tests
- Ship stuff: Docs, linting, flaky fixes

- [ ] Orientation meetings with manager, team, and HR
- [ ] Setup tools for your stack and access provisioning
- [ ] Documentation basics
- [ ] Schedule recurring 1:1s with manager (weekly 30 min check-ins): "What are my top 3 priorities for first 30 days?," "What are my role expectations?"
- [ ] Schedule intro 1:1 with buddy/mentor
- [ ] Contribute fast: Fix a small bug or doc tweak if access allows
- [ ] Create personal onboarding documentation tracking progress, questions
- [ ] Questions: "What are my day 1 priorities?," "Who is my onboarding buddy/mentor?"

### First 30 days
### First 90 days

## Open questions

- [ ] 

## First 30 days (Learn the process)

- [ ] Confirm learning, role clarity, and early progress
- [ ] 30 day review: 1:1 discussing role-level expectations vs. next-level goals (e.g., autonomy by day 90)
- [ ] Review documentation:
  - [ ] Company culture/values
  - [ ] Processes
  - [ ] Tools
- [ ] Shadow team members
- [ ] Complete initial training modules
- [ ] Small contributions: Low-stakes tasks with feedback
- [ ] "Am I on track for success metrics?," "Any blockers for ramp-up?"

- **By day 30, learn the process:** Go through one or two development cycles / sprints / units of development time
- Understand how different meetings are run, how estimates work, how completed work is reviewed, etc.
- Get a sense of the shipping process as well
- Know your repos
- Know your pipelines
- Know your process to take in work
- Know your backlog: Understand what decisions have already been discussed and why

## First 60 days (Learn to collaborate)

- [ ] Bi-weekly 1:1s: Feedback on early work, cross-team intros
- [ ] Lead small projects
- [ ] Deeper process documentation review
- [ ] Meet key stakeholders (ceremonial or functional)
- [ ] Questions: "How can I contribute more independently?," "Feedback on collaboration style?"

- Show your personality:
  - How do you approach work?
  - How can you make the team process better?
  - Do you document your "Today I learned"?
  - What's in your toolbelt?
  - What is your definition of done?

## First 90 days (Learn the code)

- [ ] Formal 90-day review 1:1: Full expectations recap, performance goals, next steps
- [ ] Present contributions (e.g., project recap)
- [ ] Update personal documentation/wiki
- [ ] Plan ongoing 1:1 cadence and development goals
- [ ] Questions: "What defines success at my level/next level?," "Opportunities for growth/impact?"

- **By dat 90, learn the code:** Learn enough of the code to be comfortable taking on larger tasks, and have a general idea of the strengths and weaknesses of the architecture
- "Know where to look"
- Do you follow through to get your ideas past the finish line?
- Do you leave work unfinished?
- Have you identified and proposed in a compelling way ways to improve our process/business?
- Do your day to day work and exceed expectations

## First 30 days

### Team and process
### Codebase

- Goal: Deepen understanding; 5+ merged PRs; end-to-end intuition; team map
- Team:
  - 30min chats (manager list): 25min their world (direction/wins, system/owners, experts); 3min challenges; 2min next names. Repeat to exhaustion.
  - Pair: Workflows/files/debug; "why" on tasks/business.
  - Monitor: Chats, incidents/alerts.
- Codebase:
  - Summarize sections: Functions (input/output/gaps), patterns/abstractions.
  - Build: Diagrams (flows/relations); command cheatsheet; domain notes.
  - Explore: Tests/IDE (hierarchy/usages/hints); commits/PRs for "why".

Reflect: System desc? Interactions? Surprises/gaps?

Contribute: Templated issues (logs/fixes); docs/runbooks.
- 

## First 60 days

### Team and process
### Codebase

- Goal: Consistent PRs; basic ownership
- 

## First 90 days

### Team and process
### Codebase

- Goal: Own sub-system, advocate for improvements
- 

## Ongoing

- 

## Credits

- [https://medium.com/runkeeper-everyone-every-run/better-short-term-goals-for-new-engineering-hires-9a180f1ebc0f](https://medium.com/runkeeper-everyone-every-run/better-short-term-goals-for-new-engineering-hires-9a180f1ebc0f)
- [https://www.reddit.com/r/devops/comments/zdlrwk/whats_generally_in_your_306090_day_plan/](https://www.reddit.com/r/devops/comments/zdlrwk/whats_generally_in_your_306090_day_plan/)
