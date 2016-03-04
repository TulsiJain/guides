# Git

### General
- Don't put sensitive information like database details, access keys, passwords in source control
- Avoid including files in source control that are specific to your development machine or process

### Basic Workflow
- Use [Fork & pull] model
- Fork the repo
- [Clone][git clone] your fork locally
- Create a new branch from `master` for each independent feature and work on it
```sh
git checkout -b <new_branch_name>
```
- Make sure all tests are passing and commit your changes on the feature branch
- Submit a [pull request]

### Sync Fork
- Add the upstream repo (repo from which you created fork)
```sh
git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git
```
- Whenever you have to sync your work with the main repo, first commit all your changes and then pull the changes
```sh
git pull upstream master
```

### Commits
- If a project has multiple components each commit should have changes in one component only
- Prefix commit messages with the component name

```
[Component1] Fix bug in SomeClass
[Component2] Add SomeOtherClass
```

## Further Reading
- https://help.github.com/categories/collaborating-on-projects-using-pull-requests/
- https://sethrobertson.github.io/GitBestPractices/
- https://github.com/thoughtbot/guides/tree/master/protocol/git
- https://github.com/thoughtbot/guides/tree/master/style/git

[Fork & pull]: https://help.github.com/articles/types-of-collaborative-development-models/#fork--pull
[git clone]: https://help.github.com/articles/cloning-a-repository/
[pull request]: https://help.github.com/articles/creating-a-pull-request/
