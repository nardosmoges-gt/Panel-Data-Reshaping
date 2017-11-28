# Panel-Data-Reshaping
x <- read.table(header=T, text="
X    Y D 
a 2010 10
a 2011 20
a 2012 50
b 2010 40
b 2011 30
b 2012 60
c 2010 10 
c 2011 20
c 2012 25")

x=data.frame(x)#######stores data as data frame
g=data.frame(reshape(x, idvar="X", timevar="Y", direction="wide")
)######this transforms the data with individual observations listed horixontally and Year listed vertically.
