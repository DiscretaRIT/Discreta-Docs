# Issue Guidelines
The following document is a general guide on creating issues and fixing issues in `Discreta`.

# Creating issues
Issues and bugs that are found by testers must be created on the **team**'s repo and must be fixed by the team before contributing to the main repo.

Issues must include some important headings like so:
```md
# Description
Your issue description and relevant screenshots go here. You can even include the commit that introduced this bug here.

# Steps to Reproduce
A set of steps that you can perform to reproduce this issue goes here.

# Suggestions for potential fix
Your suggestions on what could be done to fix it goes here. (this is not compulsory)

# Suggested Assignee
You can suggest assignee(s) to this issue if you'd like. This will most likely be the contributor(s) who pushed the commit listed above in the description.
```

# Fixing issues
If you are looking to fix an issue, first create a fork of the team repo for yourself (if you are a contributor already, you can skip this step).

Now create an issue branch as `issue/<issue number on the repo>` where `<issue number on the repo>` is replaced with the issue number. Eg: If you are trying to fix issue #8 on your team's repo, then you'd name your branch as `issue/8`.

You can now commit code to your issue branch to fix the issue completely and then make a pull request to the team's repo for the same.