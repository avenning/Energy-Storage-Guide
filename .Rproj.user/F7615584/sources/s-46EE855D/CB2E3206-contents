{
# Reactivate library calls and data introduction before uploading to server
#library(shiny)
#library(shinyjs)
#library(shinyWidgets)
#library(tidyverse)
#library(lubridate)
#library(ggthemes)
#library(janitor)
#library(flextable)
#library(shinyWidgets)
#library(officer)
#library(hms)

#Sml_House <- read_csv("Sml_House.csv")
#Med_House_Intro <- read_csv("Med_House.csv")
#Med_House <- read_csv("Med_House.csv")
#Lrg_House <- read_csv("Lrg_House.csv")
#Res_Solar <- read_csv("Res_Solar.csv")
#Med_House.rps <- read_csv("Med_House_PS.csv")
#Commercial_TOU <- read_csv("Commercial_TOU.csv")
#Commercial_PS <- read_csv("Commercial_PS.csv")
#Generation <- read_csv("MISO_Generation.csv")
} # Package installation and data loading - reactivate before uploading to server

shinyServer(function(input, output, session) {
  
### JavaScripts for Page Navigation ###
  
  {   
  {
  onclick(id = "Intro", expr = list(hide(selector = "div.tabcontent"), shinyjs::show(id = "Introduction"),
          addClass(id = "Intro", class = "activeTab"), removeClass(id = "useCase", class = "activeTab"), removeClass(id = "Guide", class = "activeTab")))
  onclick(id = "Res", expr = list(hide(selector = "div.tabcontent"), shinyjs::show(id = "Residential"),
          addClass(id = "useCase", class = "activeTab"), removeClass(selector = "a.tablink", class = "activeTab")))
  onclick(id = "Comm", expr = list(hide(selector = "div.tabcontent"), shinyjs::show(id = "Commercial"),
          addClass(id = "useCase", class = "activeTab"), removeClass(selector = "a.tablink", class = "activeTab")))
  onclick(id = "Guide", expr = list(hide(selector = "div.tabcontent"), shinyjs::show(id = "Guidebook"),
          addClass(id = "Guide", class = "activeTab"), removeClass(id = "Intro", class = "activeTab"), removeClass(id = "useCase", class = "activeTab")))
  } ### ShinyJS for Main Navbar Header
  
  {
  onclick(id = "tablink2-H", expr = list(hide(selector = "div.intropage"), shinyjs::show(id = "Intro-H"),
                                    removeClass(selector = "a.tablink2", class = "activeSidebar"), addClass(id = "tablink2-H", class = "activeSidebar")))  
  onclick(id = "tablink2-1", expr = list(hide(selector = "div.intropage"), shinyjs::show(id = "Intro-1"),
                                    removeClass(selector = "a.tablink2", class = "activeSidebar"), addClass(id = "tablink2-1", class = "activeSidebar")))
  onclick(id = "tablink2-2", expr = list(hide(selector = "div.intropage"), shinyjs::show(id = "Intro-2"),
                                    removeClass(selector = "a.tablink2", class = "activeSidebar"), addClass(id = "tablink2-2", class = "activeSidebar")))
  onclick(id = "tablink2-3", expr = list(hide(selector = "div.intropage"), shinyjs::show(id = "Intro-3"),
                                    removeClass(selector = "a.tablink2", class = "activeSidebar"), addClass(id = "tablink2-3", class = "activeSidebar")))
  onclick(id = "tablink2-4", expr = list(hide(selector = "div.intropage"), shinyjs::show(id = "Intro-4"),
                                    removeClass(selector = "a.tablink2", class = "activeSidebar"), addClass(id = "tablink2-4", class = "activeSidebar")))
  onclick(id = "tablink2-5", expr = list(hide(selector = "div.intropage"), shinyjs::show(id = "Intro-5"),
                                    removeClass(selector = "a.tablink2", class = "activeSidebar"), addClass(id = "tablink2-5", class = "activeSidebar")))
  } ### ShinyJS for Intro Page Sidenav Column
  
  {
   onclick(id = "tablink3-1", expr = list(hide(selector = "div.guidebook"), shinyjs::show(id = "Guide-1"),
                                          removeClass(selector = "a.tablink3", class = "activeSidebar"), addClass(id = "tablink3-1", class = "activeSidebar")))
   onclick(id = "tablink3-2", expr = list(hide(selector = "div.guidebook"), shinyjs::show(id = "Guide-2"),
                                           removeClass(selector = "a.tablink3", class = "activeSidebar"), addClass(id = "tablink3-2", class = "activeSidebar")))
   onclick(id = "tablink3-3", expr = list(hide(selector = "div.guidebook"), shinyjs::show(id = "Guide-3"),
                                           removeClass(selector = "a.tablink3", class = "activeSidebar"), addClass(id = "tablink3-3", class = "activeSidebar")))
   onclick(id = "tablink3-4", expr = list(hide(selector = "div.guidebook"), shinyjs::show(id = "Guide-4"),
                                           removeClass(selector = "a.tablink3", class = "activeSidebar"), addClass(id = "tablink3-4", class = "activeSidebar")))
   onclick(id = "tablink3-5", expr = list(hide(selector = "div.guidebook"), shinyjs::show(id = "Guide-5"),
                                           removeClass(selector = "a.tablink3", class = "activeSidebar"), addClass(id = "tablink3-5", class = "activeSidebar")))
   onclick(id = "tablink3-6", expr = list(hide(selector = "div.guidebook"), shinyjs::show(id = "Guide-6"),
                                          removeClass(selector = "a.tablink3", class = "activeSidebar"), addClass(id = "tablink3-6", class = "activeSidebar")))
  } ### ShinyJS for Guidebook Sidenav Column
  
  {
  onclick("solarAccordion_res", toggle(id = "solarAccordionPanel_res"))   # Residential Solar Accordion
  onclick("solarAccordion_comm", toggle(id = "solarAccordionPanel_comm")) # Commercial Solar Accordion
  } ### ShinyJS for Solar Accordion Buttons
  
  {
  onclick(id = "est1-1", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "leadAcid")))
  onclick(id = "est1-2", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "lithiumIon")))
  onclick(id = "est1-3", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "redoxFlow")))
  onclick(id = "est1-4", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "sodiumSulfur")))
  onclick(id = "est1-5", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "NiMH")))
  onclick(id = "est1-6", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "solidState")))
  
  onclick(id = "est2-1", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "flywheel")))
  onclick(id = "est2-2", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "pumpedHydro")))
  onclick(id = "est2-3", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "CAES")))
  
  onclick(id = "est3-1", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "hotWater")))
  onclick(id = "est3-2", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "moltenSalt")))
  onclick(id = "est3-3", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "thermalEnvelope")))
  
  onclick(id = "est4-1", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "superCap")))
  onclick(id = "est4-2", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "SMES")))
  
  onclick(id = "est5-1", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "H2")))
  onclick(id = "est5-2", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "NH3")))
  onclick(id = "est5-3", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "coal")))
  onclick(id = "est5-4", expr = list(hide(selector = "div.ESTechPanel"), shinyjs::show(id = "CH4")))
  } ### ShinyJS for Energy Storage Technologies Card Selection
  
  {
    onclick(id = "ESTX1-1",  expr = hide(selector = "div.ESTechPanel"))
    onclick(id = "ESTX1-2",  expr = hide(selector = "div.ESTechPanel"))
    onclick(id = "ESTX1-3",  expr = hide(selector = "div.ESTechPanel"))
    onclick(id = "ESTX1-4",  expr = hide(selector = "div.ESTechPanel"))
    onclick(id = "ESTX1-5",  expr = hide(selector = "div.ESTechPanel"))
    onclick(id = "ESTX1-6",  expr = hide(selector = "div.ESTechPanel"))
    
    onclick(id = "ESTX2-1",  expr = hide(selector = "div.ESTechPanel"))
    onclick(id = "ESTX2-2",  expr = hide(selector = "div.ESTechPanel"))
    onclick(id = "ESTX2-3",  expr = hide(selector = "div.ESTechPanel"))
    
    onclick(id = "ESTX3-1",  expr = hide(selector = "div.ESTechPanel"))
    onclick(id = "ESTX3-2",  expr = hide(selector = "div.ESTechPanel"))
    
    onclick(id = "ESTX4-1",  expr = hide(selector = "div.ESTechPanel"))
    onclick(id = "ESTX4-2",  expr = hide(selector = "div.ESTechPanel"))
    onclick(id = "ESTX4-3",  expr = hide(selector = "div.ESTechPanel"))
    
    onclick(id = "ESTX5-1",  expr = hide(selector = "div.ESTechPanel"))
    onclick(id = "ESTX5-2",  expr = hide(selector = "div.ESTechPanel"))
    onclick(id = "ESTX5-3",  expr = hide(selector = "div.ESTechPanel"))
    onclick(id = "ESTX5-4",  expr = hide(selector = "div.ESTechPanel"))
  } ### ShinyJS for Energy Storage Exit Buttons
  
  {
  onclick(id = "cust-1", expr = list(hide(selector = "div.useCasePanel"), shinyjs::show(id = "backupPower")))
  onclick(id = "cust-2", expr = list(hide(selector = "div.useCasePanel"), shinyjs::show(id = "pvFirm")))
  onclick(id = "cust-3", expr = list(hide(selector = "div.useCasePanel"), shinyjs::show(id = "demandMgmt")))
  onclick(id = "cust-4", expr = list(hide(selector = "div.useCasePanel"), shinyjs::show(id = "touMgmt")))
  
  onclick(id = "util-1", expr = list(hide(selector = "div.useCasePanel"), shinyjs::show(id = "deferral")))
  onclick(id = "util-2", expr = list(hide(selector = "div.useCasePanel"), shinyjs::show(id = "deferral")))
  onclick(id = "util-3", expr = list(hide(selector = "div.useCasePanel"), shinyjs::show(id = "congRlf")))
  onclick(id = "util-4", expr = list(hide(selector = "div.useCasePanel"), shinyjs::show(id = "resAdqcy")))
  
  onclick(id = "grid-1", expr = list(hide(selector = "div.useCasePanel"), shinyjs::show(id = "rampPeak")))
  onclick(id = "grid-2", expr = list(hide(selector = "div.useCasePanel"), shinyjs::show(id = "reserve")))
  onclick(id = "grid-3", expr = list(hide(selector = "div.useCasePanel"), shinyjs::show(id = "freqReg")))
  onclick(id = "grid-4", expr = list(hide(selector = "div.useCasePanel"), shinyjs::show(id = "voltSup")))
  onclick(id = "grid-5", expr = list(hide(selector = "div.useCasePanel"), shinyjs::show(id = "blkStart")))
  } ### ShinyJS for Use Case Card Selection
  
  {
  onclick(id = "UCX-1",  expr = hide(selector = "div.useCasePanel"))
  onclick(id = "UCX-2",  expr = hide(selector = "div.useCasePanel"))
  onclick(id = "UCX-3",  expr = hide(selector = "div.useCasePanel"))
  onclick(id = "UCX-4",  expr = hide(selector = "div.useCasePanel"))
  
  onclick(id = "UCX-5",  expr = hide(selector = "div.useCasePanel"))
  onclick(id = "UCX-6",  expr = hide(selector = "div.useCasePanel"))
  onclick(id = "UCX-7",  expr = hide(selector = "div.useCasePanel"))
  onclick(id = "UCX-8",  expr = hide(selector = "div.useCasePanel"))
  
  onclick(id = "UCX-9",  expr = hide(selector = "div.useCasePanel"))
  onclick(id = "UCX-10", expr = hide(selector = "div.useCasePanel"))
  onclick(id = "UCX-11", expr = hide(selector = "div.useCasePanel"))
  onclick(id = "UCX-12", expr = hide(selector = "div.useCasePanel"))
  onclick(id = "UCX-13", expr = hide(selector = "div.useCasePanel"))
  } ### ShinyJS for Use Case Exit Buttons
  
  {
  onclick(id = "toggle-1", expr = toggle(selector = "div.Electrochem"))
  onclick(id = "toggle-2", expr = toggle(selector = "div.Electromech"))
  onclick(id = "toggle-3", expr = toggle(selector = "div.Electrical"))
  onclick(id = "toggle-4", expr = toggle(selector = "div.Thermal"))
  onclick(id = "toggle-5", expr = toggle(selector = "div.Chemical"))
  onclick(id = "toggle-0", expr = toggle(selector = "div.NonCommunity"))
  } ### ShinyJS for Energy Storage Technology Intro Page Plots
    
  {
  onclick(id = "down_timeshift", expr = list(hide(id = "down_timeshift"), shinyjs::show(id = "timeshift_box"), shinyjs::show(id = "up_timeshift")))
  onclick(id = "up_timeshift", expr = list(hide(id = "up_timeshift"), shinyjs::show(id = "down_timeshift"), hide(id = "timeshift_box")))
  onclick(id = "down_solar", expr = list(hide(id = "down_solar"), shinyjs::show(selector = "div.solar_box"), shinyjs::show(id = "up_solar")))
  onclick(id = "up_solar", expr = list(hide(id = "up_solar"), shinyjs::show(id = "down_solar"), hide(selector = "div.solar_box")))
  onclick(id = "down_resil", expr = list(hide(id = "down_resil"), shinyjs::show(selector = "div.resil_box"), shinyjs::show(id = "up_resil")))
  onclick(id = "up_resil", expr = list(hide(id = "up_resil"), shinyjs::show(id = "down_resil"), hide(selector = "div.resil_box")))
  
  onclick(id = "down_emissions", expr = list(hide(id = "down_emissions"), shinyjs::show(id = "emissions_box"), shinyjs::show(id = "up_emissions")))
  onclick(id = "up_emissions", expr = list(hide(id = "up_emissions"), shinyjs::show(id = "down_emissions"), hide(id = "emissions_box")))
  onclick(id = "down_microgrid", expr = list(hide(id = "down_microgrid"), shinyjs::show(selector = "div.microgrid_box"), shinyjs::show(id = "up_microgrid")))
  onclick(id = "up_microgrid", expr = list(hide(id = "up_microgrid"), shinyjs::show(id = "down_microgrid"), hide(selector = "div.microgrid_box")))
  } ### ShinyJS for Purpose and Use Case Page
  } # ShinyJS Scripts
  
 # # # # RESIDENTIAL SECTION # # # #
  
