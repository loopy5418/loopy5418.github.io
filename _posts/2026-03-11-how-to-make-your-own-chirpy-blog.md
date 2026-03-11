---
title: "How to make your own chirpy blog in 10 minutes"
date: 2026-03-11 02:50:00 +03:00
categories: ["Generic Tutorials"]
tags: ["Jekyll", "GitHub Pages"]
author: loopy
---

When you first entered TLog, you probably thought to yourself: "Wow, this website is so cool and fast.". <span class="text-muted">(or maybe im just going crazy)</span>
If you did, you're in luck. Because you can make your own Chirpy blog within just 10 minutes!

# Creating the repository
To make our life a thousand times easier, we will be using a pre-made chirpy template. Head over to [cotes2020/chirpy-starter](https://github.com/cotes2020/chirpy-starter).
Since this is a template repository, we can easily use the repository to clone and modify it to our needs. Click the very big "Use this template" button, and then click "Create a new repository".
> If you do not see the "Use this template" button, please make sure you're signed in.
{: .prompt-info }
You do not need to change that many options when creating the repository. The only stuff you have to do are:
- Make sure the repository's name is `yourname.github.io` <span class="text-muted">(make sure you replace **yourname** with your actual GitHub username)</span>
- Set the repository's visibility to **Public**
- Leave the Copilot field empty
After that, your repository should be created after a few seconds. If you check the "Actions" tab, it will show Ruby's build and deployment stage in real time. When all stages are done, the plain template should be available to view at `yourname.github.io`.
> **Nice Fact:** GitHub Pages will never limit your hosting or charge you for hosting. It is a thousand percent free.
{: .prompt-tip }

# The _config file
Now comes the most important part. Configuring Chirpy will pick how it looks, functions, and gets the data about you.
(Optional) Clone and cd into your repository by running: 
```bash
git clone https://github.com/yourname/yourname.github.io.git && cd yourname.github.io
```
Start editing the `_config.yml` file. Every option is well-explained by the comments, but I will still explain what to touch and what not to touch:
- Make sure you set the `url` field to your blog's domain. Include the `https://`.
- In the `social.links` field, the first URL you list will be the one readers are redirected to when they click your name.
- To add an avatar from local assets, upload your image to the `assets/` folder. From there, you can link that image to the `avatar` field by just setting it to `/avatar/filename.jpg`.

# The first post
To create a post, make a new file in the `_posts` folder.
> The post file's name format should be `YYYY-MM-DD-post-name.md`.
> So if the date is March 11th 2026, the file name should be `2026-03-11-this-is-my-post.md`.
{: .prompt-warning }
Add the markdown table below to the very beginning of your file:
```md
---
title: "How to find huzz"
date: 2026-03-11 10:50:00 +03:00 # Date Formst: YYYY-MM-DD HH-MM-SS +/-OFFSET
categories: ["Category 1"]
tags: ["Tag 1", "Tag 2"]
---
```
This contains the basics of a posts metadata. The rest of the file can be your post in markdown.
Now push your changes to your GitHub repository by running
```bash
git add .
git commit -m "Customize chirpy and make first post"
git push origin main
```

# Conclusion
After the building stages complete, your Chirpy site should be available to view and browse.
You can also edit tabs in `_tabs`, like the about tab or adding more tabs.
Be sure to expetiement a lot and improve your site to your liking.

> That's it for this post. If you have any questions, or need help troubleshooting, please feel free to mail me at lo@5418.org, or by messaging me on Discord (@loopy5418)
{: .prompt-info }
