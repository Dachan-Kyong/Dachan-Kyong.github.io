---
title: "Create Github Blog (3): Applying Jekyll Chirpy Theme"
author: Dachan Kyong
date: 2023-08-02 13:00:00 +0900
categories: [Github Blog]
tags: [Github_blog]
collection: blog
render_with_liquid: false
---

## **Previous Posts**
[Create Github Blog (1): MacBook Pro, M1, Initial Setup](http://127.0.0.1:4000/posts/creating-blog-1/)

[Create Github Blog (2): Github & jekyll Setup](http://127.0.0.1:4000/posts/creating-blog-1/)

## **Applying Jekull Theme**

### **Step 1**: Download Chirpy Theme

- Go to [jekyllthemes.org](http://jekyllthemes.org/themes/jekyll-theme-chirpy/) and download jekyll-theme-master.zip file (used version 6.1.0)


### **Step 2**: copy and paste to the local folder created before
- copy all the files and replace the files already created before with them.

```bash
tools/init // "This will initialize."

npm install // "This will install node modules and create files need be created, which prevents errors: * internal script /assets/js/dis/***.min.js does not exist (line 1)"
```

### **Step 3**: Configuration: Config.yml & .gitignore
For `Config.yml` (in order):
- `lang`: Change displayed language. Check options available in your `_data/locales`.
- `timezone`: Change time.
- `title`: This will be your main title.
- `tagline`: This will be your sub-title.
- `description`: This will be displayed in your .xml.
- `url`: change to your GitHub blog URL. If you don't change you cannot build and deploy.
- `github` > `username`: This will be your GitHub username.
- `social` >: This will be displayed as the default author of the posts and the copyright owner in the Footer.
    + `name`: Change to your name.
    + `email`: Change yo your email address.
- `avatar`: change to your avatar image.

For `.gitignore`:
- Add: `Gemfile.lock`
- Add `node_modules`


### **Step 4**: Github Pages Setting
Go to `Settings` > `Pages`:

For **Source**, you need to set it as `Deploy from a branch` to `GitHub Actions`. And click `GitHub Pages Jekyll` > `Configure` button and Commit Changes. This will create `jekyll.yml` in `.github/workflows` on your main branch. We need this setting to prevent `Error:  The jekyll-theme-chirpy theme could not be found.`

if you cannot build `jekyll.yml` with an error `Error: The process '/opt/hostedtoolcache/Ruby/3.1.4/x64/bin/bundle' failed with exit code 16`, this is because of playforms difference. Since M1 MacBook uses x86_64-linux you need:

```bash
bundle lock --add-platform x86_64-linux // "this will add x86_64-linux platform in your Gemfile.lock."
```

For **Branch**, you need to set it as:
`main` > `/(root)`

There are many information related to `gh-pages` branch, but I decided to utilize Author's orginal setting. So this post will not show how to initialize and start a blog from nothing.


### **Step 5**: Commit & Push to Your Github

```bash
git init // "initialization"
git add . //
git commit -m "Applying Jekyll Chirpy Theme" // "A commit message."
git push origin main // "Push to your main branch"
```

Now we are ready to start our blog with chirpy theme. In future blog posts, I will delve into additional usage methods and settings.

## References
- <https://kiffblog.tistory.com/233>
- <https://1221jyp.com/posts/github-blog_2/>
- <https://www.irgroup.org/posts/jekyll-chirpy/>