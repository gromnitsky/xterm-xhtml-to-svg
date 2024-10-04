A silly, but surprisingly effective method of producing a high quality
SVG from an XTerm screen dump.

1. Run any ncurses app in xterm, e.g., mutt.
2. Click <kbd>Ctrl + Mouse-1</kbd>, select `XHTML Screen Dump`; it'll
   generate an .xhtml file named `xterm.YYYY.MM.DD.HH.MM.SS.xhtml` in
   the directory in which xterm was started.
3. Type `./xterm-xhtml-to-svg i=file.xhtml o=output.svg`

To change the font, pass `font='Roboto Mono Light'`.

## Reqs

* `npm i puppeteer`
* `gem install nokogiri`
* `cargo install svgcleaner`
* `dnf install pdf2svg inkscape`

## License

MIT
