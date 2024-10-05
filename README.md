A silly, but surprisingly effective method of producing a high quality
SVG from an Xterm screen dump.

1. Run any ncurses app, e.g., htop.

2. Click <kbd>Ctrl + Mouse-1</kbd>, select *XHTML Screen Dump*; this
   will generate an .xhtml file named
   `xterm.YYYY.MM.DD.HH.MM.SS.xhtml` in the directory in which Xterm
   was started.

3. Type `./xterm-xhtml-to-svg i=input.xhtml o=output.svg`

### Options

<table>

<tr><td>`font=`</td><td>use a different font instead of `monospace`, e.g., `font='Roboto Mono Light'`</td></tr>

<tr><td>`w=`</td><td>set width of a viewport in case the screenshot doesn't fit in 1920px</td></tr>

<tr><td>`h=`</td><td>height</td></tr>

</table>

## Install

~~~
$ sudo dnf install inkscape poppler-utils
$ gem install nokogiri
$ cargo install svgcleaner
$ npm i
~~~

## License

MIT
