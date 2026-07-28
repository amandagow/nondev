In this unit, we'll review these parts of how work moves through GitHub:

- Branches
- Commits
- Pull Requests
- The GitHub Flow
- Git flow

## Components of GitHub Flow

Git is the underlying system that tracks changes over time. GitHub makes that system easier to use through a visual interface and team workflows such as branches, commits, and pull requests. 

Even if you do not write code, understanding these concepts helps you follow progress, give feedback and approve work confidently.

## What are branches

In the last section, we created a new file and a new branch in your repository.

A **branch** is a separate workspace where changes can be prepared safely before affecting the main version of a project.

Think of it like drafting edits in a copy of a document instead of editing the official final copy directly.
- The default branch (often named main) is the primary approved version.
- A new branch lets you try updates or fixes without disrupting that primary version.
- Changes only affect the default branch after review and merge.

If a mistake is made in a branch, you can adjust or revert it before it becomes part of the main work.

Your branch is a safe place to experiment with new features or fixes. If you make a mistake, you can revert your changes or push more changes to fix the mistake. Your changes won't update on the default branch until you merge your branch.

> [!NOTE]
> Technical users can also create branches from a terminal using `git checkout -b newBranchName`
> Non-technical contributors usually do this through the GitHub web interface.

## What are commits

In the previous unit, you added a file by creating a commit.

A **commit** is a change to one or more files on a branch. Each commit is tracked by a unique ID, timestamp, and contributor, regardless of whether it's made via the command line or directly in GitHub's web interface. Commits provide a clear audit trail for anyone reviewing the history of a file or linked item, such as an issue or pull request.

A **commit** is a saved record of one or more file changes in a branch. Each commit includes:
- a unique ID
- time/date information
- the person who made the change

This creates a clear history and audit trail, which helps with accountability and review.

> Technical users can create commits from a terminal with:
> ```
> git commit -m "Add a helpful commit message"
> ```
> Non-technical users can commit changes directly in GitHub.com without using a terminal. 

:::image type="content" source="../media/2-commits.png" alt-text="A screenshot of a list of GitHub commits to a main branch." border="false":::

In Git, files move through several statuses. For non-technical learners, the key idea is simple: a file can be either not yet tracked or tracked with different stages of change.

- Untracked: Git does not yet manage this file.
- Tracked: Git is managing this file, and it can be:
    - **Unmodified**: no new changes since last save/commit
    - **Modified**: changed, but not prepared for the next commit
    - **Staged**: prepared for the next commit
    - **Committed**: officially saved in project history
These statuses help teams understand what is draft work versus what is officially recorded.


## What are pull requests?

A **pull request** is how someone asks for changes from one branch to be reviewed and merged into another branch.

In business terms, this is like submitting a draft for formal review and approval.

Reviewers can:
- comment
- request changes
- suggest improvements
- approve when ready
- 
GitHub also supports **Draft Pull Requests**, which are useful when work is still in progress and not ready for final review.

After required approvals, the source branch is merged into the target branch (often main).

:::image type="content" source="../media/2-pull-request.png" alt-text="A screenshot of a pull request and a comment within the pull request." border="false":::

Now that you’ve seen how branches, commits, and pull requests work, let’s walk through how they come together in GitHub Flow.

## The GitHub flow

:::image type="content" source="../media/2-branching.png" alt-text="Screenshot showing a visual representation of the GitHub flow in a linear format that includes a new branch, commits, pull request, and merging the changes back to main in that order." border="false":::

GitHub Flow is a simple, practical workflow for making changes safely and collaboratively.

> [!NOTE]
> GitHub flow is one common workflows. Others include Git flow and trunk-based development.

### GitHub Flow steps

1. Create a branch so your updates do not affect the main branch immediately.
2. Make your updates in that branch.
3. Open a pull request so others can review and comment.
4. Update your work based on feedback.
5. After approval, merge into the main branch.
6. Delete the branch after merge to keep workspaces clean and avoid confusion from outdated branches.

For non-technical contributors, this process is valuable because it creates visibility, review checkpoints, and safer change management.

## Git flow

While GitHub Flow is lightweight and fast-moving, Git flow is a more structured model often used in release-based environments.

Git flow has existed for many years, so you may still see `master` used where newer projects use `main`.

:::image type="content" source="../media/nvie-git-flow.png" alt-text="Nvie's diagram of a Git branching model showing feature branches, a develop branch, release branches, hotfixes, and the master branch over time. Colored commit nodes and arrows illustrate how features are merged into develop, how release branches are created for version 1.0, how bug fixes flow back into develop, and how hotfixes are applied directly to master. Tags mark releases 0.1, 0.2, and 1.0." border="false":::

*Image by Vincent Driessen, from ['A successful Git branching model'](https://nvie.com/posts/a-successful-git-branching-model/)*

### Git flow Branch Types

Git flow uses multiple branch types for different purposes:

- **master**: production-ready/live version
- **develop**: ongoing work for the next release
- **feature/***: work on individual features
- **release/***: final preparation before release
- **hotfix/***: urgent fixes to production issues


### When to Use Git flow

Git flow is often best when teams need:
- scheduled/versioned releases
- support for multiple active production versions
- formal or regulated release controls
- stronger structure and predictability

It is more process-heavy than GitHub Flow because it requires more branch coordination.

> [!NOTE]
> Git flow is designed around merge commits. Other merge methods (like rebase/squash) can reduce clarity in this model.

For many GitHub teams, GitHub Flow is simpler and faster.
For teams needing strict release planning, Git flow can be a better fit.

Congratulations—you’ve now seen how work moves through GitHub Flow and how Git flow provides a structured alternative.

Next, we’ll cover the difference between issues and discussions.

