rm(list=ls())
gc()

interventions <- read.csv("data/interventions.csv")
interventions$stay.at.home <- as.Date(interventions$stay.at.home, origin = "0001-01-01")

X <- aggregate(interventions$stay.at.home, by=list(interventions$stay.at.home), FUN=length)
names(X) <- c("date", "stay_at_home_orders")
barplot(X$stay_at_home_orders, col='blue')

# what drives SAH orders? Other lockdown measures?