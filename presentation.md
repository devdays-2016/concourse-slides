# [fit] Concourse CI
### https://concourse.ci/
---
# Why did we look at this?
- All configuration is source controlled
  - no GUI config even possible!
- Isolated builds
  - Docker, all the way
- Open Source
---
# So we dug deeper...
- very scalable
  - just add `workers` which host containers
  - lots of parallelism
- debuggable builds
  - `hijack` recent builds
- add your own resources
  - as long as they support basic API
---
# Three core concepts
1. tasks
2. resources
3. jobs
---
# Tasks
"A task is the execution of a script in an isolated environment with dependent resources available to it."
---
# Demo
