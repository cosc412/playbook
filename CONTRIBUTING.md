# Contributing
## Logging issues
When finding and creating new issues (such as finding a bug or new feature request) it is important to log them as issues on GitHub 
in the correct repository.  For instance, if we have a bug in our frontend then you would not log an issue in our backend.

If you are looking for work or are currently tackling a task that is logged as an issue IT IS ESSENTIAL that you assign yourself to
that issue.  This way we do not have multiple people working on their own way to resolve a singular issue and can focus more on developing
or fixing other things.

You can also add tags to issues to describe the nature of them.  For instance, is it a bug?  Feature?  Small?  Needs improvement?

## Branching
Branching is fairly common when contributing in a team.  When you decide to tackle a new issue, pull the latest version of the master
branch and create a new branch.  You can name the branch whatever you would like, however try to keep the name concise and to the point.

## Commiting
After creating a new branch to work on an issue, it is important that you regularly commit to that branch.  Do not commit until a stage in
solving the issue is finished.  For instance, if you wrote a few console logs and some lines of code that has not worked to solve
the issue in a significant way then do not commit.  If you want to switch to another branch then use git stash to stash your changes.

The reason why we regularly commit is so that if a change is made that breaks the functionality of your branch, we can easily revert it to
a point where functionality is normal and work back up from there.

When writing a commit message try not to sum up what the other previous commits have been doing.  For instance, suppose I have a login
function to write and I want to link it to a button:

Commit #1: Write logic for login function

Commit #2: Create button and link to login function

This keeps our commit messages short and others can easily see and follow your progress throughout the branch.

## Pull Requests (PRs)
Pull requests, or PRs, are also fairly common when working in a large group.  When you decide that your branch is done and ready to be
merged into master, you create a PR.  MAKE SURE TO REMOVE ANY CONSOLE LOGS AND UNNESSARY COMMENTS BEFORE MAKING THE PR.  You do not need
to remove every comment, actually it is important to document what functions or function parts do.  But if you write a comment that says:

There is an error here

When you resolved the error, then you should delete that comment.

PRs should also be approved by at least one person in our group before merging.  This helps prevent merging code that has bugs or other
small errors.  For the time being, assign everyone in the organization to the PR and whoever has time to review it go review it.  DO
NOT approve a PR if you have not thoroughly looked at it and understand what the person is adding (another reason why comments are
helpful).

If the PR helps resolve a bigger issue, like a use case or new feature, use the keywords: resolves, closes, and/or needs followed by 
the issue number:

Resolves means that there is more then one issue that is needed to close a bigger issue.

Closes means that the PR will close an issue opened on GitHub.  This should only be used if the issue is not part of a bigger issue.

Needs means that the pull request is blocked until another pull request is successfully merged.  For instance, if a UI requires data that
is inaccessable at the time until another PR is merged use needs.

The syntax for this would be "Closes #issue_number", or if the issue is in another repository in our organization
"Closes #cosc412/repository_name#issue_number"

After the PR has been merged, delete the branch.

## Versioning
Since the majority of the programs we will be working with uses node.js or npm we will be using versioning as well.  AFTER A PR IS
APPROVED, be sure to version the branch before merging.  This helps use keep track of our progress and we can see how much we have
accomplished.

There are 3 types of versions we will be using for this project: major, minor, and patch (major.minor.patch).  Major is reserved for
large, backwards compatability breaking changes such as restructuring our database or adding new significant UI capabilities.  Minor
is reserved for small, added features such as adding a new route in a API or new UI component.  Patch is reserved for editing a existing
change like fixing a bug.

How you version is quite simple.  Simply write the following command into the command line: npm version major/minor/patch.  Choosing
the version type that most closely relates to what your branch accomplished.

It is important to note that while versioning is not nessesary in this project, it creates a good habit if you version when contributing
to a large project.  I will not be enforcing this as much as the other sections in this document, as the sections above are more
important to our workflow.
