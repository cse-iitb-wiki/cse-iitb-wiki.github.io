---
layout: page
title: Contribution Guide
permalink: /contributing/
---

Edits to this wiki can be made by modifying the source .md files in the following github repo: [https://github.com/cse-iitb-wiki/cse-iitb-wiki.github.io/](https://github.com/cse-iitb-wiki/cse-iitb-wiki.github.io/) . If you do not have access, please message in the "IITB CSE PhDs" WhatsApp group. You may either create a new branch for your edits or push directly to `master` in case of small changes. If you create a new branch, then you must open a pull request and merge the branch to master in order for your changes to reflect on the site.


## Folder Layout
All content is in markdown (.md) files. Following is a useful resource for markdown: [https://guides.github.com/features/mastering-markdown/](https://guides.github.com/features/mastering-markdown/)

Following are useful folders:
* \_posts/ : contains all post .md files
* \_pages/ : contains all page .md files

**Posts** will be the main source of our shared knowledge. This is what you should generally create or edit.

**Pages** will generally contain meta information about the wiki. The landing page will contain helpful links to get started. 

Please read this short guide for creating and managing posts: [https://jekyllrb.com/docs/posts/](https://jekyllrb.com/docs/posts/) . Some of that information is also provided below to get you started.

## Editing a post

Edit the markdown file corresponding to a post. For example, to edit the post [CC Facilities](https://cse-iitb-wiki.github.io/cc-facilities/), you should edit the file 

```
_posts/2020-09-13-cc-facilities.md
```

Pages can be edited on github itself. Look for the edit button when browsing the file on github repository:

[![Screenshot-2020-09-13-cse-iitb-wiki-cse-iitb-wiki-github-io-2.png](https://i.postimg.cc/fRv2h086/Screenshot-2020-09-13-cse-iitb-wiki-cse-iitb-wiki-github-io-2.png)](https://postimg.cc/cvrMR6ym)

## Creating a post

Create a file in the \_posts directory in the following format
```
_posts/YYYY-MM-DD-post-title.md
```
This will appear at the following URL:
```
https://cse-iitb-wiki.github.io/post-title
```

Pages can be created on github itself - you don't need to install git. Look for "Add File" while browsing the `_posts/` folder. For example:

[![Screenshot-2020-09-13-cse-iitb-wiki-cse-iitb-wiki-github-io.png](https://i.postimg.cc/gkJxG9c4/Screenshot-2020-09-13-cse-iitb-wiki-cse-iitb-wiki-github-io.png)](https://postimg.cc/BtrSCVK1)

## Creating a page
Same as creating a post, except it must be added to `_pages/` folder.

## Adding a page to the nav bar
TBD

## Using Latex commands in markdown

Example latex:
```
$$x^2 + y^2 = 42$$
```
Renders as:

$$x^2 + y^2 = 42$$

More examples of latex: $$\pi^2$$, 

\(2+3^2\)

<!-- Github by default does not support latex/math. However, there is a workaround as mentioned in [this stackoverflow answer](https://stackoverflow.com/a/53981118/). 
In order to use math in a  -->

## Adding images/screenshots

Upload your image to [https://postimg.cc](https://postimg.cc) . They provide code to embed the image in various formats. Copy the code for Github Markdown (4th in the list) and paste to your .md file. For example,

```md
[![Alt-text for the image](https://i.postimg.cc/gkJxG9c4/Screenshot-2020-09-13-cse-iitb-wiki-cse-iitb-wiki-github-io.png)](https://postimg.cc/BtrSCVK1)
```
