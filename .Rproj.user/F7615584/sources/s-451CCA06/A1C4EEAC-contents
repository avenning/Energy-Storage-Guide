############### LOAD PACKAGES AND DATAFRAMES

library(shiny)
library(shinyjs)
library(lubridate)
library(ggthemes)
library(janitor)
library(flextable)
library(shinyWidgets)
library(officer)
library(hms)
library(tidyverse)


################# Load DFs
getwd()
#setwd("~/Desktop/Community_Energy_Storage_Guide/Energy-Storage-Guide")

Sml_House <- read_csv("Sml_House.csv")
Med_House_Intro <- read_csv("Med_House.csv")
Med_House <- read_csv("Med_House.csv")
Lrg_House <- read_csv("Lrg_House.csv")
Res_Solar <- read_csv("Res_Solar.csv")
Med_House.rps <- read_csv("Med_House_PS.csv")
Commercial_TOU <- read_csv("Commercial_TOU.csv")
Commercial_PS <- read_csv("Commercial_PS.csv")
Generation <- read_csv("MISO_Generation.csv")

###########################################

{
Sml_House %>%
  mutate(Date_Time = mdy_hm(Date_Time),
         Date = mdy(Date)) %>%
  write_csv("Sml_House.csv")

Med_House %>%
  mutate(Date_Time = mdy_hm(Date_Time),
         Date = mdy(Date)) %>%
  write_csv("Med_House.csv")

Lrg_House %>%
  mutate(Date_Time = mdy_hm(Date_Time),
         Date = mdy(Date)) %>%
  write_csv("Lrg_House.csv")

Res_Solar %>%
  mutate(Date_Time = mdy_hm(Date_Time)) %>%
  write_csv("Res_Solar.csv")

Med_House.rps %>%
  mutate(Date_Time = mdy_hm(Date_Time),
         Date = mdy(Date)) %>%
  write_csv("Med_House_PS.csv")

Commercial_TOU %>%
  mutate(Date_Time = mdy_hm(Date_Time),
         Date = mdy(Date)) %>%
  write_csv("Commercial_TOU.csv")

Commercial_PS %>%
  mutate(Date_Time = mdy_hm(Date_Time),
         Date = mdy(Date)) %>%
  write_csv("Commercial_PS.csv")

Generation %>%
  mutate(Date_Time = mdy_hm(Date_Time),
         Date = mdy(Date)) %>%
  write_csv("MISO_Generation.csv")
} # Script for converting Date_Time and Date columns to dttm and date variable types
