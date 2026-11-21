# 📰 Stus-News-Web
Welcome to the GitHub repository for the Stu's News website! :D</br>
If you don't know what's going on here, this place hosts the source code that runs the website.
If you do, I'll try to make this README as useful as possible :)

## Contributing
If you have any ideas, find any errors, or would like to improve something, feel free to [submit an issue](https://github.com/DanielBdT-git/stus-news-web/issues/new) or [fork this repo](https://github.com/DanielBdT-git/stus-news-web/fork) and make a pull request. I'll do my best to keep in touch and maybe I'll merge your stuff :)</br>
###### please don't use AI though

## Uploading Stories
Until I get the CMS up and running, contributors can simply upload a markdown file in `/src/pages/stories`. If you want to do so and are not a contributor, you may [fork the repo](https://github.com/DanielBdT-git/stus-news-web/fork) and submit a pull request.

Here's how to upload stories manually:
1. either come right back to this GitHub repo or clone it in your terminal and `cd` into it
2. make sure you're in the "**uploads**" branch
    - if you're using your browser, it's in the top-left somewhere
    - if you're using your terminal, use `git checkout uploads`
3. head to `/public/story_images` and place your image there if you want to upload one. The WebP image format is strongly encouraged as it tends to load faster. You may also use an image from the internet; that will come back in step 5.
    - if you're using your browser, click "Add file" and choose "Upload files"
4. head to `/src/pages/stories` and make a new file named `[week_number]-[story_number]-[title].md`, which would look something like: `3-2-story-title.md`. Make sure you keep everything lowercase and use hyphens instead of spaces. Note that this naming scheme is temporary and I will get rid of week/story numbers in the near future. This just makes it easier for me while the site is in development
    - if you're using your browser, click "Add file" in the `stories` folder
    - if you're using your terminal, just make the file at that directory
5. paste the [template](#markdown-template) into the file and fill in every data field *except `layout`*.
    - `image.url` can take either a web link (obtained through "copy image link") **or** a filepath relative to `/public`. For example, an image at `/public/story_images/image.webp` is expressed as `url: /story_images/image.webp`.
    - you may omit `credits.sources` if you did not use any. In that case, delete that entire line.
6. commit (and push if using your terminal) your changes to the "uploads" branch.
> [!important]
> Remember to `git pull` before doing anything if you're using your terminal

### What happens next
Once all that is done, I will review and (hopefully) merge your story into the "main" branch to publish it 😄

### Markdown Template
```md
---
layout: "/src/layouts/StoryLayout.astro"
title: "Story Title"
author: "Author's Name"
date: YYYY-MM-DD
image:
  url: "https://example.com/image"
  alt: "Describe the image"
credits:
  image: "Where you got it / who took it"
  sources: ["https://source.com/article"]
---
This is where the actual story goes.
```

## Development
The website is built with the [Astro framework](https://astro.build). You can read their docs [here](https://docs.astro.build).</br>
I'm also planning to use [Pages CMS](https://pagescms.org/) to make adding content super easy :)

Here's a list of essential commands for development. Make sure you have nodejs and npm installed and that you're currently in the project directory (`.../stus-news-web`).
|🧑‍💻 Command|Fuction|
|-------|-------|
|`npm install`|Install all dependencies|
|`npm run dev`|Start the live dev server|
|`npm run build`|Build the project into the `dist` folder|
|`npm run preview`|Preview what's in the `dist` folder|

## Deployment
I'll be using Vercel to deploy the website and I'll probably buy a domain from [Web Hosting Canada](https://whc.ca/en). While the site is still in development, it'll be deployed as https://stus-news-web.vercel.app, which will also be used as a fallback in case I encounter any issues with the custom .ca domain.

## Tasks
|📋Item|Status|
|----|------|
|Initial Setup|🟢done|
|Basic Functionality|🟡working|
|Accessibility|🔴to do|
|Pages CMS|🔴to do|
|Newsletter|🔴to do|
|Donations|🔴to do?|
