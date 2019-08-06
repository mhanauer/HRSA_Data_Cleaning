---
title: "HRSA"
output: html_document
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

HRSA Code

```{r}
##HRSA
setwd("S:/Indiana Research & Evaluation/HRSA Healthy Start/Monthly Client-Level Data - HSMED/July 2019")
hrsa = read.csv("July 2019 Data Export.csv", header = TRUE)
head(hrsa)
library(lubridate)
library(tidyr)
hrsa$admindate =mdy(hrsa$admindate)

hrsa_july = subset(hrsa, admindate >= "2019-07-01" & admindate <= "2019-07-31")
hrsa_july = unite(data = hrsa_july, col = new_race, racelist___1, racelist___2, sep = ",") 
head(hrsa_july_test)
library(stringr)
hrsa_july$new_race = str_replace(hrsa_july$new_race, ",0", "")
hrsa_july$new_race
head(hrsa_july)

```


