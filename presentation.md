# ![inline](concourse-logo.png) Concourse CI
### https://concourse.ci/

---

# Why did we look at this?
- All configuration is source controlled
  - no GUI config even possible!
- Isolated builds
  - Docker, all the way
- Open Source

^ Docker, sort of... we'll get into the architecture soon.

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

> A task is the execution of a script in an isolated environment with dependent resources available to it.
-- concourse.ci

---

# Tasks
- Run off of :whale: images
- Exit 0 :white_check_mark:
- Exit !0 :x:

---

# :no_entry: :whale: :no_entry:

---

# :no_entry: :whale: :no_entry:
- Tasks run inside Garden :seedling: Container
- Same primitive as Cloud Foundry
- Compatible with Docker images, can even build them.

---

# Resources

> A resource is any entity that can be checked for new versions, pulled down at a specific version, and/or pushed up to idempotently create new versions.
-- concourse.ci

---

# Resources - Get
- Git resources
- Time <- scheduler
- S3 bucket
- Etc.

---

# Resources - Put
- Email
- Slack/HipChat notification
- GitHub Release
- CF Deployment

---

# Jobs

> At a high level, a job describes some actions to perform when dependent resources change (or when manually triggered).
-- concourse.ci

---

# Demo
