# My Git Mastery Challenge Journey

## Student Information
- Name: T. Karthik
- Student ID: 23A91A6160
- Repository: https://github.com/karthikthorlapati/git-solved-23A91A6160.git
- Date Started: 28/10/2025
- Date Completed: 30/10/2025

## Task Summary
Cloned instructor's repository with pre-built conflicts and resolved all 
merge conflicts across multiple branches using proper Git workflows.

## Commands Used

| Command | Times Used | Purpose |
|---------|------------|----------|
| git clone | 1 | Clone instructor's repository |
| git checkout | 20+ | Switch between branches |
| git branch | 10+ | View and manage branches |
| git merge | 2 | Merge dev and conflict-simulator into main |
| git add | 30+ | Stage resolved conflicts |
| git commit | 15+ | Commit resolved changes |
| git push | 10+ | Push to my repository |
| git fetch | 2 | Fetch updates from instructor |
| git pull | 1 | Pull updates |
| git stash | 2 | Save temporary work |
| git cherry-pick | 1 | Copy specific commit |
| git rebase | 1 | Rebase feature branch |
| git reset | 3 | Undo commits (soft/mixed/hard) |
| git revert | 1 | Safe undo |
| git tag | 2 | Create release tags |
| git status | 50+ | Check repository state |
| git log | 30+ | View history |
| git diff | 20+ | Compare changes |

## Conflicts Resolved

### Merge 1: main + dev (6 files)

#### Conflict 1: config/app-config.yaml
- *Issue*: Production used port 8080, development used 3000
- *Resolution*: Created unified config with environment-based settings
- *Strategy*: Keep production as default, add dev as optional
- *Difficulty*: Medium
- *Time*: 15 minutes

#### Conflict 2: config/database-config.json
- *Issue*: Different database hosts and SSL modes
- *Resolution*: Created separate profiles for production and development
- *Strategy*: Restructured JSON to support both environments
- *Difficulty*: Medium
- *Time*: 10 minutes

#### Conflict 3: scripts/deploy.sh
- *Issue*: Different deployment strategies (production vs docker-compose)
- *Resolution*: Added conditional logic based on DEPLOY_ENV variable
- *Strategy*: Made script handle both environments dynamically
- *Difficulty*: Hard
- *Time*: 20 minutes

#### Conflict 4: scripts/monitor.js
- *Issue*: Different monitoring intervals and log formats
- *Resolution*: Environment-based configuration object
- *Strategy*: Used process.env.NODE_ENV to determine behavior
- *Difficulty*: Medium
- *Time*: 15 minutes

#### Conflict 5: docs/architecture.md
- *Issue*: Different architectural descriptions
- *Resolution*: Merged both descriptions into comprehensive document
- *Strategy*: Created sections for each environment
- *Difficulty*: Easy
- *Time*: 10 minutes

#### Conflict 6: README.md
- *Issue*: Different feature lists and version numbers
- *Resolution*: Combined all features with clear environment labels
- *Strategy*: Organized features by category
- *Difficulty*: Easy
- *Time*: 10 minutes

### Merge 2: main + conflict-simulator (6 files)

#### Conflict 1: config/app-config.yaml

- *Issue*: Conflict between simulated environment configuration (used mock API endpoints) and main branch (used live production endpoints)
- *Resolution*: Added environment toggle for SIMULATION_MODE to switch between mock and live endpoints
- *Strategy*: Default to production unless explicitly running in simulation mode
- *Difficulty*: Medium
- *Time*: 15 minutes

#### Conflict 2: config/database-config.json

- *Issue*: Simulator used an in-memory SQLite DB; main used PostgreSQL
- *Resolution*: Introduced dual configuration support — fallback to SQLite for simulation
- *Strategy*: Added "mode": "simulation" flag and dynamic DB selection logic
- *Difficulty*: Medium
- *Time*: 10 minutes

#### Conflict 3: scripts/deploy.sh

- *Issue*: Simulator added mock deployment steps conflicting with production deploy logic
- *Resolution*: Integrated simulation deployment path controlled by DEPLOY_MODE variable
- *Strategy*: Modularized script to support both live and simulated deployment
- *Difficulty*: Hard
- *Time*: 25 minutes

#### Conflict 4: scripts/monitor.js

- *Issue*: Simulator monitored dummy endpoints at 5s intervals; main monitored live services at 60s intervals
- *Resolution*: Created unified monitoring system configurable by environment
- *Strategy*: Used environment variable MONITOR_INTERVAL and mock/live endpoints array
- *Difficulty*: Medium
- *Time*: 15 minutes

#### Conflict 5: docs/architecture.md

- *Issue*: Simulator described fake service interactions; main described actual microservice flow
- *Resolution*: Combined both into one document under separate “Simulation Mode” and “Production Mode” sections
- *Strategy*: Clearly labeled diagrams and flow descriptions
- *Difficulty*: Easy
- *Time*: 10 minutes

#### Conflict 6: README.md

- *Issue*: Simulator added testing instructions and mock service details; main contained production setup steps
- *Resolution*: Merged both sections with clear headings for "Production Setup" and "Simulation Setup"
- *Strategy*: Ensured README guides users through either path without confusion
- *Difficulty*: Easy
- *Time*: 10 minutes



## Most Challenging Partse

1. *Understanding Conflict Markers*: Initially confused by <<<<<<<, =======, >>>>>>> symbols. Learned that HEAD is current branch and the other side is incoming changes.

2. *Deciding What to Keep*: Hardest part was choosing between conflicting code. Learned to read both versions completely before deciding.

3. *Complex Logic Conflicts*: deploy.sh had completely different logic. Had to understand both approaches before combining.

4. *Testing After Resolution*: Making sure resolved code actually worked was crucial.

## Key Learnings

### Technical Skills
- Mastered conflict resolution process
- Understood merge conflict markers
- Learned to use git diff effectively
- Practiced all major Git commands

### Best Practices
- Always read both sides of conflict before resolving
- Test resolved code before committing
- Write detailed merge commit messages
- Use git status frequently
- Commit atomically

### Git Workflow Insights
- Conflicts are normal, not errors
- Take time to understand both changes
- When in doubt, ask for clarification
- Document your resolution strategy
- Keep calm and read carefully

## Reflection
This challenge taught me that merge conflicts aren't scary - they're 
just Git asking "which version do you want?". The key is understanding 
what each side is trying to do before combining them. I now feel 
confident handling conflicts in real projects.

The hands-on practice with all Git commands (especially rebase and 
cherry-pick) was invaluable. I understand the difference between merge 
and rebase, and when to use each. Most importantly, I learned that 
git reflog is a lifesaver!