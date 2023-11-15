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

It can be useful to include openly licensed images in the web-page. These can be linked to directly if the image is on
the internet.

### Location Links

Trying to stick with the Open Source theme, links to building locations can be provided using
[OpenStreetMap](https://www.openstreetmap.org). Navigate, via zooming in, to the location of the building and
right-click on the map and select "_Center map here_" and you can then copy the URL ("_Ctrl + l_" followed by "_Ctrl +
c_" in most browsers) and paste that into the web-page you are creating.

## Links

+ [Reproducibilitea Sheffield Mailing List](https://groups.google.com/a/sheffield.ac.uk/g/reproducibilitea)
+ [Reproducibilitea Journal Club](https://reproducibilitea.org)
