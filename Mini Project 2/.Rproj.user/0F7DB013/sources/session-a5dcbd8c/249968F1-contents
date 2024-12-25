res.figs <- function(modObj)
{

# to obtain diagnostic values
std.res <- rstandard(modObj)
fit.vals <- fitted(modObj)
lev.vals <- hatvalues(modObj)
cook.dist <- cooks.distance(modObj)


#cut off for leverage
p <- length(coefficients(modObj))
n <- summary(modObj)$df[2] + summary(modObj)$df[1]
lev.cut <- (2*p)/n


par(mfrow=c(2,2)) 

#residual plot
plot(x=fit.vals, y=std.res, xlab="Fitted values", ylab="Standardized residuals") 
abline(h=3, col="blue")
#qq plot of standardized residuals
qqnorm(std.res, main="") 
qqline(std.res, col="blue") #reference line in qqplot
#plot of leverages
plot(lev.vals, xlab="Index", ylab="Leverages") 
abline(h=lev.cut, col="blue")
#plot of cook's distances
plot(cook.dist)
abline(h=1, col="blue")
}
