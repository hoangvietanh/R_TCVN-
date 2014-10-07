R_TCVN-
=======

R code to convert TCVN3 to Unicode UTF-8 using command line tool uconv.exe (http://prdownloads.sourceforge.net/unikey/uvconv-w32-1.1.3b.zip)
R code from here

require("foreign")
setwd("c:/todel/uconv")
map=read.dbf(file="DARON_RUNGKK.DAT",as.is = TRUE,)
write.csv(map,file="in.csv")
system("uvconv in.csv -f TCVN3 -t UTF-8 -o out.csv",intern = TRUE, ignore.stderr = TRUE)
