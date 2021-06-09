# Configuring GitHub Pages settings

GitHub can render web contents hosted on your repository through its [GitHub Pages](https://pages.github.com) service, and to enable this you need to configure the corresponding settings correctly.

## Deploying your custom site

If you are building your static pages, you will need to change the default setting. We will assume that we have a repository structure as below, that is currrently under the branch `main`:

```yml
.
├─css
│   └─style.css
├─img
│   ├─favicon.png
│   └─icon.png
├─javascript
│   └─app.js
├─pages
│   ├─about.html
│   └─project.html
└─index.html
```

It can be inferred from the tree above that the home page of the site is `index.html`.  
Importantly, this file is placed in the **root** directory, or technically `./`

With these information, the following should be done:  
  
1. Go to the Pages settings for your wiki repository via the link  
    ```
    https://www.github.com/idec{year}/{assigned repo name}/settings/pages
    ```  
    You will see the user interface below:  
    ![GH Pages settings](img/tutorial_gh_pages.png){ width=600px }  

2. Click on the button that contains **Branch**

3. From the drop down menu, select the branch **main**

4. In the next button with a **folder icon**, select `/ (root)` as the path to deploy from  
    This is where the `index.html` file is.

5. Click on the **Save** button and save the settings.

6. Within a few minutes, you should be able to visit  
    ```
    https://idec{year}.github.io/{assigned repo name}
    ```  
    and your home page should now be displayed

## Deploying the default Material for MkDocs Wiki

If you decide to use the default wiki setup built with Material for MkDocs, you need not do anything as the settings is already configured for you. In case you changed it accidentally, you can always revert to the settings below:  

- Source branch: **gh-pages**
- Source folder: `/ (root)`