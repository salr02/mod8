# mod8
#1
require(pryr)
require(ISLR)
require(boot)
library(data.table)
library(plyr)


Student_assignment_6 <- read.table("/Users/salmarahmouni/Downloads/Assignment 6 Dataset.txt", header = TRUE, sep = ",")

StudentAverage = ddply(Student_assignment_6,"Sex",transform,Grade.Average = mean(Grade))

StudentAverage

#2
write.table(StudentAverage,"Sorted_Average")
Student_i <- subset(Student_assignment_6,grepl("[iI]",Student_assignment_6$Name)) 
Student_i

#3
write.table(Student_i, "DataSubset", sep = ",")
