


setwd("/Users/Kelsey/Dropbox/Graduate School UF/Coursework/Fall 2017/Networks")

#install.packages("ggplot2")
library(ggplot2)

RustData <- read.csv("StripeRust.csv", header = TRUE)

head(RustData)

RustData

## Graph by 

WithR <- c(8.5, 6.5, 4, 1, 3, 10, 5, 5, 5, 1, 1, 6, 6)

WithR
summary(WithR)
hist(WithR, xlab = "Self-Reported R Proficiency")

ggplot(data = RustData) +
  geom_point(mapping = aes(x = DAI, y = Severity, color = Year))
  
ggplot(data = RustData) +
  geom_line(mapping = aes(x = DAI, y = Severity, color = Year))

ggplot(data = RustData) +
  geom_line(mapping = aes(x = DAI, y = Severity, color = Year))

ggplot(data = RustData) +
  geom_point(mapping = aes(x = DAI, y = Severity)) +
  facet_wrap(~Year) +
  labs(title = "Stripe Rust Severity Over Time")


