# Wiki site for iDEC

Displayed site url: [wiki.idec.io](https://wiki.idec.io)

Root url: [idechq.github.io/idec-wiki](https://idechq.github.io/idec-wiki)

This iDEC Wiki is powered by [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/), which is a static site generator. Information are written in the Markdown language and saved as `.md` files under the `docs` directory. Whenever a commit is pushed to the repository a GitHub action (`.github/workflows/ci.yml`) is carried out to deploy the site to the branch `gh-pages`.

## A Docker container for preview while editing this wiki

Wiki contributors who are familar with Git, GitHub and Python can fork, clone this repository, make edits, and then push back to this repository. We recommend running the live server in a Docker container to ensure smooth installation. To do so, follow the steps below:

1. Open a command line terminal.  
   (For Windows users, open a PowerShell terminal / a linux distribution through WSL2).
2. In the terminal, navigate into the `idec-wiki` folder.
3. Create a Docker Image:  

       docker build -t squidfunk/mkdocs-material .
   
4. Set up a local live server:  

       docker run --rm -it -p 8000:8000 -v ${PWD}:/docs squidfunk/mkdocs-material  

   If an error message shows up here, please contact us at [support@idechq.org](mailto:support@idechq.org)
5. Open a browser and connect to `localhost:8000`  
   You should now see the wiki site being rendered locally.  

6. Hit `Ctrl + C` on your keyboard to exit the live server when done.

### Step-by-step guide

For editors who are new to Git, GitHub, Docker, we provide a [step-by-step guide](https://github.com/idechq/idec-wiki/wiki/SetupAnEditingEnvr) to setting up an environemnt on your computer for editing and collaborating. For editors who need to make changes to the navigation menu, please read the [Managing the navigation menu](https://github.com/idechq/idec-wiki/wiki/ManageNavigation) wiki page.

Editors who are new to the Markdown language can visit [commonmark.org](https://commonmark.org/), where you can pick up the language in as little as 10 minutes. It is recommended that editors set up a Markdown editor of thier choice. A list of recommendations can be found in a [blog post](https://www.oberlo.co.uk/blog/markdown-editors) written by Oberlo.
