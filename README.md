# Wiki site for iDEC

Present site url: [wiki.idec.io](https://wiki.idec.io)

Old site url: [idechq.github.io/idec-wiki](https://idechq.github.io/idec-wiki)

This iDEC Wiki is powered by [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/), which is a static site generator. Essentially, information are written in the Markdown language and saved as `.md` files under the `docs` directory. Whenever a commit is pushed to the repository a GitHub action (`.github/workflows/ci.yml`) is carried out to deploy the site to the branch `gh-pages`.

The Markdown language can easily format texts into HTML elements. Writers who are new to Markdown can use editors like [StackEdit](https://stackedit.io).

## A Docker container for preview while editing this wiki

Wiki contributors who are familar with Git, GitHub and Python can fork, clone this repository, make edits, and then push back to this repository. We recommend running the live server in a Docker container to ensure smooth installation.

We provide a step-by-step guide below assuming an editor is not yet familiar with any of the tools above.

### First time editors

1.  Register for a GitHub account
2.  Fork this repository under
3.  Install [Docker Desktop]()
4.  Install [GitHub Desktop]()
5.  In **GitHub Desktop**, clone this repository to your local computer.
6.  Open a command line terminal  
   (For Windows users, open a PowerShell terminal).
7.  In the terminal, navigate into the `idec-wiki` folder where this repository is cloned, i.e.:  
   `cd.. Documents/GitHub/idec-wiki`
8.  Run the command `ls`, you should see a file named `Dockerfile`.
9.  Create a Docker Image by running the following command:  
   `docker build -t squidfunk/mkdocs-material .`
10. Run the following command to set up a local live server:  
    `docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material`
11. Open your browser of choice (e.g. Chrome, Safari, Firefox, etc.),  
    connect to the live server by typing the following in the address bar and hit `Return`:  
    `localhost:8000`
12. Open a text editor, make any changes and save it.
13. Preview the changes in your browser, refresh the page if necessary.
14. When you are done editing and no longer need your browser, hit `Ctrl + C` on your keyboard to exit the live server.  
    Once you have done so, refreshing the page should give you a 404 error.
15. Open up GitHub Desktop again. By now it should have detected the changes you made.
16. Once you are certain that the changes are finalized, "commit" the changes.  
    It is always a good habit to leave a commit message that concisely summarizes what your changes are.  
    For example, "Add references for Genome Evolution page" is better than "Update Genome Evolution"  
    [Read more](https://chris.beams.io/posts/git-commit/) on how to write better commit messages.
17. In GitHub Desktop, "push" the commit(s) to your remote, forked repository hosted on GitHub.
18. Open a browser, travel to your forked repository on GitHub, the address should look be:  
    `https://www.github.com/{your username}/idec-wiki`  
    At this point, all changes you made are yours, i.e. they are not yet incorporated in our main repository.  
    Hence, not yet reflected on [wiki.idec.io](wiki.idec.io).  
    At the same time, you should see a message saying:
    > This branch is { a number } commits ahead of idechq:main.  

19. Click on the `pull request` link, which should be right next to the above message.
20. Click on the `Create pull request` button.  
    This page will show the differences between your edits and the original files.
21. Leave behind a subject and a message describing what the changes are, and submit the pull request.
22. Our wiki team will then review your edits and incorporate them if they are deemed ok.  
    The more information you provide, the easier it is for us to review your changes.  
    In cases where there are issues, our wiki team will reply to you in the thread and discuss the changes with you.

### Subsequent editing

The process of editing is the same as above. The only thing to bear in mind is to update your own local repository and incorporate any new changes made by others before you start. This can be done by doing a "fetch" on GitHub Desktop before starting step 6 above.
