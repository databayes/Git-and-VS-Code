# VS Code + Git Folder Setup – A Simple, Safe Starting Point

If you’ve read the first post in this series (*Git vs GitHub – Plain English for Data & Analytics People*), the next natural question is:

> *Where do I actually put my files, and how do I set this up safely?*

This post walks through setting up **Visual Studio Code** with a **local Git folder** — no developer background required.

---

## What we’re setting up (big picture)

By the end of this, you’ll have:

- A **normal folder** on your machine
- Opened in **Visual Studio Code**
- Turned into a **Git repository**
- Ready to sync with GitHub later (if you want)

Nothing clever. Nothing fragile.

---

## Where should your Git folder live?

This is a really common question — especially if you’re used to working in **OneDrive** or **SharePoint**.

Short answer: **no, you don’t need OneDrive or SharePoint when working with Git**.

### Recommended setup (my strong preference)

Create a **local folder** on your machine, for example:

- `C:\Users\Sue\Documents\git`
- `~/git` (Mac / Linux)

Inside that, create subfolders as needed:

- `blog-posts`
- `notebooks`
- `demos`

This folder is now your **Git workspace**.

---

## Why not OneDrive or SharePoint?

OneDrive and SharePoint:

- Sync files **automatically and silently**
- Maintain their *own* version history
- Can change files in the background

Git does the same thing — deliberately and explicitly.

When you mix the two, you can get:

- Confusing file states
- Unexpected merge conflicts
- Git showing changes you didn’t consciously make

**In short:** OneDrive versioning and Git versioning don’t play nicely together.

### When OneDrive *is* OK

OneDrive and SharePoint are still useful for:

- Final exports
- Read-only copies
- Files you are **not actively versioning with Git**

A simple pattern that works well:

- **Git** → source of truth while writing and editing
- **OneDrive / SharePoint** → backup or distribution *after* publishing

---

## Opening the folder in Visual Studio Code

1. Open **Visual Studio Code**
2. Select **File → Open Folder**
3. Choose your local Git folder (for example `git` or `blog-posts`)

At this point:

- It’s just a folder
- Git is **not** involved yet

---

## Initialising Git (the key moment)

In VS Code:

- Open the **Source Control** panel (branch icon)
- Click **“Initialize Repository”**

Behind the scenes, VS Code runs:

- `git init`

What changes:

- A hidden `.git` folder is created
- Git now tracks everything inside this folder

---

## Making your first commit

1. Create or edit a file (for example a `.md` blog post)
2. VS Code will show it as **Modified**
3. Add a short commit message, such as:

   **`Initial blog post setup`**

4. Click **Commit**

You now have a **snapshot in time** you can always return to.

**My view:** If it’s worth writing, it’s worth committing.

---

## Linking to GitHub (optional, but recommended)

You can do this later, but the usual flow is:

- Create an **empty repository** on GitHub
- In VS Code, publish the branch or add a remote
- Push your commits

From that point on:

- Local folder → commit → push
- GitHub stays in sync

---

## Common mistakes I see (worth avoiding)

- Putting Git repos *inside* OneDrive folders
- Mixing blogs, client work, and experiments in one repo
- Waiting too long to commit because “it’s not finished”

**Strong view:** Commit early. Commit small. Finish later.

---

## Final takeaway

- Use a **local folder** for Git-tracked work
- Let **Git** handle versioning
- Add **GitHub** when you want sharing, backup, or collaboration

This setup is simple, robust, and scales surprisingly well.

---

