# Moving forward

Upon completing this tutorial you should know the basics on how to edit and submit your team wiki.  
Below we offer some suggestions on how to take a step further and be more effective in the process.

## MkDocs and Material for MkDocs

We presented some of the most important features for customizing your wiki contents, but you may wish to know that these static site generators allow many more customizations, like changing theme colors and adding emojis.

For more information on the underlying mechanism of [MkDocs](http://mkdocs.org), please check their documentation site.

For information on customizing the theme, please see [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/).

## Useful features in Material for MkDocs

In the [mock wiki](https://idec2021.github.io/team-wiki/) for this tutorial, we have a [page](https://idec2021.github.io/team-wiki/useful_features/) demonstrating 3 useful features enabled by default:
- Mathematical equations input by LaTeX
- Sortable Tables
- Markdown footnotes for citations

Be sure to check the [Markdown file](https://raw.githubusercontent.com/idec2021/team-wiki/main/docs/useful_features.md) behind if your team use Material for MkDocs for your wiki.

## Git and GitHub

Throughout this tutorial we used GitHub Desktop for version control illustration. GitHub Desktop provides an intuitive graphic user interface (GUI) which is great for beginners. You can find a lot of help from the [documentation](https://docs.github.com/en/desktop) of GitHub Desktop and our tutorial is to some extent based on it.

As you move forward, you may find the [command line interface (CLI) version](https://git-scm.com/downloads) more powerful since it permits automation of tasks.

## Fork a forked repository

In this tutorial, you forked the repository `idec2021/team-wiki`, push commits and submit pull requests to it. When you are dealing with your team repository, it is far better to have only the lead web developer fork your team wiki repository, with other contributing members forking the forked repository. For example, if your team repository is named `idec-team` and `user1` is the lead web developer, your team should fork the repository in the scheme below:

```yml
idec2021 / idec-team
└──user1 / idec-team
   ├─user2 / idec-team
   ├─user3 / idec-team
   └─user4 / idec-team
```

In this way, it is easier for iDEC HQ to know or guess that a pull request from your lead developer is likely final, and this should reduce the chances of encountering merge conflicts.

Alternatively, have your organization fork the base repository and allow all contributors to commit directly to the forked repository.