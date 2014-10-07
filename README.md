R_TCVN-
=======

R code to convert TCVN3 to Unicode UTF-8 using command line tool uconv.exe (http://prdownloads.sourceforge.net/unikey/uvconv-w32-1.1.3b.zip)
uconv syntax
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

R code from here

require("foreign")
setwd("c:/todel/uconv")
map=read.dbf(file="DARON_RUNGKK.DAT",as.is = TRUE,)
write.csv(map,file="in.csv")
system("uvconv in.csv -f TCVN3 -t UTF-8 -o out.csv",intern = TRUE, ignore.stderr = TRUE)
