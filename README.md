# asciitools
Miscellaneous tools for working with ASCII files, particularly data in columns

# Contents
asciimod
Simple additive or multiplicative manipulation of columnar ASCII data.  Modified lines
are printed to stdout.  Optional skip lines can be specified at the start of the file
and will be output unmodified.  

Usage:
    asciimod [options] file [ file2 ... ]

    Options: Help: --help, -? Brief help message --man Full documentation

            Required:
            --op                    Operation to perform, must be one of 
                                    add, sub, mult, or div
            --mod                   The number to modify by

            Optional:
            --column                Column to modify, defaults to 1
            --skip                  File header lines to skip over, defaults to 0
            --comment               Character(s) indicating a comment line to skip, 
                                    defaults to none
            --format                printf-stype format to use for modified field, 
                                    defaults to allowing Perl to decide
            --delimiter             Delimiter character[s] in the input file
            --output-separator      Delimiter in output file.  Defaults to the first 
                                    input delimiter character if specified, otherwise 
                                    defaults to two spaces

Options:
    --help, -?
            Prints a brief help message and exits

    --man   Prints the full manual page and exits

    --op    The operation to perform on the indicated column. Must be one of
            'add', 'sub', 'mult', or 'div'

    --mod   The value to use as the modification

    --column
            The column to modify, starting at 1. Defaults to 1 if not
            specified

    --skip  The number of lines at the header of the file to return without
            modification. Defaults to 0

    --comment
            One or more characters that indicate a comment line that is to
            be returned without modification. Defaults to no comment
            characters.

    --format
            The format to be used for the modified value (other values are
            returned as original). Default allows Perl to decide using its
            own default format.

    --delimiter
            One or more characters to be treated as column delimiters.
            Defaults to whitespace.

    --output-separator
            Character(s) to be used as an output separator. Defaults to two
            spaces or the first character of the --delimiter option