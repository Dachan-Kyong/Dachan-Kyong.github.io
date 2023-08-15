---
title: "Create Github Blog (2): Github & jekyll Setup"
author: Dachan Kyong
date: 2023-08-03 16:00:00 +0900
categories: [Github Blog]
tags: [github blog]
collection: blog
render_with_liquid: false
---

## **Previous Post**
[Create Github Blog (1): MacBook Pro, M1, Initial Setup](http://127.0.0.1:4000/posts/creating-blog-1/)

## **Development Environment Setup**
- [Visual Studio Code](https://code.visualstudio.com/download): Download Apple silicon
- Jekyll
- Git


## **Creating Github Blog Pages**, based on August 2, 2023

### **Step 1**: Install Jekyll & bundler

```bash
gem install jekyll bundler // "this will install jekyll & bundler"

gem install github-pages // rendering dependencies

jekyll -v // "If jekyll 4.*.* shown success."

bundler -v // "If Bundler version 2.*.* shown success."
```

Then check versions:
```bash
jekyll -v // "If jekyll 4.*.* shown success."

bundler -v // "If Bundler version 2.*.* shown success."
```

### **Step 2**: GitHub Login and Repository Creation
- Go to [GitHub](https://github.com/), sign up and sign in. 
- Click **create a new repository** button.
    + **Repository name**: `YOUR_USERNAME.github.io`, where `YOUR_USERNAME` represents your GitHub username.
- Click **Create repository** button.

### **Step 3**: Git Installation & setting
As we already downloaded brew, we can install git through brew command in macOS terminal:
```bash
brew install git // "This will install git."

git --version // "If git version 2.*.* shown success."
```

As you created your Github, you need to set your `user.name` and `user email`:
```bash
$ git config --global user.name "YOUR_USERNAME"
$ git config --global user.email YOUR_EMAIL_ADDRESS
```
You can check registered account:
```bash
git config --list
```


### **Step 4**: Clone the created repository to a local environment
- Go to the repository you made.
- Click `Code`, a green dropdown button.
- Copy `HTTPS` URL.
- Create a Folder for Managing the Blog Locally in Your Desired Location.
- Open Visual Studio Code, press `F1`, search `Git: Clone`, and paste the copied URL.
- Go to the folder you created and select it as repository destination.

Now we are ready to create a blog through jekyll:
```bash
jekyll new ./ // "This will create blog related files."
```
Next, we need to install bundle and update it again:
```bash
bundle install // "This will install bundle."
bundle update // "This will update installed bundle."
bundle install // "This will install bundle again."
```
Let's check if everything is installed correctly by running the local server:
```bash
bundle exec jekyll serve // "This will run the local server."
```
We can visit the local server URL: <http://127.0.0.1:4000/> to confirm. If you can see the page with `Welcome to Jekyll!`, you are success.

If you see error related with `webrick`:
```bash
bundle add webrick
```

If there is no issue you can commit and push code to your github. You will see the deployed result in your github blog URL: `YOUR_USERNAME.github.io`.


We are now ready with the basic preparations to start a GitHub blog using a theme by jekyll on macOS, M1. The next post will cover how to apply the theme and commit and push the final code to github.

## References
- <https://mihee0703.tistory.com/49>
- <https://devpro.kr/posts/Github-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0-(2)/>