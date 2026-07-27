In this unit, we review the following learning objectives:

- Brief overview of the GitHub Enterprise Platform
- How to create a repository
- Adding files to a repository
- How to search for repositories
- Introduction to gists and wikis

## GitHub

Before we explore the GitHub platform in detail, it's important to understand the foundation behind it: Git.

**Git** is a system for tracking changes over time. Technical teams use it to manage updates and keep a record of who changed what and when. GitHub is built on top of Git and adds collaboration tools, automation, and a user-friendly web experience. Even if you are not writing code, understanding a few basic terms—such as commits, branches, and merges—will make it easier to follow team activity and participate in reviews.

:::image type="content" source="../media/github-enterprise-platform.png" alt-text="A conceptual image of the GitHub Platform with layers from top to bottom: AI, Collaboration, Productivity, Security, and Scale." border="false":::

**GitHub** is a cloud platform that helps teams organize work, collaborate, and keep an auditable history of project changes. It provides a website, command-line tools, and workflows that support both technical and non-technical contributors.

As introduced earlier, GitHub provides an AI-powered platform to help organizations build, scale, and deliver secure software. The GitHub Enterprise platform is centered around five core pillars: AI, Collaboration, Productivity, Security, and Scale.

### AI

Generative AI is changing how teams work. In GitHub Enterprise, AI improves collaboration through AI-powered pull requests and issues, booosts productivity through tools like Copilot, **Copilot Chat**, and **Copilot Agents**, and helps security by providing faster feedback that can reduce risk earlier.

### Collaboration

Collaboration is central to GitHub. GitHub provides shared workflows that help teams coordinate efficiently, reduce delays, and move work forward with more clarity.

Repositories, issues, pull requests, and related tools help teams across different roles work together, shorten review and approval cycles, and improve delivery speed.

### Productivity

GitHub Enterprise improves productivity through automation. With built-in CI/CD (Continuous Integration and Continuous Delivery), teams can automate repetitive steps and reduce manual work. This helps contributors spend more time on high-value problem solving and less time on routine tasks.

### Security

GitHub includes security checks throughout the development lifecycle from the start. GitHub Enterprise provides built-in tools such as CodeQL, secret scanning, Dependabot, and security overview to help identify and reduce risk.

Organizations can keep code private while still benefiting from integrated security analysis. GitHub also supports enterprise-grade security and compliance expectations used by highly regulated industries.

### Scale

GitHub serves a massive global community, with insights from over 100 million developers and hundreds of millions of repositories. This scale helps GitHub continuously improve its products based on real-world usage.

Because GitHub is also extensible and connected to open source communities, it evolves quickly to meet changing needs. Insights from this large ecosystem help GitHub improve how teams collaborate and deliver at scale.

In summary, GitHub Enterprise brings collaboration, automation, security, and AI capabilities into one unified platform experience.

Now let’s move to the backbone of GitHub: repositories.

## Introduction to repositories

Let’s first review:

- What is a repository?
- How to create a repository
- Adding files to a repository
- How to search for repositories
- Introduction to gists, wikis, and GitHub pages

### What is a repository?

A repository is a shared workspace that stores project files and the history of changes made to them. It is a core part of how teams coordinate work, track updates, and collaborate over time.

### How to create a repository

You can create a repository in your personal account or within an organization where you have appropriate permissions.

Follow these steps on GitHub.com.

1. In the upper-right corner of any page, use the drop-down menu, and select **New repository**.

    :::image type="content" source="../media/2-new-repo-option.png" alt-text="A screenshot of the drop-down menu of the plus sign in the top right corner of GitHub.com, with the first option being New repository." border="false":::

2. Use the **Owner** drop-down menu to select the account will own the repository.

    :::image type="content" source="../media/2-selecting-repo-owner.png" alt-text="A screenshot of the drop-down menu of who should be the owner of the new repository." border="false":::

3. Enter a repository name, and an optional short-description.

    :::image type="content" source="../media/2-repo-name-text-box.png" alt-text="An image of the text box of the repository name highlighted." border="false":::

4. Choose a repository visibility:
    - **Public repositories** are visible to anyone on the internet.
    - **Private repositories** are visible only to you and people you explicitly grant access to (plus certain organization members, if applicable). 

5. Select **Create repository** and congratulations! You just created a repository!

### How to clone a repository

In many cases, non-technical users do **not** need to clone a repository.

**What “clone” means:**  
Cloning creates a full copy of a repository on your computer.

**Why some people use it:**  
Technical contributors (such as developers) often clone repositories so they can use local tools, run tests, or make larger changes before uploading updates back to GitHub.

**What is a terminal?**  
A terminal is a text-based window used to run commands on your computer. It is a common tool for developers, but most non-technical contributors won’t need to use it for everyday GitHub tasks.

**For non-technical contributors:**  
You can usually review files, leave comments, open issues, and suggest many changes directly on GitHub.com—no terminal required.

**If your role does require cloning**, here are the standard steps:

1. On GitHub.com, go to the repository’s main page.
2. Select **Code** above the file list.

    :::image type="content" source="../media/2-selecting-code-button.png" alt-text="Screenshot of the Code button dropdown menu with clone options." border="false":::

3. Copy the repository URL (HTTPS, SSH, or GitHub CLI option).
4. Open a terminal and move to the folder where you want the repository copy.
5. Run:

   ```bash
   git clone <repository-url>
   ```

6. Move into the repository folder:

   ```bash
   cd <repository-name>
   ```

You now have a local copy of the repository on your computer.

### How to add a file to your repository