### Residential TOU Section ###
  
  {
  {
  Res_TOU <- function(DataSet, Batt_kW, Batt_kWh, Batt_Efficiency, Batt_DoD, Batt_Backup) {
      Res_Battery <- DataSet %>%
        mutate(Discharge_Factor = ifelse(Month == "Jan", 0.0, ifelse(Month == "Feb", 0.0, ifelse(Month == "Mar", 0.0, ifelse(Month == "Apr", 0.0,
                                  ifelse(Month == "May", 0.2, ifelse(Month == "Jun", 0.75, ifelse(Month == "Jul", 0.75, ifelse(Month == "Aug", 0.75,
                                  ifelse(Month == "Sep", 0.1, ifelse(Month == "Oct", 0.0, ifelse(Month == "Nov", 0.0, ifelse(Month == "Dec", 0.0, NA)))))))))))),
               Batt_State = ifelse(Time < hms::as.hms("6:00:00"), "Charge",
                            ifelse(Time >= hms::as.hms("6:00:00") & Electric_Use > (Mean * Discharge_Factor), "Discharge", "Standby")),
               Charge = ifelse(Batt_State == "Charge" , Batt_kW,
                        ifelse(Batt_State == "Standby", 0,
                        ifelse(Batt_State == "Discharge" & TOU == "Peak" & Electric_Use <  Batt_kW / Batt_Efficiency, -Electric_Use / Batt_Efficiency,
                        ifelse(Batt_State == "Discharge" & TOU == "Peak" & Electric_Use >= Batt_kW / Batt_Efficiency, -Batt_kW / (Batt_Efficiency), 
                        ifelse(Batt_State == "Discharge" & TOU == "Mid-Peak" & (Electric_Use - Mean *  Discharge_Factor) <  Batt_kW / (Batt_Efficiency), (Mean * Discharge_Factor - Electric_Use) / (Batt_Efficiency),
                        ifelse(Batt_State == "Discharge" & TOU == "Mid-Peak" & (Electric_Use - Mean *  Discharge_Factor) >= Batt_kW / (Batt_Efficiency), -Batt_kW / (Batt_Efficiency), 0)))))),
               Cumulative_Charge = Charge * 0.5)
      
      f <- function(x, y) max(min(x + y, Batt_kWh), Batt_kWh * (1-Batt_DoD) + (Batt_kWh - Batt_kWh * (1-Batt_DoD)) * (Batt_Backup)) # First term of minimum charge value is DoD value, second is amount witheld for backup power.
      Batt_Charge <- Reduce(f, Res_Battery$Cumulative_Charge, 0, accumulate = TRUE)[-1]
      Batt_Charge.df <- tibble(Res_Battery$Date_Time, Batt_Charge)
      
      Res_Final <-  Res_Battery %>%
        left_join(Batt_Charge.df, by = c("Date_Time" = "Res_Battery$Date_Time")) %>%
        mutate(Charge_Discharge = Batt_Charge-lag(Batt_Charge, default = 0), # Determining the charge or discharge state of the battery by kW
               Charge_Discharge_Inefficient = ifelse(Charge_Discharge >= 0, Charge_Discharge, # Introducing the round-trip inefficiency to the dischargee
                                              ifelse(Charge_Discharge < 0, Charge_Discharge * (Batt_Efficiency), 0)),
               Batt_Load = Charge_Discharge_Inefficient/0.5, # Determining how much load is offset or added from the battery.
               Grid_Load = Electric_Use + Batt_Load, # Determining the net load on the grid, including battery use.
               Batt_Reg_Cost = Grid_Load * Regular_Rate * 0.5,
               Batt_TOU_Cost = Grid_Load * TOU_Rate * 0.5) %>%
        filter(!is.na(Charge_Discharge))
    }
  Res_TOU_df <- reactive({Res_TOU(DataSet = get(input$DataSet.res), 
                                  Batt_kW = input$Batt_kW.res, 
                                  Batt_kWh = input$Batt_kWh.res, 
                                  Batt_Efficiency = input$Batt_Efficiency.res * 0.01, 
                                  Batt_DoD = input$Batt_DoD.res * 0.01,
                                  Batt_Backup = input$Batt_Backup.res * 0.01)})
} # General Algorithms

  {    
  output$RTU_Intro1 <- renderPlot({
    Med_House_Intro %>%
      filter(Weekend == 0) %>%
      select(Date_Time, Date, Time, Month, Electric_Use) %>%
      group_by(Time) %>%
      summarize(Electric_Use = mean(Electric_Use)) %>%
      mutate(Hour = hour(Time),
             TOU = ifelse(Hour < 6, "Off-Peak",
                          ifelse(Hour >= 15 & Hour < 20, "Peak", "Mid-Peak")),
             Grid_Load = ifelse(TOU == "Off-Peak", Electric_Use + 0.17*input$RTU_IntroplotSlider,          # Adding load to off-peak hours
                         ifelse(TOU == "Mid-Peak", Electric_Use - 0.05*input$RTU_IntroplotSlider,          # Reducing load from mid-peak hours
                                                   Electric_Use - 0.11*input$RTU_IntroplotSlider))) %>%    # Reducing load from peak hours
      gather(key = key, value = kW, -Hour, -Time, -TOU) %>%
      
      ggplot(aes(x = Time, y = kW, fill = TOU, col = TOU)) +
      geom_col() +
      facet_wrap(key~., scales = "free", ncol = 1,
                 labeller = labeller(key = c(`Electric_Use` = "Without Storage",
                                             `Grid_Load` = "With Storage"))) +
      theme_tufte() + 
      theme(axis.line = element_line(color = "black", size = 0.3),
            strip.text = element_text(size = 13, face = "bold"), 
            axis.title.x = element_blank(),
            axis.title.y = element_text(size = 13),
            axis.text.x = element_text(size = 11, vjust = -0.25),
            axis.text.y = element_text(size = 11),
            legend.title = element_text(size = 13, hjust = 0.5),
            legend.text = element_text(size = 11),
            plot.background = element_rect(fill = "#e3e3e3",
                                           color = "#e3e3e3")) +
      ylab("Average Electricity Use (kW)") +
      scale_x_time(expand = c(0,0),
                   breaks = c(0, 21600, 43200, 64800, 85500),
                   labels = c("12 am", "6 am", "12 pm", "6 pm", "12 am")) +
      scale_y_continuous(expand = c(0,0)) +
      scale_color_manual(name = "Time-of-Use\nPeriod",
                         values = c("slategray3", "slategray2", "slategray4"),
                         breaks = c("Peak", "Mid-Peak", "Off-Peak")) +
      scale_fill_manual(name = "Time-of-Use\nPeriod",
                        values = c("slategray3", "slategray2", "slategray4"),
                        breaks = c("Peak", "Mid-Peak", "Off-Peak"))
  }, height = 300, width = 350)
} # General Information Tab
    
  {
  output$datePlot_Grid.rtu <- renderPlot({
    Res_TOU_df() %>%
      mutate(Cycle_Change = ifelse(Batt_State != lag(Batt_State, default = ""), 1, 0),
             Cycle_Number = factor(cumsum(Cycle_Change))) %>%
      filter(between(x = Date, left = input$date_res[1], right = input$date_res[2])) %>%
      select(Date_Time, Date, Time, Electric_Use, Grid_Load, Batt_State, Cycle_Number) %>%
      ggplot(aes(x = Date_Time, ymin = Electric_Use, ymax = Grid_Load)) +
      geom_ribbon(aes(group = Cycle_Number, fill = Batt_State), alpha = 0.3) +
      geom_line(aes(x = Date_Time, y = Electric_Use), color = "grey20", size = 0.6, linetype = 2) +
      geom_line(aes(x = Date_Time, y = Grid_Load), color = "black", size = 0.7) +
      theme_tufte() + 
      theme(axis.line = element_line(color = "black", size = 0.3),
            axis.title.x = element_blank(),
            axis.title.y = element_text(size = 14.5, vjust = 2, family = "Helvetica"),
            axis.text = element_text(size = 12, family = "Helvetica"),
            legend.position = "none",
            plot.margin = unit(c(0.5,1,0.5,0.75), "lines")) +
      scale_x_datetime(expand = c(0,0)) +
      scale_fill_manual(name = "Battery State",
                        breaks = c("Charge", "Discharge", "Standby"),
                        labels = c("Charge", "Discharge", ""),
                        values = c("red4", "skyblue4", "white")) +
      ylab("Electricity Use (kW)")
  }, height = 300) # Res TOU load curve by date graph
  
  output$datePlot_Batt.rtu <- renderPlot({
    Res_TOU_df() %>%
      mutate(Cycle_Change = ifelse(Batt_State != lag(Batt_State, default = ""), 1, 0),
             Cycle_Number = factor(cumsum(Cycle_Change))) %>%
      filter(between(x = Date, left = input$date_res[1], right = input$date_res[2])) %>%
      select(Date_Time, Date, Time, Batt_Charge, Batt_Load, Batt_State, Cycle_Number) %>%
      ggplot(aes(x = Date_Time)) +
      geom_area(aes(y = Batt_Load, group = Cycle_Number, fill = Batt_State), alpha = 0.3) +
      geom_line(aes(y = Batt_Load), color = "slategrey") +
      geom_line(aes(y = Batt_Charge), color = "black", size = 1) + 
      geom_hline(yintercept = 0, size = 0.3) +
      theme_tufte() + 
      theme(axis.line = element_line(color = "black", size = 0.3),
            axis.title.x = element_blank(),
            axis.title.y = element_text(size = 14.5, vjust = 2, family = "Helvetica"),
            axis.text = element_text(size = 12, family = "Helvetica"),
            legend.position = "none",
            plot.margin = unit(c(0.5,1,0.5,0.75), "lines")) +
      scale_x_datetime(expand = c(0,0)) +
      scale_fill_manual(name = "Battery State",
                        breaks = c("Charge", "Discharge", "Standby"),
                        labels = c("Charge", "Discharge", ""),
                        values = c("red4", "skyblue4", "white")) +
      ylab("Battery Activity (kW or kWh)")
  }, height = 300) # Res TOU batt state by date graph
  } # Daily Load Curve Tab
  
  {
  output$monthPlot_Grid.rtu <- renderPlot({
    Res_TOU_df() %>%
      select(Date_Time, Time, Month, Day, Electric_Use, Grid_Load, Batt_Charge, Batt_Load) %>%
      group_by(Month, Time) %>%
      summarize(Electric.Use = mean(Electric_Use), 
                Grid.Load = mean(Grid_Load), 
                Batt.Charge = mean(Batt_Charge),
                Batt.Load = mean(Batt_Load)) %>%
      filter(Month == input$Month.res) %>%
      ggplot(aes(x = Time)) +
      geom_ribbon(aes(ymin = Grid.Load, ymax = Electric.Use,
                      fill = Electric.Use >= Grid.Load), alpha = 0.3) +
      geom_line(aes(y = Electric.Use), col = "slategrey", size = 0.6, linetype = 2) +
      geom_line(aes(y = Grid.Load), col = "black", size = 1) +
      theme_tufte() + 
      theme(axis.line = element_line(color = "black", size = 0.3),
            axis.title.x = element_blank(),
            axis.title.y = element_text(size = 14.5, vjust = 2, family = "Helvetica"),
            axis.text = element_text(size = 12, family = "Helvetica"),
            axis.text.x = element_text(vjust = -1),
            legend.position = "none",
            plot.margin = unit(c(0.5,1.5,0.5,0.75), "lines")) +
      scale_x_time(expand = c(0,0),
                   breaks = c(0, 21300, 42900, 64500, 84600),
                   labels = c("12am", "6am", "12pm", "6pm", "12am")) +
      scale_fill_manual(breaks = c(FALSE, TRUE),
                        labels = c("Charge", "Discharge"),
                        name = "Battery State",
                        values = c("red4", "skyblue4")) +
      ylab("Electricity Use (kW)")
  }, height = 300)
  
  output$monthPlot_Batt.rtu <- renderPlot({
    Res_TOU_df() %>%
      select(Date_Time, Time, Month, Day, Electric_Use, Grid_Load, Batt_Charge, Batt_Load) %>%
      group_by(Month, Time) %>%
      summarize(Electric.Use = mean(Electric_Use), 
                Grid.Load = mean(Grid_Load), 
                Batt.Charge = mean(Batt_Charge),
                Batt.Load = mean(Batt_Load)) %>%
      filter(Month == input$Month.res) %>%
      ggplot(aes(x = Time)) +
      geom_area(aes(y = Batt.Load, fill = Electric.Use >= Grid.Load), alpha = 0.3) +
      geom_line(aes(y = Batt.Load), color = "slategrey") +
      geom_line(aes(y = Batt.Charge), color = "black", size = 1.2) +
      geom_hline(yintercept = 0, color = "black", size = 0.3) +
      theme_tufte() +
      theme(axis.line = element_line(color = "black", size = 0.3),
            axis.title.x = element_blank(),
            axis.title.y = element_text(size = 14.5, vjust = 2, family = "Helvetica"),
            axis.text = element_text(size = 12, family = "Helvetica"),
            axis.text.x = element_text(vjust = -1),
            legend.position = "none",
            plot.margin = unit(c(0.5,1.5,0.5,0.75), "lines")) +
      scale_x_time(expand = c(0,0),
                   breaks = c(0, 21300, 42900, 64500, 84600),
                   labels = c("12am", "6am", "12pm", "6pm", "12am")) +
      scale_fill_manual(breaks = c(FALSE, TRUE),
                        labels = c("Charge", "Discharge"),
                        name = "Battery State",
                        values = c("red4", "skyblue4")) +
      ylab("Battery Activity (kW or kWh)")
  }, height = 300) # Res TOU monthly average load curve plot
  } # Monthly Load Curve Tab
    
  {
  output$BillComp.rtu <- renderUI({
    Res_TOU_df() %>%
      group_by(Month) %>%
      summarize(`Trad.Nobatt` = sum(Electric_Use * Regular_Rate * elapsed_time),
                `TOU.Nobatt` = sum(Electric_Use * TOU_Rate * elapsed_time),
                ` ` = NA,
                `Trad.Batt` = sum(Grid_Load * Regular_Rate * elapsed_time),
                `TOU.Batt` = sum(Grid_Load * TOU_Rate * elapsed_time), 
                `  ` = NA,
                `kWh.Nobatt` = sum(Electric_Use * elapsed_time),
                `kWh.Batt` = sum(Grid_Load * elapsed_time)) %>%
      arrange(match(Month, month.abb)) %>%
      adorn_totals("row") %>%
      
      flextable() %>%
      border_remove() %>%
      
      set_header_labels(Trad.Nobatt = "Standard Bill",
                        TOU.Nobatt = "Time-of-Use Bill",
                        Trad.Batt = "Standard Bill",
                        TOU.Batt = "Time-of-Use Bill",
                        kWh.Nobatt = "w/o Battery",
                        kWh.Batt = "w/ Battery") %>%
      add_header(Trad.Nobatt = "No Battery",
                 TOU.Nobatt = "No Battery",
                 Trad.Batt = "With Battery",
                 TOU.Batt = "With Battery",
                 kWh.Nobatt = "Energy Use (kWh)",
                 kWh.Batt = "Energy Use (kWh)") %>%
      merge_h(part = "header") %>%
      flextable::align(j = 1, align = "center") %>%
      flextable::align(part = "header", i = 1:2, align = "center") %>%
      hline(i = 1, j = 2:3, part = "header",
            border = fp_border(color = "black", width = 1)) %>%
      hline(i = 1, j = 5:6, part = "header",
            border = fp_border(color = "black", width = 1)) %>%
      hline(i = 1, j = 8:9, part = "header",
            border = fp_border(color = "black", width = 1)) %>%
      hline(i = 2, part = "header",
            border = fp_border(color = "black", width = 1.3)) %>%
      hline(i = 12, part = "body",
            border = fp_border(color = "black", width = 1.3)) %>%
      color(i = 13, j = c(4, 7), color="white") %>%
      bold(part = "header") %>%
      bold(part = "body", i = 13, j = 1:9) %>%
      fontsize(part = "all", size = 13) %>%
      width(width = 1.2) %>%
      width(j = 4, width = 0.5) %>%
      width(j = 7, width = 0.5) %>%
      height(part = "body", height = 0.3) %>%
      bg(i = 1:13, j = 2,  bg = "grey95") %>%
      bg(i = 1:13, j = 6,  bg = "grey95") %>%
      colformat_num(col_keys = c("Trad.Nobatt", "TOU.Nobatt",
                                 "Trad.Batt", "TOU.Batt"), big.mark = ",", digits = 2) %>%
      colformat_num(col_keys = c("kWh.Nobatt", "kWh.Batt"),
                    big.mark = ",", digits = 0) %>%
      htmltools_value()
  })
  
  yearlySavings.rtu <- reactive({
    Res_TOU_df() %>%
      summarize(Trad_Bill = sum(Electric_Use * Regular_Rate * elapsed_time),
                TOU_Bill = sum(Grid_Load * TOU_Rate * elapsed_time)) %>%
      summarize(Savings = Trad_Bill - TOU_Bill) %>%
      as.numeric() %>%
      round(digits = 2)
  })
  
  output$YearlySavings.rtu <- renderText({
    paste0("$", format(yearlySavings.rtu(), big.mark = ",", nsmall = 2))
  })
  
  output$expLife.rtu <- renderText({
    paste(input$BattLife.rtu, "years")
  })
  
  output$discountRate.rtu <- renderText({
    paste0(input$discRate.rtu, "%")
  })
  
  output$batteryCost.rtu <- renderText({
    paste0("$", format(input$BattCost.rtu, big.mark = ",", scientific = FALSE))
  })
  
  output$PaybackPlot.rtu <- renderPlot({
      upfrontCost <- -(input$BattCost.rtu)
      expLife <- input$BattLife.rtu
      yearlySavings <- yearlySavings.rtu()
      payBack <- (-upfrontCost)/yearlySavings
      profitLoss = upfrontCost + expLife * yearlySavings
    
    ggplot(data = tibble(a = c(1))) +
      geom_hline(yintercept = 0) +
      geom_vline(xintercept = 0) +
      geom_abline(intercept = upfrontCost, slope = yearlySavings, color = "navyblue", size = 1) +
      geom_vline(xintercept = expLife, linetype = 2) +
      geom_vline(xintercept = -(upfrontCost) / yearlySavings, linetype = 2) +
      
      geom_point(aes(x = 0, y = upfrontCost), size = 2.5) +
      geom_point(aes(x = 0, y = upfrontCost), size = 1.5, color = "white", fill = "white", shape = 18) +
      
      geom_point(aes(x = payBack, y = 0), size = 2.5) +
      geom_point(aes(x = payBack, y = 0), size = 1.5, color = "white", fill = "white", shape = 18) +
      
      geom_segment(aes(x = .4, xend = .4, y = 0, yend = profitLoss),
                   color = ifelse(profitLoss > 0, "darkgreen", 
                                  ifelse(profitLoss < 0, "indianred4", "black")),
                   size = 1.1, arrow = arrow(ends = "last", angle = 90, length = unit(0.25, "lines"))) +
      geom_segment(aes(x = .4, xend = expLife, y = profitLoss, yend = profitLoss),
                   linetype = 3, size = 0.9, 
                   color = ifelse(profitLoss > 0, "darkgreen", 
                                  ifelse(profitLoss < 0, "indianred4", "black"))) +
      
      geom_text(aes(x = 0.5, y = upfrontCost-800), hjust = 0, label = "Initial Investment/\nUpfront Cost", fontface = "bold", size = 4.5) +
      geom_text(aes(x = .8, y = ifelse(profitLoss < -1000 | (profitLoss >= 0 & profitLoss < 1100), profitLoss + 600, profitLoss - 600)),
                hjust = 0, label = "Total Expected Lifetime Savings", fontface = "bold", size = 5) +
      geom_label(aes(x = ifelse(payBack <= 22.5 | payBack > 25.1, payBack + 1.45, payBack - 1.45), y = 0), 
                 label = "Break Even\nPoint", vjust = ifelse(payBack <= 22.5 | payBack > 25.1, 1.05, -0.05),
                 size = 4.5, fontface = "bold", fill = "white", alpha = 0.7,
                 label.size = NA, label.padding = unit(0.4, "lines")) +
      geom_text(aes(x = ifelse(expLife >= payBack, expLife + 1.8, expLife - 1.7),
                    y = upfrontCost*0.8), 
                label = "Expected Useful\nLife of Battery",
                size = 4.5, fontface = "bold") +
      
      theme_tufte() +
      coord_cartesian(xlim = c(0,
                               25),
                               #ifelse(payBack > expLife, payBack * 1.3, expLife * 1.3)), 
                      ylim = c((upfrontCost -1500), 
                               ifelse(profitLoss > 0, profitLoss + 1500, 1500))) +
      
      scale_x_continuous(name = "Years", 
                         breaks = c(5, 10, 15, 20, 25, 30),
                         labels = c("5 yrs", "10 yrs", "15 yrs", "20 yrs", "25 yrs", "30 yrs"),
                         expand = c(0,0)) +
      scale_y_continuous(name = "Cost (Dollars)",
                         breaks = seq.int(from = -100000, to = 100000, by = 2500)) +
      
      theme(axis.title = element_blank(),
            axis.text = element_text(size = 12),
            plot.margin = unit(c(1,1,1,1), "lines"))
  })
  } # Bill Comparison and Savings Tab
  
  {
  output$GenPlot.rtu <- renderPlot({
    a <- Res_TOU_df() %>%
        select(Time, Electric_Use, Grid_Load) %>%
        group_by(Time) %>%
        summarize(Electric_Use = mean(Electric_Use),
                  Grid_Load = mean(Grid_Load)) %>%
        mutate(C = Electric_Use,
               D = Grid_Load,
               E = Electric_Use) %>%
        rename("A" = Electric_Use,
               "B" = Grid_Load) %>%
        gather(key = Line, value = kW, -Time, -E) %>%
        mutate(Plot = ifelse(Line == "A", "1",
                             ifelse(Line %in% c("B", "C"), "2", "3")),
               Fill = ifelse(E >= kW, "Discharge", "Charge"))
      
    ggplot(a, aes(x = Time, y = kW, color = Line)) +
        geom_rect(inherit.aes = FALSE, aes(ymin = 0, ymax = Inf, xmin = 52800, xmax = 70500), fill = "grey90") +
        geom_ribbon(data = filter(a, Line == "B"),
                    aes(ymin = kW, ymax = E, fill = Fill),
                    alpha = 0.9, color = "white") +
        geom_line(size = 0.7, aes(linetype = Line)) +
        facet_wrap(~Plot, ncol = 1,
                   labeller = labeller(Plot = c(`1` = "Old Load Curve without Storage",
                                                `2` = "Storage Device Charge/Discharge Activity",
                                                `3` = "New Load Curve with Storage")),
                   scales = "free_y") +
        geom_hline(yintercept = 0, color = "black", size = 0.3) +
        theme_tufte() +
        theme(axis.line.y = element_line(color = "black", size = 0.3),
              axis.title.x = element_blank(),
              axis.title.y = element_text(size = 14, family = "Helvetica", vjust = 4),
              axis.text = element_text(size = 10, family = "Helvetica"),
              axis.text.x = element_text(vjust = -1),
              strip.text = element_text(size = 12, family = "Helvetica", face = "bold", vjust = 1),
              legend.position = "none",
              plot.margin = unit(c(1,1.7,0.5,1), "lines"),
              panel.spacing = unit(1, "lines")) +
        ylab("Average Electricity Use (kW)") +
        scale_x_time(breaks = c(0, 14100, 28200, 42300, 56400, 70500, 84400), 
                     labels = c("12:00am", "4:00am", "8:00am", "12:00pm", "4:00pm", "8:00pm", "12:00am"), 
                     expand = c(0,0)) +
        scale_y_continuous(expand = c(0.005,0.005)) +
        scale_color_manual(breaks = c("A", "B", "C", "D"),
                           values = c("grey65", "black", "grey80", "black")) +
        scale_linetype_manual(breaks = c("A", "B", "C", "D"),
                              values = c(5,1,5,1)) +
        scale_fill_manual(breaks = c("Charge", "Discharge"),
                          values = c("#d9b6b6", "#c6d1d9"))
  }, width = 375)
  
  output$Generation.rtu <- renderUI({
    Res_TOU_df() %>%
      left_join(Generation, by = "Date_Time") %>%
      select(Date_Time, Month, Electric_Use, Grid_Load, Pct_Renew, Pct_Clean, Carbon_per_kWh) %>%
      filter(!is.na(Pct_Renew)) %>%
      mutate(kWh_Renew_Reg = Pct_Renew * 0.01 * Electric_Use,
             kWh_Renew_Bat = Pct_Renew * 0.01 * Grid_Load,
             kWh_Clean_Reg = Pct_Clean * 0.01 * Electric_Use,
             kWh_Clean_Bat = Pct_Clean * 0.01 * Grid_Load,
             kg_Carbon_Reg = Carbon_per_kWh * Electric_Use,
             kg_Carbon_Bat = Carbon_per_kWh * Grid_Load) %>%
      summarize(Total.kWh_Reg = sum(Electric_Use),
                Total.kWh_Bat = sum(Grid_Load),
                Pct.Renew_Reg = sum(kWh_Renew_Reg)/sum(Electric_Use) * 100,
                Pct.Renew_Bat = sum(kWh_Renew_Bat)/sum(Grid_Load) * 100,
                Pct.Clean_Reg = sum(kWh_Clean_Reg)/sum(Electric_Use) * 100,
                Pct.Clean_Bat = sum(kWh_Clean_Bat)/sum(Grid_Load) * 100,
                kg.Carbon_Reg = sum(kg_Carbon_Reg),
                kg.Carbon_Bat = sum(kg_Carbon_Bat),
                C.Cost_Reg    = kg.Carbon_Reg * input$SCC.res * 0.00110231,
                C.Cost_Bat    = kg.Carbon_Bat * input$SCC.res * 0.00110231) %>%
      gather(key = key, value = value) %>%
      separate(key, sep = "_", into = c("Key", "Status")) %>%
      spread(key = Status, value = value) %>%
      arrange(desc(Key)) %>%
      select(Key, Reg, Bat) %>%
      mutate(Key = c("Total kWh Used", "Percent Renewable (%)", "Percent Clean (%)", "Carbon Emissions* (kg)", "Social Cost ($)")) %>%
      
      flextable() %>%
      set_header_labels(`Key` = " ",
                        `Reg` = "Without Storage",
                        `Bat` = "With Storage") %>%
      fontsize(part = "all", size = 14) %>%
      height(height = 0.3) %>%
      width(width = 1.8) %>%
      width(j = 1, width = 2.3) %>%
      colformat_num(col_keys = c("Reg", "Bat"), big.mark = ",", digits = 0) %>%
      bg(i = 4, j = 1:3,  bg = "#d7d2c6") %>%
      bold(part = "header") %>%
      htmltools_value()
  })
  } # Generation Resources Tab
  } # End of Residential Time-of-Use
  
