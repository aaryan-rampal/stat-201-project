# dsci-100-project_template
Template project repository for DSCI-100

library(cowplot)
library(datateachr)
library(digest)
library(infer)
library(repr)
library(taxyvr)
library(tidyverse)
ds_salaries<-read.csv("ds_salaries.csv")

d_salaries<- ds_salaries %>%
             filter(employee_residence == "CA" & (job_title == "Data Scientist" | job_title == "Data Analyst")) %>%
             select(job_title, employee_residence,salary_in_usd ) 
d_salaries  
