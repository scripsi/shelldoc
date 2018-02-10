# shelldoc
A shellscript documentation system

The  shelldoc  system provides a simple way to embed user documentation
into Unix shell scripts. Shelldoc searches for specially formatted com‐
ments  in  text  input  (usually a Unix script file) on STDIN which are
then emitted as the user documentation in  reStructuredText  format  on
STDOUT. All other code and standard comments within the source text are
quietly ignored.