### Residential Solar Firming Section ###
  
  {
  {
  Res_RSF <- function(DataSet, Batt_kW, Batt_kWh, Batt_Efficiency, Batt_DoD, Solar_kW, Batt_Backup) {
    Res_Battery <- DataSet %>%
      select(-TOU, -TOU_Rate, -TOU_Cost, -Regular_Cost) %>%
      filter(minute(Date_Time) == 0, Day_in_Year != 60) %>%
      left_join(Res_Solar, by = "Date_Time") %>%
      mutate(Solar = Solar * Solar_kW,
             Solar = ifelse(is.na(Solar), 0, Solar),
             Solar_Charge = ifelse(Solar - Electric_Use < 0, 0, 
                            ifelse(Solar - Electric_Use < Batt_kW, Solar - Electric_Use, Batt_kW)),
             Over_Gen = ifelse(Solar > Electric_Use, Solar - Electric_Use, 0),
             Net_Use = ifelse(Electric_Use > Solar, Electric_Use - Solar, 0),
             Cumulative_Charge = Solar_Charge - Net_Use)
    
    f <- function(x, y) max(min(x + y, Batt_kWh), Batt_kWh * (1-Batt_DoD) + (Batt_kWh - Batt_kWh * (1-Batt_DoD)) * (Batt_Backup))
    Batt_Charge <- Reduce(f, Res_Battery$Cumulative_Charge, 0, accumulate = TRUE)[-1]
    Batt_Charge.df <- tibble(Res_Battery$Date_Time, Batt_Charge)
    
    Res_Final <- Res_Battery %>%
      left_join(Batt_Charge.df, by = c("Date_Time" = "Res_Battery$Date_Time")) %>%
      mutate(Charge_Discharge = Batt_Charge-lag(Batt_Charge, default = 0),
             Batt_Load = ifelse(Charge_Discharge >= 0, Charge_Discharge,
                         ifelse(Charge_Discharge < 0, Charge_Discharge * Batt_Efficiency, 0)),
             Batt_Charge_Solar = ifelse(Batt_Load > 0, Batt_Load, 0),
             To_Grid = ifelse(Solar_Charge - Batt_Charge_Solar > 0, Solar_Charge - Batt_Charge_Solar, 0),
             Grid_Load = Net_Use + Batt_Load - Solar_Charge,
             Grid_Load = ifelse(Grid_Load > 0, Grid_Load, 0))
  }
  Res_RSF_df <- reactive({Res_RSF(DataSet = get(input$DataSet.res), 
                                  Batt_kW = input$Batt_kW.res, 
                                  Batt_kWh = input$Batt_kWh.res, 
                                  Batt_Efficiency = input$Batt_Efficiency.res * 0.01, 
                                  Batt_DoD = input$Batt_DoD.res * 0.01,
                                  Batt_Backup = input$Batt_Backup.res * 0.01,
                                  Solar_kW = input$Solar.res)})
  } # General Algorithms
    
  {
  Res_RSF_Intro <- reactive({Res_RSF(DataSet = Med_House, 
                                     Batt_kW = input$RSF_IntroplotSlider*1, 
                                     Batt_kWh = input$RSF_IntroplotSlider*1.5, 
                                     Batt_Efficiency = 0.8, 
                                     Batt_DoD = 0.99,
                                     Batt_Backup = 0,
                                     Solar_kW = 4) %>%
      filter(Month %in% c("Jan", "Feb", "Mar", "Apr", "May", "Sep", "Oct", "Nov", "Dec")) %>%
      group_by(Time) %>%
      summarize(Grid.Load = mean(Grid_Load),
                Net.Use = mean(Net_Use),
                Electric.Use = mean(Electric_Use),
                Solar = mean(Solar))
    })
  
  output$RSF_Intro1 <- renderPlot({
    Res_RSF_Intro() %>%
      ggplot(aes(x = Time, ymin = Net.Use, ymax = Electric.Use)) +
      geom_ribbon(fill = "slategray3") +
      geom_line(aes(y = Net.Use), color = "black", size = 1) +
      geom_line(aes(y = Electric.Use), color = "slategray4", linetype = 2) +
      geom_line(aes(y = Solar), color = "#7a0019", size = 0.9) +
      theme_tufte() + 
      theme(axis.line = element_line(color = "black", size = 0.3),
            axis.text = element_text(size = 12, family = "Arial"),
            axis.title.x = element_blank(),
            axis.title.y = element_text(vjust = 3, size = 13, family = "Arial"),
            plot.title = element_text(hjust = 0.5, size = 13, face = "bold", family = "Arial"),
            plot.background = element_rect(fill = "#e3e3e3",
                                           color = "#e3e3e3"),
            plot.margin = unit(c(1,1.5,0,1), "lines")) +
      scale_x_time(expand = c(0,0),
                   breaks = c(0, 21600, 43200, 64800, 82800),
                   labels = c("12 am", "6 am", "12 pm", "6 pm", "12 am")) +
      labs(title = "Without Storage") +
      ylab("Average Electricity\nUse/Generation (kW)")
  }) # RSF Introplot1 - Could probably be converted to an image - isnt actually reactive
  
  output$RSF_Intro2 <- renderPlot({
    Res_RSF_Intro() %>%
      ggplot(aes(x = Time, ymin = Grid.Load, ymax = Electric.Use)) +
        geom_ribbon(fill = "slategray2", alpha = 0.5) +
        geom_ribbon(aes(ymin = Grid.Load + Net.Use - Grid.Load, ymax = Electric.Use), fill = "slategray3") +
        geom_line(aes(y = Grid.Load), color = "black", size = 1) +
        geom_line(aes(y = Electric.Use), color = "slategray4", linetype = 2) +
        geom_line(aes(y = Solar), color = "#7a0019", size = 0.9) +
        theme_tufte() + 
        theme(axis.line = element_line(color = "black", size = 0.3),
              axis.text = element_text(size = 12, family = "Arial"),
              axis.title.x = element_text(vjust = -2, size = 13, family = "Arial"),
              axis.title.y = element_text(vjust = 3, size = 13, family = "Arial"),
              plot.title = element_text(hjust = 0.5, size = 13, face = "bold", family = "Arial"),
              plot.background = element_rect(fill = "#e3e3e3",
                                             color = "#e3e3e3"),
              plot.margin = unit(c(1,1.5,1,1), "lines")) +
        scale_x_time(expand = c(0,0),
                     breaks = c(0, 21600, 43200, 64800, 82800),
                     labels = c("12 am", "6 am", "12 pm", "6 pm", "12 am")) +
        labs(title = "With Storage") +
        ylab("Average Electricity\nUse/Generation (kW)")
  }) # Solar Firming Introplot 2
  } # General Information Tab
    
  {
  output$datePlot_One.rsf   <- renderPlot({
    Res_RSF_df() %>%
      select(Date_Time, Date, Time, Electric_Use, Grid_Load, Solar, To_Grid, Net_Use, Batt_Load, Batt_Charge_Solar, Day_in_Year) %>%
      filter(between(x = Date, left = input$date_res[1], right = input$date_res[2])) %>%
      ggplot(aes(x = Date_Time)) +
        geom_area(aes(y = Electric_Use), fill = "#e3e3e3") +
        geom_line(aes(y = Solar), color = "darkred", size = 1) +
        geom_line(aes(y = Electric_Use), size = 0.3) +
        theme_tufte() +
        theme(axis.line = element_line(color = "black", size = 0.3),
              axis.title.x = element_blank(),
              axis.title.y = element_text(size = 14.5, vjust = 3, family = "Helvetica"),
              axis.text = element_text(size = 12, family = "Helvetica"),
              legend.position = "none",
              plot.margin = unit(c(0.5,0.5,0.5,1), "lines")) +
        scale_x_datetime(expand = c(0,0)) +
        scale_y_continuous(expand = c(0,0)) +
        ylab("Electric Use and Generation (kW)")
  }, height = 300)  
    
  output$datePlot_Two.rsf   <- renderPlot({
    Res_RSF_df() %>%
      select(Date_Time, Date, Time, Electric_Use, Grid_Load, Solar, To_Grid, Net_Use, Batt_Charge_Solar, Day_in_Year) %>%
      mutate(Direct_Use = Electric_Use - Net_Use,
             Solar_Self = Solar - To_Grid) %>%
      filter(between(x = Date, left = input$date_res[1], right = input$date_res[2])) %>%
      ggplot(aes(x = Date_Time)) +
        geom_area(aes(y = Solar), fill = "#a67f87") +
        geom_area(aes(y = Electric_Use), fill = "#e3e3e3", alpha = 0.6) +
        geom_area(aes(y = Solar_Self), fill = "#bbbbbb") +
        geom_area(aes(y = Direct_Use), fill = "slategray4", alpha = 0.8, color = "black") +
        geom_line(aes(y = Solar), color = "#7a0019", size = 0.6) +
        geom_line(aes(y = Electric_Use), color = "darkgrey", size = 0.3, alpha = 1) +
        theme_tufte() +
        theme(axis.line = element_line(color = "black", size = 0.5),
              axis.title.x = element_blank(),
              axis.title.y = element_text(size = 14.5, vjust = 3, family = "Helvetica"),
              axis.text = element_text(size = 12, family = "Helvetica"),
              legend.position = "none",
              plot.margin = unit(c(0.5,0.5,0.5,1), "lines")) +
        scale_x_datetime(expand = c(0,0)) +
        scale_y_continuous(expand = c(0,0)) +
        ylab("Electric Generation (kW)")
  }, height = 300)
  
  output$datePlot_Three.rsf <- renderPlot({
    Res_RSF_df() %>%
      select(Date_Time, Date, Time, Electric_Use, Grid_Load, Solar, To_Grid, Net_Use, Batt_Charge_Solar, Day_in_Year) %>%
      mutate(Direct_Use = Electric_Use - Net_Use) %>%
      filter(between(x = Date, left = input$date_res[1], right = input$date_res[2])) %>%
      ggplot(aes(x = Date_Time, ymin = Grid_Load, ymax = Electric_Use)) +
        geom_ribbon(fill = "slategray2", alpha = 0.5) +
        geom_ribbon(aes(ymin = Grid_Load, ymax = Grid_Load + Direct_Use), fill = "slategray3") +
        geom_line(aes(y = Grid_Load), color = "black", size = 0.8) +
        geom_line(aes(y = Electric_Use), color = "slategray4", alpha = 0.7) +
        #geom_line(aes(y = Solar), color = "darkred", size = 0.9, alpha = 0.2) +
        theme_tufte() +
        theme(axis.line = element_line(color = "black", size = 0.3),
              axis.title.x = element_blank(),
              axis.title.y = element_text(size = 14.5, vjust = 3, family = "Helvetica"),
              axis.text = element_text(size = 12, family = "Helvetica"),
              legend.position = "none",
              plot.margin = unit(c(0.5,0.5,0.5,1), "lines")) +
        scale_x_datetime(expand = c(0,0)) +
        scale_y_continuous(expand = c(0,0)) +
        ylab("Electric Consumption (kW)")
  }, height = 300)
  } # Daily Load Curves
    
  {
  output$monthPlot_Solar.rsf <- renderPlot({
    Res_RSF_df() %>%
        filter(Month == input$Month.res) %>%
        group_by(Time) %>%
        summarize(Grid.Load = mean(Grid_Load),
                  Net.Use = mean(Net_Use),
                  Electric.Use = mean(Electric_Use),
                  Solar = mean(Solar)) %>%
        ggplot(aes(x = Time, ymin = Net.Use, ymax = Electric.Use)) +
            geom_ribbon(fill = "lightsteelblue2") +
            geom_line(aes(y = Net.Use), color = "black", size = 1.2) +
            geom_line(aes(y = Electric.Use), color = "slategrey", linetype = 2) +
            geom_line(aes(y = Solar), color = "darkred", size = 1.2) +
            theme_tufte() + 
            theme(axis.line = element_line(color = "black", size = 0.3),
                  axis.title.x = element_blank(),
                  axis.title.y = element_text(size = 14.5, vjust = 3, family = "Helvetica"),
                  axis.text = element_text(size = 12, family = "Helvetica"),
                  axis.text.x = element_text(vjust = -1),
                  plot.margin = unit(c(0.5,1.2,0.5,1.2), "lines")) +
            scale_x_time(expand = c(0,0),
                         breaks = c(0, 20730, 42330, 63930, 82800),
                         labels = c("12am", "6am", "12pm", "6pm", "12am")) +
            ylab("Electricity Use/Generation (kW)")
    }, height = 300)
    
  output$monthPlot_Batt.rsf <- renderPlot({
    Res_RSF_df() %>%
        filter(Month == input$Month.res) %>%
        group_by(Time) %>%
        summarize(Grid.Load = mean(Grid_Load),
                  Net.Use = mean(Net_Use),
                  Electric.Use = mean(Electric_Use),
                  Solar = mean(Solar)) %>%
        ggplot(aes(x = Time, ymin = Grid.Load, ymax = Electric.Use)) +
            geom_ribbon(fill = "slategray2", alpha = 0.5) +
           #geom_ribbon(aes(ymin = Grid.Load, ymax = Grid.Load - Net.Use + Electric.Use), fill = "#b8c5d6") + # Alternative plot having direct self-consumption 
            geom_ribbon(aes(ymin = Grid.Load + Net.Use - Grid.Load, ymax = Electric.Use), fill = "lightsteelblue2") + # shading below stored shading rather than above it.
            geom_line(aes(y = Grid.Load), color = "black", size = 1.2) +
            geom_line(aes(y = Electric.Use), color = "slategrey", linetype = 2) +
            geom_line(aes(y = Solar), color = "darkred", size = 1.2) +
        
            theme_tufte() +
            theme(axis.line = element_line(color = "black", size = 0.3),
                  axis.title.x = element_blank(),
                  axis.title.y = element_text(size = 14.5, vjust = 3, family = "Helvetica"),
                  axis.text = element_text(size = 12, family = "Helvetica"),
                  axis.text.x = element_text(vjust = -1),
                  plot.margin = unit(c(0.5,1.2,0.5,1.2), "lines")) +
            scale_x_time(expand = c(0,0),
                         breaks = c(0, 20730, 42330, 63930, 82800),
                         labels = c("12am", "6am", "12pm", "6pm", "12am")) +
            ylab("Electricity Use/Generation (kW)")
    }, height = 300) 
  } # Monthly Load Curves
    
  {
  output$BillComp.rsf <- renderUI({
      Res_RSF_df() %>%
        mutate(NEM_Rate = ifelse(Season == "Summer", NEMRateSummer.rsf() * 0.01, NEMRateWinter.rsf() * 0.01)) %>%
        group_by(Month) %>%
        summarize(Trad.Nobatt = round(sum(Electric_Use * Regular_Rate), digits = 2),
                  ` ` = NA,
                  SoldBack.Solar = round(sum(Over_Gen), digits = 1),
                  NEMBill.Solar = round(sum(Net_Use * Regular_Rate - Over_Gen * Regular_Rate), digits = 2),
                  AdjustBill.Solar = round(sum(Net_Use * Regular_Rate - Over_Gen * NEM_Rate), digits = 2),
                  `  ` = NA,
                  SoldBack.Batt = round(sum(To_Grid), digits = 1),
                  NEMBill.Batt = round(sum(Grid_Load * Regular_Rate - To_Grid * Regular_Rate), digits = 2),
                  AdjustBill.Batt = round(sum(Grid_Load * Regular_Rate - To_Grid * NEM_Rate), digits = 2)) %>%
        arrange(match(Month, month.abb)) %>%
        adorn_totals("row") %>%
        
        flextable() %>%
        border_remove() %>%
        set_header_labels(Trad.Nobatt = "Standard Bill",
                          SoldBack.Solar = "kWh Returned to Grid",
                          NEMBill.Solar = "Net-Metered Bill",
                          AdjustBill.Solar = "Adjusted Bill",
                          SoldBack.Batt = "kWh Returned to Grid",
                          NEMBill.Batt = "Net-Metered Bill",
                          AdjustBill.Batt = "Adjusted Bill") %>%
        add_header(Trad.Nobatt = "No Solar or Storage",
                   SoldBack.Solar = "With Solar",
                   NEMBill.Solar = "With Solar",
                   AdjustBill.Solar = "With Solar",
                   SoldBack.Batt = "With Solar and Storage",
                   NEMBill.Batt = "With Solar and Storage",
                   AdjustBill.Batt = "With Solar and Storage") %>%
        merge_h(part = "header") %>%
        flextable::align(j = 1, align = "center") %>%
        flextable::align(part = "header", i = 1:2, align = "center") %>%
        hline(i = 1, j = 2, part = "header",
              border = fp_border(color = "black", width = 1)) %>%
        hline(i = 1, j = 4:6, part = "header",
              border = fp_border(color = "black", width = 1)) %>%
        hline(i = 1, j = 8:10, part = "header",
              border = fp_border(color = "black", width = 1)) %>%
        hline(i = 2, part = "header",
              border = fp_border(color = "black", width = 1.3)) %>%
        hline(i = 12, part = "body",
              border = fp_border(color = "black", width = 1.3)) %>%
        color(i = 13, j = c(3, 7), color="white") %>%
        bold(part = "header") %>%
        bold(part = "body", i = 13, j = 1:10) %>%
        fontsize(part = "all", size = 13) %>%
        width(width = 1.2) %>%
        width(j = c(4, 8), width = 1.4) %>%
        width(j = c(3, 7), width = 0.3) %>%
        height(part = "body", height = 0.3) %>%
        bg(i = 1:13, j = 2,  bg = "grey95") %>%
        bg(i = 1:13, j = 6,  bg = "grey95") %>%
        bg(i = 1:13, j = 10,  bg = "grey95") %>%
        colformat_num(col_keys = c("Trad.Nobatt", "NEMBill.Solar", "AdjustBill.Solar",
                                   "NEMBill.Batt", "AdjustBill.Batt"), big.mark = ",", digits = 2) %>%
        colformat_num(col_keys = c("SoldBack.Solar", "SoldBack.Batt"),
                      big.mark = ",", digits = 1) %>%
        htmltools_value()
    })
  
      
  NEMRateSummer.rsf <- reactive({
    input$NetMeterRate.rsf * 0.13437
  })
    
  output$NEMRateSummer.rsf <- renderText({
    paste0(round(NEMRateSummer.rsf(), digits = 2), "¢ per kW")
  })
  
  output$NEMDiffSummer.rsf <- renderText({
    paste0(round(13.437 - NEMRateSummer.rsf(), digits = 2), "¢ per kW")
  })
  
  NEMRateWinter.rsf <- reactive({
    input$NetMeterRate.rsf * 0.11742
  })
  
  output$NEMRateWinter.rsf <- renderText({
    paste0(round(NEMRateWinter.rsf(), digits = 2), "¢ per kW")
  })
  
  output$NEMDiffWinter.rsf <- renderText({
    paste0(round(11.742 - NEMRateWinter.rsf(), digits = 2), "¢ per kW")
  })
  
  
  yearlySavings.rsf <- reactive({
    Res_RSF_df() %>%
      mutate(NEM_Rate = ifelse(Season == "Summer", NEMRateSummer.rsf() * 0.01, NEMRateWinter.rsf() * 0.01)) %>%
      summarize(Trad_Bill = sum(Electric_Use * Regular_Rate),
                Solar_Bill = sum(Net_Use * Regular_Rate) - sum(Over_Gen * NEM_Rate),
                Batt_Bill = sum(Grid_Load * Regular_Rate) - sum(To_Grid * NEM_Rate)) %>%
      summarize(Savings = ifelse(input$ROI_Subj.rsf == "Both",
                                 Trad_Bill - Batt_Bill,
                                 Solar_Bill - Batt_Bill)) %>%
      as.numeric() %>%
      round(digits = 2)
  })
  
  output$YearlySavings.rsf <- renderText({
    paste0("$", format(yearlySavings.rsf(), big.mark = ",", nsmall = 2))
  })
  
  output$expLife.rsf <- renderText({
    paste(input$BattLife.rsf, "years")
  })
  
  output$discountRate.rsf <- renderText({
    paste0(input$discRate.rsf, "%")
  })
  
  output$batteryCost.rsf <- renderText({
    paste0("$", format(input$BattCost.rsf, big.mark = ",", scientific = FALSE))
  })
  
  output$PaybackPlot.rsf <- renderPlot({
    upfrontCost <- -(input$BattCost.rsf)
    expLife <- input$BattLife.rsf
    yearlySavings <- yearlySavings.rsf()
    payBack <- (-upfrontCost)/yearlySavings
    profitLoss = upfrontCost + expLife * yearlySavings
    
    ggplot(data = tibble(a = c(1))) +
      geom_hline(yintercept = 0) +
      geom_vline(xintercept = 0) +
      geom_abline(intercept = upfrontCost, slope = yearlySavings, color = "navyblue", size = 1) +
      geom_vline(xintercept = expLife, linetype = 2) +
      geom_vline(xintercept = -(upfrontCost) / yearlySavings, linetype = 2) +
      
      geom_point(aes(x = 0, y = upfrontCost), size = 2.5) +
      geom_point(aes(x = 0, y = upfrontCost), size = 1.5, color = "white", fill = "white", shape = 18) +
      
      geom_point(aes(x = payBack, y = 0), size = 2.5) +
      geom_point(aes(x = payBack, y = 0), size = 1.5, color = "white", fill = "white", shape = 18) +
      
      geom_segment(aes(x = .4, xend = .4, y = 0, yend = profitLoss),
                   color = ifelse(profitLoss > 0, "darkgreen", 
                                  ifelse(profitLoss < 0, "indianred4", "black")),
                   size = 1.1, arrow = arrow(ends = "last", angle = 90, length = unit(0.25, "lines"))) +
      geom_segment(aes(x = .4, xend = expLife, y = profitLoss, yend = profitLoss),
                   linetype = 3, size = 0.9, 
                   color = ifelse(profitLoss > 0, "darkgreen", 
                                  ifelse(profitLoss < 0, "indianred4", "black"))) +
      
      geom_text(aes(x = 0.5, y = upfrontCost-800), hjust = 0, label = "Initial Investment/\nUpfront Cost", fontface = "bold", size = 4.5) +
      geom_text(aes(x = .8, y = ifelse(profitLoss < -1000 | (profitLoss >= 0 & profitLoss < 1100), profitLoss + 600, profitLoss - 600)),
                hjust = 0, label = "Total Expected Lifetime Savings", fontface = "bold", size = 5) +
      geom_label(aes(x = ifelse(payBack <= 22.5 | payBack > 25.1, payBack + 1.45, payBack - 1.45), y = 0), 
                 label = "Break Even\nPoint", vjust = ifelse(payBack <= 22.5 | payBack > 25.1, 1.05, -0.05),
                 size = 4.5, fontface = "bold", fill = "white", alpha = 0.7,
                 label.size = NA, label.padding = unit(0.4, "lines")) +
      geom_text(aes(x = ifelse(expLife >= payBack, expLife + 1.8, expLife - 1.7),
                    y = upfrontCost*0.8), 
                label = "Expected Useful\nLife of Battery",
                size = 4.5, fontface = "bold") +
      
      theme_tufte() +
      coord_cartesian(xlim = c(0,
                               25),
                      #ifelse(payBack > expLife, payBack * 1.3, expLife * 1.3)), 
                      ylim = c((upfrontCost -1500), 
                               ifelse(profitLoss > 0, profitLoss + 1500, 1500))) +
      
      scale_x_continuous(name = "Years", 
                         breaks = c(5, 10, 15, 20, 25, 30),
                         labels = c("5 yrs", "10 yrs", "15 yrs", "20 yrs", "25 yrs", "30 yrs"),
                         expand = c(0,0)) +
      scale_y_continuous(name = "Cost (Dollars)",
                         breaks = seq.int(from = -100000, to = 100000, by = 2500)) +
      
      theme(axis.title = element_blank(),
            axis.text = element_text(size = 12),
            plot.margin = unit(c(1,1,1,1), "lines"))
  })
  } # Bill Comparison and Savings Tab
    
  {
  output$GenPlot.rsf <- renderPlot({
    a <- Res_RSF_df() %>%
      select(Time, Electric_Use, Grid_Load, Net_Use) %>%
      group_by(Time) %>%
      summarize(Electric_Use = mean(Electric_Use),
                Grid_Load = mean(Grid_Load),
                Net_Use = mean(Net_Use)) %>%
      mutate(C = Electric_Use,
             D = Grid_Load,
             G = Net_Use) %>%
      rename("A" = Electric_Use,
             "B" = Grid_Load,
             "E" = Net_Use) %>%
      gather(key = Line, value = kW, -Time, -G) %>%
      mutate(Plot = ifelse(Line == "A", "1",
                           ifelse(Line %in% c("B", "C", "E"), "2", "3")))
    
    ggplot(a, aes(x = Time, y = kW, color = Line)) +
      geom_rect(inherit.aes = FALSE, 
                aes(ymin = 0, ymax = Inf, xmin = 51500, xmax = 68950), 
                fill = "grey90") +
      geom_ribbon(data = filter(a, Line == "B"), inherit.aes = FALSE,
                  aes(x = Time, ymax = G, ymin = kW),
                  fill = "#c6d1d9", alpha = 0.9) +
      geom_ribbon(data = filter(a, Line == "C"), inherit.aes = FALSE,
                  aes(x = Time, ymin = G, ymax = kW),
                  fill = "#d9b6b6", alpha = 0.9) +
      geom_line(size = 0.7, aes(linetype = Line)) +
      facet_wrap(~Plot, ncol = 1,
                 labeller = labeller(Plot = c(`1` = "Old Load Curve without Solar or Storage",
                                              `2` = "Energy Use Direct from Solar/Stored and Used Later",
                                              `3` = "New Load Curve with Solar and Storage"))) +
      #scales = "free_y") +
      geom_hline(yintercept = 0, color = "black", size = 0.3) +
      theme_tufte() +
      theme(axis.line.y = element_line(color = "black", size = 0.3),
            axis.title.x = element_blank(),
            axis.title.y = element_text(size = 14, family = "Helvetica", vjust = 4),
            axis.text = element_text(size = 10, family = "Helvetica"),
            axis.text.x = element_text(vjust = -1),
            strip.text = element_text(size = 12, family = "Helvetica", face = "bold", vjust = 1),
            legend.position = "none",
            plot.margin = unit(c(1,1.7,0.5,1), "lines"),
            panel.spacing = unit(1, "lines")) +
      ylab("Average Electricity Use (kW)") +
      scale_x_time(breaks = c(0, 13550, 27400, 41250, 55100, 68950, 82500), 
                   labels = c("12:00am", "4:00am", "8:00am", "12:00pm", "4:00pm", "8:00pm", "12:00am"), 
                   expand = c(0,0)) +
      scale_y_continuous(expand = c(0.005,0.005)) +
      scale_color_manual(breaks = c("A", "B", "C", "D", "E"),
                         values = c("grey65", "black", "grey80", "black", "slategray")) +
      scale_linetype_manual(breaks = c("A", "B", "C", "D", "E"),
                            values = c(5,1,5,1,3))
    }, width = 375)
    
  output$Generation.rsf <- renderUI({
      Res_RSF_df() %>%
        left_join(Generation, b = "Date_Time") %>%
        select(Date_Time, Month, Electric_Use, Season, Solar, Solar_Charge, 
               Net_Use, Grid_Load, To_Grid, Pct_Renew, Pct_Clean, Carbon_per_kWh) %>%
        filter(!is.na(Pct_Renew)) %>%
        mutate(kWh_Renew_Reg = Pct_Renew * 0.01 * Electric_Use,
               kWh_Renew_Sol = Pct_Renew * 0.01 * Net_Use,
               kWh_Renew_Bat = Pct_Renew * 0.01 * Grid_Load,
               kWh_Clean_Reg = Pct_Clean * 0.01 * Electric_Use,
               kWh_Clean_Sol = Pct_Clean * 0.01 * Net_Use,
               kWh_Clean_Bat = Pct_Clean * 0.01 * Grid_Load,
               kg_Carbon_Reg = Carbon_per_kWh * Electric_Use,
               kg_Carbon_Sol = Carbon_per_kWh * Net_Use,
               kg_Carbon_Bat = Carbon_per_kWh * Grid_Load) %>%
        summarize(Total.kWh_Reg = sum(Electric_Use),
                  Total.kWh_Sol = sum(Net_Use),
                  Total.kWh_Bat = sum(Grid_Load),
                  Pct.Renew_Reg = sum(kWh_Renew_Reg)/sum(Electric_Use) * 100,
                  Pct.Renew_Sol = sum(kWh_Renew_Sol)/sum(Net_Use) * 100,
                  Pct.Renew_Bat = sum(kWh_Renew_Bat)/sum(Grid_Load) * 100,
                  Pct.Clean_Reg = sum(kWh_Clean_Reg)/sum(Electric_Use) * 100,
                  Pct.Clean_Sol = sum(kWh_Clean_Sol)/sum(Net_Use) * 100,
                  Pct.Clean_Bat = sum(kWh_Clean_Bat)/sum(Grid_Load) * 100,
                  kg.Carbon_Reg = sum(kg_Carbon_Reg),
                  kg.Carbon_Sol = sum(kg_Carbon_Sol),
                  kg.Carbon_Bat = sum(kg_Carbon_Bat),
                  C.Cost_Reg    = kg.Carbon_Reg * input$SCC.res * 0.00110231,
                  C.Cost_Sol    = kg.Carbon_Sol * input$SCC.res * 0.00110231,
                  C.Cost_Bat    = kg.Carbon_Bat * input$SCC.res * 0.00110231) %>%
        gather(key = key, value = value) %>%
        separate(key, sep = "_", into = c("Key", "Status")) %>%
        spread(key = Status, value = value) %>%
        arrange(desc(Key)) %>%
        select(Key, Reg, Sol, Bat) %>%
        mutate(Key = c("Total kWh Used", "Percent Renewable (%)", "Percent Clean (%)", "Carbon Emissions (kg)", "Social Cost ($)")) %>%
        
        flextable() %>%
        set_header_labels(`Key` = " ",
                          `Reg` = "None",
                          `Sol` = "With Solar*",
                          `Bat` = "With Storage") %>%
        fontsize(part = "all", size = 14) %>%
        height(height = 0.3) %>%
        width(width = 1.8) %>%
        width(j = 1, width = 2.3) %>%
        colformat_num(col_keys = c("Reg", "Sol", "Bat"), big.mark = ",", digits = 0) %>%
        bold(part = "header") %>%
        bg(i = 4, j = 1:4,  bg = "#d7d2c6") %>%
        htmltools_value()
    })
  } # Generation Resources Tab
  } # End of Residential Solar Firming
  
  
 # # # # COMMERCIAL SECTION # # # #
  
