# qMRLab website

This public repository contains all the material for publishing the qMRLab website (https://qmrlab.org/). Commits merged to this repository will trigger an automated build to generate html pages to be published. For detailed information please visit [here](https://pages.github.com/).

## For content contributors


### Frontpage: _includes/qmrlab-top.html

The carousel that appears at the top of the page.

To add a new image to the carousel: i) upload the image under assets/images and ii) add respective entry to the _data/carousel.json file. This entry should contain the following key-value pairs:

* `image`: the name of the image as stored under /assets/images/
* `label`: the label that is going to be displayed under the image
* `color`: the color of the label

### Frontpage: _includes/qmrlab-about.html

The about section that appears just below of the carousel.

### Frontpage: _includes/contributors.json

The contributors section that appears below the Featured posts section.

The section is built up using the information contained in the _data/contributors.json file.
Entires in the contributors.json have the following format for each author:

`name`: Full name of the contributor.
`twitter` (Optional): A link to contributor's twitter account
`github`: A link to contributor's GitHub account. This link fetches the contributor's GitHub profile picture to display it.
`facebook` (Optional): A link to contributor's Facebook account.

If the contributor does not have Twitter of Facebook account, please assign the respective field with the `#` entry.

### Frontpage: _includes/affiliation.html

The affiliations section that appears at the bottom of the Frontpage.

This section is based on the information contained in the _data/affiliations.json file.

Entries in the affiliations.json respect the following format:

`name`: The name of the institution.
`image` : The name of the affiliation's image file as stored under /assets/images
`web`: A link to the affiliation's website


## How to add new posts?

### 1) Add author information to the _config.yml file.

Please add an entry in this file (under the 'authors' field) to link your name and GitHub account (along with additional information). For example:

```
nickname:
  name: Jon Doe
  display_name: Jonny Doe
  email: jonny@gmail.com
  git_name: jodoe
  web: http://jondoe.com
  twitter: https://twitter.com/jodoe
  description: `Interested in qMRI. He is a coffee master ....`
```
* `name`: Self-explanatory
* `nickname`: Displayed under your profile photo in a blog post. Please keep it short (due to layout concerns).
* `github`: Your GitHubhandle. *Required*
* `twitter`: (Optional) Your twitter handle. A link will appear under your image in a blog post.
* `website`: (Optional) A link to your personal website (or other). A link will appear under your image in a blog post.

### 2) Creating a new post

All blog posts that are written in markdown language are stored in `_posts` directory.
Please respect the following convention for naming of the markdown files:

`YYYY-MM-DD-the_name_oft_the_file.md`

All `.md` posts must start with the following snippet:

```
---
layout: post
title:  "The title of the post"
author: Author's_Nickname
categories: [ jekyll ]
image: assets/images/image_name.png
featured: false
hidden: false
---

```

* `title` is the title of the post.
* `author`  is the nickname of the author (see previous step).
* `image` is the link to the featured image (e.g. assets/images/foo.png).  
* The `featured` and `hidden` takes boolean inputs (true/false) to set the visibility of the post and that of the featured image, respectively.

* IMPORTANT NOTE: Please avoid modifications to the layout of the snippet. The `categories` tag should always contain the '[ jekyll ]' entry.


After completing these steps, you can start creating the body your post.

* NOTE: As stated above, posts should be written in markdown language.
Once you are done with creating the post, please save it in the '_posts' folder by following the naming convention described above. Commit your changes and make a pull request.


## Problems / Suggestions ?

If you encounter any issues with the website or have any suggestions, please create a new GitHub issue [here](https://github.com/qMRLab/qmrlab.github.io/issues).
