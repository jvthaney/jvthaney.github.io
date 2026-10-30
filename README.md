# jvthaney.github.io

The personal website of Jessica Trout-Haney, published at
**https://jvthaney.github.io**.

Freshwater ecology: plankton, cyanobacteria, and the food webs they make up.

## Updating the site

The site is plain HTML and CSS. There is no build step: whatever is committed to the
`master` branch is what visitors see, usually within a minute of pushing.

```bash
cd ~/Documents/GitHub/jvthaney.github.io
# edit index.html, add images, and so on
git add -A
git commit -m "Describe what changed"
git push
```

Or do the same through GitHub Desktop, which shows what changed before you commit.

To see a change before publishing it, open `index.html` in a browser straight from the
folder, or serve the folder locally so that paths behave exactly as they will online:

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## What is where

| Path | What it holds |
| --- | --- |
| `index.html` | the whole site: it is a one-page layout, so every section lives here |
| `images/` | photographs, figures and video used on the page |
| `images/gallery/` | the gallery, which needs a matching pair in `thumbs/` and `fulls/` |
| `assets/css/` | the stylesheet. `main.css` is generated from the Sass files |
| `assets/sass/` | the Sass source, only needed if the design itself is being changed |
| `assets/js/` | the scripts the template relies on |
| `assets/webfonts/` | icon fonts |

## Adding a picture

Resize it before committing. A photograph straight from a camera can be 10 MB or more,
which makes the page slow on a phone and the repository larger for ever, since git
keeps every version of every file.

```bash
sips -Z 2000 ~/Desktop/newphoto.jpg --out images/newphoto.jpg
```

That caps the longest side at 2000 pixels, which is ample for a full-width image and
usually brings a photograph under 1 MB. Then reference it in `index.html`.

Avoid spaces in file names: `under_ice.jpg` rather than `under ice.jpg`. Spaces work
locally and then cause odd failures once published.

## Credit

Built on the [Story](https://html5up.net/story) template by
[HTML5 UP](https://html5up.net), used under the
[Creative Commons Attribution 3.0 licence](https://html5up.net/license). The template's
own readme and licence are kept in `README.txt` and `LICENSE.txt`.

Icons from [Font Awesome](https://fontawesome.com). Scripts include
[jQuery](https://jquery.com) and
[Scrollex](https://github.com/ajlkn/jquery.scrollex).

Photographs are my own unless credited otherwise on the page.
