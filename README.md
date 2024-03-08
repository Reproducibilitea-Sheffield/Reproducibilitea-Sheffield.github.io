# Reproducibilitea-Sheffield.github.io

This repository is the source code for the [Reproducibilitea Sheffield](https://Reproducibilitea-Sheffield.github.io)
website.

## Creating a new Post

Typically you will have [booked a room](https://sites.google.com/sheffield.ac.uk/pooledroomdirectory/home) to hold the
event in and if money is available for catering have organised that too.

To create a new blog post you need to...

1. Have a GitHub account and be added as a collaborator on the repository.
2. Have cloned the repository locally.

Once setup you can then...

1. Ensure you are up-to-date with the `main` branch by `git pull`.
2. Create a branch locally, typically using your GitHub username and the issue number and date makes it easy to see what
   branches relate to, e.g. `ns-rse/2-dec-2023` was created by user `ns-rse`, it pertains to issue `2` which is about
   the `dec-2023` meeting.
3. Within the `posts` directory create a new sub-directory with the nomenclature `YYYY-MM` reflecting the year and month
   the event will happen.
4. Within the newly created directory create an `index.qmd` file.
5. Open the `2023-12/index.qmd` and copy and paste the contents into your new file.
6. Modify the `title`, `date` and `image` fields in the [YAML](https://yaml.org) header.
7. Edit the body of text (everything from line 29 onwards) to reflect the meeting you are organising. Be sure to
   include...
   + A link to the original paper.
   + The abstract as a Markdown quote.
   + Details of who is providing the brief summary of the paper.
   + Details of the room and building, with an [OpenStreetMap](https://openstreetmap.org) link to the building.
   + To get the URL for Google Calendar for people to add easily...
     1. Edit the event in the calendar and under _More actions_ select _Publish Event_.
     2. Copy the _HTML code_ and paste it into the web-page.
     3. Delete everything _except_ the URL that follows `href="` and everything after the closing double-quote.
     4. Use this in the `[link]` on line 59.
   + To get the Google Meet link
     1. Edit the event in the calendar and under the _Join with Google Meet_ button is a URL.
     2. Copy and paste this URL.
     3. Paste and replace the URL on line 62 and prefix it with `https://` i.e. it should read similar to `[Google
        Meet](https://meet.google.com/ehu-zapk-awt)`.

### Images

A useful source of images to use in posts are those produced for [The Turing
Way](https://the-turing-way.netlify.app/). Many can be found in the DOI
[10.5281/zenodo.3332807](https://doi.org/10.5281/zenodo.3332807) note there are different versions (linked from the
right hand side). Note however that these are the original images and are quite large files and so they can take a while
to load. An alternative option is to use the URL for the images in the GitHub repository for The Turing Way website
where [smaller versions of the images](https://github.com/the-turing-way/the-turing-way/tree/main/book/website/figures)
can be found, or you can use the URL from the image as hosted on the website itself (_Right Click > Copy Image Address_)

Regardless of the image source you should include the appropriate caption for the image which cites the images
correctly. For convenience you can copy and paste the Markdown below, replacing the `<insert_image_url>` with the URL of
the image.

``` markdown
![This illustration is created by Scriberia with The Turing Way community. Used under a CC-BY 4.0 licence. DOI:
[https://doi.org/10.5281/zenodo.3332807](https://doi.org/10.5281/zenodo.3332807)](<insert_image_url)
```

### Location Links

Trying to stick with the Open Source theme, links to building locations can be provided using
[OpenStreetMap](https://www.openstreetmap.org). Navigate, via zooming in, to the location of the building and
right-click on the map and select "_Center map here_" and you can then copy the URL ("_Ctrl + l_" followed by "_Ctrl +
c_" in most browsers) and paste that into the web-page you are creating.

### pre-commit

This repository uses [pre-commit](https://pre-commit.com) to check files and link Markdown using
[markdownlint-cli2](https://github.com/DavidAnson/markdownlint-cli2). If you are unfamiliar with Git Hooks and
pre-commit a useful article is [Pre-Commit : Protecting your future self](https://ns-rse.github.io/posts/pre-commit/)
(there are [subsequent posts on pre-commit](https://ns-rse.github.io/index.html#category=pre-commit)). Ideally you would
install `pre-commit` locally using the included `.pre-commit-configy.yaml` and `.markdownlint-cli2.yaml` files and
address issues before committing. If you don't do this locally the code will be checked when Pull Requests are made
using [pre-commit.ci](https://pre-commit.ci). Where possible fixes will be made automatically but sometimes the linters
can't fix all errors that they find. If this is the case the log-file from the linked check will explain what changes
need to be made.

## Meeting Setup

There is an [issue
   template](https://github.com/Reproducibilitea-Sheffield/Reproducibilitea-Sheffield.github.io/issues/new?assignees=&labels=meetings&projects=&template=meeting_setup.md&title=Prepare+session+on+%5BYYYY-MM-DD+HH%3Amm%5D+for+%5BLEAD+NAME%5D)
for setting up new meetings that details all of the tasks that are required for setting up a Journal Club and
advertising it. Where possible fill in details at creation time and tick off items (to tick of an item in Markdown put
in `x` in the square brackets, i.e. `[x]`).

## Links

+ [Reproducibilitea Sheffield Mailing List](https://groups.google.com/a/sheffield.ac.uk/g/reproducibilitea)
+ [Reproducibilitea Journal Club](https://reproducibilitea.org)
