# Git Guide
The following is a general guide to using git and github to contribute to `Discreta`.

# Commit Styling
Commits must be styled as `<action>: <description>`. Here are some examples: `fix: Code styling in frontend.`, `ci: Add test runners.`, `feat: Add more games.`, etc.

# Contributing
Contributors are to fork their respective team's repo into their **personal** accounts and create a feature branch for the features they are working on to contribute to the team's repository.

Example:

If the contributor is working on a feature called `poset_game` or something along those lines, they would fork their respective team's repo (please contact your team coordinator before you do this just to make sure you are forking the correct repo) and make a new branch on their fork named `feature/poset_game` and start working by importing only the contents of that branch into their local system (can be done very easily in VSCode, you can refer online for more info).

Refer [here](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo) for a guide on creating forks on GitHub.

After creating the fork on your **personal** Github account, you can clone the repo to your local by opening a command prompt or terminal and typing in:
```bash
git clone <link to your github repo>
```
Here the `<link to your github repo>` should be replaced with the link. Eg: `https://github.com/sathya-pramodh/seedqueue` which is a fork of `https://github.com/kingcontaria/seedqueue`.

Now you are ready to make changes, open up VSCode (or your favourite IDE) and open this cloned repository inside of it.

Once you are done editing, you can push your code to a new feature branch in your repository by opening up a terminal in VSCode and typing in:
```bash
git push -u origin feature/<feature name>
```
Here the `<feature name>` has to be replaced with whatever feature you are working on. Eg: `feature/poset_game`.

This will automatically create a feature branch on your fork and you can make a Pull Request to your team's repo from this branch by clicking on the `Contribute` button while in the branch that you just created on GitHub.

Drafting a PR(pull request) is also very essential in letting the maintainer know what your code does so please make sure to follow the guidelines below.

# Pull Request guidelines
A pull request must follow the same title styling as the commit styling, i.e., must be styled as `<action>: <description>`. Here are some examples: `fix: Code styling in frontend.`, `ci: Add test runners.`, `feat: Add more games.`, etc.

For most feature additions, it can be styled as `feat: Add <feature_name>.` where the `<feature_name>` is replaced with the actual feature name. Eg: `feat: Add poset_game.`.

In the description of the pull request, contributors should add relevant changelogs as separate points. Eg:
```md
# Changelog
- Refactored `TitleBar` component into a separate file.
- Fix coloring not working in `App` component.
- Fix API endpoint `/api/get-game`.
```

Any other comments like breaking changes can also be added under the changelog under a separate heading called `# Breaking Changes`, for example.