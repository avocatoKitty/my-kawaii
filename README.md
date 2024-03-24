# My Kawaii

This is a [Quarto](https://quarto.org) website for my blog of how to draw Kawaii animals.


## How to Add Posts

These instructions take you throw the steps require to add posts to the website.


### Drawing Scribbles

You need to have a new Scrbble to add to the website. This involves doing two drawings.

1. The picture you want to show how to draw.
2. The six steps to drawing the picture.

Draw these in a sketch book or on paper and use your phone to take pictures of them.

### Getting pictures from phone to laptop

The phone and laptop are setup so that when the phone is plugged in to charge it will automatically synchronise the
pictures from the phone to the laptop.

1. Turn the laptop on.
2. Plug the phone in to charge.

The pictures will be found under `/Users/isla/Pictures/phone/Camera/` and the filenames take the form
`IMG_YYYYMMDD_hhmmss###.jpg` where.

| Letters | Meaning                               |
|:--------|---------------------------------------|
| `YYYY`  | Year in four digits.                  |
| `MM`    | Month in two digits.                  |
| `DD`    | Day in two digits.                    |
| `hh`    | Hour in two digits (uses 24hr clock). |
| `mm`    | Minutes in two digits.                |
| `ss`    | Seconds in two digits.                |
| `###`   | Microseconds in three digits.         |

You can therefore work out the newest picture taken by looking at these dates. The _Finder_ application, started by
clicking on the icon with a smiley face with the left hand side blue and the right light-grey, lists files in ascending
chronological order so the newest will be at the bottom.

### Creating a new Page

1. Start RStudio.
2. Got to _File > Open Project_ and navigate to `/Users/isla/www/my-kawaii`, select the `my-kawaii.Rproj` file and open
   the project if it is not already open by default.
3. In the bottom right-hand panel select the _Files_ tab.
4. Navigate to the `posts` directory.
5. Use the _New Folder_ button to create a new folder and give it the current days date in the format `YYYY-MM-DD` (see
   table above for what these mean).
6. Open the folder you just created.
7. Use the _New Blank File_ button to create a _Quarto Doc..._ and call it `index.qmd`.
8. Open the `index.qmd` you just created, it will be empty. You need to add the following at the very top of the file
   (you can copy and paste this in).

``` yaml
---
title: "Scribble Scribble <drawing>"
author: "AvocatoKitty"
date: "YYYY-MM-DD"
categories: [drawing, <subject1>, <subject2>]
---
```

9. Replace `<drawing>` with the name of the drawing you are posting about.
10. Replace `YYYY-MM-DD` with the current date.
11. Replace `<subject1>` and `<subject2>` with words that indicate the something about the subject you are posting
    about. You can add just one word or you can add many.
12. Add some text about what you are drawing, e.g.

``` markdown
Today we are going to draw some shoes!

We have a picture of some shoes, scroll down to see how to draw them,
```

#### Copying Pictures

You now need to copy the pictures from `/Users/isla/Pictures/phone/Camera` to the directory you have created. You can do
this using _Finder_.

1. Open _Finder_ and navigate to `/Users/isla/Pictures/phone/Camera/`.
2. Find the two pictures you want to use, one will be of the final picture and one showing how to draw them.
3. Hold down the Command button and click both pictures.
4. Copy both pictures using the Command and C button.
5. Navigate to `/Users/isla/www/my-kawaii/posts/YYYY-MM-DD` for the folder you have just created (it will be today's
   date which is always shown in the top-right of the computer on the toolbar).
6. Paste the pictures into this directory.
7. Rename the pictures, the final image should be the name of the subject (e.g. `shoe.jpg`) whilst the picture that
   shows how to draw it should have the same name followed by `_draw` (e.g. `shoe_draw.jpg`).

#### Including Pictures

You now need to go back to RStudio and include links to these images in the `index.qmd` that you created.

Links to pictures look like this.

``` markdown
![This is a scribble of some shoes](shoes.jpg)

![This is how scribble some shoes](shoes_draw.jpg)
```

The images should appear underneath, if they don't check very carefully the filenames.

Once the images are showing in-line save the `index.qmd` by pressing Command and `s` (or `Ctrl + s`). RStudio/Quarto
should render the web-page and open it in the Firefox Web browser. Read it carefully and make user there are no
mistakes, if there are return to RStudio and correct them. RStudio will probably show you spelling and grammar errors by
underlining them with a faint wavy line.


### Publishing the Page

Once you are happy with the changes you need to publish them. This means moving your changes from the laptop to
somewhere on line, in this case the [GitHub repository](https://github.com/avocatoKitty/my-kawaii) where the website
will be updated and the new page published.

To do this you need to stage your changes and commit them to Git then "push" the changes to GitHub. In the top-right
panel there is a "Git" tab, it will list the new files.

1. Tick the boxes next to each file underneath the _Stage_ column.
2. Once all are ticked click the _Commit_ button a new window will appear.
3. In the top-right of the new window is a box labelled _Commit message_. Add a short message such as "_Adding a
   scribble about shoes_".
4. Click the Commit button, the window should disappear.
5. In RStudio in the top-right panel on the _Git_ tab you can now click the _Push_ button which copies your new files to
   GitHub.

GitHub will automatically build your website. You can check the status of this build process by going to
[here](https://github.com/avocatoKitty/my-kawaii/actions). The build in progress will have a yellow circle button next
to it, if it completes successfully it will change to a green circle with a tick in it. You can click on either and see
the build stages and click on these to see the steps happening.