### Commercial TOU Section ###
  
  {
  {
  Comm_TOU <- function(DataSet, Batt_kW, Batt_kWh, Batt_Efficiency, Batt_DoD, Batt_Backup) {
    Comm_Battery <- Commercial_TOU %>%
      filter(Company == DataSet) %>%
      mutate(Max_Charge = ifelse(Batt_kWh > Batt_kW * 6, Batt_kW * 6, Batt_kWh),
             Mid_Peak_Avail = ifelse(Max_Charge - Peak_Area > 0, Max_Charge - Peak_Area, 0),
             MP_Discharge = Mid_Peak_Avail / 6,
             Weekend_Discharge = Mid_Peak_Avail / 16,
             TOU = ifelse(Weekend == 0 & TOU == "Mid_Peak",
                   ifelse(hour %in% c(7:14), "Mid_Peak_Y", "Mid_Peak_N"), TOU),
             Charge = ifelse(TOU == "Peak",
                             ifelse(Batt_kW >= Electric_Use, -Electric_Use, -Batt_kW),
                      ifelse(TOU == "Mid_Peak",
                             ifelse(Weekend_Discharge >= Electric_Use, -Electric_Use, -Weekend_Discharge),       
                      ifelse(TOU == "Mid_Peak_Y",
                             ifelse(MP_Discharge >= Electric_Use, -Electric_Use, -MP_Discharge),
                      ifelse(TOU == "Mid_Peak_N", 0, Batt_kW)))),
             Cumulative_Charge = Charge * 0.5)
    
    h <- function(x, y) max(min(x + y, Batt_kWh), Batt_kWh*(1-Batt_DoD) + (Batt_kWh - Batt_kWh * (1-Batt_DoD)) * (Batt_Backup))
    Batt_Charge <- Reduce(h, Comm_Battery$Cumulative_Charge, Batt_kWh, accumulate = TRUE)[-1]
    Batt_Charge.df <- tibble(Comm_Battery$Date_Time, Batt_Charge)
    
    Comm_Final <-  Comm_Battery %>%
      left_join(Batt_Charge.df, by = c("Date_Time" = "Comm_Battery$Date_Time")) %>%
      mutate(Charge_Discharge = Batt_Charge-lag(Batt_Charge, default = NA), # Determining the charge or discharge state of the battery by kW
             Charge_Discharge_Inefficient = ifelse(Charge_Discharge >= 0, Charge_Discharge, # Introducing the round-trip inefficiency to the dischargee
                                            ifelse(Charge_Discharge < 0, Charge_Discharge * Batt_Efficiency, 0)),
             Batt_Load = Charge_Discharge_Inefficient/0.5, # Determining how much load is offset or added from the battery.
             Grid_Load = Electric_Use + Batt_Load, # Determining the net load on the grid, including battery use.
             Batt_Reg_Cost = Grid_Load * Regular_Rate * 0.5,
             Batt_TOU_Cost = Grid_Load * TOU_Rate * 0.5) %>%
      filter(!is.na(Charge_Discharge))
  }
  Comm_TOU_df <- reactive({Comm_TOU(DataSet = input$Comm_Type, 
                                    Batt_kW = input$Batt_kW.comm, 
                                    Batt_kWh = input$Batt_kWh.comm, 
                                    Batt_Efficiency = input$Batt_Efficiency.comm * 0.01, 
                                    Batt_DoD = input$Batt_DoD.comm * 0.01,
                                    Batt_Backup = input$Batt_Backup.comm * 0.01)})
  } # General Algorithms
    
  {
    output$CTU_Intro <- renderPlot({
      Med_House_Intro %>%
        filter(Weekend == 0) %>%
        select(Date_Time, Date, Time, Month, Electric_Use) %>%
        group_by(Time) %>%
        summarize(Electric_Use = mean(Electric_Use)) %>%
        mutate(Hour = hour(Time),
               TOU = ifelse(Hour < 6, "Off-Peak",
                            ifelse(Hour >= 15 & Hour < 20, "Peak", "Mid-Peak")),
               Grid_Load = ifelse(TOU == "Off-Peak", Electric_Use + 0.17*input$CTU_IntroplotSlider,          # Adding load to off-peak hours
                                  ifelse(TOU == "Mid-Peak", Electric_Use - 0.05*input$CTU_IntroplotSlider,          # Reducing load from mid-peak hours
                                         Electric_Use - 0.11*input$CTU_IntroplotSlider))) %>%    # Reducing load from peak hours
        gather(key = key, value = kW, -Hour, -Time, -TOU) %>%
        
        ggplot(aes(x = Time, y = kW, fill = TOU, col = TOU)) +
        geom_col() +
        facet_wrap(key~., scales = "free", ncol = 1,
                   labeller = labeller(key = c(`Electric_Use` = "Without Storage",
                                               `Grid_Load` = "With Storage"))) +
        theme_tufte() + 
        theme(axis.line = element_line(color = "black", size = 0.3),
              strip.text = element_text(size = 13, face = "bold"), 
              axis.title.x = element_blank(),
              axis.title.y = element_text(size = 13),
              axis.text.x = element_text(size = 11, vjust = -0.25),
              axis.text.y = element_text(size = 11),
              legend.title = element_text(size = 13, hjust = 0.5),
              legend.text = element_text(size = 11),
              plot.background = element_rect(fill = "#e3e3e3",
                                             color = "#e3e3e3")) +
        ylab("Average Electricity Use (kW)") +
        scale_x_time(expand = c(0,0),
                     breaks = c(0, 21600, 43200, 64800, 85500),
                     labels = c("12 am", "6 am", "12 pm", "6 pm", "12 am")) +
        scale_y_continuous(expand = c(0,0)) +
        scale_color_manual(name = "Time-of-Use\nPeriod",
                           values = c("slategray3", "slategray2", "slategray4"),
                           breaks = c("Peak", "Mid-Peak", "Off-Peak")) +
        scale_fill_manual(name = "Time-of-Use\nPeriod",
                          values = c("slategray3", "slategray2", "slategray4"),
                          breaks = c("Peak", "Mid-Peak", "Off-Peak"))
    }, height = 300, width = 350)
  } # General Information Tab
  
  {  
  output$datePlot_Grid.ctu <- renderPlot({
    Comm_TOU_df() %>%
      filter(between(x = Date, left = input$date_comm[1], right = input$date_comm[2])) %>%
      select(Date_Time, Date, Time, Electric_Use, Grid_Load, Batt_Load) %>%
      mutate(Batt_State = ifelse(Batt_Load > 0, "Charge",
                          ifelse(Batt_Load < 0, "Discharge", "Standby")),
             Cycle_Change = ifelse(Batt_State != lag(Batt_State, default = ""), 1, 0),
             Cycle_Number = factor(cumsum(Cycle_Change))) %>%
      ggplot(aes(x = Date_Time, ymin = Electric_Use, ymax = Grid_Load)) +
        geom_ribbon(aes(group = Cycle_Number, fill = Batt_State), alpha = 0.3) +
        geom_line(aes(x = Date_Time, y = Electric_Use), color = "#aaaaaa", size = 0.5, linetype = 5) +
        geom_line(aes(x = Date_Time, y = Grid_Load), color = "black", size = 1.0) +
        theme_tufte() + 
        theme(axis.line = element_line(color = "black", size = 0.3),
              axis.title.x = element_blank(),
              axis.title.y = element_text(size = 14),
              axis.text = element_text(size = 12),
              legend.position = "none") +
        scale_fill_manual(breaks = c("Charge", "Discharge", "Standby"),
                          name = "Battery State",
                          values = c("red4", "skyblue4", "white")) +
        ylab("Electricity Use (kW)")
  }, height = 300)
    
  output$datePlot_Batt.ctu <- renderPlot({
      Comm_TOU_df() %>%
        mutate(Batt_State = ifelse(Batt_Load > 0, "Charge",
                            ifelse(Batt_Load < 0, "Discharge", "Standby")),
             Cycle_Change = ifelse(Batt_State != lag(Batt_State, default = ""), 1, 0),
             Cycle_Number = factor(cumsum(Cycle_Change))) %>%
        filter(between(x = Date, left = input$date_comm[1], right = input$date_comm[2])) %>%
        ggplot(aes(x = Date_Time)) +
          geom_area(aes(y = Batt_Load, group = Cycle_Number, fill = Batt_State), alpha = 0.3) +
          geom_line(aes(y = Batt_Load), color = "slategrey") +
          geom_line(aes(y = Batt_Charge), color = "black", size = 1.0) + 
          geom_hline(yintercept = 0, size = 0.3) +
          theme_tufte() + 
          theme(axis.line = element_line(color = "black", size = 0.3),
                axis.title.x = element_blank(),
                axis.title.y = element_text(size = 14),
                axis.text = element_text(size = 12),
                legend.position = "none") +
          scale_fill_manual(breaks = c("Charge", "Discharge", "Standby"),
                            name = "Battery State",
                            values = c("red4", "skyblue4", "white")) +
          ylab("Battery Activity (kW or kWh)")
  }, height = 300)
  } # Daily Load Curve Tab
  
  {  
  output$monthPlot_Grid.ctu <- renderPlot({
    Comm_TOU_df() %>%
      filter(Month == input$Month_comm) %>%
      group_by(Time) %>%
      summarize(Electric.Use = mean(Electric_Use), 
                Grid.Load =   mean(Grid_Load), 
                Batt.Charge = mean(Batt_Charge),
                Batt.Load =   mean(Batt_Load)) %>%
      ggplot(aes(x = Time)) +
      geom_ribbon(aes(ymin = Grid.Load, ymax = Electric.Use,
                      fill = Electric.Use >= Grid.Load), alpha = 0.3) +
      geom_line(aes(y = Electric.Use), col = "slategrey", size = 0.8, linetype = 2) +
      geom_line(aes(y = Grid.Load), col = "black", size = 1) +
      #geom_line(aes(y = Mean)) +
      ylab("Electricity Use (kW)") + xlab("Time") +
      scale_x_time(expand = c(0,0),
                   breaks = c(0, 21300, 42900, 64500, 84600),
                   labels = c("12am", "6am", "12pm", "6pm", "12am")) +
      scale_fill_manual(name = "Battery State",
                        breaks = c(FALSE, TRUE),
                        labels = c("Charging", "Discharging"),
                        values = c("red4", "skyblue4")) +
      theme_tufte() + 
      theme(axis.line = element_line(color = "black", size = 0.3),
            axis.title.x = element_blank(),
            axis.title.y = element_text(size = 14, family = "Helvetica"),
            axis.text = element_text(size = 12),
            legend.position = "none",
            plot.margin = unit(c(0.5,1.5,0.5,0.75), "lines"))
  }, height = 300)
    
  output$monthPlot_Batt.ctu <- renderPlot({
    Comm_TOU_df() %>%
      filter(Month == input$Month_comm) %>%
      group_by(Month, Time) %>%
      summarize(Electric.Use = mean(Electric_Use), 
                Grid.Load =    mean(Grid_Load), 
                Batt.Charge =  mean(Batt_Charge),
                Batt.Load =    mean(Batt_Load)) %>%
      ggplot(aes(x = Time)) +
      geom_area(aes(y = Batt.Load, fill = Electric.Use >= Grid.Load), alpha = 0.3) +
      geom_line(aes(y = Batt.Load), color = "slategrey") +
      geom_line(aes(y = Batt.Charge), color = "black", size = 1.2) +
      geom_hline(yintercept = 0, color = "black", size = 0.3) +
      ylab("Battery Activity (kW or kWh)") + xlab("Time") +
      scale_x_time(expand = c(0,0),
                   breaks = c(0, 21300, 42900, 64500, 84600),
                   labels = c("12am", "6am", "12pm", "6pm", "12am")) +
      scale_fill_manual(name = "Battery State",
                        breaks = c(FALSE, TRUE),
                        labels = c("Charging", "Discharging"),
                        values = c("red4", "skyblue4")) +
      theme_tufte() + 
      theme(axis.line = element_line(color = "black", size = 0.3),
            axis.title.x = element_blank(),
            axis.title.y = element_text(size = 14, family = "Helvetica"),
            axis.text = element_text(size = 12),
            legend.position = "none",
            plot.margin = unit(c(0.5,1.5,0.5,0.75), "lines"))
  }, height = 300)
  } # Monthly Load Curve Tab
    
  {  
  output$BillComp.ctu <- renderUI({
      Comm_TOU_df() %>%
        filter(Day_in_Year != 60) %>%
        mutate(Season = ifelse(Month %in% c("Jun", "Jul", "Aug", "Sep"), "Summer", "Winter"),
               TOU = ifelse(hour < 6, "Off-Peak", 
                            ifelse(hour >=15 & hour < 20 & Weekend == 0, "Peak", "Mid-Peak")),
               TOU_Rate = ifelse(TOU == "Off-Peak", 0.03830,
                          ifelse(TOU == "Mid-Peak" & Season == "Winter", 0.06897,
                          ifelse(TOU == "Mid-Peak" & Season == "Summer", 0.08352,
                          ifelse(TOU == "Peak" & Season == "Winter", 0.14788, 
                          ifelse(TOU == "Peak" & Season == "Summer", 0.17875, NA))))),
               Regular_Cost = Electric_Use * 0.5 * Regular_Rate,
               TOU_Cost = Electric_Use * 0.5 * TOU_Rate,
               Batt_Reg_Cost = Grid_Load * 0.5 * Regular_Rate,
               Batt_TOU_Cost = Grid_Load * 0.5 * TOU_Rate) %>%
      
        group_by(Month) %>%
        summarize(`Trad.Nobatt` = sum(Regular_Cost),
                  `TOU.Nobatt` = sum(TOU_Cost),
                  ` ` = NA,
                  `Trad.Batt` = sum(Batt_Reg_Cost),
                  `TOU.Batt` = sum(Batt_TOU_Cost), 
                  `  ` = NA,
                  `kWh.Nobatt` = sum(Electric_Use*0.5),
                  `kWh.Batt` = sum(Grid_Load*0.5)) %>%
        arrange(match(Month, month.abb)) %>%
        adorn_totals("row") %>%
        
        flextable() %>%
        border_remove() %>%
        
        set_header_labels(Trad.Nobatt = "Standard Bill",
                          TOU.Nobatt = "Time-of-Use Bill",
                          Trad.Batt = "Standard Bill",
                          TOU.Batt = "Time-of-Use Bill",
                          kWh.Nobatt = "w/o Battery",
                          kWh.Batt = "w/ Battery") %>%
        add_header(Trad.Nobatt = "No Battery",
                   TOU.Nobatt = "No Battery",
                   Trad.Batt = "With Battery",
                   TOU.Batt = "With Battery",
                   kWh.Nobatt = "Energy Use (kWh)",
                   kWh.Batt = "Energy Use (kWh)") %>%
        merge_h(part = "header") %>%
        flextable::align(j = 1, align = "center") %>%
        flextable::align(part = "header", i = 1:2, align = "center") %>%
        hline(i = 1, j = 2:3, part = "header",
              border = fp_border(color = "black", width = 1)) %>%
        hline(i = 1, j = 5:6, part = "header",
              border = fp_border(color = "black", width = 1)) %>%
        hline(i = 1, j = 8:9, part = "header",
              border = fp_border(color = "black", width = 1)) %>%
        hline(i = 2, part = "header",
              border = fp_border(color = "black", width = 1.3)) %>%
        hline(i = 12, part = "body",
              border = fp_border(color = "black", width = 1.3)) %>%
        color(i = 13, j = c(4, 7), color="white") %>%
        bold(part = "header") %>%
        bold(part = "body", i = 13, j = 1:9) %>%
        fontsize(part = "all", size = 13) %>%
        width(width = 1.2) %>%
        width(j = 4, width = 0.5) %>%
        width(j = 7, width = 0.5) %>%
        height(part = "body", height = 0.3) %>%
        bg(i = 1:13, j = 2,  bg = "grey95") %>%
        bg(i = 1:13, j = 6,  bg = "grey95") %>%
        colformat_num(col_keys = c("Trad.Nobatt", "TOU.Nobatt",
                                   "Trad.Batt", "TOU.Batt"), big.mark = ",", digits = 2) %>%
        colformat_num(col_keys = c("kWh.Nobatt", "kWh.Batt"),
                      big.mark = ",", digits = 0) %>%
        htmltools_value()
    })

  yearlySavings.ctu <- reactive({
    Comm_TOU_df() %>%
      filter(Day_in_Year != 60) %>%
      mutate(Season = ifelse(Month %in% c("Jun", "Jul", "Aug", "Sep"), "Summer", "Winter"),
             TOU = ifelse(hour < 6, "Off-Peak", 
                          ifelse(hour >=15 & hour < 20 & Weekend == 0, "Peak", "Mid-Peak")),
             TOU_Rate = ifelse(TOU == "Off-Peak", 0.03830,
                        ifelse(TOU == "Mid-Peak" & Season == "Winter", 0.06897,
                        ifelse(TOU == "Mid-Peak" & Season == "Summer", 0.08352,
                        ifelse(TOU == "Peak" & Season == "Winter", 0.14788, 
                        ifelse(TOU == "Peak" & Season == "Summer", 0.17875, NA))))),
             Regular_Cost = Electric_Use * 0.5 * Regular_Rate,
             TOU_Cost = Electric_Use * 0.5 * TOU_Rate,
             Batt_Reg_Cost = Grid_Load * 0.5 * Regular_Rate,
             Batt_TOU_Cost = Grid_Load * 0.5 * TOU_Rate) %>%
        summarize(Trad_Bill = sum(Regular_Cost),
                  TOU_Bill = sum(Batt_TOU_Cost)) %>%
        summarize(Savings = Trad_Bill - TOU_Bill) %>%
        as.numeric() %>%
        round(digits = 2)
    })
    
  output$YearlySavings.ctu <- renderText({
      paste0("$", format(yearlySavings.ctu(), big.mark = ",", nsmall = 2))
  })
    
  output$expLife.ctu <- renderText({
      paste(input$BattLife.ctu, "years")
    })
    
  output$discountRate.ctu <- renderText({
      paste0(input$discRate.ctu, "%")
    })
    
  output$batteryCost.ctu <- renderText({
      paste0("$", format(input$BattCost.ctu, big.mark = ",", scientific = FALSE))
    })
    
  output$PaybackPlot.ctu <- renderPlot({
      upfrontCost <- -(input$BattCost.ctu)
      expLife <- input$BattLife.ctu
      yearlySavings <- yearlySavings.ctu()
      payBack <- (-upfrontCost)/yearlySavings
      profitLoss = upfrontCost + expLife * yearlySavings
      
      ggplot(data = tibble(a = c(1))) +
        geom_hline(yintercept = 0) +
        geom_vline(xintercept = 0) +
        geom_abline(intercept = upfrontCost, slope = yearlySavings, color = "navyblue", size = 1) +
        geom_vline(xintercept = expLife, linetype = 2) +
        geom_vline(xintercept = -(upfrontCost) / yearlySavings, linetype = 2) +
        
        geom_point(aes(x = 0, y = upfrontCost), size = 2.5) +
        geom_point(aes(x = 0, y = upfrontCost), size = 1.5, color = "white", fill = "white", shape = 18) +
        
        geom_point(aes(x = payBack, y = 0), size = 2.5) +
        geom_point(aes(x = payBack, y = 0), size = 1.5, color = "white", fill = "white", shape = 18) +
        
        geom_segment(aes(x = .4, xend = .4, y = 0, yend = profitLoss),
                     color = ifelse(profitLoss > 0, "darkgreen", 
                                    ifelse(profitLoss < 0, "indianred4", "black")),
                     size = 1.1, arrow = arrow(ends = "last", angle = 90, length = unit(0.25, "lines"))) +
        geom_segment(aes(x = .4, xend = expLife, y = profitLoss, yend = profitLoss),
                     linetype = 3, size = 0.9, 
                     color = ifelse(profitLoss > 0, "darkgreen", 
                                    ifelse(profitLoss < 0, "indianred4", "black"))) +
        
        geom_label(aes(x = 0.5, y = upfrontCost-2000), hjust = 0, label = "Initial Investment/\nUpfront Cost", 
                   fontface = "bold", size = 4.5, label.size = NA, alpha = 0.5) +
        geom_text(aes(x = .8, y = ifelse(profitLoss < -4000 | (profitLoss >= 0 & profitLoss < 4100), profitLoss + 2500, profitLoss - 2500)),
                  hjust = 0, label = "Total Expected Lifetime Savings", fontface = "bold", size = 5) +
        geom_label(aes(x = ifelse(payBack <= 22.5 | payBack > 25.1, payBack + 1.45, payBack - 1.45), y = 0), 
                   label = "Break Even\nPoint", vjust = ifelse(payBack <= 22.5 | payBack > 25.1, 1.05, -0.05),
                   size = 4.5, fontface = "bold", fill = "white", alpha = 0.7,
                   label.size = NA, label.padding = unit(0.4, "lines")) +
        geom_label(aes(x = ifelse(expLife >= payBack, expLife + 1.8, expLife - 1.8),
                      y = upfrontCost*0.8), 
                  label = "Expected Useful\nLife of Battery",
                  size = 4.5, fontface = "bold", label.size = NA, alpha = 0.5) +
        
        theme_tufte() +
        coord_cartesian(xlim = c(0,
                                 25),
                        #ifelse(payBack > expLife, payBack * 1.3, expLife * 1.3)), 
                        ylim = c((upfrontCost -2500), 
                                 ifelse(profitLoss > 2500, profitLoss + 2500, 5000))) +
        
        scale_x_continuous(name = "Years", 
                           breaks = c(5, 10, 15, 20, 25, 30),
                           labels = c("5 yrs", "10 yrs", "15 yrs", "20 yrs", "25 yrs", "30 yrs"),
                           expand = c(0,0)) +
        scale_y_continuous(name = "Cost (Dollars)",
                           breaks = seq.int(from = -500000, to = 500000, by = 10000)) +
        
        theme(axis.title = element_blank(),
              axis.text = element_text(size = 12),
              plot.margin = unit(c(1,1,1,1), "lines"))
    })
    
  } # Bill Comparison and Savings Tab
    
  {
  output$GenPlot.ctu <- renderPlot({
      a <- Comm_TOU_df() %>%
        select(Time, Electric_Use, Grid_Load) %>%
        group_by(Time) %>%
        summarize(Electric_Use = mean(Electric_Use),
                  Grid_Load = mean(Grid_Load)) %>%
        mutate(C = Electric_Use,
               D = Grid_Load,
               E = Electric_Use) %>%
        rename("A" = Electric_Use,
               "B" = Grid_Load) %>%
        gather(key = Line, value = kW, -Time, -E) %>%
        mutate(Plot = ifelse(Line == "A", "1",
                             ifelse(Line %in% c("B", "C"), "2", "3")),
               Fill = ifelse(E >= kW, "Discharge", "Charge"))
      
      ggplot(a, aes(x = Time, y = kW, color = Line)) +
        geom_rect(inherit.aes = FALSE, aes(ymin = 0, ymax = Inf, xmin = 52800, xmax = 70500), fill = "grey90") +
        geom_ribbon(data = filter(a, Line == "B"),
                    aes(ymin = kW, ymax = E, fill = Fill),
                    alpha = 0.9, color = "white") +
        geom_line(size = 0.7, aes(linetype = Line)) +
        facet_wrap(~Plot, ncol = 1,
                   labeller = labeller(Plot = c(`1` = "Old Load Curve without Storage",
                                                `2` = "Storage Device Charge/Discharge Activity",
                                                `3` = "New Load Curve with Storage")),
                   scales = "free_y") +
        geom_hline(yintercept = 0, color = "black", size = 0.3) +
        theme_tufte() +
        theme(axis.line.y = element_line(color = "black", size = 0.3),
              axis.title.x = element_blank(),
              axis.title.y = element_text(size = 14, family = "Helvetica", vjust = 4),
              axis.text = element_text(size = 10, family = "Helvetica"),
              axis.text.x = element_text(vjust = -1),
              strip.text = element_text(size = 12, family = "Helvetica", face = "bold", vjust = 1),
              legend.position = "none",
              plot.margin = unit(c(1,1.7,0.5,1), "lines"),
              panel.spacing = unit(1, "lines")) +
        ylab("Average Electricity Use (kW)") +
        scale_x_time(breaks = c(0, 14100, 28200, 42300, 56400, 70500, 84400), 
                     labels = c("12:00am", "4:00am", "8:00am", "12:00pm", "4:00pm", "8:00pm", "12:00am"), 
                     expand = c(0,0)) +
        scale_y_continuous(expand = c(0.005,0.005)) +
        scale_color_manual(breaks = c("A", "B", "C", "D"),
                           values = c("grey65", "black", "grey80", "black")) +
        scale_linetype_manual(breaks = c("A", "B", "C", "D"),
                              values = c(5,1,5,1)) +
        scale_fill_manual(breaks = c("Charge", "Discharge"),
                          values = c("#d9b6b6", "#c6d1d9"))
    }, width = 375)
    
  output$Generation.ctu <- renderUI({
      Comm_TOU_df() %>%
        left_join(Generation, by = "Date_Time") %>%
        select(Date_Time, Month, Electric_Use, Grid_Load, Pct_Renew, Pct_Clean, Carbon_per_kWh) %>%
        filter(!is.na(Pct_Renew)) %>%
        mutate(kWh_Renew_Reg = Pct_Renew * 0.01 * Electric_Use,
               kWh_Renew_Bat = Pct_Renew * 0.01 * Grid_Load,
               kWh_Clean_Reg = Pct_Clean * 0.01 * Electric_Use,
               kWh_Clean_Bat = Pct_Clean * 0.01 * Grid_Load,
               kg_Carbon_Reg = Carbon_per_kWh * Electric_Use,
               kg_Carbon_Bat = Carbon_per_kWh * Grid_Load) %>%
        summarize(Total.kWh_Reg = sum(Electric_Use),
                  Total.kWh_Bat = sum(Grid_Load),
                  Pct.Renew_Reg = sum(kWh_Renew_Reg)/sum(Electric_Use) * 100,
                  Pct.Renew_Bat = sum(kWh_Renew_Bat)/sum(Grid_Load) * 100,
                  Pct.Clean_Reg = sum(kWh_Clean_Reg)/sum(Electric_Use) * 100,
                  Pct.Clean_Bat = sum(kWh_Clean_Bat)/sum(Grid_Load) * 100,
                  kg.Carbon_Reg = sum(kg_Carbon_Reg),
                  kg.Carbon_Bat = sum(kg_Carbon_Bat),
                  C.Cost_Reg    = kg.Carbon_Reg * input$SCC.comm * 0.00110231,
                  C.Cost_Bat    = kg.Carbon_Bat * input$SCC.comm * 0.00110231) %>%
        gather(key = key, value = value) %>%
        separate(key, sep = "_", into = c("Key", "Status")) %>%
        spread(key = Status, value = value) %>%
        arrange(desc(Key)) %>%
        select(Key, Reg, Bat) %>%
        mutate(Key = c("Total kWh Used", "Percent Renewable (%)", "Percent Clean (%)", "Carbon Emissions* (kg)", "Social Cost ($)")) %>%
        
        flextable() %>%
        set_header_labels(`Key` = " ",
                          `Reg` = "Without Storage",
                          `Bat` = "With Storage") %>%
        fontsize(part = "all", size = 14) %>%
        height(height = 0.3) %>%
        width(width = 1.8) %>%
        width(j = 1, width = 2.3) %>%
        colformat_num(col_keys = c("Reg", "Bat"), big.mark = ",", digits = 0) %>%
        bg(i = 4, j = 1:3,  bg = "#d7d2c6") %>%
        bold(part = "header") %>%
        htmltools_value()
    })
  } # Generation Resources Tab
  } # End of Commercial Time-of-Use
  
