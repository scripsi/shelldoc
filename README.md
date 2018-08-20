
# shelldoc

A shell script documentation system

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

The _shelldoc_ system provides a simple way to embed user documentation into Unix shell scripts. _shelldoc_ is a Bourne shell compatible script that searches for specially formatted comments in text input (usually a Unix script file) on STDIN which are then emitted as the user documentation in reStructuredText format on STDOUT. All other code and standard comments within the source text are quietly ignored.

reStructuredText is a very lightweight form of markup that does not interfere with the human readability of the text. The [Docutils](http://docutils.sourceforge.net) project defnes the standard and provides filters to convert reStructuredText into html, latex (and on to PDF), and man format. Thus the same shelldoc documentation comments within a script can be extracted into a text file, a web page, a man page or a PDF file, covering all the main forms of electronic documentation.

Other text documentation, such as README files, licenses and version histories can also be included in the source text as numbered appendices. This makes it possible to maintain and distrubute a single script file that contains all of its necessary user documentation.

The _shelldoc_ script file serves as full documentation, a "feature-complete" test of the shelldoc system and an example for usage of all features of the shelldoc syntax.

## Installation and use

Download the [shelldoc](https://github.com/scripsi/shelldoc/raw/master/shelldoc) script file and save it somewhere in your $PATH, for example:

```
~/bin/shelldoc
```

then make sure that it is executable:

```
chmod +x ~/bin/shelldoc
```

Then you can try the following commands to see how it works:

```
# print shelldoc's documentation to the terminal:
shelldoc < shelldoc
# or view it as a manual page (requires Docutils):
shelldoc < shelldoc | rst2man | man -l -
# or save it as a web page (requires Docutils):
shelldoc < shelldoc | rst2html | shelldoc.html
# or save it as a plain text file:
shelldoc < shelldoc > shelldoc.txt
# view the licence:
shelldoc -a 1 < shelldoc
# save the version history:
shelldoc -a 2 < shelldoc > versions.txt
# save this readme file:
shelldoc -a 3 < shelldoc > README.md
# add a documentation template to another script:
shelldoc -t < myscript > mydocumentedscript
# strip documentation from a script:
shelldoc -s < mydocumentedscript > mycleanscript
```

## Colophon

The mascot of shelldoc is a Shelduck -- _Tadorna tadorna_ (_Linnaeus_, 1758) -- a large and colourful duck found mainly in coastal areas across Eurasia. It nests in rabbit burrows or tree holes. The hatchlings leave the nest quickly and are led by their parents to nurseries on ponds lakes or rivers, often up to a mile away. There, they join other broods to form crêches of up to 100 young birds. A small number of adults stay behind to watch over these youngsters, while most of the parents fly off to join huge moulting flocks in coastal waters. These moulting flocks can contain many thousands of birds and are a spectacular sight on the Dutch and German Northern coast, as well as smaller gatherings on the Wash in England and the Firth of Forth in Scotland.
