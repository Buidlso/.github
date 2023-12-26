# Solving Features/Bugs

- Pickup up Major Features/Bugs
- Break down into small issues
- Assign to team members
- Merge to major issue

# Git Branches

- **`main`**: Production branch, only `dev` branches can be merged into this branch, After a merge old `dev` branch needs to be deleted and new `dev` should be created.

- **`dev`**: Development branch, only `cycle-n` branches can be merged into this branch, After a merge old `cycle-n` branch should be deleted and a new `cycle-n+1` branch needs to be created.

- **` cycle-*`**: Cycle branch or weekly branch followed by a number, This branch should be created and merged into the `dev` branch weekly. Ex: `cycle-1`

- **`issueType-issueId`**: Normal issue branches, could be `feat`, `fix`,` test`, etc. These branches will be merged into corresponding `cycle` branches weekly. Ex: `feat-BMERN-1`, `fix-FMERN-10`

![task (1)](https://github.com/Buidlso/.github/assets/86586277/42974c10-8335-4da7-babb-2b0f942a420f)

# Issues

- **`Issue Title`**: Issue title should follow commitlint convention. Ex: `feat: direct message with mentors`

- **`Issue Level`**: Each issue should have appropriate level

# Commits

- **`Commit Style`**: Each commit should follow [Commitlint Convention](https://gist.github.com/qoomon/5dfcdf8eec66a051ecd85625518cfd13)

# CI/CD:

- **`cycle-*`**:

  - `PR`: Build & Test
  - `PUSH`: CodeQl Check (optional)
  - `workflow_dispatch`: Deploy to dev (urgent deployment to dev)

- **`dev`**:

  - `PR`: Build & Test
  - `PUSH`:
    - Deploy to Dev environment
    - CodeQl Check (optional)

- **`main`**:
  - `PR`: Build & Test
  - `PUSH`:
    - Release version
    - Deploy to the Production environment

# Resolve Conflict:

- Conflict needs to be resolved locally and should have to be pushed with a new commit `chore: conflict resolved`

# Urgent Bug Fixes:

- Urgent bug fixes should be merged immediately to `cycle` > `dev` > `main`
- Again create new `dev` > `cycle` branch from `main`
