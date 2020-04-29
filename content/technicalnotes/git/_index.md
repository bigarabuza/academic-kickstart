---
# Course title, summary, and position.
linktitle: Git & Github
summary: Basic Git Usage.
weight: 1

# Page metadata.
title: Basic Github Usage
date: "2020-04-29T00:00:00Z"
lastmod: "2020-04-29T00:00:00Z"
draft: false  # Is this a draft? true/false
toc: true  # Show table of contents? true/false
type: docs  # Do not modify.

# Add menu entry to sidebar.
# - name: Declare this menu item as a parent with ID `name`.
# - weight: Position of link in menu.
menu:
    git:
        weight: 1
---

## Create New Git Repository

```bash
git init
```

## Clone a Repository

```bash
git clone https://github.com/USER_NAME/REPO_NAME.git
```

## Commit changes
```bash
git add .

git commit -m "Changes made"

git push origin [Branch being worked on]
```

## View all branches
```bash
git branch
```