### Commercial Peak-Shaving Section ###
  
  {
  {
  Comm_PS <- function(DataSet, Batt_kW, Batt_kWh, Batt_Efficiency, Batt_DoD, Batt_Backup) {
      PS_Battery <- Commercial_PS %>%
          filter(Company == DataSet) %>%
          mutate(a = (Batt_kWh*Batt_DoD)/Batt_Efficiency - Peak_kWh) %>%
          filter(Charge_kWh >= Peak_kWh / Batt_Efficiency,
                 Peak_kWh <= Batt_kWh * Batt_DoD * Batt_Efficiency,
                 a >= 0,
                 Max_kW <= Batt_kW) %>%
          group_by(Date) %>%
          mutate(b = min(a)) %>%
          ungroup() %>%
          arrange(Date) %>%
          filter(a == b) %>%
          mutate(Peak_kW = ifelse(Electric_Use - Daily_Max > 0, Electric_Use - Daily_Max, 0),
                 Batt_State = ifelse(Peak_kW == 0, "Charge",
                              ifelse(Peak_kW > 0, "Discharge", NA)),
                 Charge = ifelse(Batt_State == "Charge",
                                 ifelse(Daily_Max - Electric_Use >= Batt_kW, Batt_kW, Daily_Max - Electric_Use),
                          ifelse(Peak_kW/Batt_Efficiency >= Batt_kW, -Batt_kW, -Peak_kW / Batt_Efficiency)),
                 Cumulative_Charge = Charge * 0.5)
        
      i <- function(x, y) max(min(x + y, Batt_kWh), Batt_kWh*(1-Batt_DoD) + (Batt_kWh - Batt_kWh * (1-Batt_DoD)) * (Batt_Backup))
      Peak_Batt_Charge <- Reduce(i, PS_Battery$Cumulative_Charge, Batt_kWh, accumulate = TRUE)[-1]
      Peak_Batt_Charge.df <- tibble(PS_Battery$Date_Time, Peak_Batt_Charge)
        
      PS_Final <- PS_Battery %>%
          left_join(Peak_Batt_Charge.df, by = c("Date_Time" = "PS_Battery$Date_Time")) %>%
          mutate(Batt_Charge = Peak_Batt_Charge,
                 Charge_Discharge = Batt_Charge-lag(Batt_Charge, default = NA), # Determining the charge or discharge state of the battery by kW
                 Charge_Discharge_Inefficient = ifelse(Charge_Discharge >= 0, Charge_Discharge, # Introducing the round-trip inefficiency to the dischargee
                                                ifelse(Charge_Discharge < 0, Charge_Discharge * Batt_Efficiency, 0)),
                 Batt_Load = Charge_Discharge_Inefficient/0.5, # Determining how much load is offset or added from the battery.
                 Grid_Load = Electric_Use + Batt_Load) %>%
          filter(!is.na(Charge_Discharge))
  }
  Comm_PS_df <- reactive({Comm_PS(DataSet = input$Comm_Type,
                                  Batt_kW = input$Batt_kW.comm, 
                                  Batt_kWh = input$Batt_kWh.comm, 
                                  Batt_Efficiency = input$Batt_Efficiency.comm * 0.01,
                                  Batt_DoD = input$Batt_DoD.comm * 0.01,
                                  Batt_Backup = input$Batt_Backup.comm * 0.01)}) 
  } # General Algorithms
    
  {
  output$CPS_Intro1 <- renderPlot({
    Batt_kW <- input$CPS_IntroplotSlider * 0.5
    
    PS_Battery <- Med_House.rps %>%
      mutate(Date_Time = ymd_hms(Date_Time),
             Date = ymd(Date),
             Time = as.hms(hour(Date_Time)*3600 + minute(Date_Time)*60),
             a = (50) - Peak_kWh,
             b = ifelse(a < 0, NA, a),
             Pct = as.numeric(Pct),
             Daily_Max = Pct * Max * 0.01,
             Max_kW = Max - Daily_Max) %>%
      filter(Charge_kWh >= Peak_kWh,
             Peak_kWh <= 50,
             !is.na(b),
             Max_kW <= (Batt_kW)) %>%
      group_by(Date) %>%
      mutate(c = min(b)) %>%
      ungroup() %>%
      arrange(Date) %>%
      filter(a == c) %>%
      mutate(Peak_kW = ifelse(Electric_Use - Daily_Max > 0, Electric_Use - Daily_Max, 0),
             Batt_State = ifelse(Peak_kW == 0, "Charge",
                                 ifelse(Peak_kW > 0, "Discharge", NA)),
             Charge = ifelse(Batt_State == "Charge" & Daily_Max - Electric_Use >= Batt_kW, Batt_kW,
                             ifelse(Batt_State == "Charge" & Daily_Max - Electric_Use < Batt_kW, Daily_Max-Electric_Use,
                                    ifelse(Batt_State == "Discharge" & Peak_kW >= Batt_kW, -Batt_kW,
                                           ifelse(Batt_State == "Discharge" & Peak_kW < Batt_kW, -Peak_kW, NA)))),
             Cumulative_Charge = Charge * elapsed_time)
    
    g <- function(x, y) max(min(x + y, 50), 0)
    Peak_Batt_Charge <- Reduce(g, PS_Battery$Cumulative_Charge, 50, accumulate = TRUE)[-1]
    Peak_Batt_Charge.df <- tibble(PS_Battery$Date_Time, Peak_Batt_Charge)
    
    PS_Final <-  PS_Battery %>%
      left_join(Peak_Batt_Charge.df, by = c("Date_Time" = "PS_Battery$Date_Time")) %>%
      filter(elapsed_time != 0) %>%
      mutate(Batt_Charge = Peak_Batt_Charge,
             Charge_Discharge = Batt_Charge-lag(Batt_Charge, default = NA), # Determining the charge or discharge state of the battery by kW
             Charge_Discharge_Inefficient = ifelse(Charge_Discharge >= 0, Charge_Discharge, # Introducing the round-trip inefficiency to the dischargee
                                                   ifelse(Charge_Discharge < 0, Charge_Discharge, 0)),
             Batt_Load = Charge_Discharge_Inefficient/elapsed_time, # Determining how much load is offset or added from the battery.
             Grid_Load = Electric_Use + Batt_Load) %>%
      filter(!is.na(Charge_Discharge)) %>%
      filter(Month == "Aug", Day == 14) %>%
      select(Time, Grid_Load, Electric_Use, Daily_Max, Batt_Load) %>%
      mutate(Grid_Load_Max = max(Grid_Load), 
             Electric_Use_Max = max(Electric_Use),
             Batt_State = ifelse(Batt_Load > 0, "Charge",
                                 ifelse(Batt_Load < 0, "Discharge", "Standby")),
             Electric_Use_Cut = ifelse(Electric_Use <= Daily_Max, Electric_Use, Daily_Max),
             Grid_Load_Cut = Electric_Use_Cut,
             Grid_Load_Before = Electric_Use) %>%
      gather(key = key, value = kW, -Time, -Daily_Max, -Batt_Load, -Batt_State) %>%
      mutate(Plot = ifelse(startsWith(key, "Electric_Use"), "Plot_1", "Plot_2"))
    
    
    PS_Final %>%
      filter(!endsWith(key, "Max"), !endsWith(key, "Before")) %>%
      ggplot(aes(x = Time, y = kW, fill = key)) +
        geom_line(data = filter(PS_Final, endsWith(key, "Before")), color = "grey60", linetype = 2) +
        geom_area(position = "identity", color = "black", size = 0.2) +
        geom_line(data = filter(PS_Final, endsWith(key, "Max")), color = "grey10", size = 0.8) +
        geom_hline(yintercept = 0) +
        facet_wrap(Plot~., ncol = 1,
                   labeller = labeller(Plot = c(`Plot_1` = "Without Energy Storage",
                                                `Plot_2` = "With Energy Storage"))) +
        theme_tufte() + 
        theme(axis.line = element_line(color = "black", size = 0.4), 
              legend.position = "none",
              strip.text = element_text(size = 13, face = "bold", family = "Helvetica"),
              axis.title.x = element_blank(),
              axis.title.y = element_text(size = 14, vjust = 4, family = "Helvetica"),
              axis.text.y = element_text(size = 13, family = "Helvetica"),
              axis.text.x = element_text(size = 12, vjust = -0.75, family = "Helvetica"),
              plot.margin = unit(c(0.5, 1, 1, 1.3), "lines"),
              panel.spacing = unit(1, "lines"),
              plot.background = element_rect(fill = "#e3e3e3", color = "#e3e3e3")) +
        ylab("Electricity Use (kW)") +
        scale_x_time(expand = c(0,0),
                     breaks = c(0, 21600, 43200, 64800, 85400),
                     labels = c("12am", "6am", "12pm", "6pm", "12am")) +
        scale_y_continuous(expand = c(0, 0)) +
        scale_fill_manual(breaks = c("Electric_Use", "Electric_Use_Cut", "Electric_Use_Max", "Grid_Load", "Grid_Load_Before", "Grid_Load_Cut", "Grid_Load_Max"),
                          values = c("#ab6666", "grey97", "black", "#a0b4c8", "black", "grey97", "black")) +
        coord_cartesian(ylim = c(0,8.5))
  })
  } # General Information Tab
    
  {
  output$datePlot_Grid.cps <- renderPlot({
      Comm_PS_df() %>%
        mutate(Batt_State = ifelse(Batt_Load > 0, "Charge",
                          ifelse(Batt_Load < 0, "Discharge", "Standby")),
             Cycle_Change = ifelse(Batt_State != lag(Batt_State, default = ""), 1, 0),
             Cycle_Number = factor(cumsum(Cycle_Change))) %>%
        filter(between(x = Date, left = input$date_comm[1], right = input$date_comm[2])) %>%
        ggplot(aes(x = Date_Time, ymin = Electric_Use, ymax = Grid_Load)) +
          geom_line(aes(y = Electric_Use), color = "slategrey", size = 0.6, linetype = 2) +
          geom_line(aes(y = Grid_Load), color = "black", size = 1.0) +
          geom_ribbon(aes(group = Cycle_Number, fill = Batt_State), alpha = 0.3) +
          theme_tufte() + 
          theme(axis.line = element_line(color = "black", size = 0.3),
                axis.title.x = element_blank(),
                axis.title.y = element_text(size = 14),
                axis.text = element_text(size = 12),
                legend.position = "none") +
          scale_x_datetime(expand = c(0,0)) +
          scale_fill_manual(breaks = c("Charge", "Discharge", "Standby"),
                            name = "Battery State",
                            values = c("red4", "skyblue4", "white")) +
          ylab("Electricity Use (kW)")
    }, height = 300)
    
  output$datePlot_Batt.cps <- renderPlot({
      Comm_PS_df() %>%
        mutate(Batt_State = ifelse(Batt_Load > 0, "Charge",
                            ifelse(Batt_Load < 0, "Discharge", "Standby")),
               Cycle_Change = ifelse(Batt_State != lag(Batt_State, default = ""), 1, 0),
               Cycle_Number = factor(cumsum(Cycle_Change))) %>%
        filter(between(x = Date, left = input$date_comm[1], right = input$date_comm[2])) %>%
        ggplot(aes(x = Date_Time)) +
            geom_area(aes(y = Batt_Load, group = Cycle_Number, fill = Batt_State), alpha = 0.3) +
            geom_line(aes(y = Batt_Load), color = "slategrey") +
            geom_line(aes(y = Batt_Charge), color = "black", size = 1.0) + 
            geom_hline(yintercept = 0, size = 0.3) +
            theme_tufte() + 
            theme(axis.line = element_line(color = "black", size = 0.3),
                  axis.title.x = element_blank(),
                  axis.title.y = element_text(size = 14),
                  axis.text = element_text(size = 12),
                  legend.position = "none") +
            scale_x_datetime(expand = c(0,0)) +
            scale_fill_manual(breaks = c("Charge", "Discharge", "Standby"),
                              name = "Battery State",
                              values = c("red4", "skyblue4", "white")) +
            ylab("Battery Activity (kW or kWh)")
    }, height = 300)
  } # Daily Load Curve Tab
    
  {
  output$monthPlot_Grid.cps <- renderPlot({
    
      Old_Max <- Comm_PS_df() %>%
          filter(Month == input$Month_comm) %>%
          summarize(Old_Max = max(Electric_Use)) %>%
          as.numeric()
      
      New_Max <- Comm_PS_df() %>%
          filter(Month == input$Month_comm) %>%
          summarize(New_Max = max(Grid_Load)) %>%
          as.numeric()
    
      Comm_PS_df() %>%
          filter(Month == input$Month_comm) %>%
          select(Date_Time, Grid_Load, Electric_Use) %>%
          mutate(Max_Grid_Load = max(Grid_Load), 
                 Max_Electric_Use = max(Electric_Use)) %>%
          gather(key = key, value = kW, -Date_Time) %>%
      
          ggplot(aes(x = Date_Time, y = kW, col = key)) +
              geom_line(size = 0.8) +
              annotate(geom = "text", label = paste("Monthly Peak without Storage:", round(Old_Max, digits = 1), "kW"),
                       x = ymd_hms(paste0("2016-", input$Month_comm, "-01 03:00:00")), y = Old_Max,
                       hjust = -0.03, vjust = -0.7, size = 5, color = "grey20", fontface = "bold") +
              annotate(geom = "label", label = paste("Monthly Peak with Storage:", round(New_Max, digits = 1), "kW"),
                       x = ymd_hms(paste0("2016-", input$Month_comm, "-01 03:00:00")), y = New_Max,
                       hjust = 0, vjust = -0.05, size = 5, color = "navyblue",
                       fontface = "bold", fill = "white", alpha = 0.5,
                       label.size = NA, label.padding = unit(0.4, "lines")) +
              ylab("Electricity Use (kW)") + 
              xlab("Date") +
              scale_x_datetime(expand = c(0,0)) +
              scale_color_manual(name = "Use",
                                 breaks = c("Electric_Use", "Grid_Load", "Max_Electric_Use", "Max_Grid_Load"),
                                 labels = c("Electric Use w/o Battery", "Electric Use w/ Battery", "Peak w/o Battery", "Peak w/ Battery"),
                                 values = c("grey70", "navyblue", "grey50", "navyblue")) +
              theme_tufte() + 
              theme(axis.line = element_line(color = "black", size = 0.3),
                    axis.title.x = element_blank(),
                    axis.title.y = element_text(size = 14.5, vjust = 3, family = "Helvetica"),
                    axis.text = element_text(size = 12, family = "Helvetica"),
                    axis.text.x = element_text(vjust = -1),
                    legend.position = "none",
                    plot.margin = unit(c(1,0.5,0.5,0.5), "lines"))
    }, height = 400)  
  } # Monthly Load Curve Tab
    
  {
  output$BillComp.cps <- renderUI({
      Comm_PS_df() %>%
        filter(yday(Date) != 60) %>%
        mutate(Reg_Rate = ifelse(Month %in% c("Jun", "Jul", "Aug", "Sep"), 0.09256, 0.07757),
               Peak_Rate = ifelse(Month %in% c("Jun", "Jul", "Aug", "Sep"), input$Demand_Charge_Rate * 2.958, input$Demand_Charge_Rate * 2.098)) %>%
        group_by(Month) %>%
        summarize(Trad.Bill = sum(Electric_Use * 0.5 * Reg_Rate),
                  #` ` = NA,
                  kWh.Charge.Nobatt = sum(Electric_Use * 0.5 * input$kWh_Rate * 0.01),
                  Demand.Charge.Nobatt = max(Electric_Use) * mean(Peak_Rate),
                  Bill.Nobatt = kWh.Charge.Nobatt + Demand.Charge.Nobatt,
                  Bill.Nobatt.Bar = Bill.Nobatt,
                  ` ` = NA,
                  kWh.Charge.Batt = sum(Grid_Load * 0.5 * input$kWh_Rate * 0.01),
                  Demand.Charge.Batt = max(Grid_Load) * mean(Peak_Rate),
                  Bill.Batt = kWh.Charge.Batt + Demand.Charge.Batt,
                  Bill.Batt.Bar = Bill.Batt,
                  `  ` = NA,
                  kWh.Nobatt = sum(Electric_Use * 0.5),
                  kWh.Batt = sum(Grid_Load * 0.5)) %>%
        arrange(match(Month, month.abb)) %>%
        adorn_totals("row") %>%
        flextable() %>%
        border_remove() %>%
        set_header_labels(Trad.Bill = "Standard Bill",
                          kWh.Charge.Nobatt = "kWh Charge",
                          Demand.Charge.Nobatt = "Demand Charge",
                          Bill.Nobatt = "Total Bill",
                          Bill.Nobatt.Bar = "Total Bill",
                          kWh.Charge.Batt = "kWh Charge",
                          Demand.Charge.Batt = "Demand Charge",
                          Bill.Batt = "Total Bill",
                          Bill.Batt.Bar = "Total Bill",
                          kWh.Nobatt = "w/o Battery",
                          kWh.Batt = "w/ Battery") %>%
        add_header(Trad.Bill = " ",
                   kWh.Charge.Nobatt = "No Battery",
                   Demand.Charge.Nobatt = "No Battery",
                   Bill.Nobatt = "No Battery",
                   Bill.Nobatt.Bar = "No Battery",
                   kWh.Charge.Batt = "With Battery",
                   Demand.Charge.Batt = "With Battery",
                   Bill.Batt = "With Battery",
                   Bill.Batt.Bar = "With Battery",
                   kWh.Nobatt = "Energy Use (kWh)",
                   kWh.Batt = "Energy Use (kWh)") %>%
        merge_h(part = "header") %>%
        merge_at(i = 2, j = 5:6, part = "header") %>%
        merge_at(i = 2, j = 10:11, part = "header") %>%
        merge_h_range(i = 1:13, j1 = 5, j2 = 6) %>%
        merge_h_range(i = 1:13, j1 = 9, j2 = 10) %>%
        flextable::align(j = 1, align = "center") %>%
        flextable::align(part = "header", i = 1:2, align = "center") %>%
        hline(i = 1, j = 3, part = "header",
              border = fp_border(color = "black", width = 1)) %>%
        hline(i = 1, j = 8, part = "header",
              border = fp_border(color = "black", width = 1)) %>%
        hline(i = 1, j = 13, part = "header",
              border = fp_border(color = "black", width = 1)) %>%
        hline(i = 2, part = "header",
              border = fp_border(color = "black", width = 1.3)) %>%
        hline(i = 12, part = "body",
              border = fp_border(color = "black", width = 1.3)) %>%
        color(i = 13, j = c(7, 12), color="white") %>%
        bold(part = "header") %>%
        bold(part = "body", i = 13, j = 1:14) %>%
        fontsize(part = "all", size = 13) %>%
        width(width = 1.0) %>%
        width(j = 7, width = 0.45) %>%
        width(j = 12, width = 0.45) %>%
        height(part = "body", height = 0.35) %>%
        bg(i = 1:13, j = 2,  bg = "grey95") %>%
        bg(i = 1:13, j = 5,  bg = "grey95") %>%
        bg(i = 1:13, j = 11, bg = "grey95") %>%
        colformat_num(col_keys = c("Trad.Bill", "kWh.Charge.Nobatt",
                                   "Bill.Nobatt", "Demand.Charge.Nobatt",
                                   "kWh.Charge.Batt", "Demand.Charge.Batt",
                                   "Bill.Batt.Bar"), big.mark = ",", digits = 2) %>%
        colformat_num(col_keys = c("kWh.Nobatt", "kWh.Batt"),
                      big.mark = ",", digits = 0) %>%
        htmltools_value()
    })
    
  output$Usage_Rate <- renderText({
      paste0(input$kWh_Rate, "¢ per kWh")
  })
    
  output$Summer_Rate <- renderText({
      paste0("$", format(round(input$Demand_Charge_Rate * 2.958, digits = 2), nsmall = 2), " per kW")
  })
  
  output$Winter_Rate <- renderText({
    paste0("$", format(round(input$Demand_Charge_Rate * 2.098, digits = 2), nsmall = 2), " per kW")
  })
  
  
  yearlySavings.cps <- reactive({
    Comm_PS_df() %>%
      filter(yday(Date) != 60) %>%
      mutate(Reg_Rate = ifelse(Month %in% c("Jun", "Jul", "Aug", "Sep"), 0.09256, 0.07757),
             Peak_Rate = ifelse(Month %in% c("Jun", "Jul", "Aug", "Sep"), input$Demand_Charge_Rate * 2.958, input$Demand_Charge_Rate * 2.098)) %>%
      group_by(Month) %>%
      summarize(kWh.Charge.Nobatt = sum(Electric_Use * 0.5 * input$kWh_Rate * 0.01),
                Demand.Charge.Nobatt = max(Electric_Use) * mean(Peak_Rate),
                Bill.Nobatt = kWh.Charge.Nobatt + Demand.Charge.Nobatt,
                
                kWh.Charge.Batt = sum(Grid_Load * 0.5 * input$kWh_Rate * 0.01),
                Demand.Charge.Batt = max(Grid_Load) * mean(Peak_Rate),
                Bill.Batt = kWh.Charge.Batt + Demand.Charge.Batt) %>%
      summarize(Savings = sum(Bill.Nobatt) - sum(Bill.Batt)) %>%
      as.numeric() %>%
      round(digits = 2)
  })
  
  output$YearlySavings.cps <- renderText({
    paste0("$", format(yearlySavings.cps(), big.mark = ",", nsmall = 2))
  })
  
  output$expLife.cps <- renderText({
    paste(input$BattLife.cps, "years")
  })
  
  output$discountRate.cps <- renderText({
    paste0(input$discRate.cps, "%")
  })
  
  output$batteryCost.cps <- renderText({
    paste0("$", format(input$BattCost.cps, big.mark = ",", scientific = FALSE))
  })
  
  output$PaybackPlot.cps <- renderPlot({
    upfrontCost <- -(input$BattCost.cps)
    expLife <- input$BattLife.cps
    yearlySavings <- yearlySavings.cps()
    payBack <- (-upfrontCost)/yearlySavings
    profitLoss = upfrontCost + expLife * yearlySavings
    
    ggplot(data = tibble(a = c(1))) +
      geom_hline(yintercept = 0) +
      geom_vline(xintercept = 0) +
      geom_abline(intercept = upfrontCost, slope = yearlySavings, color = "navyblue", size = 1) +
      geom_vline(xintercept = expLife, linetype = 2) +
      geom_vline(xintercept = -(upfrontCost) / yearlySavings, linetype = 2) +
      
      geom_point(aes(x = 0, y = upfrontCost), size = 2.5) +
      geom_point(aes(x = 0, y = upfrontCost), size = 1.5, color = "white", fill = "white", shape = 18) +
      
      geom_point(aes(x = payBack, y = 0), size = 2.5) +
      geom_point(aes(x = payBack, y = 0), size = 1.5, color = "white", fill = "white", shape = 18) +
      
      geom_segment(aes(x = .4, xend = .4, y = 0, yend = profitLoss),
                   color = ifelse(profitLoss > 0, "darkgreen", 
                                  ifelse(profitLoss < 0, "indianred4", "black")),
                   size = 1.1, arrow = arrow(ends = "last", angle = 90, length = unit(0.25, "lines"))) +
      geom_segment(aes(x = .4, xend = expLife, y = profitLoss, yend = profitLoss),
                   linetype = 3, size = 0.9, 
                   color = ifelse(profitLoss > 0, "darkgreen", 
                                  ifelse(profitLoss < 0, "indianred4", "black"))) +
      
      geom_label(aes(x = 0.5, y = upfrontCost-2000), hjust = 0, label = "Initial Investment/\nUpfront Cost", 
                 fontface = "bold", size = 4.5, label.size = NA, alpha = 0.5) +
      geom_text(aes(x = .8, y = ifelse(profitLoss < -4000 | (profitLoss >= 0 & profitLoss < 4100), profitLoss + 2500, profitLoss - 2500)),
                hjust = 0, label = "Total Expected Lifetime Savings", fontface = "bold", size = 5) +
      geom_label(aes(x = ifelse(payBack <= 22.5 | payBack > 25.1, payBack + 1.45, payBack - 1.45), y = 0), 
                 label = "Break Even\nPoint", vjust = ifelse(payBack <= 22.5 | payBack > 25.1, 1.05, -0.05),
                 size = 4.5, fontface = "bold", fill = "white", alpha = 0.7,
                 label.size = NA, label.padding = unit(0.4, "lines")) +
      geom_label(aes(x = ifelse(expLife >= payBack, expLife + 1.8, expLife - 1.8),
                     y = upfrontCost*0.8), 
                 label = "Expected Useful\nLife of Battery",
                 size = 4.5, fontface = "bold", label.size = NA, alpha = 0.5) +
      
      theme_tufte() +
      coord_cartesian(xlim = c(0,
                               25),
                      #ifelse(payBack > expLife, payBack * 1.3, expLife * 1.3)), 
                      ylim = c((upfrontCost -2500), 
                               ifelse(profitLoss > 2500, profitLoss + 2500, 5000))) +
      
      scale_x_continuous(name = "Years", 
                         breaks = c(5, 10, 15, 20, 25, 30),
                         labels = c("5 yrs", "10 yrs", "15 yrs", "20 yrs", "25 yrs", "30 yrs"),
                         expand = c(0,0)) +
      scale_y_continuous(name = "Cost (Dollars)",
                         breaks = seq.int(from = -500000, to = 500000, by = 10000)) +
      
      theme(axis.title = element_blank(),
            axis.text = element_text(size = 12),
            plot.margin = unit(c(1,1,1,1), "lines"))
  })
  
  } # Bill Comparison and Savings Tab
    
  {
  output$GenPlot.cps <- renderPlot({
      a <- Comm_PS_df() %>%
        select(Time, Electric_Use, Grid_Load) %>%
        group_by(Time) %>%
        summarize(Electric_Use = mean(Electric_Use),
                  Grid_Load = mean(Grid_Load)) %>%
        mutate(C = Electric_Use,
               D = Grid_Load,
               E = Electric_Use) %>%
        rename("A" = Electric_Use,
               "B" = Grid_Load) %>%
        gather(key = Line, value = kW, -Time, -E) %>%
        mutate(Plot = ifelse(Line == "A", "1",
                             ifelse(Line %in% c("B", "C"), "2", "3")),
               Fill = ifelse(E >= kW, "Discharge", "Charge"),
               Cycle_Change = ifelse(Fill != lag(Fill, default = ""), 1, 0),
               Cycle_Number = factor(cumsum(Cycle_Change)))
      
      ggplot(a, aes(x = Time, y = kW, color = Line)) +
        geom_rect(inherit.aes = FALSE, aes(ymin = 0, ymax = Inf, xmin = 52800, xmax = 70500), fill = "grey90") +
        geom_ribbon(data = filter(a, Line == "B"),
                    aes(ymin = kW, ymax = E, fill = Fill, group = Cycle_Number),
                    alpha = 0.9, color = "white") +
        geom_line(size = 0.7, aes(linetype = Line)) +
        facet_wrap(~Plot, ncol = 1,
                   labeller = labeller(Plot = c(`1` = "Old Load Curve without Storage",
                                                `2` = "Storage Device Charge/Discharge Activity",
                                                `3` = "New Load Curve with Storage"))) +
        geom_hline(yintercept = 0, color = "black", size = 0.3) +
        theme_tufte() +
        theme(axis.line.y = element_line(color = "black", size = 0.3),
              axis.title.x = element_blank(),
              axis.title.y = element_text(size = 14, family = "Helvetica", vjust = 4),
              axis.text = element_text(size = 10, family = "Helvetica"),
              axis.text.x = element_text(vjust = -1),
              strip.text = element_text(size = 12, family = "Helvetica", face = "bold", vjust = 1),
              legend.position = "none",
              plot.margin = unit(c(1,1.7,0.5,1), "lines"),
              panel.spacing = unit(1, "lines")) +
        ylab("Average Electricity Use (kW)") +
        scale_x_time(breaks = c(0, 14100, 28200, 42300, 56400, 70500, 84400), 
                     labels = c("12:00am", "4:00am", "8:00am", "12:00pm", "4:00pm", "8:00pm", "12:00am"), 
                     expand = c(0,0)) +
        scale_y_continuous(expand = c(0.005,0.005)) +
        scale_color_manual(breaks = c("A", "B", "C", "D"),
                           values = c("grey65", "black", "grey80", "black")) +
        scale_linetype_manual(breaks = c("A", "B", "C", "D"),
                              values = c(5,1,5,1)) +
        scale_fill_manual(breaks = c("Charge", "Discharge"),
                          values = c("#d9b6b6", "#c6d1d9"))
    }, width = 375)
    
  output$Generation.cps <- renderUI({
      Comm_PS_df() %>%
        left_join(Generation, by = "Date_Time") %>%
        select(Date_Time, Month, Electric_Use, Grid_Load, Pct_Renew, Pct_Clean, Carbon_per_kWh) %>%
        filter(!is.na(Pct_Renew)) %>%
        mutate(kWh_Renew_Reg = Pct_Renew * 0.01 * Electric_Use,
               kWh_Renew_Bat = Pct_Renew * 0.01 * Grid_Load,
               kWh_Clean_Reg = Pct_Clean * 0.01 * Electric_Use,
               kWh_Clean_Bat = Pct_Clean * 0.01 * Grid_Load,
               kg_Carbon_Reg = Carbon_per_kWh * Electric_Use,
               kg_Carbon_Bat = Carbon_per_kWh * Grid_Load) %>%
        summarize(Total.kWh_Reg = sum(Electric_Use),
                  Total.kWh_Bat = sum(Grid_Load),
                  Pct.Renew_Reg = sum(kWh_Renew_Reg)/sum(Electric_Use) * 100,
                  Pct.Renew_Bat = sum(kWh_Renew_Bat)/sum(Grid_Load) * 100,
                  Pct.Clean_Reg = sum(kWh_Clean_Reg)/sum(Electric_Use) * 100,
                  Pct.Clean_Bat = sum(kWh_Clean_Bat)/sum(Grid_Load) * 100,
                  kg.Carbon_Reg = sum(kg_Carbon_Reg),
                  kg.Carbon_Bat = sum(kg_Carbon_Bat),
                  C.Cost_Reg    = kg.Carbon_Reg * input$SCC.comm * 0.00110231,
                  C.Cost_Bat    = kg.Carbon_Bat * input$SCC.comm * 0.00110231) %>%
        gather(key = key, value = value) %>%
        separate(key, sep = "_", into = c("Key", "Status")) %>%
        spread(key = Status, value = value) %>%
        arrange(desc(Key)) %>%
        select(Key, Reg, Bat) %>%
        mutate(Key = c("Total kWh Used", "Percent Renewable (%)", "Percent Clean (%)", "Carbon Emissions* (kg)", "Social Cost ($)")) %>%
        
        flextable() %>%
        set_header_labels(`Key` = " ",
                          `Reg` = "Without Storage",
                          `Bat` = "With Storage") %>%
        fontsize(part = "all", size = 14) %>%
        height(height = 0.3) %>%
        width(width = 1.8) %>%
        width(j = 1, width = 2.3) %>%
        colformat_num(col_keys = c("Reg", "Bat"), big.mark = ",", digits = 0) %>%
        bg(i = 4, j = 1:3,  bg = "#d7d2c6") %>%
        bold(part = "header") %>%
        htmltools_value()
    })
  } # Generation Resources Tab
  } # End of Commercial Peak-Shaving
  
