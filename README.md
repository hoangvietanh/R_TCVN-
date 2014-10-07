R_TCVN-
=======
R code to convert TCVN3 to Unicode UTF-8 using command line tool uconv.exe  (unikey.org)

uvconv [file] [OPTIONS]\n"
    file: Input file [Default: stdin - keyboard input]"
Options
    -h --help     Print Help and exit
    -f --from     Input charset [Default: TCVN3]
    -t --to       Output charset [Default: UTF-8]
    -o --output   Output file [Default: stdout - console output]
    -l --list     Print charset list and exit
    -m --mviqr    Mixed VIQR characters present in input
    -s --sviqr    Strict VIQR input, converting everything, not checking
                  escapes for URLs, etc. (a bit faster, but not recommended).
Example: 
    uvconv in.txt -f VNI -t UTF-8 -o out.txt
