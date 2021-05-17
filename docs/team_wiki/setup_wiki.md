# Set up your team wiki

We wish to give as much control as possible to teams in styling their project wikis and project documentations. For this reason, we are setting up [GitHub](https://www.github.com/) repositories so that teams can display their wikis using [GitHub Page](https://pages.github.com/).

iDEC teams are encouraged to be creative and to fully utilize the freedom that comes with the assigned GitHub repository.

If you are not familiar with the concept of Git and GitHub, imagine the following scenario:  

We are hosting a blog (iDEC HQ repository) that we write essays. You read some contents on your blog and you felt that something should change, so you downloaded (forked and cloned) a copy of our blog posts, made some edits (commits) on your own copy (your repository) and kept a chronological record of what and how edits are made (a history of commmits). Then, you send a note (pull request) to us, with those **edits (but not the modified blog posts)** attached. We reviewed the note, checked if the changes are reasonable or necessary, and decided to carry out (merge) the changes on our original blog posts.  

This is a simplified analogy on how software enigneers collaborate on projects. This year, iDEC HQ will piggy back on this mechanism to provide the wiki platform. So essentially, we will create iDEC HQ-owned repositories which are mostly empty, and an iDEC team will fork and clone that repository under their own their personal / organizational account. The team will then create wiki contents on its forked repository, and commit these changes. Once the team wiki is ready, the team shall submit a pull request to us. The request will automatically have the history attached, and when we accept the request, the history and hence changes will be reflected on the iDEC HQ-owned repository. The contents will be rendered as a publicly accessible websie through the GitHub Page function.  

## Wiki content upload and wiki freeze

The GitHub repositories for teams in 2021 will be hosted under the GitHub Organization "idec2021". For example, the team "idechq" will have the repository at:  
`https://www.github.com/idec2021/idechq`
To edit the wiki, iDEC teams will need to fork their assigned repository (base) under their personal / organizational account. All uploads and edits of wiki contents should then be performed on the forked repository (head). Before the wiki freeze deadline, an iDEC team should submit a pull request to update the base repository. iDEC HQ will accept any pull requests opened prior to the wiki freeze deadline and ignore any requests after the deadline. The iDEC team also needs to specify which branch they want the GitHub Page to be deployed from, and iGEM HQ will configure to the correct setting.

## Methods of creating the wiki contents

We do not impose restrictions on what technologies, packages, or languages that team use to generate their wikis. A wiki can be created using traditional HTML, CSS and Javascript, through a static site generator, or a content-management system, or anything else, so long as the final site is **static**.

By default, the assigned GitHub repositories are populated with template wiki contents. The wiki contents are rendered into a project documentation wiki site using MkDocs with the Material for MkDocs theme. This is a solution for teams who will not develop their own websites.

An example of such wiki is available [here](https://idec2021.github.io/team-wiki/).

We have a [introductory tutorial](mkdocs.md) that covers how to edit the contents using MkDocs.

If your team wish to use other technologies you can empty the assigned repository and upload your own web contents. This will necessitate a change in configuring the GitHub Page setting. Please notify iDEC HQ on which "Source" branch to be used in your pull request.