### Commercial Solar Firming Section ###
  
  {
  {
  Comm_CSF <- function(DataSet, Batt_kW, Batt_kWh, Batt_Efficiency, Batt_DoD, Solar_kW, Batt_Backup) {
      Comm_Battery <- Commercial_TOU %>%
        filter(Company == DataSet,
               minute(Date_Time) == 0, Day_in_Year != 60) %>%
        left_join(Res_Solar, by = "Date_Time") %>%
        mutate(Solar = Solar * Solar_kW,
               Solar = ifelse(is.na(Solar), 0, Solar),
               Solar_Charge = ifelse(Solar - Electric_Use < 0, 0, 
                              ifelse(Solar - Electric_Use < Batt_kW, Solar - Electric_Use, Batt_kW)),
               Over_Gen = ifelse(Electric_Use < Solar, Solar - Electric_Use, 0),
               Net_Use = ifelse(Electric_Use > Solar, Electric_Use - Solar, 0),
               Cumulative_Charge = Solar_Charge - Net_Use)
      
      f <- function(x, y) max(min(x + y, Batt_kWh), Batt_kWh * (1-Batt_DoD) + (Batt_kWh - Batt_kWh * (1-Batt_DoD)) * (Batt_Backup))
      Batt_Charge <- Reduce(f, Comm_Battery$Cumulative_Charge, 0, accumulate = TRUE)[-1]
      Batt_Charge.df <- tibble(Comm_Battery$Date_Time, Batt_Charge)
      
      Comm_Final <- Comm_Battery %>%
        left_join(Batt_Charge.df, by = c("Date_Time" = "Comm_Battery$Date_Time")) %>%
        mutate(Charge_Discharge = Batt_Charge-lag(Batt_Charge, default = 0),
               Batt_Load = ifelse(Charge_Discharge >= 0, Charge_Discharge,
                           ifelse(Charge_Discharge < 0, Charge_Discharge * Batt_Efficiency, 0)),
               Batt_Charge_Solar = ifelse(Batt_Load > 0, Batt_Load, 0),
               To_Grid = ifelse(Solar_Charge - Batt_Charge_Solar > 0, Solar_Charge - Batt_Charge_Solar, 0),
               Grid_Load = Net_Use + Batt_Load - Solar_Charge,
               Grid_Load = ifelse(Grid_Load > 0, Grid_Load, 0))
  }
  Comm_CSF_df <- reactive({Comm_CSF(DataSet =         input$Comm_Type, 
                                    Batt_kW =         input$Batt_kW.comm, 
                                    Batt_kWh =        input$Batt_kWh.comm, 
                                    Batt_Efficiency = input$Batt_Efficiency.comm * 0.01, 
                                    Batt_DoD =        input$Batt_DoD.comm * 0.01,
                                    Batt_Backup =     input$Batt_Backup.comm * 0.01,
                                    Solar_kW =        input$Solar.comm)
  })
  } # General Algorithms
    
  {
    CSF_Intro <- reactive({Res_RSF(DataSet = Med_House, 
                                   Batt_kW = input$CSF_IntroplotSlider*1, 
                                   Batt_kWh = input$CSF_IntroplotSlider*1.5, 
                                   Batt_Efficiency = 0.8, 
                                   Batt_DoD = 0.99,
                                   Batt_Backup = 0,
                                   Solar_kW = 4) %>%
        filter(Month %in% c("Jan", "Feb", "Mar", "Apr", "May", "Sep", "Oct", "Nov", "Dec")) %>%
        group_by(Time) %>%
        summarize(Grid.Load = mean(Grid_Load),
                  Net.Use = mean(Net_Use),
                  Electric.Use = mean(Electric_Use),
                  Solar = mean(Solar))
    })
    
    output$CSF_Intro1 <- renderPlot({
      CSF_Intro() %>%
        ggplot(aes(x = Time, ymin = Net.Use, ymax = Electric.Use)) +
        geom_ribbon(fill = "slategray3") +
        geom_line(aes(y = Net.Use), color = "black", size = 1) +
        geom_line(aes(y = Electric.Use), color = "slategray4", linetype = 2) +
        geom_line(aes(y = Solar), color = "#7a0019", size = 0.9) +
        theme_tufte() + 
        theme(axis.line = element_line(color = "black", size = 0.3),
              axis.text = element_text(size = 12, family = "Arial"),
              axis.title.x = element_blank(),
              axis.title.y = element_text(vjust = 3, size = 13, family = "Arial"),
              plot.title = element_text(hjust = 0.5, size = 13, face = "bold", family = "Arial"),
              plot.background = element_rect(fill = "#e3e3e3",
                                             color = "#e3e3e3"),
              plot.margin = unit(c(1,1.5,0,1), "lines")) +
        scale_x_time(expand = c(0,0),
                     breaks = c(0, 21600, 43200, 64800, 82800),
                     labels = c("12 am", "6 am", "12 pm", "6 pm", "12 am")) +
        labs(title = "Without Storage") +
        ylab("Average Electricity\nUse/Generation (kW)")
    }) # RSF Introplot 1 - Could probably be converted to an image - isnt actually reactive
    
    output$CSF_Intro2 <- renderPlot({
      CSF_Intro() %>%
        ggplot(aes(x = Time, ymin = Grid.Load, ymax = Electric.Use)) +
        geom_ribbon(fill = "slategray2", alpha = 0.5) +
        geom_ribbon(aes(ymin = Grid.Load + Net.Use - Grid.Load, ymax = Electric.Use), fill = "slategray3") +
        geom_line(aes(y = Grid.Load), color = "black", size = 1) +
        geom_line(aes(y = Electric.Use), color = "slategray4", linetype = 2) +
        geom_line(aes(y = Solar), color = "#7a0019", size = 0.9) +
        theme_tufte() + 
        theme(axis.line = element_line(color = "black", size = 0.3),
              axis.text = element_text(size = 12, family = "Arial"),
              axis.title.x = element_text(vjust = -2, size = 13, family = "Arial"),
              axis.title.y = element_text(vjust = 3, size = 13, family = "Arial"),
              plot.title = element_text(hjust = 0.5, size = 13, face = "bold", family = "Arial"),
              plot.background = element_rect(fill = "#e3e3e3",
                                             color = "#e3e3e3"),
              plot.margin = unit(c(1,1.5,1,1), "lines")) +
        scale_x_time(expand = c(0,0),
                     breaks = c(0, 21600, 43200, 64800, 82800),
                     labels = c("12 am", "6 am", "12 pm", "6 pm", "12 am")) +
        labs(title = "With Storage") +
        ylab("Average Electricity\nUse/Generation (kW)")
    }) # Solar Firming Introplot 2
  } # General Information Tab
  
  {
  output$datePlot_One.csf   <- renderPlot({
      Comm_CSF_df() %>%
        select(Date_Time, Date, Time, Electric_Use, Grid_Load, Solar, To_Grid, Net_Use, Batt_Load, Batt_Charge_Solar, Day_in_Year) %>%
        filter(between(x = Date, left = input$date_comm[1], right = input$date_comm[2])) %>%
        ggplot(aes(x = Date_Time)) +
          geom_area(aes(y = Electric_Use), fill = "#e3e3e3") +
          geom_line(aes(y = Solar), color = "darkred", size = 1) +
          geom_line(aes(y = Electric_Use), size = 0.3) +
          theme_tufte() +
          theme(axis.line = element_line(color = "black", size = 0.3),
                axis.title.x = element_blank(),
                axis.title.y = element_text(size = 14),
                axis.text = element_text(size = 12),
                legend.text = element_text(size = 12),
                legend.title = element_text(size = 14)) + 
          scale_x_datetime(expand = c(0,0)) +
          scale_y_continuous(expand = c(0,0)) +
          ylab("Electric Use and Generation (kW)")
    }, height = 300)  
    
  output$datePlot_Two.csf   <- renderPlot({
      Comm_CSF_df() %>%
        select(Date_Time, Date, Time, Electric_Use, Grid_Load, Solar, To_Grid, Net_Use, Batt_Charge_Solar, Day_in_Year) %>%
        mutate(Direct_Use = Electric_Use - Net_Use,
               Solar_Self = Solar - To_Grid) %>%
        filter(between(x = Date, left = input$date_comm[1], right = input$date_comm[2])) %>%
        ggplot(aes(x = Date_Time)) +
          geom_area(aes(y = Solar), fill = "#a67f87") +
          geom_area(aes(y = Electric_Use), fill = "#e3e3e3", alpha = 0.6) +
          geom_area(aes(y = Solar_Self), fill = "#bbbbbb") +
          geom_area(aes(y = Direct_Use), fill = "slategray4", alpha = 0.8, color = "black") +
          geom_line(aes(y = Solar), color = "#7a0019", size = 0.6) +
          geom_line(aes(y = Electric_Use), color = "darkgrey", size = 0.3, alpha = 1) +
          theme_tufte() +
          theme(axis.line = element_line(color = "black", size = 0.5),
                axis.title.x = element_blank(),
                axis.title.y = element_text(size = 14),
                axis.text = element_text(size = 12),
                legend.text = element_text(size = 12),
                legend.title = element_text(size = 14)) + 
          scale_x_datetime(expand = c(0,0)) +
          scale_y_continuous(expand = c(0,0)) +
          ylab("Electric Generation (kW)")
    }, height = 300)
    
  output$datePlot_Three.csf <- renderPlot({
      Comm_CSF_df() %>%
        select(Date_Time, Date, Time, Electric_Use, Grid_Load, Solar, To_Grid, Net_Use, Batt_Charge_Solar, Day_in_Year) %>%
        mutate(Direct_Use = Electric_Use - Net_Use) %>%
        filter(between(x = Date, left = input$date_comm[1], right = input$date_comm[2])) %>%
        ggplot(aes(x = Date_Time, ymin = Grid_Load, ymax = Electric_Use)) +
          geom_ribbon(fill = "slategray2", alpha = 0.5) +
          geom_ribbon(aes(ymin = Grid_Load, ymax = Grid_Load + Direct_Use), fill = "slategray3") +
          geom_line(aes(y = Grid_Load), color = "black", size = 0.8) +
          geom_line(aes(y = Electric_Use), color = "slategray4", alpha = 0.7) +
          #geom_line(aes(y = Solar), color = "darkred", size = 0.9, alpha = 0.2) +
          theme_tufte() +
          theme(axis.line = element_line(color = "black", size = 0.3),
                axis.title.x = element_blank(),
                axis.title.y = element_text(size = 14),
                axis.text = element_text(size = 12),
                legend.text = element_text(size = 12),
                legend.title = element_text(size = 14)) + 
          scale_x_datetime(expand = c(0,0)) +
          scale_y_continuous(expand = c(0,0)) +
          ylab("Electric Consumption (kW)")
    }, height = 300)
  } # Daily Load Curve Tab
    
  { 
  output$monthPlot_Solar.csf <- renderPlot({
      Comm_CSF_df() %>%
        filter(Month == "Jun") %>%
        group_by(Time) %>%
        summarize(Grid.Load = mean(Grid_Load),
                  Net.Use = mean(Net_Use),
                  Electric.Use = mean(Electric_Use),
                  Solar = mean(Solar)) %>%
        ggplot(aes(x = Time, ymin = Net.Use, ymax = Electric.Use)) +
        geom_ribbon(fill = "lightsteelblue2") +
        geom_line(aes(y = Net.Use), color = "black", size = 1.2) +
        geom_line(aes(y = Electric.Use), color = "slategrey", linetype = 2) +
        geom_line(aes(y = Solar), color = "darkred", size = 1.2) +
        theme_tufte() + 
        theme(axis.line = element_line(color = "black", size = 0.3),
              axis.title.x = element_blank(),
              axis.title.y = element_text(size = 16, vjust = 4, family = "Helvetica"),
              axis.text = element_text(size = 13, family = "Helvetica"),
              axis.text.x = element_text(vjust = -1),
              plot.margin = unit(c(0.5,1.2,0.5,1.2), "lines")) +
        scale_x_time(expand = c(0,0),
                     breaks = c(0, 20730, 42330, 63930, 82800),
                     labels = c("12am", "6am", "12pm", "6pm", "12am")) +
        ylab("Electricity Use/Generation (kW)")
  }, height = 300)
    
  output$monthPlot_Batt.csf  <- renderPlot({
      Comm_CSF_df() %>%
        filter(Month == "Jun") %>%
        group_by(Time) %>%
        summarize(Grid.Load = mean(Grid_Load),
                  Net.Use = mean(Net_Use),
                  Electric.Use = mean(Electric_Use),
                  Solar = mean(Solar)) %>%
        ggplot(aes(x = Time, ymin = Grid.Load, ymax = Electric.Use)) +
            geom_ribbon(fill = "slategray2", alpha = 0.5) +
            #geom_ribbon(aes(ymin = Grid.Load, ymax = Grid.Load - Net.Use + Electric.Use), fill = "#b8c5d6") +          # Alternative plot having direct self-consumption 
            geom_ribbon(aes(ymin = Grid.Load + Net.Use - Grid.Load, ymax = Electric.Use), fill = "lightsteelblue2") +   # shading below stored shading rather than above it.
            geom_line(aes(y = Grid.Load), color = "black", size = 1.2) +
            geom_line(aes(y = Electric.Use), color = "slategrey", linetype = 2) +
            geom_line(aes(y = Solar), color = "darkred", size = 1.2) +
            
            theme_tufte() +
            theme(axis.line = element_line(color = "black", size = 0.3),
                  axis.title.x = element_blank(),
                  axis.title.y = element_text(size = 16, vjust = 4, family = "Helvetica"),
                  axis.text = element_text(size = 13, family = "Helvetica"),
                  axis.text.x = element_text(vjust = -1),
                  plot.margin = unit(c(0.5,1.2,0.5,1.2), "lines")) +
            scale_x_time(expand = c(0,0),
                         breaks = c(0, 20730, 42330, 63930, 82800),
                         labels = c("12am", "6am", "12pm", "6pm", "12am")) +
            ylab("Electricity Use/Generation (kW)")
    }, height = 300)
  } # Monthly Load Curve Tab
    
  {
  MeterType <- reactive(input$MeterType_csf)
    
  Non_Demand.csf <- reactive({ 
        Comm_CSF_df() %>%
            mutate(NEM_Rate = input$NetMeterRate.csf * Regular_Rate * 0.01) %>%
            group_by(Month) %>%
            summarize(None.Bill = sum(Electric_Use * Regular_Rate),
                      ` ` = NA,
                      SoldBack.Solar = round(sum(Solar_Charge), digits = 1),
                      NEM.Solar.Bill = round(sum(Net_Use * Regular_Rate) - sum(Solar_Charge * Regular_Rate), digits = 2),
                      Adj.Solar.Bill = round(sum(Net_Use * Regular_Rate) - sum(Solar_Charge * NEM_Rate), digits = 2),
                      `  ` = NA,
                      SoldBack.Batt = round(sum(To_Grid), digits = 1),
                      NEM.Batt.Bill = round(sum(Grid_Load * Regular_Rate) - sum(To_Grid * Regular_Rate), digits = 2),
                      Adj.Batt.Bill = round(sum(Grid_Load * Regular_Rate) - sum(To_Grid * NEM_Rate), digits = 2)) %>%
            arrange(match(Month, month.abb)) %>%
            adorn_totals("row")
    })

  Demand.csf <- reactive({
        Comm_CSF_df() %>%
            mutate(NEM_Rate = input$NetMeterRate.csf * 0.0003407,
                   Peak_Rate = ifelse(Month %in% c("Jun", "Jul", "Aug", "Sep"), 14.79, 10.49)) %>%
            group_by(Month) %>%
            summarize(#kWh = sum(Electric_Use * 0.03407),
                      #kW = max(Electric_Use) * mean(Peak_Rate),
                      None.Bill = round(sum(Electric_Use * 0.03407) +      # None.kWh
                                        max(Electric_Use) * mean(Peak_Rate),    # None.kW
                                        digits = 2),
                      ` ` = NA,
                      SoldBack.Solar = round(sum(Solar_Charge), digits = 1),
                      NEM.Solar.Bill = round((sum(Net_Use * Regular_Rate) - sum(Solar_Charge * Regular_Rate)) + 
                                              max(Net_Use) * mean(Peak_Rate), 
                                              digits = 2),
                      Adj.Solar.Bill = round((sum(Net_Use * Regular_Rate) - sum(Solar_Charge * NEM_Rate)) + 
                                              max(Net_Use) * mean(Peak_Rate), 
                                              digits = 2),
                      `  ` = NA,
                      SoldBack.Batt = round(sum(To_Grid), digits = 1),
                      NEM.Batt.Bill = round((sum(Grid_Load * Regular_Rate) - sum(To_Grid * Regular_Rate)) + 
                                            max(Grid_Load) * mean(Peak_Rate), 
                                            digits = 2),
                      Adj.Batt.Bill = round((sum(Grid_Load * Regular_Rate) - sum(To_Grid * NEM_Rate)) + 
                                            max(Grid_Load) * mean(Peak_Rate), 
                                            digits = 2)) %>%
            arrange(match(Month, month.abb)) %>%
            adorn_totals("row")
    })

  BillComp.csf <- reactive({
    if (MeterType() == "Non_Demand") {
      Non_Demand.csf()
    } else {
      Demand.csf()
    }
  })
  
  output$BillComp.csf <- renderUI({
      BillComp.csf() %>%
          flextable() %>%
          border_remove() %>%
          set_header_labels(None.Bill = "Standard Bill",
                            SoldBack.Solar = "kWh Returned to Grid",
                            NEM.Solar.Bill = "Net-Metered Bill",
                            Adj.Solar.Bill = "Adjusted Bill",
                            SoldBack.Batt = "kWh Returned to Grid",
                            NEM.Batt.Bill = "Net-Metered Bill",
                            Adj.Batt.Bill = "Adjusted Bill") %>%
          add_header(None.Bill = "No Solar or Storage",
                     SoldBack.Solar = "With Solar",
                     NEM.Solar.Bill = "With Solar",
                     Adj.Solar.Bill = "With Solar",
                     SoldBack.Batt = "With Solar and Storage",
                     NEM.Batt.Bill = "With Solar and Storage",
                     Adj.Batt.Bill = "With Solar and Storage") %>%
          merge_h(part = "header") %>%
          flextable::align(j = 1, align = "center") %>%
          flextable::align(part = "header", i = 1:2, align = "center") %>%
          hline(i = 1, j = 2, part = "header",
                border = fp_border(color = "black", width = 1)) %>%
          hline(i = 1, j = 4:6, part = "header",
                border = fp_border(color = "black", width = 1)) %>%
          hline(i = 1, j = 8:10, part = "header",
                border = fp_border(color = "black", width = 1)) %>%
          hline(i = 2, part = "header",
                border = fp_border(color = "black", width = 1.3)) %>%
          hline(i = 12, part = "body",
                border = fp_border(color = "black", width = 1.3)) %>%
          color(i = 13, j = c(3, 7), color="white") %>%
          bold(part = "header") %>%
          bold(part = "body", i = 13, j = 1:10) %>%
          fontsize(part = "all", size = 13) %>%
          width(width = 1.2) %>%
          width(j = c(4, 8), width = 1.4) %>%
          width(j = c(3, 7), width = 0.3) %>%
          height(part = "body", height = 0.3) %>%
          bg(i = 1:13, j = 2,  bg = "grey95") %>%
          bg(i = 1:13, j = 6,  bg = "grey95") %>%
          bg(i = 1:13, j = 10,  bg = "grey95") %>%
          colformat_num(col_keys = c("None.Bill", "NEM.Solar.Bill", "Adj.Solar.Bill",
                                     "NEM.Batt.Bill", "Adj.Batt.Bill"), big.mark = ",", digits = 2) %>%
          colformat_num(col_keys = c("SoldBack.Solar", "SoldBack.Batt"),
                        big.mark = ",", digits = 1) %>%
          htmltools_value()
    }) 
    
  output$NEMRateSummer.csf <- renderText({
    paste0(round(input$NetMeterRate.csf * 0.09256, digits = 2), "¢ per kWh")
  })
  
  output$NEMRateWinter.csf <- renderText({
    paste0(round(input$NetMeterRate.csf * 0.07757, digits = 2), "¢ per kWh")
  })
  
  output$NEMRateDemand.csf <- renderText({
    paste0(round(input$NetMeterRate.csf * 0.03407, digits = 2), "¢ per kWh")
  })
  
  
  yearlySavings.csf <- reactive({
    BillComp.csf() %>%
      filter(Month == "Total") %>%
      select(None.Bill, Adj.Solar.Bill, Adj.Batt.Bill) %>%
      summarize(Savings = ifelse(input$ROI_Subj.csf == "Both",
                                 None.Bill      - Adj.Batt.Bill,
                                 Adj.Solar.Bill - Adj.Batt.Bill)) %>%
      as.numeric() %>%
      round(digits = 2)
  })
  
  output$YearlySavings.csf <- renderText({
    paste0("$", format(yearlySavings.csf(), big.mark = ",", nsmall = 2))
  })
  
  output$expLife.csf <- renderText({
    paste(input$BattLife.csf, "years")
  })
  
  output$discountRate.csf <- renderText({
    paste0(input$discRate.csf, "%")
  })
  
  output$batteryCost.csf <- renderText({
    paste0("$", format(input$BattCost.csf, big.mark = ",", scientific = FALSE))
  })
  
  output$PaybackPlot.csf <- renderPlot({
    upfrontCost <- -(input$BattCost.csf)
    expLife <- input$BattLife.csf
    yearlySavings <- yearlySavings.csf()
    payBack <- (-upfrontCost)/yearlySavings
    profitLoss = upfrontCost + expLife * yearlySavings
    
    ggplot(data = tibble(a = c(1))) +
      geom_hline(yintercept = 0) +
      geom_vline(xintercept = 0) +
      geom_abline(intercept = upfrontCost, slope = yearlySavings, color = "navyblue", size = 1) +
      geom_vline(xintercept = expLife, linetype = 2) +
      geom_vline(xintercept = -(upfrontCost) / yearlySavings, linetype = 2) +
      
      geom_point(aes(x = 0, y = upfrontCost), size = 2.5) +
      geom_point(aes(x = 0, y = upfrontCost), size = 1.5, color = "white", fill = "white", shape = 18) +
      
      geom_point(aes(x = payBack, y = 0), size = 2.5) +
      geom_point(aes(x = payBack, y = 0), size = 1.5, color = "white", fill = "white", shape = 18) +
      
      geom_segment(aes(x = .4, xend = .4, y = 0, yend = profitLoss),
                   color = ifelse(profitLoss > 0, "darkgreen", 
                                  ifelse(profitLoss < 0, "indianred4", "black")),
                   size = 1.1, arrow = arrow(ends = "last", angle = 90, length = unit(0.25, "lines"))) +
      geom_segment(aes(x = .4, xend = expLife, y = profitLoss, yend = profitLoss),
                   linetype = 3, size = 0.9, 
                   color = ifelse(profitLoss > 0, "darkgreen", 
                                  ifelse(profitLoss < 0, "indianred4", "black"))) +
      
      geom_label(aes(x = 0.5, y = upfrontCost-2000), hjust = 0, label = "Initial Investment/\nUpfront Cost", 
                 fontface = "bold", size = 4.5, label.size = NA, alpha = 0.5) +
      geom_text(aes(x = .8, y = ifelse(profitLoss < -4000 | (profitLoss >= 0 & profitLoss < 4100), profitLoss + 2500, profitLoss - 2500)),
                hjust = 0, label = "Total Expected Lifetime Savings", fontface = "bold", size = 5) +
      geom_label(aes(x = ifelse(payBack <= 22.5 | payBack > 25.1, payBack + 1.45, payBack - 1.45), y = 0), 
                 label = "Break Even\nPoint", vjust = ifelse(payBack <= 22.5 | payBack > 25.1, 1.05, -0.05),
                 size = 4.5, fontface = "bold", fill = "white", alpha = 0.7,
                 label.size = NA, label.padding = unit(0.4, "lines")) +
      geom_label(aes(x = ifelse(expLife >= payBack, expLife + 1.8, expLife - 1.8),
                     y = upfrontCost*0.8), 
                 label = "Expected Useful\nLife of Battery",
                 size = 4.5, fontface = "bold", label.size = NA, alpha = 0.5) +
      
      theme_tufte() +
      coord_cartesian(xlim = c(0,
                               25),
                      #ifelse(payBack > expLife, payBack * 1.3, expLife * 1.3)), 
                      ylim = c((upfrontCost -2500), 
                               ifelse(profitLoss > 2500, profitLoss + 2500, 5000))) +
      
      scale_x_continuous(name = "Years", 
                         breaks = c(5, 10, 15, 20, 25, 30),
                         labels = c("5 yrs", "10 yrs", "15 yrs", "20 yrs", "25 yrs", "30 yrs"),
                         expand = c(0,0)) +
      scale_y_continuous(name = "Cost (Dollars)",
                         breaks = seq.int(from = -500000, to = 500000, by = 10000)) +
      
      theme(axis.title = element_blank(),
            axis.text = element_text(size = 12),
            plot.margin = unit(c(1,1,1,1), "lines"))
  })
  
  } # Bill Comparison and Savings Tab
    
  {
  output$GenPlot.csf <- renderPlot({
      a <- Comm_CSF_df() %>%
        select(Time, Electric_Use, Grid_Load, Net_Use) %>%
        group_by(Time) %>%
        summarize(Electric_Use = mean(Electric_Use),
                  Grid_Load = mean(Grid_Load),
                  Net_Use = mean(Net_Use)) %>%
        mutate(C = Electric_Use,
               D = Grid_Load,
               G = Net_Use) %>%
        rename("A" = Electric_Use,
               "B" = Grid_Load,
               "E" = Net_Use) %>%
        gather(key = Line, value = kW, -Time, -G) %>%
        mutate(Plot = ifelse(Line == "A", "1",
                             ifelse(Line %in% c("B", "C", "E"), "2", "3")))
      
      ggplot(a, aes(x = Time, y = kW, color = Line)) +
        geom_rect(inherit.aes = FALSE, 
                  aes(ymin = 0, ymax = Inf, xmin = 51500, xmax = 68950), 
                  fill = "grey90") +
        geom_ribbon(data = filter(a, Line == "B"), inherit.aes = FALSE,
                    aes(x = Time, ymax = G, ymin = kW),
                    fill = "#c6d1d9", alpha = 0.9) +
        geom_ribbon(data = filter(a, Line == "C"), inherit.aes = FALSE,
                    aes(x = Time, ymin = G, ymax = kW),
                    fill = "#d9b6b6", alpha = 0.9) +
        geom_line(size = 0.7, aes(linetype = Line)) +
        facet_wrap(~Plot, ncol = 1,
                   labeller = labeller(Plot = c(`1` = "Old Load Curve without Solar or Storage",
                                                `2` = "Energy Use Direct from Solar/Stored and Used Later",
                                                `3` = "New Load Curve with Solar and Storage"))) +
        #scales = "free_y") +
        geom_hline(yintercept = 0, color = "black", size = 0.3) +
        theme_tufte() +
        theme(axis.line.y = element_line(color = "black", size = 0.3),
              axis.title.x = element_blank(),
              axis.title.y = element_text(size = 14, family = "Helvetica", vjust = 4),
              axis.text = element_text(size = 10, family = "Helvetica"),
              axis.text.x = element_text(vjust = -1),
              strip.text = element_text(size = 12, family = "Helvetica", face = "bold", vjust = 1),
              legend.position = "none",
              plot.margin = unit(c(1,1.7,0.5,1), "lines"),
              panel.spacing = unit(1, "lines")) +
        ylab("Average Electricity Use (kW)") +
        scale_x_time(breaks = c(0, 13550, 27400, 41250, 55100, 68950, 82500), 
                     labels = c("12:00am", "4:00am", "8:00am", "12:00pm", "4:00pm", "8:00pm", "12:00am"), 
                     expand = c(0,0)) +
        scale_y_continuous(expand = c(0.005,0.005)) +
        scale_color_manual(breaks = c("A", "B", "C", "D", "E"),
                           values = c("grey65", "black", "grey80", "black", "slategray")) +
        scale_linetype_manual(breaks = c("A", "B", "C", "D", "E"),
                              values = c(5,1,5,1,3))
    }, width = 375)
    
  output$Generation.csf <- renderUI({
      Comm_CSF_df() %>%
        left_join(Generation, b = "Date_Time") %>%
        select(Date_Time, Month, Electric_Use, Solar, Solar_Charge, 
               Net_Use, Grid_Load, To_Grid, Pct_Renew, Pct_Clean, Carbon_per_kWh) %>%
        filter(!is.na(Pct_Renew)) %>%
        mutate(kWh_Renew_Reg = Pct_Renew * 0.01 * Electric_Use,
               kWh_Renew_Sol = Pct_Renew * 0.01 * Net_Use,
               kWh_Renew_Bat = Pct_Renew * 0.01 * Grid_Load,
               kWh_Clean_Reg = Pct_Clean * 0.01 * Electric_Use,
               kWh_Clean_Sol = Pct_Clean * 0.01 * Net_Use,
               kWh_Clean_Bat = Pct_Clean * 0.01 * Grid_Load,
               kg_Carbon_Reg = Carbon_per_kWh * Electric_Use,
               kg_Carbon_Sol = Carbon_per_kWh * Net_Use,
               kg_Carbon_Bat = Carbon_per_kWh * Grid_Load) %>%
        summarize(Total.kWh_Reg = sum(Electric_Use),
                  Total.kWh_Sol = sum(Net_Use),
                  Total.kWh_Bat = sum(Grid_Load),
                  Pct.Renew_Reg = sum(kWh_Renew_Reg)/sum(Electric_Use) * 100,
                  Pct.Renew_Sol = sum(kWh_Renew_Sol)/sum(Net_Use) * 100,
                  Pct.Renew_Bat = sum(kWh_Renew_Bat)/sum(Grid_Load) * 100,
                  Pct.Clean_Reg = sum(kWh_Clean_Reg)/sum(Electric_Use) * 100,
                  Pct.Clean_Sol = sum(kWh_Clean_Sol)/sum(Net_Use) * 100,
                  Pct.Clean_Bat = sum(kWh_Clean_Bat)/sum(Grid_Load) * 100,
                  kg.Carbon_Reg = sum(kg_Carbon_Reg),
                  kg.Carbon_Sol = sum(kg_Carbon_Sol),
                  kg.Carbon_Bat = sum(kg_Carbon_Bat),
                  C.Cost_Reg    = kg.Carbon_Reg * input$SCC.comm * 0.00110231,
                  C.Cost_Sol    = kg.Carbon_Sol * input$SCC.comm * 0.00110231,
                  C.Cost_Bat    = kg.Carbon_Bat * input$SCC.comm * 0.00110231) %>%
        gather(key = key, value = value) %>%
        separate(key, sep = "_", into = c("Key", "Status")) %>%
        spread(key = Status, value = value) %>%
        arrange(desc(Key)) %>%
        select(Key, Reg, Sol, Bat) %>%
        mutate(Key = c("Total kWh Used", "Percent Renewable (%)", "Percent Clean (%)", "Carbon Emissions (kg)", "Social Cost ($)")) %>%
        
        flextable() %>%
        set_header_labels(`Key` = " ",
                          `Reg` = "None",
                          `Sol` = "With Solar*",
                          `Bat` = "With Storage") %>%
        fontsize(part = "all", size = 14) %>%
        height(height = 0.3) %>%
        width(width = 1.8) %>%
        width(j = 1, width = 2.3) %>%
        colformat_num(col_keys = c("Reg", "Sol", "Bat"), big.mark = ",", digits = 0) %>%
        bold(part = "header") %>%
        bg(i = 4, j = 1:4,  bg = "#d7d2c6") %>%
        htmltools_value()
    })
  } # Generation Resources Tab
  } # End of Commercial Solar Firming
  
})