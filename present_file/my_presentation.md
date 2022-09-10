---
title: Git Event

author: Alireza Soltani Neshan

date: Thu Shahrivar 10
---

# First Hour

- Git Servers 
- Accessibility
  - GitHub
  - GitLab
  - Code-berg
  - Bitbucket
  - AWS CodeCommit
- Documentation
  - What is my presentation server topic?
  - Doc, doc, doc, Documentation
  - Read GH Documentation completely
  - What I used from the gh?
  - What I used and I enjoyed gh issue api endpoint
  - You can use both api and graphql as client
- GitHub Features
  - GitHub CLI
    - How to install gh in different Operating Systems

    ```bash
      brew install gh
    ```

    - authorization
      - login
    - Config Your gh
      - gh config --help
      - gh config list
      - gh config get <key>
      - gh config set <key> <value>
    - repo
      - gh repo list
      - gh repo create 
      - gh repo clone
      - gh repo view (md viewer)
    - versions and releases
      - gh release create
      - gh release view
    - What is CI/CD, Actions! (devops) 
    - CI
      - Compile code
      - Run test
      - Code linter
      - Sec checks
      - Code coverage
      - Functional test
    - CD
      - Deployment and development
    - What is `yml`, `JSON`
    - What is actions
    - You can find GH actions in marketplace
    - What is events
    - What is jobs
    - What is actions
    - What is runners
    - Parallel and `SJF` default mode
    - What's Artifacts -> Download/Upload
    - actions
      - run
        - list
        - view
        - watch
        - rerun
        - download (Artifacts)
      - workflows
        - list
        - view
        - enable/disable
        - run
    - Create an app and getting start with new pipeline
      - Create md2pdf pipeline
      - Create more advance about build apk file from flutter CI/CD
    - GitHub APIs
      - What we can do with it?
      - When You will need to GitHuB Apis

- Server spec
  - All limits in free plan

Richard Stallman's Personal [Site](https://stallman.org/)

- See `GH API` in action:

```bash
  gh api repos/{owner}/{repo-name}/{features}
  gh api repos/Asncodes-80/git-event/
  gh api repos/bdlukaa/fluent_ui/
  gh api repos/bdlukaa/fluent_ui/issues/
  gh api repos/Asncodes-80/mci-users/releases/
  # posting an issue to my git-event repo
  gh api repos/Asncodes/git-event/issues/1/coments -f body='hi from CLI'
```

Before any request, go to this [site](developer.github.com/v4/explorer)

```zsh
  gh api graphql --paginate -f query='
    query($endCursor: String) {
      viewer {
        repositories(first: 100, after: $endCursor) {
          nodes { nameWithOwner }
          pageInfo { hasNextPage
            endCursor
          }
        }
      }
    }
```
