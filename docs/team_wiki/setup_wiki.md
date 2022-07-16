# Setting up your team wiki

!!! info "TL DR"
    Teams will be assigned a GitHub repository owned by iDEC HQ. Team members will be able to add themselves as collaborators to the wiki repository through [reg.idec.io](https://reg.idec.io) and upload their web contents. Write access to the repository will be revoked by wiki freeze.  

We intend to give as much control as possible to teams in styling their project wikis and project documentations. For this reason, we are setting up [GitHub](https://www.github.com/) repositories so that teams can display their wikis using [GitHub Pages](https://pages.github.com/).

iDEC teams are encouraged to be creative and to fully utilize the freedom that comes with the assigned GitHub repository.

If you are not familiar with the concept of Git and GitHub, imagine the following scenario:  

We are hosting a blog (**iDEC HQ repository**) that we write essays. You read some contents on your blog and you felt that something should change, so you downloaded (**forked** and **cloned**) a copy of our blog posts, made some edits (**commits**) on your own copy (**your repository**) and kept a chronological record of what and how edits are made (a **history** of commmits). Then, you send a note (**pull request**) to us, with those **edits (but not the modified blog posts)** attached. We reviewed the note, checked if the changes are reasonable or necessary, and decided to carry out (**merge**) the changes on our original blog posts.  

Moreover, in some ocassions, you might write a slightly different copy of the original blog post, and you wish to keep a copy of both the original text (**trunk**) and the derived text (**branch**). Instead of saving the derived text, you save *how* the derived text is different. You then continue working on the original text and when the moment comes, you can choose to apply the changes back onto main verison of the text. Abstractly, this is like a tree, with a **main** trunk that develops upwards with different smaller changes **branching out** from the trunk.

This is a simplified analogy on how software enigneers use [distributed version control](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control) to collaborate on projects. This year, iDEC HQ will provide the wiki platform through this mechanism. So essentially, we will assign each team an iDEC HQ-owned repository, which is basically a cloud space for hosting web contents. The contents will be rendered as a publicly accessible websie through the GitHub Pages function.  

## Wiki content upload and wiki freeze

A team will be given permissions to manage their assigned repository. The permissions include read-write access, pull requests management and configuration of settings related to web page deployment. These permissions will be downgraded to "read-only" as wiki-freeze commences, so it is imperative that teams complete all uploads *and* set up their GitHub Pages properly before the deadline. 

## Accessing and configuring your team repository

!!! caution "Wiki URL"
    Starting from 2022, all landing pages of the team wikis must be pointed to `https://www.github.com/idec-teams/{assigned repo name}`. Failure to comply will result in disqualification on the Wiki requirement.

The GitHub repositories for teams in 2021 will be hosted under the GitHub Organization "idec2021". Check your assigned repository on the [wiki list](wiki_list.md).

To obtain the permissions for wiki-editing, iDEC team members will need to add themselves as collaborator to the wiki repository. To do so, follow the instructions on our page [Accessing your wiki repository](access_repo.md). Joining as collaborator will grant the user "maintain" permission to the repository.

GitHub turns uploaded web contents into a website through its GitHub Pages service, and it is important that a team notifies GitHub which **branch** should be used for the source. Check out our [quick guide](gh_pages.md) on how to do so.

## Making using of forks to coordinate your site development

Even though every team member who join their team wiki repository will have nearly full access, we recommend that team members fork their assigned repository (base) under their personal / organizational account. All uploads and edits of wiki contents can then be performed on the forked repository (head). Pull requests can then be submitted to the base, such that changes can be reviewed by the more experienced web developers within the team before those changes are applied.

Teams are also encouraged to utilize features like Issues and Projects to keep track of their web development processes.

## Methods of creating the wiki contents

We do not impose restrictions on what technologies, packages, or languages that team use to generate their wikis. A wiki can be created using traditional HTML, CSS and Javascript, through a static site generator, or a content-management system, or anything else, so long as the final site is **static**.  

By default, the assigned GitHub repositories are populated with template wiki contents. The wiki contents are rendered into a project documentation wiki site using [MkDocs](http://mkdocs.org) with the [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) theme. This is a solution for teams who will not develop their own websites.  

An example of such wiki is available [here](https://idec2021.github.io/team-wiki/).  

We have an [introductory tutorial](mkdocs.md) that covers how to edit the contents using MkDocs.  

If your team wish to use other technologies (which we hope you do!), you can empty and overwrite the assigned repository and upload your own web contents. This will necessitate a change in [configuring the GitHub Pages](gh_pages.md) source branch setting.

## Additional material

- [Official 10 mins guide to GitHub](https://guides.github.com/activities/hello-world/)