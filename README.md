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
<tr><td style="width: 25%">`font=STRING`</td><td>[`monospace`] use a different font name, e.g., `font='Roboto Mono Light'`</td></tr>

<tr><td>`font-embed=INT`</td><td>
[`2`]. One of:
<ul>
<li>`0`: no embedding; not recommended unless you know what are you doing;</li>
<li>`1`: embed fonts in woff2 format; buggy, use with caution; works only with web browsers;</li>
<li>`2`: convert text to path; renders everywhere, but the resulting file size
could be an issue.</li>
</ul>
</td></tr>

<tr><td>`w=INT`</td><td>[`1920`] width of a viewport</td></tr>
<tr><td>`h=INT`</td><td>[`1080`] height</td></tr>
</table>

## Install

*dvisvgm* at least v3.4.1 is required, unless `font-embed=0`.

~~~
$ sudo dnf install inkscape mupdf
$ cargo install svgcleaner
$ npm i
~~~

## License

MIT
