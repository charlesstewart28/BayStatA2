# Assignment 2 - Pre Processing File
# Author: Charles Stewart
# Student: s3628786
# Date: 10/09/22

graphics.off() # This closes all of R's graphics windows.
rm(list=ls())  # Careful! This clears all of R's memory!
library(ggplot2)
library(ggpubr)
library(ks)
library(rjags)
library(runjags)
library(ggplot2)
library(tidyverse)
library(gtsummary)
library(gapminder)
library(skimr)
library(DT)


myData <- read.csv("Assignment2PropertyPrices.csv")

yName = "SalePrice.100K."
xName = c("Area",	"Bedrooms",	"Bathrooms", 	"CarParks",  	"PropertyType")

head(myData)

# Descriptive stats
desStat <- datatable(table1,
                     rownames = FALSE,
                     colnames = c('Type', 'Attribute', 'MissingValues', 'CompleteRate', 'Mean', 'StandDev', 'Min', '25%', '50%', '75%', 'Max', 'Hist'),
                     caption = 'Descriptive Statistics - Table 1.1')
desStat

# Sales price 
hist(myData$SalePrice.100K.)
figure1.1 <- plot(kde(myData$SalePrice.100K.), xlab='Price ($100k)') + 
  title('Price Density Function - Figure 1.1')


# Scatter plots
p1 <- ggplot(myData, aes(x=Area, y=SalePrice.100K.)) +
  geom_point() +
  xlab('Area (m^2)') +
  ylab('Sale Price ($100K)')

p2 <- ggplot(myData, aes(x=Bedrooms, y=SalePrice.100K.)) +
  geom_point() +
  xlab('Bedrooms') +
  ylab('Sale Price ($100K)')

p3 <- ggplot(myData, aes(x=Bathrooms, y=SalePrice.100K.)) +
  geom_point() +
  xlab('Bathrooms') +
  ylab('Sale Price ($100K)')

p4 <- ggplot(myData, aes(x=CarParks, y=SalePrice.100K.)) +
  geom_point() +
  xlab('Car Parks') +
  ylab('Sale Price ($100K)')

p5 <- ggplot(myData, aes(x=PropertyType, y=SalePrice.100K.)) +
  geom_point() +
  xlab('Property Type') +
  ylab('Sale Price ($100K)')

figure1.2 <- ggarrange(p1, p2, p3, p4, p5, nrow = 3, ncol = 2)
annotate_figure(figure1.2, top = text_grob('Sales Price x Attributes - Figure 1.2'))

figure1.2



