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
<tr><td>font=STRING</td><td>monospace</td><td>use a different font name, e.g., <code>font='Roboto Mono Light'</code></td></tr>

<tr><td style="white-space: nowrap;">font-embed=INT</td><td>2</td><td>
One of:
<ul>
<li>0: no embedding; <code>monospace</code> fallback is added automatically;</li>
<li>1: embed fonts in woff2 format; works only with web browsers (at
the time of writing, webkit-based have minor rendering issues);</li>
<li>2: convert text to path; renders everywhere.</li>
</ul>
</td></tr>

<tr><td>w=INT</td><td>1920</td><td>width of a viewport</td></tr>
<tr><td>h=INT</td><td>1080</td><td>height</td></tr>
</table>

## Install

*dvisvgm* at least v3.4.2 is required, unless `font-embed=0`.

~~~
$ sudo dnf install inkscape mupdf
$ gem install nokogiri # only for font-embed=0
$ cargo install svgcleaner
$ npm i
~~~

## License

MIT