Files in GitHub store project information (documentation, configuration, assets, and more). To add files, you need at least **Write** access.

Let’s review how to add a file to your repository.

1. On GitHub.com, open the repository's main page.
2. Navigate to the folder where you want the new file, or choose to upload an existing file.
3. Select the **Add file ᐁ** drop-down menu, then choose **Create new file**.

    :::image type="content" source="../media/add-file-options.png" alt-text="A screenshot of the option to add a file to your new repository highlighted in red with the add file button towards the right of the screen." border="false":::

4. Enter a file name (including extension). Use / to create subfolders if needed.
5. Enter the file content.
6. To review formatting and output, select Preview above the editor.

    :::image type="content" source="../media/2-preview-option-in-a-file.png" alt-text="Screenshot showing a yml file with the preview button highlighted in the top left." border="false":::

7. Select **Commit changes**.

8. Add a short commit message describing what changed.

9. Choose whether to commit directly to the current branch or create a new branch. If you are on the default branch, best practice is to create a new branch and then open a pull request. We will go over Branches in depth later in this module. 

     :::image type="content" source="../media/2-create-a-new-branch.png" alt-text="Screenshot showing creating a new branch from a commit option select with the textbox of the new branch below it." border="false":::

10. Select **Commit changes** or **Propose changes**.

Congratulations, you just created a new file in your repository! You have also created a new branch and made a commit.

Before we review branches and commits in the next unit, let’s quickly review gists, wikis, and GitHub pages because they're similar to repositories.

### What are Gists?

Gists are a lightweight way to share small pieces of content—such as short code snippets, notes, examples, or configuration text—without creating a full repository.

You can think of a gist as a mini repository with version history. That means changes are tracked over time, and gists can be copied or downloaded like regular repositories.

#### Key Features of Gists:
1. **Public and Secret Gists**
   - **Public Gists** can be discovered by others.
   - **Secret Gists** are not publicly listed, but anyone with the link can access them.

2. **Version history**
   - Each edit is saved, so you can review or restore previous versions.

3. **Forking and cloning**
   - Others can copy your gist and adapt it for their own use.

4. **Embedding**
   - Gists can be embedded in websites, blogs, and documentation.
     
5. **Markdown support**
   - You can include headings, links, images, and formatted text for context.

7. **Lightweight Collaboration**
   - Teams can share, comment on, and iterate quickly.


#### Use cases for Gists:
- Sharing quick code examples or solutions.
- Storing configuration files or scripts for personal use.
- Creating templates for commonly used code patterns.
- Sharing error logs or debugging information with others.
- Embedding code snippets in blogs, forums, or documentation.

> [!IMPORTANT]
> **Never use gists to store sensitive or confidential data, such as passwords, secrets, or API keys—even in scripts or config files.**  
> Gists are not fully private: even secret gists can be accessed by anyone with the link. Always review your content carefully before sharing.

#### Limitations of Gists:
- Gists are not entirely private, even if marked as secret. Anyone with the URL can access them, so they should not be used for sensitive or confidential information.
- They are best suited for small snippets or single files. For larger projects or multi-file structures, a full repository is more appropriate.

To learn more about how to create and manage gists, refer to the GitHub documentation in the Resources section of this module or visit the [GitHub Gists documentation](https://docs.github.com/en/github/writing-on-github/creating-gists).

### Forking and cloning Gists

You can fork a gist to create a copy of someone else's gist in your account.

1. Navigate to the gist you want to fork.
2. Select **Fork** at the top-right of the gist page.

To clone a gist locally:

```bash
git clone https://gist.github.com/your-gist-id.git
```

To learn more about gists, see the linked article in our Resources section at the end of this module titled *Creating Gists*.

---

### What are wikis?

Every repository on GitHub.com comes equipped with a section for hosting documentation, called a wiki. You can use your repository's wiki to share long-form content about your project, such as how to use it, how you designed it, or its core principles. While a README file quickly tells what your project can do, you can use a wiki to provide additional documentation.

It’s worth a reminder that if your repository is private, only people who have at least read access to your repository will have access to your wiki.

#### Creating, editing, and deleting wiki pages

You can use the GitHub wiki to create and manage documentation for your project.

**To create a wiki page:**

1. Navigate to the repository.
2. Select the **Wiki** tab.
3. Select **Create the first page** if no pages exist, or **New Page** to add a page.
4. Enter a title and content, then select **Save Page**.

**To edit a wiki page:**

1. Navigate to the wiki page you want to edit.
2. Select **Edit** at the top-right.
3. Make changes and select **Save Page**.

**To delete a wiki page:**

- Deleting a wiki page requires using Git. Clone the wiki repository, remove the file, and push the change.

Learn more about managing wikis in [GitHub Docs - Adding or editing wiki pages](https://docs.github.com/en/communities/documenting-your-project-with-wikis/adding-or-editing-wiki-pages).


### What are Feature Previews?

Feature Previews allow you to try out experimental features on GitHub before they are officially released. These previews give you early access to new functionality and allow you to provide feedback to help shape the final product.

To enable or disable a feature preview:

1. Navigate to your GitHub account by selecting your profile picture in the top-right corner of GitHub.com.
1. Select **Feature preview** from the drop-down menu.
1. Browse the list of available previews and toggle the features you want to try.

Feature Previews are a great way to stay ahead of the curve and explore new tools that can enhance your GitHub experience.

> [!TIP]
> GitHub frequently adds new experimental features for users to explore, so keep an eye on the **Feature review** to discover new tools and enhancements.


