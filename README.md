# Talk: Puzzle Fonts About Puzzles

This repository contains slides for a talk “**Puzzle Fonts About Puzzles**”
(originally titled “**New Adventures in Puzzle Fonts**”),
presented (remotely) at the
[14th Gathering 4 Gardner Conference (G4G14)](https://www.gathering4gardner.org/g4g14/)
held April 6–10, 2022 in Atlanta, Georgia.

The slides demonstrate the following five
[interactive mathematical puzzle fonts](https://erikdemaine.org/fonts/)
about puzzles:

1. [Tetris Font](https://erikdemaine.org/fonts/tetris/)
2. [Sudoku Font](https://erikdemaine.org/fonts/sudoku/)
3. [Yin-Yang Font](https://erikdemaine.org/fonts/yinyang/)
4. [Path Puzzles Font](https://erikdemaine.org/fonts/pathpuzzles/)
5. [Tatamibari Font](https://erikdemaine.org/fonts/tatamibari/)

## [Watch Video](https://youtu.be/K6M3ELHr5Ls)

[Here's a recording](https://youtu.be/K6M3ELHr5Ls) of the live talk.

## [View Slides](https://edemaine.github.io/talk-puzzle-fonts-about-puzzles/)

[![Title slide](title_slide.jpg)](https://edemaine.github.io/talk-puzzle-fonts-about-puzzles/)

## Technology: reveal.js + KaTeX + Pug + Stylus + CoffeeScript <!--+ [SVG Tiler] + [SVG.js]-->

This repository uses the
[reveal-pug-talk template](https://github.com/edemaine/reveal-pug-talk)
to make slides by combining the following technology (all free and open source):

* [reveal.js](https://revealjs.com/): a flexible HTML presentation framework,
  extendable by plugins and themes.  Here we use:
  * [Chalkboard](https://github.com/rajgoel/reveal.js-plugins/tree/master/chalkboard):
    enables live drawing annotation on the slides (using pen or touch or mouse)
  * [Merriweather](https://fonts.google.com/specimen/Merriweather) font
  * [KaTeX](https://katex.org): a library for translating LaTeX math into HTML
* [Pug](https://pugjs.org/): a concise indentation-based notation for HTML,
  which makes it easier to express reveal.js slides,
  and to mix together other languages, such as the following
* [Stylus](https://stylus-lang.com/): a concise indentation-based notation
  for CSS (styling of HTML)
* [CoffeeScript](https://coffeescript.org/): an indentation-based language
  that compiles to JavaScript
<!--
* [SVG Tiler](https://github.com/edemaine/svgtiler):
  a library for converting ASCII art in slides into high-quality SVG graphics
* [SVG.js](https://svgdotjs.github.io/):
  a library that makes it easy to add animations to SVG drawings
  (including those made by SVG Tiler)
-->
* [Gulp](https://gulpjs.com/): a tool that builds the Pug code into HTML

## Structure

Here's an overview of the individual files and what they do:

* [`gulpfile.coffee`](gulpfile.coffee): Definitions of `build` and `watch`
  rules that run Pug on `index.pug` and compile other `.coffee` files to `.js`.
* [`index.pug`](index.pug): Top-level Pug file that calls all other files.
  Defines the top-level structure of the document, but has no slides.
* [`slides.pug`](slides.pug): Slides and specific animations are defined here.
* [`index.styl`](index.styl): Custom reveal.js styling,
  and specific styling for the slides.

<!-- Add any .coffee, images, etc. files here, if desired -->

## Build Instructions

To build the slides HTML (`index.html`) from the source files:

1. Install [NodeJS](https://nodejs.org/) if you haven't already.
2. Clone the repository
3. Run the following:

   ```sh
   npm install
   npm run build
   ```

If you're live-editing source files and want `index.html` to continually build
and update, use the following command:

```sh
npm run watch
```

To assemble just the needed files into a `dist` directory
(as defined by `deploySet` in `gulpfile.coffee`),
use the following command:

```sh
npm run dist
```

To deploy these files to GitHub Pages, use the following command:

```sh
npm run deploy
```
