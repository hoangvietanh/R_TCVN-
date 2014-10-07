R_TCVN-
=======

R code to convert TCVN3 to Unicode UTF-8 using command line tool uconv.exe  (unikey.org)

require("foreign")
setwd("c:/todel/uconv")
map=read.dbf(file="DARON_RUNGKK.DAT",as.is = TRUE,)
write.csv(map,file="in.csv")
system("uvconv in.csv -f TCVN3 -t UTF-8 -o out.csv",intern = TRUE, ignore.stderr = TRUE)
