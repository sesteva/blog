## Requirements

There are two options:

### Option 1 - Using Docker

Docker is way of shipping replicable environments.
This option requires you to setup Docker only.

Follow instructions for your operating system.

- [Mac][3]
- [Windows][4]
- [Linux][5]

## Option 2 - Installing all dependencies on your local computer.

You can follow the instructions provided at [Jekyll Installation Guide][6]

## Setup

Clone the blog into your desired local folder. Example:

    cd /Projects/Sabre/one
    git clone thisRepo

## Running the blog locally

Depending on which option you went on the requirements

### Using Docker

Go into the blog's folder

    cd ~/Projects/Sabre/one/blog
    sudo docker run --name sabre-one-blog --rm -v "$PWD:/src" -p 4000:4000 grahamc/jekyll serve -H 0.0.0.0

You can access the site at localhost:4000

While this is running, you can edit the files and see the site change live.

### Without Docker

    cd ~/Projects/Sabre/one/blog
    jekyll serve -w

You can access the site at localhost:4000

While this is running, you can edit the files and see the site change live.

## Flow - Writing a new entry

Create a new file in _posts

     ---
     layout: post
     title:  "This is the tile"
     date:   2015-01-16 21:39:54
     categories: lookAndFeel
     ---

     This is the text of my post

 Then add/commit/push

    git commit -am "New articule on look and feel"
    git push

The automated build/deploy system will take care.

If you would like to know more on the Engine being used for this static site please visit [Jekyll][1].
If you would like to know more on writing markdown please review this [Markdown Cheat Sheet][2]

[1]: http://jekyllrb.com/docs/structure/ "Jekyll"
[2]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet "Markdown Cheat Sheet"
[3]: https://docs.docker.com/installation/mac/
[4]: https://docs.docker.com/installation/windows/
[5]: https://docs.docker.com/installation/ubuntulinux/
[6]: http://jekyllrb.com/docs/installation/





