# Easy Hugo Blog (EHB)

Easy Hugo Blog（EHB）is a GitHub Template repo for creating a Hugo blog rapidly just by click [Use this template](https://github.com/openpress/easy-hugo-blog/generate). 

It integrates several plugins/GitHub Actions to make things easy and simple.

* [gitfx shortcode plugin](https://gitx.io/post/hugo-with-gitfx-zh_cn/) helps to insert code snippets and its outputs in post automaticly
* [hugo-with-github-issues](https://github.com/skyfe79/hugo-with-github-issues) Action is used to create/edit new blog post in Issues and then added/updated to posts automaticly
* [peaceiris/actions-gh-pages](https://github.com/peaceiris/actions-gh-pages) Action helps to update posts to `<Your username/Orgnization>.github.io` automaticly

# Quick Start

### Use mono repo to edit posts and serve GitHub Pages

1. [Use this template](https://github.com/openpress/easy-hugo-blog/generate) to create a repo, name it as `<Your GitHub username/Orgnization>.github.io`.
2. To create new posts in `content/post` folder, and commit. Generated static content will be pushed to `gh-pages` automaticly 
3. Go to repo's `Settings` page, click `Pages` in left menu and set Pages' branch as `gh-pages` as below:

![](https://user-images.githubusercontent.com/1658618/194678227-1bd97f07-46e6-4d76-b3db-b77d9ef78b82.png)

4. A minute or two, your GitHub Pages site will be updated.

### Use one repo to edit posts, another one to serve GitHub Pages

(TBD)
