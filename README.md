# Schreibtischtäter

## Rücken- und andere Leiden lindern

In dieser Präsentation geht es um einseitige Belastungen des Körpers
durch das viele Sitzen vorm Rechner.  Es wird auf die Einseitigkeit und
Art der Belastung auf den Körper eingegangen.  Und es werden Übungen und
Strategien gezeigt, um die einseitigen Belastungen möglichst
auszugleichen.


----


## Technical Details

This is a [reveal.js](http://lab.hakim.se/reveal-js/) presentation
([source](https://github.com/hakimel/reveal.js)) which means that this
presentation is a static HTML5 website using a lot of JavaScript and CSS.

The presentation itself (file `slides.md`) is written in [markdown][4].


## Open The Presentation:

Several possibilities exist:


### Open `index.html` Directly

Just open file `index.html` with Firefox:

    firefox index.html

(Does not work with Chromium which does not import the markdown file
`slides.md`.)


### Serve locally

Assure the symbolic links exist required for starting from within the subdir
`reveal.js`:

```sh
ln -snf  ../img  img
ln -snf  ../index.html  index.html
ln -snf  ../reveal.js  reveal.js
ln -snf  ../slides.md  slides.md
```

Change into `reveal.js` subdir, update third libs and start the site:

```sh
cd reveal.js
npm update  # only required once
npm start
```

Open with your browser:

http://localhost:8000

Hints:
* Works better (and smoother) with Chromium than with Firefox
* [Speaker Notes](https://github.com/hakimel/reveal.js#speaker-notes)
  (*push 's'*) and PDF export require Chromium/Chrome


### Open github.io page

If this repo has its origin master repo at github and githup page is configured
to build from 'master' branch open this URL:

 https://theno.github.io/presi-nacken


## Create PDF

You need the URL of the presentation, either served locally or from github.
Then, [use decktape](https://github.com/astefanutti/decktape#usage):

```sh
cd ~/bin/decktape/active && \
./phantomjs decktape.js --size 1280x800  URL  ~/repos/my_presi/my_presi.pdf
```
(decktape [install command][2])

Or just print the `slides.md` rendered by github into a PDF:

https://github.com/theno/presi-nacken/blob/master/slides.md


[1]: https://github.com/theno/fabsetup/blob/master/howtos/revealjs.md
[2]: https://github.com/theno/fabsetup/blob/master/howtos/revealjs.md#create-pdf-of-the-presentation-with-decktape

[3]: http://lab.hakim.se/reveal-js/
[4]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
[5]: http://www.fabfile.org/
[6]: https://github.com/theno/fabsetup
