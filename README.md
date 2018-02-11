# shelldoc
A shellscript documentation system

```
                __
               ▓#.▓▒
              ▓▓▓▓▒▒▒▒
              ▓▓▓
 ___/▓▓▓▓▓▓▓▒▒   ▏
<           ▒▒   ▏
 \ shelldoc  ▒  /
~~~~~~~~~~~~~~~~~~~~~~~
```

The  shelldoc  system provides a simple way to embed user documentation into Unix shell scripts. Shelldoc searches for specially formatted comments in text input (usually a Unix script file) on STDIN which are then emitted as the user documentation in reStructuredText format on STDOUT. All other code and standard comments within the source text are quietly ignored.

reStructuredText is a very lightweight form of markup that does not interfere with the human readability of the text. The [Docutils](http://docutils.sourceforge.net) project defnes the standard and provides filters to convert reStructuredText into html, latex (and on to PDF), and man format. Thus the same shelldoc documentation comments within a script can be extracted into a text file, a web page, a man page or a PDF file, covering all the main forms of electronic documentation.

The shelldoc script file serves as full documentation, a "feature-complete" test of the shelldoc system and an example for usage of all features of the shelldoc syntax.

Just do:

```
shelldoc < shelldoc
```

## Colophon
The mascot of shelldoc is a Shelduck -- _Tadorna tadorna_ (_Linnaeus_, 1758) -- a large and colourful duck found mainly in coastal areas across Eurasia. It nests in rabbit burrows or tree holes. The hatchlings leave the nest quickly and are led by their parents to nurseries on ponds lakes or rivers, often up to a mile away. There, they join other broods to form crêches of up to 100 young birds. A small number of adults stay behind to watch over these youngsters, while most of the parents fly off to join huge moulting flocks in coastal waters. These moulting flocks can contain many thousands of birds and are a spectacular sight on the Dutch and German Northern coast, as well as smaller gatherings on the Wash in England and the Firth of Forth in Scotland.
