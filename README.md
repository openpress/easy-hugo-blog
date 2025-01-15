# Easy Hugo Blog (EHB)

Easy Hugo Blog（EHB）is a GitHub Template repo for creating a Hugo blog rapidly just by click [Use this template](https://github.com/openpress/easy-hugo-blog/generate). 

It integrates several plugins/GitHub Actions to make things easy and simple.

* [gitfx shortcode plugin](https://gitfx.github.io/post/hugo-with-gitfx/) helps to insert code snippets and its outputs in post automaticly
* [hugo-with-github-issues](https://github.com/skyfe79/hugo-with-github-issues) Action is used to create/edit new blog post in Issues and then added/updated to Hugo posts automaticly
* [peaceiris/actions-gh-pages](https://github.com/peaceiris/actions-gh-pages) Action helps to deploy posts to `<Your username/Organization>.github.io` automaticly

# Quick Start

### Use mono repo to edit posts and serve GitHub Pages

1. [Use this template](https://github.com/openpress/easy-hugo-blog/generate) to create a repo, name it as `<Your GitHub username/Orgnization>.github.io`.
2. To create new posts in `content/post` folder, and commit. Generated static content will be pushed to `gh-pages` automaticly 
3. Go to repo's `Settings` page, click `Pages` in left menu and set Pages' branch as `gh-pages` as below:

![](https://user-images.githubusercontent.com/1658618/194678227-1bd97f07-46e6-4d76-b3db-b77d9ef78b82.png)

4. A minute or two, your GitHub Pages site will be updated.

### Use one repo to edit posts, another one to serve GitHub Pages

Use case:

A GitHub Free Plan account cannot use the GitHub Pages in a private repository. To make your source contents private and deploy it with the GitHub Pages, you can deploy your site from a private repository to a public repository.

Take your username/Organization as `openpress` for example: 

* `openpress/homepage`: A private repository of `Easy Hugo Blog` template
* `openpress/openpress.github.io`: A public repository using GitHub Pages

Note: the two repos must belong to one user/organization.

And you need use `deploy_key`. Firstly set your private key to the private repository, and ensure that the Name is set as `ACTIONS_DEPLOY_KEY` 

![WX20221008-114114@2x](https://user-images.githubusercontent.com/1658618/201357562-cedbacc6-0cac-4245-bd03-0b617090c211.png)

and set your public key to your public repository. 

![WX20221006-161458@2x](https://user-images.githubusercontent.com/1658618/201357645-e660f17a-c306-4806-92b0-05da6992f64e.png)

Note: You can [use ssh-keygen Template](https://github.com/gitfx/ssh-keygen-template) to create a `deploy key` in GitHub repo instead of commandline.

Then just create posts and set the public repo's GitHub Pages' branch as `gh-pages`.

Done!
