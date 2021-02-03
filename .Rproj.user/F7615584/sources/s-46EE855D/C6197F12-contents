library(shiny)
library(shinyjs)
library(shinyWidgets)

shinyUI(fluidPage(
  {tags$head(
    tags$link(rel = "stylesheet", type = "text/css", href = "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.7.0/css/font-awesome.min.css"),
    tags$link(rel = "stylesheet", type = "text/css", href = "Stylesheet.css")
  )}, # Links to CSS Stylesheets
  
  tags$body(
    shinyjs::useShinyjs(), # Call to activate shinyJS package.
    
  {tags$header(
      tags$h2(class = "page-title", style = "width:1000px;", "Minnesota Community-Scale Energy Storage Guide"),
    
      tags$div(class = "topnav",
        tags$a(style = "padding: 0px;",
          tags$p(class = "menu", "Menu")
        ),
        tags$a(class = "tablink activeTab", id = "Intro",
            "Introduction"
        ),
        tags$div(class = "dropdown", id = "useCase",
          tags$button(class = "dropbtn",
            "Use Case Examples",
            tags$i(class = "fa fa-caret-down")
          ),
          tags$div(class = "dropdown-content", style = "z-index:3;",
            tags$a(style = "background-color: #f9f9f9; border-bottom: 1.5px solid #ccc",
              "Customer Type:"),
            tags$a(class = "tablink", id = "Res",
              "Residential"),
            tags$a(class = "tablink", id = "Comm",
              "Commercial")
          )
        ),
        tags$a(class = "tablink", id = "Guide",
          "Guidebook")
        
      ) # End of Main Menu TopNav
    )}, #  Page Header w/ NavBar and Title
   
###  BEGINNING OF INTRODUCTION PAGE ###

  {div(id = "Introduction", class = "tabcontent",
      div(class = "row",
        {div(class = "column left intro",
          div(class = "sidenav", style = "position: absolute;",
            a(class = "tablink2 activeSidebar", id = "tablink2-H",
                   "Home Page"),  
            a(class = "tablink2", id = "tablink2-1",
                   "What is Community Energy Storage?"),
            a(class = "tablink2", id = "tablink2-2",
                   "Energy Storage Glossary"),
            a(class = "tablink2", id = "tablink2-3",
                   "Energy Storage Technologies"),
            a(class = "tablink2", id = "tablink2-4",
                   "Services and Use Cases"),
            a(class = "tablink2", id = "tablink2-5",
                   "Data Description, Limitations, and Sources")
          )  # End of Intro Page Sidenav
          
          #tags$img(src = 'https://static1.squarespace.com/static/59d93cf118b27d3726137f2a/t/5be8a7f48a922d4a2918778e/1544726704755/UMN+Transition+Lab.png?format=500w', style = 'width:220px; position:fixed; margin-left: -10px; bottom:0;')
          
        )}, # Introduction Left Column with NavList
        
        {div(class = "column main intropage", id = "Intro-H", style = "margin-left:15px;",
            div(style = "min-width:950px; max-width:950px;",
                p(class = "section-header",
                    "Welcome to the Minnesota Community-Scale Energy Storage Guide"),
                hr(),
                p(class = "indent", style = "font-size: 13px;",
                    "This guide and web tool is a product of the Energy Transition Lab, part of the Institute on the Environment at the University of Minnesota.
                    It was created as part of a project funded by the Minnesota Environment and Natural Resources Trust Fund to install three community-scale
                    battery energy storage devices throughout the state as pilot projects. Much of the purpose of this project is to demonstrate the efficacy of
                    community-scale energy storage in Minnesota and to publicly disseminate the results of these installations and provide information and guidance
                    to those who may be interested in learning more about how energy storage can benefit them or their organization. We offer our thanks and
                    appreciation to the Minnesota Environment and Natural Resources Trust Fund for funding, the Legislative-Citizen Commission on Minnesota
                    Resources for approving the project, and to our three host sites and project partners, the Red Lake Band of Ojibwe Indians, Renewable Energy
                    Partners in Minneapolis, and the University of Minnesota, Morris.")
            ),
            br(),
            img(src = "Logos.png", width = "500px", style = "margin-left:225px;"),
            {div(style = "min-width: 950px; max-width: 950px; height: 210px; background-color: #d6dce5; border-radius: 10px; margin-top: 25px; padding:5px;",
                p(class = "section-subheader",
                    "How to Use this Guide:"),
                p(class = "indent", style = "font-size: 13px; padding: 0 10px;",
                    "This guide is meant to be a tool to investigate the use of energy storage for community-scale applications. The Introduction tab is filled with
                    general information about what energy storage is, many of the common forms used for residential and community-scale applications, and the common
                    use cases that provide value to the system's operator and to the grid. The Use Case Examples tab features interactive depictions of three common
                    energy storage use cases with residential and commercial examples. These allow you to see how each use case affects energy use over time,
                    and how manipulating the specifications of the storage device affects the this and ultimately the customer's energy bills and attributable carbon
                    emissions. Finally, the Guidebook tab is meant to be a starting point for anyone interested in pursuing energy storage for use in their community-scale
                    organization. This includes many of the challenges encountered when purchasing three community-scale pilot projects, as well as other questions
                    to consider and resources that may help the process.")
                )} # How to Use this Guide
             
        )}, # Home Page
        {hidden(
            div(class = "column main intropage", id = "Intro-1", style = "margin-left:15px;",
                div(class = "row",
                    {div(style = "min-width:480px; max-width:480px; height: 670px; margin: 10px; padding: 0 10px;",
                        p(class = "section-header center", 
                            "What is Energy Storage?"),
                        hr(),
                        p(class = "indent", style = "font-size:13px;",
                            "Energy storage is the process of converting electricity into some form of potential energy that can be kept in a stable state and saved for later use. This can be as simple as
                            pushing a ball from the bottom of a hill to the top, expending energy to move the ball and storing it in the form of kinetic potential energy. That energy can be released by rolling
                            the ball back down to the bottom."),
                        img(src = "hillBatt1.png", style = "width: 70%; margin: -10px 15% 10px;"),
                        p(class = "indent", style = "font-size:13px;",
                            "Common forms of energy storage devices such as batteries can be explored in more detail in the 'Energy Storage Technologies' tab to the left. Just like moving a ball up a hill, each 
                            of these devices uses energy when charging to transform some material into a state with elevated potential energy. When discharging, that energy is released and converted back into 
                            electricity as the material returns to its low-energy state."),
                        p(class = "indent", style = "font-size:13px;",
                            "When energy storage is used in the context of the electric grid, it can function both as a consumer and a producer of electricity, which enables it to perform many valuable services.
                            These services typically involve storing electricity when it is abundant and cheap and discharging it when demand and prices are high. Several common services can be viewed in more 
                            depth in the 'Services and Use Case Description' tab on the left."
                        )
                    )}, # What is Energy Storage
                    {div(style = "min-width:480px; max-width:480px; height: 670px; margin: 10px; padding: 0 10px;",
                        p(class = "section-header center", 
                            "What is Community-Scale Energy Storage?"),
                        hr(),
                        p(class = "indent", style = "font-size:13px;",
                            "As the energy storage market has grown and developed, much of the installations to date have either been small, residential-scale batteries or large, utility scale or industrial 
                            installations. As a result, many of the commercially available energy storage options cater to these sectors. Community-scale energy storage describes the wide capacity range between
                            residential and utility-scale. This space is occupied by small businesses, community organizations such as municipal buildings, places of worship, and community centers, and many
                            non-profit organizations."),
                        img(src = "CommScale2.png", width = "100%", style = "margin: -6px 0 4px;"),
                        p(class = "indent", style = "font-size:13px;",
                          "These organizations occupy an interesting area with respect to energy storage potential because, unlike most residential customers, many have demand-metered rate designs which create 
                            value for energy storage through demand-charge management. On the other hand, the capacity size of community-scale storage devices make them too small to participate in most auxilliary
                            services markets on their own."),
                        p(class = "indent", style = "font-size:13px;",
                        "Furthermore, the number of organizations and buildings that fall within this range and their contribution to regional loads and load curve shape make them potentially critical actors
                        in the use of energy storage to reshape system load curves to reduce stress and increase flexibility of the grid.")
                    )}  # What is Community-Scale Energy Storage
                ),
                hr(style = "margin-left:-15px;"),
                {div(
                    p(class = "section-header center", style = "width:1000px;", "Community-Scale Energy Storage Pilot Installations"),
                    div(style = "min-width: 975px; max-width: 975px; height: 250px; border: 1px solid white;",
                        p(class = "indent", style = "font-size: 13px; padding: 10px 0 0 10px; width: 100%;", 
                          "In July of 2018, the Energy Transition Lab (ETL), a part of the Institute on the Environment at the University
                          of Minnesota, was awarded a grant from the Minnesota Environment and Natural Resources Trust Fund (ENTRF)
                          to study community-scale energy storage in Minnesota. ETL is in the process of purchasing and installing three
                          redox flow battery systems at each of the three locations in the figure below."),
                        p(class = "indent", style = "font-size: 13px; padding-left: 10px; width: 100%;",
                          "The purpose of this project involves demonstrating the efficacy of community-scale battery energy storage in 
                          Minnesota and providing guidance to organizations interested in learning how energy storage can benefit them.
                          As shown in the figure below, the sites selected to host the three battery devices are spread across the state
                          and represent different organizations and building types. Each host site also has different priorities
                          and different energy needs, so the battery specifications and primary use case vary as well, providing more
                          potential to learn from this project."),
                        p(class = "indent", style = "font-size: 13px; padding-left: 10px; width: 100%;",
                          "More information on energy storage technologies including relative advantages and disadvantages is available
                          under the 'Energy Storage Technologies' tab, and descriptions of the use cases shown below as well as others
                          available can be found under the 'Services and Use Cases' tab.")
                    )
                )}, # MN Energy Storage Pilots
                img(src='FrontPage4.png', width = 900, style = "margin-left:50px;")
                
            )
        )}, # What is Community-Scale Energy Storage
        {hidden(
          div(class = "column main intropage", id = "Intro-2", style = "padding-left:30px;",
              p(class = "section-header", 
                "Energy Storage Glossary"),
              #hr(),
              {div(class = "row", style = "width:950px; border-top:1px solid black; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                   div(style = "height:100%; width:350px;",
                       tags$li(style = "size:16px; font-weight:bold;", 
                               "Load Curve")
                   ),
                   div(style = "height:100%; width:600px;",
                       p(style = "size:14px;", 
                         "A load curve depicts the amount of power that an entity (from a single customer up to an entire regional grid) is using across a certain time frame.
                         Load curves are often considered in daily segments since they often are highly time-of-day dependent, but can also be viewed in terms of average energy
                         use throughout the day.")
                   )
              )}, # Load Curve
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Energy Capacity")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "The total amount of energy that an energy storage device is capable of storing. Measured in kilowatt-hours (kWh).")
                  )
              )}, # Energy Capacity
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Power Rating")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "The amount of energy that a storage device is capable of delivering at any given moment, measured in kilowatts (kW). 
                          Many batteries often can pulse a higher power for a short period of time (~30 minutes) above their general power rating.")
                  )
              )}, # Power Rating
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Duration")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "The length of time a storage device can provide 100% power delivery, typically measured in hours. A device with 
                          one kilowatt of rated power and two kilowatt-hours of energy capacity has a duration of two hours.")
                  )
              )}, # Duration
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Round-Trip Efficiency")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                        "A perfectly efficient battery would be able to discharge one kWh for each kWh that it is charged. 
                        However, each battery experiences energy losses in the charge-discharge cycle. The round-trip 
                        efficiency is a measure of the fraction of energy that can be drawn out of a battery as a portion 
                        of the energy that has been put into it. For example, a battery which is charged with 5 kWh, but 
                        can only discharge 4 kWh has a round trip efficiency of 80%.")
                  )
              )}, # Round-Trip Efficiency
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Depth of Discharge")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;",
                          "Most batteries have to maintain some minimal level of charge at all times to avoid long-term damage 
                            or decreased capacity. The Depth of Discharge refers to the amount of the battery’s energy capacity 
                          that has been used. Each battery typically has a maximum depth of discharge, which is the fraction 
                          of energy that can be drawn from the battery without depleting its minimum charge.")
                  )
              )}, # Depth of Discharge
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Cycle Life")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "Over time, a battery’s ability to charge and discharge will slowly diminish. Cycle life refers 
                          to the rate at which this occurs with respect to the number of times the device charges and
                          discharges. A battery with a long cycle life can undergo many charge-discharge cycles with 
                          low degradation of its capacity. Storage devices often include a warrantee from their manufacturer 
                          which specifies a time period and a capacity. This warrantee guarantees that the device will maintain 
                          at least the stated capacity (often around 70%) for the designated time.")
                  )
              )}, # Cycle Life
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Energy Density / Power Density")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "Energy and power density are measurements of energy capacity and power rating per unit of mass of the storage
                          device. Typically measured in watt-hours per kilogram (Wh/kg) and watts per kilogram (W/kg) respectively.")
                  )
              )}, # Energy and Power Density
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Self-Discharge")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "If a storage device is fully charged and left in that state without discharging or charging, it will often self-discharge and lose its stored charge.
                          The mechanism for and rate of this process varies significantly by storage type and battery chemistry, but virtually all storage devices
                          lose charge over time. Rate of discharge can also depend heavily on external factors such as temperature. Self-discharge is measured in percent of
                          charge per unit of time (i.e. %/month)")
                  )
              )}, # Self-Discharge
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Electrochemical Cell")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "Electrochemical cells are the fundamental structure of all battery energy storage devices. Most cells consist of two
                          electrodes, a negatively charged anode and a positive cathode, separated by an electrolyte and/or a semi-permeable
                          barrier. When discharging, an energetically favored chemical reaction drives electrons across a circuit between the 
                          anode and the cathode. While charging an external voltage is applied to reverse the flow of electrons and thereby
                          reverse the chemical reaction.")
                  )
              )}, # Electrochemical Cell
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Anode")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "Negative electrode in an electrochemical cell where electrons accumulate when in the charged state. The anode
                          expels electrons towards the load and cathode during discharge and accepts electrons when charging.")
                  )
              )}, # Anode
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Cathode")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "Positive electrode in an electrochemical cell which accumulates positive charge when in the charged state. The cathode loses
                          electrons during charges and accepts them during discharge.")
                  )
              )}, # Cathode
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Anolyte / Catholyte")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "In flow batteries, the structure of the electrochemical cell is quite different than other battery types. Rather than solid
                          electrodes, the energy in flow batteries is stored in liquid electrolyte solutions, an anolyte and a catholyte, which are
                          stored separately in tanks. Analogous to other battery types, electrons flow from anolyte to catholyte during discharge, and
                          are reversed when charging.")
                  )
              )}, # Anolyte / Catholyte
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Electrolyte")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;",
                          "Conventionally, electrolytes are electricially conductive solutions of salt compounds in water. Electrons typically
                          cannot pass through the electrolyte alone, however, which facilitates current flow between the anode and the cathode.
                          Modern innovations include gel or solid-phase electrolytes in addition to liquid phase.")
                  )
              )}, # Electrolyte
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Thermal Runaway")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;",
                          "Many battery chemistries involve exothermic chemical reactions which release large amounts of heat and often require complex ventilation
                          and temperature control systems. If these systems are not functioning properly, the battery can experience thermal runaway, which involves
                          a cycle of heat released by the reaction warming the battery, which increases the rate of the exothermic reaction, releasing increasingly
                          more heat. In extreme examples, thermal runaway can result in fires or explosions. Lithium-ion batteries are particularly succeptable to
                          thermal runaway, and often require extensive ventilation, climate control, and fire suppression systems for large installations.")
                  )
              )}, # Thermal Runaway
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Independent System Operator (ISO) /", br(), "Regional Transmission Operator (RTO)")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "ISOs and RTOs are independent organizations that control and monitor the transmission grid across a large area, encompassing multiple electric utilities. They coordinate between
                          their constituent utilities to efficiency and reliability of the grid without direct government control or oversight.")
                  )
              )}, # Independent System Operator
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "MISO")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "The Midcontinent Idependent System Operator, or MISO, is the regional transmission organization that encompasses Minnesota and much of the midwest as well as parts of
                          the south central region of the US. It is divided into three regions: North, Central, and South. The MISO North Region includes Minnseota, Iowa, parts of the Dakotas, and
                          the province of Manitoba, and has its regional control center in Eagan, Minnesota.")
                  )
              )}, # MISO
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Transmission and Distribution")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "Transmission and distribution are two of the stages involved in transporting electricity from power plants where it is generated to homes
                          and businesses where it is consumed. The primary distinction is the voltage at which the electricity is conveyed. Transmission involves very
                          high voltages which transport electricity over long distances, since high voltage minimizes line losses. When the electricity arrives in the
                          area where it will be used, the voltage is stepped down at a substation and transmitted to homes and businesses through the lower-voltage 
                          distribution network.")
                  )
              )}, # Transmission and Distribution
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Dendrites")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "Dendrites are crystals that develop in a highly-branched, tree-like form. In the context of energy storage, dendrites form in lithium ion batteries
                          lithium is electroplated onto the electrode in an uneven fashion and forms these branching crystals that can span across the gap between the two electrodes.
                          Dendrites can have negative impacts on the function and useful life of a battery, and can even cause safety hazards, such as fires or explosions.")
                  )
              )}, # Dendrite Formation
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "In Front of / Behind the Meter")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "The location relative to 'the meter' refers to the meters measuring electricity consumption at customers' homes and businesses. Typically, the utility owns
                          and is responsible for everything in front of the meter, or before electricity reaches the customer, while the customer owns and is responsible for everything 
                          behind the meter, or after electricity has entered the home or business.")
                  )
              )}, # In Front of / Behind the Meter
              {div(class = "row", style = "width:950px; border-bottom:1px dashed darkgrey; padding:5px 5px 0 15px;",
                  div(style = "height:100%; width:350px;",
                      tags$li(style = "size:16px; font-weight:bold;", 
                          "Criteria Pollutant(s)")
                  ),
                  div(style = "height:100%; width:600px;",
                      p(style = "size:14px;", 
                          "Under the Clean Air Act, the EPA regulates air quality standards for six common air pollutants known as criteria air pollutants. These include ozone, carbon monoxide,
                          sulfur dioxide, nitrogen dioxide, lead, and particulate matter. Each of these pollutants can be formed and released from combustion of electricity generation resources, 
                          such as coal, natural gas, and biomass materials. EPA regulations affect how utilities are able to operate these generation facilities.")
                  )
              )}  # Criteria Pollutants
          )
        )}, # Energy Storage Glossary
        {hidden(
            div(class = "column main intropage", id = "Intro-3",
                {div(
                    p(class = "section-header", 
                        "Comparing the Common Energy Storage Technologies"),
                    hr(style = "margin:10px;"),
                    div(class = "row", style = "height: 410px; padding-left: 10px;",
                        {div(style = "min-width:640px; max-width:640px; height:400px; margin: 5px;",
                            tags$img(src = "DurCapPlot0.png", style = "width: 100%;"),
                            
                            div(class = "Electrochem",
                                tags$img(src = "DurCapPlot1a.png", style = "position:absolute; width: 640px; top:169px; left: 236px; z-index:1"),
                                hidden(div(class = "NonCommunity",
                                           tags$img(src = "DurCapPlot1b.png", style = "position:absolute; width: 640px; top:169px; left: 236px; z-index:1")
                                ))
                            ),
                            div(class = "Electromech",
                                hidden(div(class = "NonCommunity",
                                           tags$img(src = "DurCapPlot2b.png", style = "position:absolute; width: 640px; top:169px; left: 236px; z-index:3")
                                ))
                            ),
                            div(class = "Electrical",
                                tags$img(src = "DurCapPlot3a.png", style = "position:absolute; width: 640px; top:169px; left: 236px; z-index:1"),
                                hidden(div(class = "NonCommunity",
                                           tags$img(src = "DurCapPlot3b.png", style = "position:absolute; width: 640px; top:169px; left: 236px; z-index:1")         
                                ))
                            ),
                            div(class = "Thermal",
                                tags$img(src = "DurCapPlot4a.png", style = "position:absolute; width: 640px; top:169px; left: 236px; z-index:1"),
                                hidden(div(class = "NonCommunity",
                                           tags$img(src = "DurCapPlot4b.png", style = "position:absolute; width: 640px; top:169px; left: 236px; z-index:2") 
                                ))
                            ),
                            div(class = "Chemical",
                                tags$img(src = "DurCapPlot5a.png", style = "position:absolute; width: 640px; top:169px; left: 236px; z-index:1"),
                                hidden(div(class = "NonCommunity",
                                           tags$img(src = "DurCapPlot5b.png", style = "position:absolute; width: 640px; top:169px; left: 236px; z-index:1")
                                ))
                            )
                        )}, # Left-Top Box:  Layers of Capacity x Duration Plot
                        {div(style = "min-width:275px; max-width:275px; height:350px; margin:20px 0 90px; padding:10px 10px 0; font-size:13px; line-height:17px; box-shadow:0 4px 8px 0 rgba(0,0,0,0.2); border-radius:3px;",
                            p(class = "center", style = "font-weight: bold; font-size:18px; color: #7a0019;",
                                "Assessing Storage Options"),
                            p(style = "text-indent:30px;",
                                "Each common energy storage technology has slightly different functional specifications, arising from
                                a combination of technical and physical limitations as well as economic and financial considerations.
                                These differences provide each technology with a set of advantages and disadvantages that suit each
                                one to different application types. No one technology works equally well across all applications."),
                            p(style = "text-indent:30px;",
                                "When selecting an energy storage technology for a particular building or group of buildings, it is
                                important to consider the characteristics of each find the technology which best matches the individual
                                load profile and the intended use case of the energy storage system.")
                        )}  # Right-Top Box: Caption of Technology Intro Plots
                    ),
                    div(class = "row", style = "height: 410px; padding-left: 10px;", # Second Row
                        {div(style = "min-width:270px; max-width:270px; height:353px; margin:21px 10px 90px; padding:10px 10px 0; font-size:13px; line-height:17px; box-shadow:0 4px 8px 0 rgba(0,0,0,0.2); border-radius:3px; z-index:1;",
                            p(class = "center", style = "font-size:13px; line-height:17px; font-weight:bold;",
                                "Use the toggle switches below to view and compare characteristics of each energy storage technology."),
                            {div(style = "padding: 5px 0 0 30px;",
                                div(
                                    tags$label(class = "switch",
                                        tags$input(type = "checkbox", checked = TRUE, id = "toggle-1"),
                                        tags$span(class = "slider round tog1")
                                    ),
                                    p(style = "display:inline;", "Electrochemical Energy")
                                ),
                                div(
                                    tags$label(class = "switch",
                                        tags$input(type = "checkbox", checked = TRUE, id = "toggle-2"),
                                        tags$span(class = "slider round tog2")
                                    ),
                                    p(style = "display:inline;", "Electromechanical Energy")
                                ),
                                div(
                                    tags$label(class = "switch", 
                                        tags$input(type = "checkbox", checked = TRUE, id = "toggle-3"),
                                        tags$span(class = "slider round tog3")
                                    ),
                                    p(style = "display:inline;", "Electrical Energy")
                                ),
                                div(
                                    tags$label(class = "switch",
                                        tags$input(type = "checkbox", checked = TRUE, id = "toggle-4"),
                                        tags$span(class = "slider round tog4")
                                    ),
                                    p(style = "display:inline;", "Thermal Energy")
                                ),
                                div(
                                    tags$label(class = "switch",
                                        tags$input(type = "checkbox", checked = TRUE, id = "toggle-5"),
                                        tags$span(class = "slider round tog5")
                                    ),
                                    p(style = "display:inline;", "Chemical Energy")
                                )
                            )}, # Sliders for Energy Storage Technologies Intropage
                            hr(style = "margin: 10px 0;"),
                            p(class = "center", style = "font-weight: bold; font-size:15px; color: #7a0019;",
                                "Community-Scale Options"),
                            p(class = "center; font-size:13px; line-height:17px;",
                                "To expand selection to include energy storage technologies not typically suited for community-scale applications, select the toggle switch below."),
                            div(class = "row", style = "width:353px; height:50px; padding-left:10px;",
                                p("Community-Scale"),
                                div(style = "margin:0 10px;",
                                    tags$label(class = "switch",
                                        tags$input(type = "checkbox", id = "toggle-0"),
                                        tags$span(class = "slider round"))),
                                p("All Technologies")
                            )
                        )}, # Left-Bottom Box:  Toggle Switch Box for Technology Intro Plots
                        {div(style = "min-width:640px; max-width:640px; height:400px;",
                            tags$img(src = "DevPlot0.png", style = "width: 100%;"),
                            
                            div(class = "Electrochem",
                                tags$img(src = "DevPlot1a.png", style = "position:absolute; width: 640px; top:574px; left: 522px; z-index:1"),
                                hidden(div(class = "NonCommunity",
                                    tags$img(src = "DevPlot1b.png", style = "position:absolute; width: 640px; top:574px; left: 522px; z-index:1")
                                ))
                            ),
                            div(class = "Electromech",
                                hidden(div(class = "NonCommunity",
                                    tags$img(src = "DevPlot2b.png", style = "position:absolute; width: 640px; top:574px; left: 522px; z-index:1")
                                ))
                            ),
                            div(class = "Electrical",
                                tags$img(src = "DevPlot3a.png", style = "position:absolute; width: 640px; top:574px; left: 522px; z-index:1"),
                                hidden(div(class = "NonCommunity",
                                    tags$img(src = "DevPlot3b.png", style = "position:absolute; width: 640px; top:574px; left: 522px; z-index:1")          
                                ))
                            ),
                            div(class = "Thermal",
                                tags$img(src = "DevPlot4a.png", style = "position:absolute; width: 640px; top:574px; left: 522px; z-index:1"),
                                hidden(div(class = "NonCommunity",
                                    tags$img(src = "DevPlot4b.png", style = "position:absolute; width: 640px; top:574px; left: 522px; z-index:1") 
                                ))
                            ),
                            div(class = "Chemical",
                                tags$img(src = "DevPlot5a.png", style = "position:absolute; width: 640px; top:574px; left: 522px; z-index:1"),
                                hidden(div(class = "NonCommunity",
                                    tags$img(src = "DevPlot5b.png", style = "position:absolute; width: 640px; top:574px; left: 522px; z-index:1")
                                ))
                            )
                        )}  # Right-Bottom Box: Layers of Technology Development Plot
                    )
                )}, # Technology Intro Page Top Plots
                p(class = "section-header", 
                    "Technology-Specific Descriptions and Schematics"),
                hr(style = "margin:10px;"),
                p(class = "center", style = "width: 900px; margin-top:10px", 
                    tags$i(class = "fa fa-caret-left"), 
                        "Select an energy storage technology from the list below to view more information", 
                    tags$i(class = "fa fa-caret-right")
                ),
                {div(class = "row", style = "height:340px; margin-top:-10px;",
                    div(class = "column left ESTech", style = "padding:10px; margin:0 5px 0 20px; height: 335px; min-width:300px; max-width:300px;",
                        h4(class = "center", "Electrochemical Storage"),
                        tags$button(class = "ESTechButton electrochemical", id = "est1-1", 
                                    "Lead-Acid Batteries"),
                        tags$button(class = "ESTechButton electrochemical", id = "est1-2", 
                                    "Lithium-Ion Batteries"),
                        tags$button(class = "ESTechButton electrochemical", id = "est1-3",
                                    "Redox Flow Batteries"),
                        tags$button(class = "ESTechButton electrochemical", id = "est1-4", 
                                    "Sodium-Sulfur Batteries"),
                        tags$button(class = "ESTechButton electrochemical", id = "est1-5", 
                                    "Nickel-Metal Hydride Batteries"),
                        tags$button(class = "ESTechButton electrochemical", id = "est1-6", 
                                    "Solid State Batteries")),
                    div(class = "column left ESTech", style = "padding:10px; margin:0 5px; height: 335px; min-width:300px; max-width:300px;",
                        h4(class = "center", "Electromechanical Storage"),
                        tags$button(class = "ESTechButton electromechanical oneline", id = "est2-1", 
                                    "Flywheels"),
                        tags$button(class = "ESTechButton electromechanical oneline", id = "est2-2", 
                                    "Pumped Hydro"),
                        tags$button(class = "ESTechButton electromechanical twolines", id = "est2-3", 
                                    "Compressed Air Energy Storage (CAES)"),
                        h4(class = "center", style = "margin-top: 20px;", "Thermal Energy Storage"),
                        tags$button(class = "ESTechButton thermal oneline", id = "est3-1", 
                                    "Hot Water and Ice"),
                        tags$button(class = "ESTechButton thermal oneline", id = "est3-2", 
                                    "Molten Salt"),
                        tags$button(class = "ESTechButton thermal oneline", id = "est3-3", 
                                    "Building Thermal Envelope")),
                    div(class = "column left ESTech", style = "padding:10px; margin:0 5px; height: 335px; min-width:300px; max-width:300px;",
                        h4(class = "center", "Electrical Energy Storage"),
                        tags$button(class = "ESTechButton electrical oneline", id = "est4-1", 
                                    "Capacitors and Supercapacitors"),
                        tags$button(class = "ESTechButton electrical twolines", id = "est4-2", 
                                    "Superconducting Magnetic Energy Storage (SMES)"),
                        h4(class = "center", style = "margin-top: 20px;", "Chemical Energy Storage"),
                        tags$button(class = "ESTechButton chemical oneline", id = "est5-1", 
                                    "Hydrogen"),
                        tags$button(class = "ESTechButton chemical oneline", id = "est5-2", 
                                    "Ammonia"),
                        tags$button(class = "ESTechButton chemical oneline", id = "est5-3", 
                                    "Coal"),
                        tags$button(class = "ESTechButton chemical oneline", id = "est5-4", 
                                    "Natural Gas")
                    )
                )}, # Button Columns for Storage Technologies
                hr(),
                {div(
                    {hidden(
                    div(class = "row ESTechPanel", id = "leadAcid",
                        div(class = "column textColumn",
                            {div(class = "textCard",
                                p(tags$b("Lead Acid Batteries",
                                         tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX1-1")),
                                    hr(style = "border-top:1px solid #999999; margin:5px;"),
                                    tags$b("How do they work?"),
                                    p(class = "cardText",
                                        "Ion exchange between lead oxide and sulfuric acid - splitting 
                                        water molecules into hydrogen and oxygen when charging and 
                                        recombining them when discharging."),
                                    tags$b("Common Applications:"),
                                    p(class = "cardText",
                                        "Automotive and marine vehicle batteries, emergency backup power.",
                                        "Typically small in scale, but can be connected in series to scale up easily."),
                                    tags$b("State of Development:"),
                                    p(class = "cardText",
                                        "Mature - oldest extant battery technology, but with modern innovations."),
                                    tags$b("Advantages:"),
                                      tags$li(class = "cardText", "Inexpensive"),
                                      tags$li(class = "cardText", "High Power Density (range)"),
                                      tags$li(class = "cardText last", "Recyclable and Reusable Materials"),
                                    tags$b("Disadvantages:"),
                                      tags$li(class = "cardText", "Poor Efficiency (%-%)"), 
                                      tags$li(class = "cardText", "Poor Depth of Discharge (%-%)"),
                                      tags$li(class = "cardText", "Low Energy Density (range)"),
                                      tags$li(class = "cardText", "High Self-Discharge (range)"),
                                      tags$li(class = "cardText", "Toxic Chemicals (Pb, ", HTML("H<sub>2</sub>SO<sub>4</sub>)")),
                                      tags$li(class = "cardText last", "Poor Cycle Life (#range)"),
                                    tags$b("Variations/Advances:"),
                                    p(class = "cardText",
                                        "Absorbed Glass Mat (also called starved electrolyte) and other advanced lead acid technologies have improving the
                                        efficiency and cycle life potential for lead acid batteries.")
                                )
                            )} # Text Card
                        ), # Left Column Text Card
                        div(class = "column imageColumn",
                            {div(class = "imageCard",
                                div(class = "image_box",
                                    conditionalPanel(condition = "input.leadImage == 'leadImage1'",
                                        tags$img(class = "lead_acid", id = "leadImage1", src = "lead_acid1.png", style = "width: 96%; padding-left: 12px;")),
                                    conditionalPanel(condition = "input.leadImage == 'leadImage2'",
                                        tags$img(class = "lead_acid", id = "leadImage2", src = "lead_acid2.jpg", style = "width: 100%;")),
                                    conditionalPanel(condition = "input.leadImage == 'leadImage3'",
                                        tags$img(class = "lead_acid", id = "leadImage3", src = "lead_acid3.jpg", style = "width: 100%;"))
                                ),
                                
                                #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                div(class = "imgRadio",
                                radioGroupButtons(inputId = "leadImage",
                                                  label = NULL, 
                                                  choiceValues = c("leadImage1", "leadImage2", "leadImage3"), 
                                                  choiceNames = c("", "", ""),
                                                  size = "sm", selected = "leadImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                            )}, # Image Card
                            {div(class = "captionCard",
                                conditionalPanel(condition = "input.leadImage == 'leadImage1'",
                                    p(class = "captionText",
                                        strong("Lead Acid Battery Schematic"), br(),
                                        "The electrochemical cell of a lead-acid battery is made up of a lead (Pb) anode, a lead (IV) oxide (PbO2) cathode, and a sulfuric acid electrolyte.
                                        Shown here during discharge, the lead oxide reacts with the sulfuric acid to create lead (II) sulfate (PbSO4), generating two electrons, which create electrical
                                        force across the wire between electrodes before reacting with the lead anode to form more lead (II) sulfate. When charging, these reactions are reversed, 
                                        reforming the original material of each electrode.")),
                                conditionalPanel(condition = "input.leadImage == 'leadImage2'",
                                    p(class = "captionText",
                                        strong("Cross Section of a Flooded Lead Acid (FLA) Battery"), br(),
                                        "Lead acid batteries are composed of several cells connected together with external terminals at each end. Lead acid batteries are divided into a few categories 
                                        depending on how the sulfuric acid electrolyte is stored. The image above depicts a flooded battery where the electrolyte occupies the full volume of the battery.
                                        These batteries have the lowest upfront costs but require regular maintenance. Others, including sealed batteries and absorbant glass mat (AGM) confine the electrolyte 
                                        or separate the cathode and anode plates.")),
                                conditionalPanel(condition = "input.leadImage == 'leadImage3'",
                                    p(class = "captionText",
                                        strong("Lead Acid Battery Energy Storage System"), br(),  
                                        "Lead acid batteries can be connected together in series as shown in the above image to achieve greater
                                        power and energy capacity. These installations are commonly used for emergency backup power applications."))
                            )}  # Caption Card
                        ) # Right Column with Images and Captions
                    ))}, # Lead Acid Batteries
                    
                    {hidden(
                        div(class = "row ESTechPanel", id = "lithiumIon",
                            div(class = "column textColumn",
                                {div(class = "textCard", style = "overflow-y:scroll;",
                                  p(tags$b("Lithium Ion Batteries",
                                           tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX1-2")),
                                    hr(style = "border-top:1px solid #999999; margin:5px;"),
                                    tags$b("How do they work?"),
                                    p(class = "cardText",
                                      "Lithium ions can flow between a lithium metal oxide cathode and a graphite anode through
                                      an electrolyte barrier. Electrons cannot travel through the barrier, so they are driven 
                                      through an external circuit by charge repulsion. The lithium ions are more stable in the
                                      metal oxide than in the graphite, so it releases energy (as electricity) when traveling 
                                      from graphite to the metal oxide, and requires energy (charging) to move in the opposite direction"),
                                    tags$b("Common Applications:"),
                                    p(class = "cardText",
                                      "Consumer Electronics, electric vehicles, residential backup power, utility-scale grid services (i.e.
                                      frequency regulation, spinning reserve, etc."),
                                    tags$b("State of Development:"),
                                    p(class = "cardText",
                                      "Fairly advanced - first commercialized in the early 1990's, lithium ion batteries have seen rapid advances
                                      as a result of electric vehicle development. Still rapidly improving with respect to quality and cost."),
                                    tags$b("Advantages:"),
                                      tags$li(class = "cardText", "High energy and power density"),
                                      tags$li(class = "cardText", "High round-trip efficiency (esp. long duration batteries)"),
                                      tags$li(class = "cardText", "Modest price (and rapidly declining)"),
                                      tags$li(class = "cardText last", "Rapid/instantaneous response."),
                                    tags$b("Disadvantages:"),
                                      tags$li(class = "cardText", "Sensitive to high temperatures"),
                                      tags$li(class = "cardText", "Potential for thermal runaway, flammability concerns"),
                                      tags$li(class = "cardText", "Limited depth of discharge"),
                                      tags$li(class = "cardText", "Self-discharge rate (1.5-2.5%)"),
                                      tags$li(class = "cardText last", "Recycling lithium at end of useful life is economically inefficient."),
                                    tags$b("Variations/Advances:"),
                                    p(class = "cardText",
                                      "Changing the metal oxide can fine-tune the properties of the battery - common chemistries include lithium iron
                                      phosphate (LFP) and lithium nickel manganese cobalt oxide (NMC), among several others.")
                                    )
                                )} # Text Card
                            ), # Left Column Text Card
                        div(class = "column imageColumn",
                            {div(class = "imageCard",
                                  div(class = "image_box",
                                      conditionalPanel(condition = "input.lithiumImage == 'lithiumImage1'",
                                                       tags$img(class = "lithium_ion zoom", id = "lithiumImage1", src = "lithium1.png", style = "width: 100%; margin-top: 40px;")),
                                      conditionalPanel(condition = "input.lithiumImage == 'lithiumImage2'",
                                                       tags$img(class = "lithium_ion zoom", id = "lithiumImage2", src = "lithium2.jpg", style = "width: 100%")),
                                      conditionalPanel(condition = "input.lithiumImage == 'lithiumImage3'",
                                                       tags$img(class = "lithium_ion", id = "lithiumImage3", src = "lithium3.jpg", style = "width: 100%"))
                                  ),
                                  
                                  #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                  #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                  div(class = "imgRadio",
                                      radioGroupButtons(inputId = "lithiumImage",
                                                        label = NULL, 
                                                        choiceValues = c("lithiumImage1", "lithiumImage2", "lithiumImage3"), 
                                                        choiceNames = c("", "", ""),
                                                        size = "sm", selected = "lithiumImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                              )}, # Image Card
                            {div(class = "captionCard",
                                  conditionalPanel(condition = "input.lithiumImage == 'lithiumImage1'",
                                                   p(class = "captionText",
                                                     strong("Lithium Ion Battery Schematic"), br(),
                                                     "Lithium ions flow between the lithium metal oxide cathode and a graphite anode through an electrolyte barrier. However, electrons cannot travel
                                                      through this barrier, so they are driven through an external circuit by charge repulsion. The lithium ions are more stable in the metal oxide than
                                                      the graphite, so the cell releases energy (discharges) as lihium ions move from the graphite anode to the cathode. Charging uses an external current
                                                      to drive lithium ions back to the graphite anode.")),
                                  conditionalPanel(condition = "input.lithiumImage == 'lithiumImage2'",
                                                   p(class = "captionText",
                                                     strong("Lithium Ion Batteries in Electric Vehicles"), br(),
                                                     "In recent years, lithium ion batteries have developed a symbiotic relationship with electric vehicle development. Advances in battery technology have enabled
                                                      advances in vehicles. At the same time, the rapidly expanding market for and popularity of electric vehicles have fuelled more research into the batteries and
                                                      have contributed to rapidly declining prices.")),
                                  conditionalPanel(condition = "input.lithiumImage == 'lithiumImage3'",
                                                   p(class = "captionText",
                                                     strong("Utility-Scale Application of Lithium Ion Batteries"), br(),
                                                     "Due to their price and technical capabilities, lithium ion batteries are the most widely used battery technology for stationary applications, both for utility and 
                                                     residential applications. This technology is favored predominantly for its price, rapid response rate, and energy density. The installation shown above is located
                                                     by a utility substation, where it likely provides ancillary services for power quality regulation."))
                              )}  # Caption Card
                        ) # Right Column with Images and Captions
                      ))}, # Lithium Ion Batteries
                    
                    {hidden(
                    div(class = "row ESTechPanel", id = "redoxFlow",
                        div(class = "column textColumn",
                            {div(class = "textCard", style = "overflow-y:scroll;",
                                  p(tags$b("Redox Flow Batteries",
                                           tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX1-3")),
                                    hr(style = "border-top:1px solid #999999; margin:5px;"),
                                    tags$b("How do they work?"),
                                    p(class = "cardText",
                                      "Solid electrodes are replaced by liquid electrolytes. Electrolyte solutions are stored
                                      in holding tanks and are pumped into the cell as needed. There, the two solutions are separated by a 
                                      semipermeable membrane, which facilitates ion exchange across the barrier. Electrons are driven through
                                      charge repulsion, releasing energy as electricity. Charging the battery reverses this reaction."),
                                    tags$b("Common Applications:"),
                                    p(class = "cardText",
                                      "Typically for stationary, long-duration applications without strict weight or space limitations
                                      (i.e. Reserve capacity, time-shifting/arbitrage, renewable generation firming)."),
                                    tags$b("State of Development:"),
                                    p(class = "cardText",
                                      "Relatively new technology. Several functional installations, but rapidly developing and advancing through
                                      research on novel chemical combinations."),
                                    tags$b("Advantages:"),
                                    tags$li(class = "cardText", "Long cycle life"),
                                    tags$li(class = "cardText", "Long duration potential"),
                                    tags$li(class = "cardText", "Improved safety and fire resistance"),
                                    tags$li(class = "cardText", "Power and energy capacity can be selected independently"),
                                    tags$li(class = "cardText", "Electrolyte tanks are stackable to reduce footprint area"),
                                    tags$li(class = "cardText last", "Electrolyte solutions have value after battery's useful 
                                        life - recycling/reuse potential"),
                                    tags$b("Disadvantages:"),
                                    tags$li(class = "cardText", "More expensive than most other battery technologies"), 
                                    tags$li(class = "cardText", "Only make economic sense for duration greater than four hours"),
                                    tags$li(class = "cardText", "Low power and energy density"),
                                    tags$li(class = "cardText", "Modest round-trip efficiency"),
                                    tags$li(class = "cardText last", "System of pumps, vessels, and sensors required"),
                                    tags$b("Variations/Advances:"),
                                    p(class = "cardText",
                                      "Most successful batteries utilize vanadium solutions as electrolytes. More recent developments have focused on
                                      common, inexpensive metals such as iron and zinc. Ongoing research is exploring the use of organic (non-metallic)
                                      electrolytes.")
                                    )
                                  )} # Text Card
                        ), # Left Column Text Card
                        div(class = "column imageColumn",
                            {div(class = "imageCard",
                                div(class = "image_box",
                                    conditionalPanel(condition = "input.flowImage == 'flowImage1'",
                                                     tags$img(class = "flow_batt", id = "flowImage1", src = "flow_batt1.gif", style = "width: 65%; margin: 0 17.5%;")),
                                    conditionalPanel(condition = "input.flowImage == 'flowImage2'",
                                                     tags$img(class = "flow_batt", id = "flowImage2", src = "flow_batt2.jpg", style = "width: 100%")),
                                    conditionalPanel(condition = "input.flowImage == 'flowImage3'",
                                                     tags$img(class = "flow_batt", id = "flowImage3", src = "flow_batt3.jpg", style = "width: 100%"))
                                ),
                             
                             #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                             #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                             div(class = "imgRadio",
                                 radioGroupButtons(inputId = "flowImage",
                                                   label = NULL, 
                                                   choiceValues = c("flowImage1", "flowImage2", "flowImage3"), 
                                                   choiceNames = c("", "", ""),
                                                   size = "sm", selected = "flowImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                        )}, # Image Card
                            {div(class = "captionCard",
                             conditionalPanel(condition = "input.flowImage == 'flowImage1'",
                                  p(class = "captionText",
                                      strong("Redox Flow Battery Demonstration"), br(),
                                      "Flow batteries store their electrolyte solutions in tanks separated from each other and from the central 'stack'. When the battery is actively charging
                                      or discharging, a series of pumps and tubes transports the fluids from their respective tanks to the stack, where ions are exchanged across a barrier. Charge 
                                      repulsion then drives an electric current between the two electrodes, discharging the stored energy. When recharging, the flow of ions is reversed, 
                                      reforming the original electrolyte solutions.")),
                             conditionalPanel(condition = "input.flowImage == 'flowImage2'",
                                  p(class = "captionText",
                                      strong("Research-Scale Redox Flow Cell"), br(),
                                      "This image shows a small flow battery set up, which is testing electrolyte chemistries and other aspects of cell design. In the foreground is the stack unit
                                       with input and output tubing for each electrolyte. Behind this stack are two small tanks containing anolyte and catholyte solutions.")),
                             conditionalPanel(condition = "input.flowImage == 'flowImage3'",
                                  p(class = "captionText",
                                      strong("Commercial or Utility Scale Redox Flow Battery"), br(),
                                      "Large-scale redox flow batteries are often built in steel shipping containers. This standardizes container size and weight, enabling stacking and reducing overall
                                      footprint.A smaller battery may have the electrolyte tanks and power stack in the same container, while larger systems may feature one container with the stack
                                      connected to multiple containers filled with electrolyte tanks."))
                        )}  # Caption Card
                        ) # Right Column with Images and Captions
                    ))}, # Redox Flow Batteries
                
                    {hidden(
                    div(class = "row ESTechPanel", id = "sodiumSulfur",
                        div(class = "column textColumn",
                            {div(class = "textCard",
                                p(tags$b("Sodium Sulfur Batteries",
                                         tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX1-4")),
                                    hr(style = "border-top:1px solid #999999; margin:5px;"),
                                    tags$b("How do they work?"),
                                p(class = "cardText",
                                  "A molten sodium metal anode is separated from the molten sulfur cathode by a beta-alumina solid electrolyte
                                  (BASE.) Sodium very readily expels one electron, and the resulting ions can be transported across the electrolyte barrier.
                                  BASE is a poor conductor of electrons, so the electrons instead are driven through an external circuit by charge repulsion.
                                  Sodium ions react with the molten sulfur to form sodium polysulfide salts."), 
                                tags$b("Common Applications:"),
                                p(class = "cardText",
                                  "Large-scale, stationary applications, such as utility-scale reserve power or renewable generation firming. Proposed for use
                                  in space travel."),
                                tags$b("State of Development:"),
                                p(class = "cardText",
                                  "Fairly mature technology, though room for advencement exists.."),
                                tags$b("Advantages:"),
                                tags$li(class = "cardText", "High round-trip efficiency"),
                                tags$li(class = "cardText", "High power and energy density"),
                                tags$li(class = "cardText", "Long cycle life"),
                                tags$li(class = "cardText last", "Becomes more economical with greater capacity."),
                                tags$b("Disadvantages:"),
                                tags$li(class = "cardText", "Operates at 300-350ºC to keep electrodes in molten state"), 
                                tags$li(class = "cardText last", "Must be sealed completely from air and water"),
                                tags$b("Variations/Advances:"),
                                p(class = "cardText",
                                  "Much of the research into sodium sulfur and other molten-salt batteries involves finding electrodes which operate at lower
                                  temperatures and are less reactive with air and moisture. One strategy has been to incorporate sulfur chemistry with the
                                  mechanics of a redox flow battery.")
                                )
                              )} # Text Card
                        ), # Left Column Text Card
                        div(class = "column imageColumn",
                            {div(class = "imageCard",
                              div(class = "image_box",
                                  conditionalPanel(condition = "input.NaSImage == 'NaSImage1'",
                                                   tags$img(class = "sodiumSulfur zoom", id = "NaSImage1", src = "sodiumSulfur1.jpg", style = "width: 100%;")),
                                  conditionalPanel(condition = "input.NaSImage == 'NaSImage2'",
                                                   tags$img(class = "sodiumSulfur", id = "NaSImage2", src = "sodiumSulfur2.jpg", style = "width: 100%;")),
                                  conditionalPanel(condition = "input.NaSImage == 'NaSImage3'",
                                                   tags$img(class = "sodiumSulfur", id = "NaSImage3", src = "sodiumSulfur3.jpg", style = "width: 100%; background-color: white;"))
                              ),
                              
                              #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                              #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                              div(class = "imgRadio",
                                  radioGroupButtons(inputId = "NaSImage",
                                                    label = NULL, 
                                                    choiceValues = c("NaSImage1", "NaSImage2", "NaSImage3"), 
                                                    choiceNames = c("", "", ""),
                                                    size = "sm", selected = "NaSImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                         )}, # Image Card
                            {div(class = "captionCard",
                              conditionalPanel(condition = "input.NaSImage == 'NaSImage1'",
                                               p(class = "captionText", 
                                                 strong("Sodium Sulfur Battery Schematic"), br(),
                                                 "A sodium sulfur cell consists of an anode tube containing liquid sodium metal surrounded by a sulfur electrode, with the two separated by a
                                                 beta-aluminum solid electrolyte (BASE). Sodium ions are able to travel through this electrolyte, creating an electrical potential between
                                                 the two electrodes.")),
                              conditionalPanel(condition = "input.NaSImage == 'NaSImage2'",
                                               p(class = "captionText",
                                                 strong("Cross-Section of a Sodium Sulfur Battery"), br(),
                                                 "Sodium sulfur battery energy storage systems, as with all batteries, are made up of several individual cells wired together and attached to
                                                 positive and negative terminals. All of this is contained in a thermal enclosure to maintain adequate temperature and minimize heat/energy loss.")),
                              conditionalPanel(condition = "input.NaSImage == 'NaSImage3'",
                                               p(class = "captionText",
                                                 strong("Photograph of a Sodium Sulfur Battery"), br(),
                                                 "This image shows each individual cell inside the battery connected in series. The group of cells is held together tightly and enclosed in a
                                                 thick, insulating outer shell to minimize heat loss and maximize battery efficiency."))
                         )}  # Caption Card
                        ) # Right Column with Images and Captions
                    ))}, # Sodium Sulfur Batteries
                
                    {hidden(
                      div(class = "row ESTechPanel", id = "NiMH",
                          div(class = "column", style = "padding:0;",
                              {div(class = "textCard", style = "overflow-y:scroll;",
                                  p(tags$b("Nickel-Metal Hydride (NiMH) Batteries",
                                           tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX1-5")),
                                      hr(style = "border-top:1px solid #999999; margin:5px;"),
                                      tags$b("How do they work?"),
                                          p(class = "cardText",
                                              "The negative electrode (anode) is made of a hydrogen-ion-absorbant metal hydride. The positive cathode is made of nickel (II) hydroxide,
                                              a hydrogen ion donor. When charging, electrons are transported from the nickel cathode to the metal hydride anode. charge repulsion drives
                                              hydrogen ions from the nickel hydroxide through and alkaline water-based electrolyte solution and into the metal hydride anode. When
                                              discharging, hydrogen ions return from the metal hydride anode to the nickel cathode, driving electrons through external circuits back to the
                                              cathode."), 
                                      tags$b("Common Applications:"),
                                          p(class = "cardText",
                                              "Electric Vehicles (i.e. Toyota Prius and other hybrid electric vehicles, early fully electric vehicles such as the General Motors EV1 
                                              (1996-1999), Consumer Electronic Devices, Rechargeable standard-size, single-cell batteries (i.e. AA, AAA, etc.)"),
                                      tags$b("State of Development:"),
                                          p(class = "cardText",
                                              "Fairly mature technology. As of 2005, NiMH batteries made up 3% of the national battery market. Market share has gradually reduced since
                                              then as NiMH are replaced by lithium ion in electric vehicles and consumer electronics.",
                                              "Nickel metal hydride batteries played a large role in the early development of electric vehicles after General Motors acquired the patent
                                              for a well-functioning formulation of the battery and used it in the first mass-produced electric vehicle, the EV1. In 2000, the patent was
                                              acquired by Texaco, which was shortly thereafter acquired by the Chevron Corporation. Following ths acquisition, Chevron, through is
                                              subsidiary Cobasys, has been accused of attempting to derail NiMH and electric vehicle development by refusing to license the technology
                                              for automotive use - presumably to minimize the effects of EVs on the oil market. These patents expired in 2015."),
                                      tags$b("Advantages:"),
                                          tags$li(class = "cardText", "Good energy density"),
                                          tags$li(class = "cardText", "Low cost"),
                                          tags$li(class = "cardText", "Environmentally benign materials"),
                                          tags$li(class = "cardText", "Recyclable materials"),
                                          tags$li(class = "cardText last", "Deliver constant voltage throughoug discharge"),
                                      tags$b("Disadvantages:"),
                                          tags$li(class = "cardText", "High self-discharge (unless using specifically designed 'low discharge' batteries"), 
                                          tags$li(class = "cardText", "Overcharging produces hydrogen gas, which can damage battery or caluse flame risk"),
                                          tags$li(class = "cardText last", "Complete discharge can cause reverse polarity - potentially damaging devices connected to the battery"),
                                      tags$b("Variations/Advances:"),
                                          p(class = "cardText",
                                              "Recent innovations include a novel separator between the two electrodes which reduces self-discharge from ~30% to less than 1%. R&D has
                                              slowed somewhat as lithium has become the dominant technology for many of NiMH's applications.")
                                  )
                              )} # Text Card
                          ), # Left Column Text Card
                          div(class = "column", style = "width: 460px; height: 450px; padding:0;",
                              {div(class = "imageCard",
                                div(class = "image_box",
                                    conditionalPanel(condition = "input.NiMHImage == 'NiMHImage1'",
                                                     tags$img(class = "NiMH", id = "NiMHImage1", src = "NiMH1h.png", style = "width: 95%; margin-left: 14px;")),
                                    conditionalPanel(condition = "input.NiMHImage == 'NiMHImage2'",
                                                     tags$img(class = "NiMH", id = "NiMHImage2", src = "NiMH2.jpg", style = "width: 100%")),
                                    conditionalPanel(condition = "input.NiMHImage == 'NiMHImage3'",
                                                     tags$img(class = "NiMH", id = "NiMHImage3", src = "NiMH3.jpg", style = "width: 100%"))
                                ),
                                
                                #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                div(class = "imgRadio",
                                    radioGroupButtons(inputId = "NiMHImage",
                                                      label = NULL, 
                                                      choiceValues = c("NiMHImage1", "NiMHImage2", "NiMHImage3"), 
                                                      choiceNames = c("", "", ""),
                                                      size = "sm", selected = "NiMHImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                           )}, # Image Card
                              {div(class = "captionCard",
                                conditionalPanel(condition = "input.NiMHImage == 'NiMHImage1'",
                                    p(class = "captionText", 
                                      strong("Nickel-Metal Hydride Battery Schematic"), br(),
                                      "NiMH batteries consist of a metal-hydride anode and a nickel hydroxide cathode, separated by an alkaline aqueous electrolyte. The
                                      electrolyte facilitates the transfer of hydrogen ions from one electrode to another, which enables electric charge transfer between
                                      the electrodes. The diagram above depicts a battery while charging, with hydrogen ions being transferred from the nickel cathode to
                                      the hydrogen ion-accepting metal hydride anode.")),
                                conditionalPanel(condition = "input.NiMHImage == 'NiMHImage2'",
                                    p(class = "captionText",
                                      strong("Rechargeable, Single-Cell NiMH Batteries"), br(),
                                      "Nickel batteries have seen extensive use as rechargeable batteries for personal electronic devices. Lithium ion are more commonly used
                                      for built-in applications due to longer cycle life, but nickel continues to find use in removable/exchangeable rechargeable batteries
                                      such as AAs, AAAs, etc.")),
                                conditionalPanel(condition = "input.NiMHImage == 'NiMHImage3'",
                                    p(class = "captionText",
                                      strong("NiMH Batteries in Electric Vehicles"), br(),
                                      "Until recently, Nickel-based batteries were the chemistry most widely used for electric vehicles. While most fully electric vehicles 
                                      now employ lithium ion batteries, nickel still finds use in hybrid vehicles such as the Toyota Prius."))
                           )}  # Caption Card
                        ) # Right Column with Images and Captions
                    ))}, # Nickel Metal Hydride Batteries
                    
                    {hidden(
                        div(class = "row ESTechPanel", id = "solidState",
                            div(class = "column textColumn",
                                {div(class = "textCard", style = "overflow-y:scroll",
                                    p(tags$b("Solid State Batteries",
                                             tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX1-6")),
                                    hr(style = "border-top:1px solid #999999; margin:5px;"),
                                    tags$b("How do they work?"),
                                        p(class = "cardText",
                                            "While the vast majority of batteries feature designs with at least one major component in the liquid phase, 
                                            usually the electrolyte, solid-state batteries contain two solid electrophiles separated by a solid electrophiles.
                                            Early solid-state batteries were made of silver or lead compounds or glass. The basic function of these batteries is similar 
                                            to those with liquid electrolytes. When charging, electrons are transported from the cathode to the anode, prompting migration of 
                                            positive ions across the electrolyte in the same direction. Discharging simply reverses this process."), 
                                    tags$b("Common Applications:"),
                                        p(class = "cardText",
                                            "Pacemakers, Radiofrequency idenfication devices (RFID), wearable technology/consumer electronics, electric vehicles and stationary storage
                                            (prospective use cases"),
                                    tags$b("State of Development:"),
                                        p(class = "cardText",
                                            "Very early in development - numerous companies and laboratories are engaged in R&D efforts to develop batteries capable of EV or stationary
                                            storage use."),
                                    tags$b("Advantages:"),
                                        tags$li(class = "cardText", "Tolerance to high temperatures"),
                                        tags$li(class = "cardText", "Minimal flammability risk - fewer fire safety systems"),
                                        tags$li(class = "cardText", "Potential for high energy density"),
                                        tags$li(class = "cardText", "Potential to reduce toxic chemical/material use"),
                                        tags$li(class = "cardText", "Potential for faster charging than lithium ion"),
                                        tags$li(class = "cardText last", "Potential for long cycle life"),
                                    tags$b("Disadvantages:"),
                                        tags$li(class = "cardText", "High costs (currently)"), 
                                        tags$li(class = "cardText", "Poor performances at lower temperatures"),
                                        tags$li(class = "cardText", "May require high internal pressure"),
                                        tags$li(class = "cardText last", "Lithium electrodes can experience dendrite growth"),
                                    tags$b("Variations/Advances:"),
                                        p(class = "cardText",
                                            "A variety of solid-state electrolytes are under investigation for reducing or eliminating the formation of lithium dendrites in solid-state
                                            batteries.")
                                   )
                              )} # Text Card
                          ), # Left Column Text Card
                          div(class = "column imageColumn",
                              {div(class = "imageCard",
                                   div(class = "image_box",
                                       conditionalPanel(condition = "input.solidStateImage == 'solidStateImage1'",
                                                        tags$img(class = "solidState zoom", id = "solidStateImage1", src = "solidState1.png", style = "width: 100%; margin-top: 40px;")),
                                       conditionalPanel(condition = "input.solidStateImage == 'solidStateImage2'",
                                                        tags$img(class = "solidState", id = "solidStateImage2", src = "solidState2.jpg", style = "width: 100%; margin-top: 30px;")),
                                       conditionalPanel(condition = "input.solidStateImage == 'solidStateImage3'",
                                                        tags$img(class = "solidState zoom", id = "solidStateImage3", src = "solidState3.jpg", style = "width: 100%; margin-top: 40px;"))
                                   ),
                                   
                                   #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                   #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                   div(class = "imgRadio",
                                       radioGroupButtons(inputId = "solidStateImage",
                                                         label = NULL, 
                                                         choiceValues = c("solidStateImage1", "solidStateImage2", "solidStateImage3"), 
                                                         choiceNames = c("", "", ""),
                                                         size = "sm", selected = "solidStateImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                              )}, # Image Card
                              {div(class = "captionCard",
                                   conditionalPanel(condition = "input.solidStateImage == 'solidStateImage1'",
                                      p(class = "captionText",
                                        strong("Comparison of a Solid State Battery to Lithium Ion"), br(),
                                        "Solid state batteries bear many similarities to lithium ion batteries. However, the liquid or gel electrolyte separating
                                        the electrodes is replaced by a solid electrolyte, typically made of ceramic, glass, or sulfide.")),
                                   conditionalPanel(condition = "input.solidStateImage == 'solidStateImage2'",
                                      p(class = "captionText",
                                        strong("Electrochemical Cell of a Solid State Battery"), br(),
                                        "The use of a solid electrolyte rather than gel or liquid allows electrodes to be placed much closer together, significantly
                                        decreasing the size of each cell. This potentially enables solid state batteries to be much smaller than another battery with
                                        comparable capacity, or to fit much greater capacity into a battery of the same size. These advantages could have huge impacts
                                        on consumer electronics and electric cars respectively.")),
                                   conditionalPanel(condition = "input.solidStateImage == 'solidStateImage3'",
                                      p(class = "captionText",
                                        strong("Development Trajectory for Solid State Batteries"), br(),
                                        "Currently, solid state batteries are considered to be cost prohibitive for most commercial applications. Research is ongoing 
                                        to decrease costs and improve performance of these batteries. Finding solutions to these challenges is a key step towards
                                        commercialization and widespread application of the technology."))
                              )}  # Caption Card
                          ) # Right Column with Images and Captions
                      ))}  # Solid State Batteries
                    
                )}, # Electrochemical
                {div(
                    {hidden(
                      div(class = "row ESTechPanel", id = "flywheel",
                          div(class = "column textColumn",
                              {div(class = "textCard", style = "overflow-y: scroll;",
                                  p(tags$b("Flywheels",
                                           tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX2-1")),
                                      hr(style = "border-top:1px solid #999999; margin:5px;"),
                                      tags$b("How do they work?"),
                                          p(class = "cardText",
                                              "A circular or cylindrical rotor is accelerated to a very high speed in a vacuum-enclosed ultra-low-friction environment using a combined 
                                              motor/generator. This converts and stores electrical energy as rotational kinetic energy. When the flywheel is being 'charged,' 
                                              its speed of rotation is increased, adding kinetic energy. When 'discharging,' the flywheel is slowed down, and the motor/generator
                                              converts the lost rotational kinetic energy  back into electrical energy."), 
                                      tags$b("Common Applications:"),
                                          p(class = "cardText",
                                              "Grid frequency regulation and short-term reserve power capacity. Braking and acceleration assist in electric and hybrid electric
                                              vehicles."),
                                      tags$b("State of Development:"),
                                          p(class = "cardText",
                                              "Mature technology - 58 MW of rated power capacity installed and operating as of 2018."),
                                      tags$b("Advantages:"),
                                          tags$li(class = "cardText", "High round-trip efficiency (>85%)"),
                                          tags$li(class = "cardText", "Nearly instantaneous response time"),
                                          tags$li(class = "cardText last", "Durable materials - long useful life"),
                                      tags$b("Disadvantages:"),
                                          tags$li(class = "cardText", "Suited primarily for short-discharge applications (i.e. frequency regulation)"), 
                                          tags$li(class = "cardText last", "High self-discharge rate (~5% per day)"),
                                      tags$b("Variations/Advances:"),
                                          p(class = "cardText",
                                              "Ongoing research on flywheel energy storage systems focuses on advanced superconducting magnetic bearings which minimal friction or
                                              drift for the spinning flywheel, improving round-trip efficiency, and on durable materials for use in the flywheel's rotor, improving
                                              functional life.")
                                  )
                              )} # Text Card
                          ), # Left Column Text Card
                          div(class = "column imageColumn",
                              {div(class = "imageCard",
                                   div(class = "image_box", 
                                       conditionalPanel(condition = "input.flywheelImage == 'flywheelImage1'",
                                                        tags$img(class = "flywheel", id = "flywheelImage1", src = "flywheel1.png", style = "width: 95%; margin: 0 2%;")),
                                       conditionalPanel(condition = "input.flywheelImage == 'flywheelImage2'",
                                                        tags$img(class = "flywheel", id = "flywheelImage2", src = "flywheel2.jpg", style = "width: 95%; margin-left:10px;")),
                                       conditionalPanel(condition = "input.flywheelImage == 'flywheelImage3'",
                                                        tags$img(class = "flywheel zoom", id = "flywheelImage3", src = "flywheel3.png", style = "width: 70%; margin-left:63px;"))
                                   ),
                                   
                                   #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                   #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                   div(class = "imgRadio",
                                       radioGroupButtons(inputId = "flywheelImage",
                                                         label = NULL, 
                                                         choiceValues = c("flywheelImage1", "flywheelImage2", "flywheelImage3"), 
                                                         choiceNames = c("", "", ""),
                                                         size = "sm", selected = "flywheelImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                              )}, # Image Card
                              {div(class = "captionCard",
                                  conditionalPanel(condition = "input.flywheelImage == 'flywheelImage1'",
                                      p(class = "captionText",
                                        strong("Anatomy of a Flywheel"), br(),
                                        "Flywheels are designed to minimize friction on the rotor in order to maximize storage efficiency. Here, magnetic bearings
                                        and a vacuum virtually eliminate friction between the shaft and the motor generator to enable rapid charge-discharge cycles
                                        with high efficiency.")),
                                  conditionalPanel(condition = "input.flywheelImage == 'flywheelImage2'",
                                      p(class = "captionText",
                                        strong("Clear Creek Flywheel Wind Farm Project, Ontario, Canada"), br(),
                                        "Ten 500kW flywheels in 5 MW storage installation in Clear Creek, Ontario, Canada by NRStor. Adjacent to a 20 MW wind farm.
                                        NRStor intends to pair the flywheels with a battery storage system to take advantage of the strengths of each and maximize
                                        functional life by reducing the number of cycles on the battery. Flywheels are located beneath the round concrete blocks
                                        on the floor of the facility.")),
                                  conditionalPanel(condition = "input.flywheelImage == 'flywheelImage3'",
                                      p(class = "captionText",
                                        strong("Hybrid Flywheel-Battery Energy Storage Systems"), br(),
                                        "Due to the complementary characteristics of flywheels and batteries, several storage installers have combined the two technologies.
                                        The flywheel responds to short-duration, rapid response needs to reduce cycling the battery and prolong its useful life. Meanwhile,
                                        the battery follows longer-term storage need trends such as time-shiting applications."))
                              )}  # Caption Card
                          ) # Right Column with Images and Captions
                      ))}, # Flywheels
                    
                    {hidden(
                        div(class = "row ESTechPanel", id = "pumpedHydro",
                            div(class = "column textColumn",
                                {div(class = "textCard", style = "overflow-y:scroll;",
                                    p(tags$b("Pumped Hydroelectric Storage",
                                             tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX2-2")),
                                        hr(style = "border-top:1px solid #999999; margin:5px;"),
                                        tags$b("How does it work?"),
                                            p(class = "cardText",
                                                "Pumped hydroelectric storage facilities are comprised of two large reservoirs at different elevations separated by a 
                                                reversible turbine. When excess electricity needs to be stored, the turbine is employed to pump water uphill from the 
                                                lower reservoir to the upper reservoir When that energy is needed, water from the upper reservoir is released through the
                                                turbine, which converts the gravitational potential back into electricity."), 
                                        tags$b("Common Applications:"),
                                            p(class = "cardText",
                                                "Bulk energy management, time-shifting"),
                                        tags$b("State of Development:"),
                                            p(class = "cardText",
                                                "Mature technology - As of 2017, there were 25 GW of pumped hydro storage in the US and 184 GW around the world. Few
                                                new pumped hydro facilities are being planned or constructed due to geographic limitations and environmental concerns."),
                                        tags$b("Advantages:"),
                                            tags$li(class = "cardText", "Large-scale"),
                                            tags$li(class = "cardText last", "Potential for long duration"),
                                        tags$b("Disadvantages:"),
                                            tags$li(class = "cardText", "Geographic limitations"),
                                            tags$li(class = "cardText", "High capital costs"),
                                            tags$li(class = "cardText", "Environmental and land-use concerns"),
                                            tags$li(class = "cardText last", "Slow response time"),
                                        tags$b("Variations/Advances:"),
                                            p(class = "cardText",
                                                "Research is being conducted on underground pumped hydro, wherein an artificial underground reservoir is created and filled
                                                with water. When 'charging' the water is pumped to the surface and placed in a surface level reservoir. During discharge, the
                                                water is permitted to flow back underground, turning turbines along the way to generate electricity.")
                                    )
                                )} # Text Card
                            ), # Left Column Text Card
                            div(class = "column imageColumn",
                                {div(class = "imageCard", style = "height:400px;",
                                     div(class = "image_box",
                                         conditionalPanel(condition = "input.pumpedHydroImage == 'pumpedHydroImage1'",
                                                          tags$img(class = "pumpedHydro zoom", id = "pumpedHydroImage1", src = "pumpedHydro1.jpg", style = "width: 76%; margin-left:44px;")),
                                         conditionalPanel(condition = "input.pumpedHydroImage == 'pumpedHydroImage2'",
                                                          tags$img(class = "pumpedHydro zoom", id = "pumpedHydroImage2", src = "pumpedHydro2.jpg", style = "width: 76%; margin-left:44px;")),
                                         conditionalPanel(condition = "input.pumpedHydroImage == 'pumpedHydroImage3'",
                                                          tags$img(class = "pumpedHydro", id = "pumpedHydroImage3", src = "pumpedHydro3.jpg", style = "width: 81%; margin-left:35px;"))
                                     ),
                                     
                                     #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     div(class = "imgRadio", style = "padding-top:366px;",
                                         radioGroupButtons(inputId = "pumpedHydroImage",
                                                           label = NULL, 
                                                           choiceValues = c("pumpedHydroImage1", "pumpedHydroImage2", "pumpedHydroImage3"), 
                                                           choiceNames = c("", "", ""),
                                                           size = "sm", selected = "pumpedHydroImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                              )}, # Image Card
                                {div(class = "captionCard", style = "height: 160px;",
                                    conditionalPanel(condition = "input.pumpedHydroImage == 'pumpedHydroImage1'",
                                        p(class = "captionText",
                                          strong("Closed-Loop Pumped Hydro Storage"), br(),
                                          "A closed-loop pumped hydroelectric energy storage system requires two reservoirs, an upper and a lower, connected to each other by
                                          a tunnel or penstock. A power house with a turbine sits at the base of the tunnel and either pumps water to the upper reservoir
                                          (charges) or allows water to flow down to the lower reservoir (discharges).")),
                                    conditionalPanel(condition = "input.pumpedHydroImage == 'pumpedHydroImage2'",
                                        p(class = "captionText",
                                          strong("Open-Loop Pumped Hydro Storage"), br(),
                                          "Open-looped pumped hydro systems are very similar to closed-loop systems in requring an upper and lower reservoir, but here the lower
                                          reservoir is an open source, such as a river. These systems are often colocated with dams to ensure adequate water levels in the lower 
                                          reservoir.")),
                                    conditionalPanel(condition = "input.pumpedHydroImage == 'pumpedHydroImage3'",
                                        p(class = "captionText",
                                          strong("Hohenwarte II Pumped Storage Power Plant, Thuringia, Germany"), br(),
                                          "Hohenwarte II is an open-loop system with the Saale River as the lower reservoir. The eight penstocks fall 304 meters to the powerhouse,
                                           generating electricity with a 320 megawatt nameplate capacity."))
                                )}  # Caption Card
                            ) # Right Column with Images and Captions
                        )
                    )}, # Pumped Hydro
                    
                    {hidden(
                        div(class = "row ESTechPanel", id = "CAES",
                            div(class = "column textColumn",
                                {div(class = "textCard", style = "overflow-y:scroll;",
                                    p(tags$b("Compressed Air Energy Storage (CAES)",
                                             tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX2-3")),
                                    hr(style = "border-top:1px solid #999999; margin:5px;"),
                                    tags$b("How does it work?"),
                                        p(class = "cardText",
                                            "Multistage air compressors are employed to take atmospheric air and compress it into large underground caverns. The
                                            temperature of compressed air increases significantly, so intermediate coolers bring the internal temperature of the
                                            cavern from 300-350ºF down to 110-120ºF for storage. Upon discharging, the compressed air is released from the cavern,
                                            heated with natural gas to compensate for loss of heat during initial cooling, and piped through a turbine where 
                                            electricity is generated."), 
                                    tags$b("Common Applications:"),
                                        p(class = "cardText",
                                            "Bulk energy management, time-shifting, reserve capacity"),
                                    tags$b("State of Development:"),
                                        p(class = "cardText",
                                            "CAES has been in use since 1978, but only two large-scale CAES facilities are operating in the world as of 2018 
                                            (McIntosh, Alabama, and Huntorf, Germany), though many projects are currently in development."),
                                    tags$b("Advantages:"),
                                        tags$li(class = "cardText", "Black-start capability"),
                                        tags$li(class = "cardText last", "No hazardous materials"),
                                    tags$b("Disadvantages:"),
                                        tags$li(class = "cardText", "Use of natural gas to heat stored gas"),
                                        tags$li(class = "cardText", "Low efficiency (40-55%)"),
                                        tags$li(class = "cardText", "Geographic limitations"),
                                        tags$li(class = "cardText last", "Low energy density"),
                                    tags$b("Variations/Advances:"),
                                        p(class = "cardText",
                                            "Most CAES facilities currently under development will employ methods to extract heat from the incoming air during 
                                            compression and store it onsite (known as adiabatic CAES). This stored heat can then be used to reheat the released 
                                            air before running it through the turbine. This method avoids the use of natural gas and is projected to increase
                                            round-trip efficiency by up to 40% (to 70-80% efficient).")
                                    )
                                )} # Text Card
                            ), # Left Column Text Card
                          div(class = "column imageColumn",
                              {div(class = "imageCard", style = "height:400px;",
                                   div(class = "image_box",
                                       conditionalPanel(condition = "input.CAESImage == 'CAESImage1'",
                                                        tags$img(class = "CAES zoom", id = "CAESImage1", src = "CAES1.jpg", style = "width: 100%; margin-top: 60px;")),
                                       conditionalPanel(condition = "input.CAESImage == 'CAESImage2'",
                                                        tags$img(class = "CAES zoom", id = "CAESImage2", src = "CAES2.png", style = "width: 76%; margin-left: 49px;")),
                                       conditionalPanel(condition = "input.CAESImage == 'CAESImage3'",
                                                        tags$img(class = "CAES zoom", id = "CAESImage3", src = "CAES3.jpg", style = "width: 95%; margin-left: 15px;"))
                                   ),
                                   
                                   #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                   #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                   div(class = "imgRadio", style = "padding-top:366px;",
                                       radioGroupButtons(inputId = "CAESImage",
                                                         label = NULL, 
                                                         choiceValues = c("CAESImage1", "CAESImage2", "CAESImage3"), 
                                                         choiceNames = c("", "", ""),
                                                         size = "sm", selected = "CAESImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                              )}, # Image Card
                              {div(class = "captionCard", style = "height:160px;",
                                  conditionalPanel(condition = "input.CAESImage == 'CAESImage1'",
                                      p(class = "captionText",
                                        strong("Compressed Air Energy Storage (CAES) Schematic"), br(),
                                        "CAES uses low- and high-pressure compressors and turbines to compress air and generated electricity repectively. Heat must be released during 
                                        compression and added back to the air during decompression/discharge because gases naturally increase in temperature when compressed and cool
                                        down when allowed to expand.")),
                                  conditionalPanel(condition = "input.CAESImage == 'CAESImage2'",
                                      p(class = "captionText",
                                        strong("Underground Caverns as Storage Vessels"), br(),
                                        "Due to the vase space requirements of CAES, caverns are often used to store the air underground. These are often disused mines or natural 
                                        geological formations. This image depicts a CAES plant wherein compressors are employed to store the air underground and thermal storage is used 
                                        to heat the air back up as it is released into the turbine.")),
                                  conditionalPanel(condition = "input.CAESImage == 'CAESImage3'",
                                      p(class = "captionText",
                                        strong("Adiabatic Compressed Air Energy Storage"), br(),
                                        "The primary weakness/disadvantage of conventional CAES is the need to reheat air upon decompression in the power production process. This either 
                                        uses electricity, reducing storage efficiency, or natural gas, creating carbon emissions. Adiabatic CAES extracts heat energy from air being 
                                        compressed and stores it to be used later during decompression."))
                              )}  # Caption Card
                          ) # Right Column with Images and Captions
                      ))} # Compressed Air Energy Storage (CAES)
                    
                )}, # Electromechanical
                {div(
                    {hidden(
                        div(class = "row ESTechPanel", id = "superCap",
                            div(class = "column textColumn",
                                {div(class = "textCard", style = "overflow-y:scroll;",
                                    p(tags$b("Capacitors and Supercapacitors",
                                             tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX3-1")),
                                    hr(style = "border-top:1px solid #999999; margin:5px;"),
                                        tags$b("How do they work?"),
                                            p(class = "cardText",
                                                "Capacitors and supercapacitors are made up of two parallel conductive plates (electrodes) separated by an
                                                insulating dielectric barrier. When a voltage is applied across the capacitor, positive charges build up
                                                on one plate while negative charges build up on the other. These charges create an electric field between
                                                the two plates, which stores the electrical energy. Characteristics such as capacitance, power, and energy 
                                                capacity depend on the size of the plates and the dielectric materials."), 
                                        tags$b("Common Applications:"),
                                            p(class = "cardText",
                                                "Consumer electronics, auxiliary grid services such as power factor correction, energy recovery systems
                                                (i.e. regenerative braking in hybrid vehicles)."),
                                        tags$b("State of Development:"),
                                            p(class = "cardText",
                                                "Mature technology - developed in the late 18th and early 19th centuries. Modern versions employ advanced
                                                materials to make them smaller and more powerful, but the function and theory is the same."),
                                        tags$b("Advantages:"),
                                            tags$li(class = "cardText", "High power capacity"),
                                            tags$li(class = "cardText", "Rapid charge ability"),
                                            tags$li(class = "cardText last", "Extremely long cycle life (>1,000,000 cycles"),
                                        tags$b("Disadvantages:"),
                                            tags$li(class = "cardText", "Voltage declines steadily throughout discharge"),
                                            tags$li(class = "cardText", "Low specific energy and energy density"),
                                            tags$li(class = "cardText last", "High self-discharge rate"),
                                        tags$b("Variations/Advances:"),
                                            p(class = "cardText",
                                                "Supercapacitors and ultracapacitors function similarly to capacitors, but with an electrolyte and 
                                                ion-permeable separator between the electrodes. When charges build up on an electrode, opposite charges
                                                accumulate on its surface in the electrolyte, and a strong electric field forms across this barrier.
                                                Because two ion layers form in supercapacitors, one on each electrode, the capacitance (proportional to
                                                energy capacity) increases.")
                                    )
                                )} # Text Card
                            ), # Left Column Text Card
                            div(class = "column imageColumn",
                                {div(class = "imageCard",
                                     div(class = "image_box",
                                         conditionalPanel(condition = "input.superCapImage == 'superCapImage1'",
                                                          tags$img(class = "superCap zoom", id = "superCapImage1", src = "superCap1.png", style = "width: 100%;")),
                                         conditionalPanel(condition = "input.superCapImage == 'superCapImage2'",
                                                          tags$img(class = "superCap zoom", id = "superCapImage2", src = "superCap2.jpg", style = "width: 86%; margin-left: 26px;")),
                                         conditionalPanel(condition = "input.superCapImage == 'superCapImage3'",
                                                          tags$img(class = "superCap zoom", id = "superCapImage3", src = "superCap3.png", style = "width: 92%; margin-left: 18px;"))
                                     ),
                                     
                                     #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     div(class = "imgRadio",
                                         radioGroupButtons(inputId = "superCapImage",
                                                           label = NULL, 
                                                           choiceValues = c("superCapImage1", "superCapImage2", "superCapImage3"), 
                                                           choiceNames = c("", "", ""),
                                                           size = "sm", selected = "superCapImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                                )}, # Image Card
                                {div(class = "captionCard",
                                     conditionalPanel(condition = "input.superCapImage == 'superCapImage1'",
                                                      p(class = "captionText",
                                                        strong("Diagram of an Electrical Capacitor"), br(),
                                                        "The schematic of a capacitor depicts two electrodes separated by a dieletric made of non-conducting material.
                                                        This capacitor is shown charged, with like charges built up on each electrode. When the capacitor discharges, the electrical
                                                        charges will be evenly distributed between the two electrodes.")),
                                     conditionalPanel(condition = "input.superCapImage == 'superCapImage2'",
                                                      p(class = "captionText",
                                                        strong("Cross-Section of an Assembled Capacitor"), br(),
                                                        "Capacitors consist of two metal electrodes separated by a dielectric. These three sheets are tightly rolled into
                                                        a cylinder and encased in an aluminum shell with plastic insulation. Two terminals are connected, which facilitate
                                                        connection to external load or power sources.")),
                                     conditionalPanel(condition = "input.superCapImage == 'superCapImage3'",
                                                      p(class = "captionText",
                                                        strong("Diagram of a Super- or Ultracapacitor"), br(),
                                                        "Supercapacitors and ultracapacitors bear the same basic structure as capacitors, but have an electrolyte and semi-permeable
                                                        membrane in place of the dielectric. When the supercapacitor is charged, and charges build up on each electrode, layers of
                                                        opposite-charged ions accumulate against each side. These double layers increase the size of electric field and, correspondingly,
                                                        the storage capcity."))
                                )}  # Caption Card
                            ) # Right Column with Images and Captions
                        )
                    )}, # Capacitors and Supercapacitors
                    
                    {hidden(
                        div(class = "row ESTechPanel", id = "SMES",
                            div(class = "column textColumn",
                                {div(class = "textCard", style = "overflow-y:scroll;",
                                    p(tags$b("Superconducting Magnetic Energy Storage (SMES)",
                                             tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX3-2")),
                                        hr(style = "border-top:1px solid #999999; margin:5px;"),
                                        tags$b("How does it work?"),
                                            p(class = "cardText",
                                                "A superconducting coil is cryogenically cooled below its critical temperature so that it experiences no
                                                electrical resistence. Direct current is run through the coil, and because of the superconductivity, it can
                                                continue to flow after the power source is disconnected without attenuation from resistence. The current 
                                                creates a magnetic field around the coil through which energy is stored."), 
                                        tags$b("Common Applications:"),
                                            p(class = "cardText",
                                                "Power quality control systems, grid stability in response to rapid power/voltage fluctuations"),
                                        tags$b("State of Development:"),
                                            p(class = "cardText",
                                                "New technology - several small-scale demonstration systems installed, but yet to be applied in large numbers
                                                or at large scale."),
                                        tags$b("Advantages:"),
                                            tags$li(class = "cardText", "Virtually instantaneous response time"),
                                            tags$li(class = "cardText", "Highest efficiency of all energy storage devices (~95%)"),
                                            tags$li(class = "cardText", "No self-discharge at cryogenic temperatures"),
                                            tags$li(class = "cardText", "Highly durable and reliable - no chemical reactions or moving parts"),
                                            tags$li(class = "cardText last", "Extremely long cycle life"),
                                        tags$b("Disadvantages:"),
                                            tags$li(class = "cardText", "High cost"), 
                                            tags$li(class = "cardText", "High energy use to maintain cryogenic conditions"), 
                                            tags$li(class = "cardText last", "Challenges with large-scale manufacture of superconducting coil"),
                                        tags$b("Variations/Advances:"),
                                            p(class = "cardText",
                                                "Since the superconductors required for SMES are both very expensive and only function at cryogenic temperatures, advances
                                                with this energy storage technology may depend on the development of new superconducting materials that may be less expensive
                                                or function at warmer temperatures, reducing the cost of maintaining a cryogenic environment.")
                                    )
                                )} # Text Card
                            ), # Left Column Text Card
                            div(class = "column imageColumn",
                                {div(class = "imageCard",
                                     div(class = "image_box",
                                         conditionalPanel(condition = "input.SMESImage == 'SMESImage1'",
                                                          tags$img(class = "SMES zoom", id = "SMESImage1", src = "SMES1.jpg", style = "width: 100%; margin-top:45px;")),
                                         conditionalPanel(condition = "input.SMESImage == 'SMESImage2'",
                                                          tags$img(class = "SMES", id = "SMESImage2", src = "SMES2.jpg", style = "width: 100%")),
                                         conditionalPanel(condition = "input.SMESImage == 'SMESImage3'",
                                                          tags$img(class = "SMES", id = "SMESImage3", src = "SMES3a.png", style = "width: 92%; margin-left:15px;"))
                                     ),
                                     
                                     #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     div(class = "imgRadio",
                                         radioGroupButtons(inputId = "SMESImage",
                                                           label = NULL, 
                                                           choiceValues = c("SMESImage1", "SMESImage2", "SMESImage3"), 
                                                           choiceNames = c("", "", ""),
                                                           size = "sm", selected = "SMESImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                                )}, # Image Card
                                {div(class = "captionCard",
                                     conditionalPanel(condition = "input.SMESImage == 'SMESImage1'",
                                                      p(class = "captionText",
                                                        strong("Diagram of a Superconducting Magnetic Energy Storage System"), br(),
                                                        "SMES systems are schamatically fairly simple. A system consists of a large, highly conducting coil which is cooled to cryogenic 
                                                        temperatures, as well as power conversion and conditioning equipment. This low-temperature apparatus allows for virtually no
                                                        resistence on the metal coil.")),
                                     conditionalPanel(condition = "input.SMESImage == 'SMESImage2'",
                                                      p(class = "captionText",
                                                        strong("Creation of a Magnetic Field by Passing a Current through Coiled Wire"), br(),
                                                        "When electricity is run through the metal coils at cryogenic temperatures, the current can continue to flow around the coil undeterred
                                                        even when the power source is disconnected. This flow creates an electromagnetic field around the coil in which the energy is stored.")),
                                     conditionalPanel(condition = "input.SMESImage == 'SMESImage3'",
                                                      p(class = "captionText",
                                                        strong("Photo of an SMES System with the Coiled Wire Core Removed"), br(),
                                                        "On the right of the above image is the large wire coil which makes up the main component of a SMES apparatus. This coil is submerged
                                                        in a chamber of liquid nitrogen and liquid helium within a vacuum-insulated jacket which keeps it at cryogenic temperatures around 4 Kelvin
                                                        (-452 Fahrenheit / -269 Celsius)."))
                                )}  # Caption Card
                            ) # Right Column with Images and Captions
                        )
                    )} # Superconducting Magnetic Energy Storage (SMES)     

                )}, # Electrical
                {div(
                    {hidden(
                    div(class = "row ESTechPanel", id = "hotWater",
                        div(class = "column textColumn",
                            {div(class = "textCard",
                                 p(tags$b("Hot Water and Ice",
                                          tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX4-1")),
                                   hr(style = "border-top:1px solid #999999; margin:5px;"),
                                   tags$b("How does it work?"),
                                   p(class = "cardText",
                                     "Hot water heaters and air conditioning units can, if adequately insulated, shift much of their electricity use to
                                     night or other off-peak hours. Water heaters can be set to heat water, and air conditioning units to freeze it into
                                     ice at night when electricity costs and load are low. Then, during the day, hot water can be used as normal and ice
                                     can be employed as a coolant. This is particularly impactful for ice storage, since air conditioning typically
                                     contributes significantly to summer peak load events."), 
                                   tags$b("Common Applications:"),
                                   p(class = "cardText",
                                     "Energy time-shifting"),
                                   tags$b("State of Development:"),
                                   p(class = "cardText",
                                     "Mature technology - the primary enabling factor for this storage application is insulation quality, which is fairly
                                     robust. Many utilities run programs to reward customers for using time-shifting hot water heaters."),
                                   tags$b("Advantages:"),
                                   tags$li(class = "cardText", "Simple technology"),
                                   tags$li(class = "cardText last", "Inexpensive installation (using storage hot water heaters)"),
                                   tags$b("Disadvantages:"),
                                   tags$li(class = "cardText", "Can waste energy if hot water is not used during the day"), 
                                   tags$li(class = "cardText", "Can be complicated and confusing to implement effectively"),
                                   tags$li(class = "cardText last", "Larger physical size than alternative options"),
                                   tags$b("Variations/Advances:"),
                                   p(class = "cardText",
                                     "Much of the work currently being undertaken on hot water energy storage involves program and policy design to determine how
                                     best to coordinate or control the use of the distributed storage resources in the form of residential water heaters.")
                                 )
                            )} # Text Card
                        ), # Left Column Text Card
                        div(class = "column imageColumn",
                            {div(class = "imageCard",
                                 div(class = "image_box",
                                     conditionalPanel(condition = "input.hotWaterImage == 'hotWaterImage1'",
                                                      tags$img(class = "hotWater", id = "hotWaterImage1", src = "hotWater1.jpg", style = "width: 100%; margin-top: 35px;")),
                                     conditionalPanel(condition = "input.hotWaterImage == 'hotWaterImage2'",
                                                      tags$img(class = "hotWater zoom", id = "hotWaterImage2", src = "hotWater2.jpg", style = "width: 100%; margin-top: 20px;")),
                                     conditionalPanel(condition = "input.hotWaterImage == 'hotWaterImage3'",
                                                      tags$img(class = "hotWater zoom", id = "hotWaterImage3", src = "hotWater3.jpg", style = "width: 100%; margin-top: 20px;"))
                                 ),
                                 
                                 #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                 #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                 div(class = "imgRadio",
                                     radioGroupButtons(inputId = "hotWaterImage",
                                                       label = NULL, 
                                                       choiceValues = c("hotWaterImage1", "hotWaterImage2", "hotWaterImage3"), 
                                                       choiceNames = c("", "", ""),
                                                       size = "sm", selected = "hotWaterImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                            )}, # Image Card
                            {div(class = "captionCard",
                                 conditionalPanel(condition = "input.hotWaterImage == 'hotWaterImage1'",
                                                  p(class = "captionText",
                                                    strong("Tank-Style Hot Water Heaters"), br(),
                                                    "Residential and small commercial thermal energy storage primarily relies on large tank-style water heaters like those shown above.
                                                    These tanks are highly insulated and can keep large quantities of water hot for extended periods of time, enabling owners to heat
                                                    water at times of low energy use and cost but use it when demand and cost are higher.")),
                                 conditionalPanel(condition = "input.hotWaterImage == 'hotWaterImage2'",
                                                  p(class = "captionText",
                                                    strong("Benefits of Grid-Integrated Hot Water Heaters"), br(),
                                                    "Estimates predict that converting all water heaters in the country to electric tank-style units which can be controlled and coordinated
                                                    could provide $3.6 billion in value to the grid, utilities, and ratepayers. This is mostly made up of avoided generation and arbitrage value.")),
                                 conditionalPanel(condition = "input.hotWaterImage == 'hotWaterImage3'",
                                                  p(class = "captionText",
                                                    strong("Thermal Storage for Building Air Conditioning"), br(),
                                                    "Similar to storing thermal energy as hot water, it is possible to store cold air or water for use in air conditioning. This process
                                                    depicted above is generally the opposite of hot water storage, storing a cold medium during off-peak times and using that stored material
                                                    to augment or replace building cooling units."))
                            )}  # Caption Card
                        ) # Right Column with Images and Captions
                    ))}, # Hot Water / Ice
                        
                    {hidden(
                        div(class = "row ESTechPanel", id = "moltenSalt",
                            div(class = "column textColumn",
                                {div(class = "textCard",
                                    p(tags$b("Molten Salt",
                                             tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX4-2")),
                                        hr(style = "border-top:1px solid #999999; margin:5px;"),
                                        tags$b("How does it work?"),
                                            p(class = "cardText",
                                                "Typically used in combination with concentrating solar power (CSP), molten salt thermal energy storage uses
                                                concentrated solar rays to heat a mixture of salts (usually sodium, potassium, and calcium nitrate) in liquid 
                                                phase from 288ºC (550ºF) to 566ºC (1,051ºF). The superheated molten salt is pumped into an insulated hot storage
                                                tank, where it can be kept for up to a week. This enables the normally variable solar resource to be dispatchable
                                                to meet variable load or hold a constant generation profile."), 
                                        tags$b("Common Applications:"),
                                            p(class = "cardText",
                                                "Renewable generation (CSP) firming, time-shifting"),
                                        tags$b("State of Development:"),
                                            p(class = "cardText",
                                                "Relatively new technology - the first use of molten salt storage was by SolarTwo, a CSP facility in the Mojave
                                                Desert, in 1995. Subsequent iterations of the technology have been developed in the southwest United States and
                                                in Spain."),
                                        tags$b("Advantages:"),
                                            tags$li(class = "cardText", "Turns variable resource into firm capacity"),
                                            tags$li(class = "cardText", "High power and energy density"),
                                            tags$li(class = "cardText last", "Capable of multi-megawatt-scale storage capacity"),
                                        tags$b("Disadvantages:"),
                                            tags$li(class = "cardText", "Limited scope of application (CSP)"), 
                                            tags$li(class = "cardText last", "Extremely hot and hazardous materials"),
                                        tags$b("Variations/Advances:"),
                                            p(class = "cardText",
                                                "Advances include efforts to produce constant, smooth, baseload-type power from variable CSP resources. In 2013,
                                                Gemasolar Thermosolar in Spain continuously produced electricity for 36 straight days.")
                                    )
                                )} # Text Card
                            ), # Left Column Text Card
                            div(class = "column imageColumn",
                                {div(class = "imageCard",
                                     div(class = "image_box",
                                         conditionalPanel(condition = "input.moltenSaltImage == 'moltenSaltImage1'",
                                                          tags$img(class = "moltenSalt zoom", id = "moltenSaltImage1", src = "moltenSalt1.jpg", style = "width: 100%;")),
                                         conditionalPanel(condition = "input.moltenSaltImage == 'moltenSaltImage2'",
                                                          tags$img(class = "moltenSalt", id = "moltenSaltImage2", src = "moltenSalt2.jpg", style = "width: 100%")),
                                         conditionalPanel(condition = "input.moltenSaltImage == 'moltenSaltImage3'",
                                                          tags$img(class = "moltenSalt", id = "moltenSaltImage3", src = "moltenSalt3.jpg", style = "width: 100%"))
                                     ),
                                     
                                     #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     div(class = "imgRadio",
                                         radioGroupButtons(inputId = "moltenSaltImage",
                                                           label = NULL, 
                                                           choiceValues = c("moltenSaltImage1", "moltenSaltImage2", "moltenSaltImage3"), 
                                                           choiceNames = c("", "", ""),
                                                           size = "sm", selected = "moltenSaltImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                                )}, # Image Card
                                {div(class = "captionCard",
                                     conditionalPanel(condition = "input.moltenSaltImage == 'moltenSaltImage1'",
                                                      p(class = "captionText",
                                                        strong("Concentrating Solar Power and Molten Salt Energy Storage"), br(),
                                                        "Vast mirror arrays (shown on the left in blue) concentrate solar energy to superheat a molten mixture of salts. That mixture
                                                        is stored in heavily insulated tanks before being pumped into a heat exchanger when discharging. The heat exchanger boils water 
                                                        to make steam, which then turns a turbine, generating electricity.")),
                                     conditionalPanel(condition = "input.moltenSaltImage == 'moltenSaltImage2'",
                                                      p(class = "captionText",
                                                        strong("Large Scale Concentrating Solar Power Generation Facility"), br(),
                                                        "CSP facilities typically feature a vast, circular array of mirrors, which concentrate solar energy towards a central tower, which 
                                                        transfers the energy to the molten salt storage medium. Each mirror adjusts its orientation in unison to track the position of the
                                                        sun.")),
                                     conditionalPanel(condition = "input.moltenSaltImage == 'moltenSaltImage3'",
                                                      p(class = "captionText",
                                                        strong("Molten Salt Energy Storage System"), br(),
                                                        "'Cool' (550F) salt mixture is kpt in one storage tank, from which it is pumped into the central tower. Hot salt mixture then leaves 
                                                        the tower to be stored in the other tank, essentially charging the device. To discharge, the hot medium is pumped to another building
                                                        which houses a heat exchanger, creating steam, which turns a turbine in a subsequent building."))
                                )}  # Caption Card
                            ) # Right Column with Images and Captions
                        )
                    )}, # Molten Salt
                        
                    {hidden(
                        div(class = "row ESTechPanel", id = "thermalEnvelope",
                            div(class = "column textColumn",
                                {div(class = "textCard", style = "overflow-y:scroll;",
                                    p(tags$b("Thermal Envelopes (Building Insulation)",
                                             tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX4-3")),
                                        hr(style = "border-top:1px solid #999999; margin:5px;"),
                                        tags$b("How do they work?"),
                                            p(class = "cardText",
                                                "Thermal envelopes are the spaces that are enclosed by rooms or buildings, and in this context refer to their ability
                                                to keep heat in our out. Similarly to hat water or ice thermal energy storage, proper insulation can turn any building
                                                into a very efficient energy storage device. In winter, a well-insulated house can store the energy it absorbs from the
                                                sun during the day in the form of warm air. At night, when temperatures drop and solar energy is no longer available,
                                                less heating will be required if the house is able to retain that heat well. The same is true for cool air during the
                                                summer, reducing air conditioning use during the day."), 
                                        tags$b("Common Applications:"),
                                            p(class = "cardText",
                                                "Time-shifting, energy conservation"),
                                        tags$b("State of Development:"),
                                            p(class = "cardText",
                                                "Perhaps the oldest and most mature constructed storage technology, insulation techniques are undergoing constant 
                                                research an improvement to maximize their ability to thermally seal building envelopes."),
                                        tags$b("Advantages:"),
                                            tags$li(class = "cardText", "Most cost-effective mode of energy storage"),
                                            tags$li(class = "cardText last", "Reduces total energy use and associated externalities"),
                                        tags$b("Disadvantages:"),
                                            tags$li(class = "cardText", "Stored energy is not dispatchable as electric power"), 
                                            tags$li(class = "cardText last", "The marginal cost of energy efficiency upgrades increases while the marginal benefit decreases"),
                                        tags$b("Variations/Advances:"),
                                            p(class = "cardText",
                                                "The largest sources of heat loss in buildings are doors and windows, so much of the recent advances in insulation 
                                                technology focus on these features, including double- and triple-pane glass and specialized coatings to reduce heat loss.")
                                    )
                                )} # Text Card
                            ), # Left Column Text Card
                            div(class = "column imageColumn",
                                {div(class = "imageCard",
                                     div(class = "image_box",
                                         conditionalPanel(condition = "input.thermalEnvelopeImage == 'thermalEnvelopeImage1'",
                                                          tags$img(class = "thermalEnvelope", id = "thermalEnvelopeImage1", src = "thermalEnvelope1.jpg", style = "width: 100%; margin-top:15px;")),
                                         conditionalPanel(condition = "input.thermalEnvelopeImage == 'thermalEnvelopeImage2'",
                                                          tags$img(class = "thermalEnvelope", id = "thermalEnvelopeImage2", src = "thermalEnvelope2.jpg", style = "width: 94%; margin-left:10px;")),
                                         conditionalPanel(condition = "input.thermalEnvelopeImage == 'thermalEnvelopeImage3'",
                                                          tags$img(class = "thermalEnvelope zoom", id = "thermalEnvelopeImage3", src = "thermalEnvelope3.jpg", style = "width: 68%; margin-left:65px;"))
                                     ),
                                     
                                     #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     div(class = "imgRadio",
                                         radioGroupButtons(inputId = "thermalEnvelopeImage",
                                                           label = NULL, 
                                                           choiceValues = c("thermalEnvelopeImage1", "thermalEnvelopeImage2", "thermalEnvelopeImage3"), 
                                                           choiceNames = c("", "", ""),
                                                           size = "sm", selected = "thermalEnvelopeImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                                )}, # Image Card
                                {div(class = "captionCard",
                                     conditionalPanel(condition = "input.thermalEnvelopeImage == 'thermalEnvelopeImage1'",
                                                      p(class = "captionText",
                                                        strong("Thermal Envelope of a Residential Building"), br(),
                                                        "The thermal envelope of a building, shown above in red, is the enclosure around all of the internal livable and conditioned space
                                                        in the building. Proper insulation of the thermal envelope improves the building's ability to store thermal energy in the form of
                                                        warm or cool air and reduce energy consumption.")),
                                     conditionalPanel(condition = "input.thermalEnvelopeImage == 'thermalEnvelopeImage2'",
                                                      p(class = "captionText",
                                                        strong("Heat Map of a Home's Thermal Envelope"), br(),
                                                        "Using thermal imaging equipment, it is possible to assess the thermal envelope, essentially creating a map of the strengths and 
                                                        weaknesses of the envelope. Using this map, homeowners and businesses can target improvements to maximize their impacts on building 
                                                        insulation and energy storage capacity.")),
                                     conditionalPanel(condition = "input.thermalEnvelopeImage == 'thermalEnvelopeImage3'",
                                                      p(class = "captionText",
                                                        strong("Strategies for Improving Thermal Envelope Insulation"), br(),
                                                        "Ome of the most common weaknesses of buildings' thermal envelopes are windows. It is far easier to add several inches of opaque foam
                                                        insulation to a wall, but the same strategy does not apply to doors or windows. Instead, other strategies are used, such as using multiple
                                                        panes of low-emissivity (Low-E) glass separated by inert, low-conductivity gases."))
                                )}  # Caption Card
                            ) # Right Column with Images and Captions
                        )
                    )} # Thermal Envelopes (Building Insulation)
                        
                )}, # Thermal
                {div(
                    {hidden(
                        div(class = "row ESTechPanel", id = "H2",
                            div(class = "column textColumn",
                                {div(class = "textCard", style = "overflow-y:scroll;",
                                    p(tags$b("Hydrogen",
                                             tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX5-1")),
                                        hr(style = "border-top:1px solid #999999; margin:5px;"),
                                        tags$b("How does it work?"),
                                            p(class = "cardText",
                                                "Most hydrogen is currently produced through steam-methane reforming, in chich steam and methane are made to 
                                                react in the presence of a nickel catalyst. Other methods involve electrolysis (splitting water molecules) and
                                                biomass gasification. Once hydrogen is made and stored, it is typically consumed and converted to electrical
                                                energy by a fuel cell. Fuel cells function similarly to flow batteries, wherein hydrogen gas contacts the
                                                negative anode and splits into two hydrogen ions and two electrons. The hydrogen ions pass through the electrolyte,
                                                while the electrons are conveyed across external circuits. when the electrons reenter the cell in the positive 
                                                cathode, they react with oxygen and the hydrogen ions to form water molecules."), 
                                        tags$b("Common Applications:"),
                                            p(class = "cardText",
                                                "Hydrogen fuel cell vehicles, Space travel, potential for backup power or remote power applications"),
                                        tags$b("State of Development:"),
                                            p(class = "cardText",
                                                "Hydrogen fuel cells are not a new technology, having been first developed in the early 19th century. However, the use of
                                                hydrogen as a carbon-free fuel source and energy storage technology has taken on new interest recently. Most significantly,
                                                hydrogen has emerged as a promising way to store vast amounts of energy generated from nuclear power plants, providing versatility
                                                to an otherwise fairly inflexible energy resource."),
                                        tags$b("Advantages:"),
                                            tags$li(class = "cardText", "Highly portable"),
                                            tags$li(class = "cardText", "More rapidly rechargeable/refillable than batteries"),
                                            tags$li(class = "cardText last", "Potential for carbon-free fuel"),
                                        tags$b("Disadvantages:"),
                                            tags$li(class = "cardText", "Uses methane / natural gas in most common synthesis methods"), 
                                            tags$li(class = "cardText", "Storage challenges"),
                                            tags$li(class = "cardText", "Low energy density by volume"),
                                            tags$li(class = "cardText last", "Flammability / explosivity"),
                                        tags$b("Variations/Advances:"),
                                            p(class = "cardText",
                                                "Much of the recent research on hydrogen energy storage seeks to address one of the more significant disadvantages 
                                                with the technology, storage of hydrogen gas. Some of the options under exploration include liquid hydrogen and 
                                                cryogenic storage, metal hydride complexes, and metal-organic frameworks (MOFs), among many others.
                                                ")
                                    )
                                )} # Text Card
                            ), # Left Column Text Card
                            div(class = "column imageColumn",
                                {div(class = "imageCard", style = "height:400px;", 
                                     div(class = "image_box",
                                         conditionalPanel(condition = "input.H2Image == 'H2Image1'",
                                                          tags$img(class = "H2 zoom", id = "H2Image1", src = "H2-1c.png", style = "width: 100%; margin-top: 15px; background-color: white;")),
                                         conditionalPanel(condition = "input.H2Image == 'H2Image2'",
                                                          tags$img(class = "H2 zoom", id = "H2Image2", src = "H2-2.png", style = "width: 100%; margin-top: 2px; background-color: white;")),
                                         conditionalPanel(condition = "input.H2Image == 'H2Image3'",
                                                          tags$img(class = "H2 zoom", id = "H2Image3", src = "H2-3.jpg", style = "width: 100%; margin-top: 50px;"))
                                     ),
                                     
                                     #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     div(class = "imgRadio", style = "padding-top: 365px;",
                                         radioGroupButtons(inputId = "H2Image",
                                                           label = NULL, 
                                                           choiceValues = c("H2Image1", "H2Image2", "H2Image3"), 
                                                           choiceNames = c("", "", ""),
                                                           size = "sm", selected = "H2Image1", direction = "horizontal", individual = TRUE, width = "100px"))
                                )}, # Image Card
                                {div(class = "captionCard", style = "height:160px;",
                                     conditionalPanel(condition = "input.H2Image == 'H2Image1'",
                                                      p(class = "captionText",
                                                        strong("Hydrogen Gas Synthesis through Methane Gas Reforming"), br(),
                                                        "The vast majority of the world's synthetic hydrogen gas is manufactured through the methane gas reforming process. This is generally
                                                        viewed critically by advocates of clean energy and emissions reduction since it requires a carboniferous fuel and carbon emissions even 
                                                        though hydrogen itself has no carbon emissions.")),
                                     conditionalPanel(condition = "input.H2Image == 'H2Image2'",
                                                      p(class = "captionText",
                                                        strong("Storage of Hydrogen Gas"), br(),
                                                        "A key challenge associated with hydrogen as a fuel and energy storage medium is the storage of the gas itself. Most physical methods 
                                                        have poor energy density and flammability concerns, while material-based storage methods are still in early stages of development.")),
                                     conditionalPanel(condition = "input.H2Image == 'H2Image3'",
                                                      p(class = "captionText",
                                                        strong("Diagram of a Hydrogen Fuel Cell"), br(),
                                                        "Hydrogen duel cells function similarly to a flow battery, but with one-directional flow of material. Hydrogen and oxygen are fed into 
                                                        the cell, and a chemical reaction creates electrical potential between the electrodes, with water being the only output from the process."))
                                )}  # Caption Card
                            ) # Right Column with Images and Captions
                    ))}, # Hydrogen
                        
                    {hidden(
                        div(class = "row ESTechPanel", id = "NH3",
                            div(class = "column textColumn",
                                {div(class = "textCard", style = "overflow-y:scroll;",
                                    p(tags$b("Ammonia",
                                             tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX5-2")),
                                        hr(style = "border-top:1px solid #999999; margin:5px;"),
                                        tags$b("How does it work?"),
                                            p(class = "cardText",
                                                "Ammonia is manufactured by combining hydrogen and nitrogen gases at high temperature and pressure 
                                                through a method known as the Haber-Bosch process, which is commonly used to make fertilizers. The
                                                hydrogen used in this process can come either from methane reforming or electrolysis of water.
                                                Ammonia can be stored more easily, densely, and safely than hydrogen gas, but can readily convert back to 
                                                hydrogen when needed. Ammonia can be 'cracked' by a metal catalyst to reform hydrogen gas and nitrogen. 
                                                This mixture, known as 'forming gas' can be employed to power hydrogen fuel cells, among many other uses.
                                                Ammonia can also be used directly in a combustion engine, but the engine must be modified due to different
                                                combustion characteristics of ammonia from other common fuels."), 
                                        tags$b("Common Applications:"),
                                            p(class = "cardText",
                                                "Hydrogen fuel cells, remote backup power, long-term energy storage"),
                                        tags$b("State of Development:"),
                                            p(class = "cardText",
                                                "Mature technology"),
                                        tags$b("Advantages:"),
                                            tags$li(class = "cardText", "Higher boiling point than hydrogen, easier to store in liquid state"),
                                            tags$li(class = "cardText", "Higher energy density than hydrogen when stored"),
                                            tags$li(class = "cardText last", "Lower risk of fire and explosion due to presence of nitrogen"),
                                        tags$b("Disadvantages:"),
                                            tags$li(class = "cardText", "Haber-Bosch Process uses immense amount of energy"), 
                                            tags$li(class = "cardText last", "Challenging to produce on large scale without fossil fuel use or carbon emissions"),
                                        tags$b("Variations/Advances:"),
                                            p(class = "cardText",
                                                "Much of the research on ammonia energy storage focuses on the chemical reactions involved in formation and
                                                consumption of the ammonia. These efforts include less energy-intensive methods for the Haber-Bosch synthesis 
                                                of ammonia and ammonia-cracking techniques using low-cost metal oxide catalysts.")
                                     )
                                )} # Text Card
                            ), # Left Column Text Card
                            div(class = "column imageColumn",
                                {div(class = "imageCard", style = "height:400px;", 
                                     div(class = "image_box",
                                         conditionalPanel(condition = "input.NH3Image == 'NH3Image1'",
                                                          tags$img(class = "NH3 zoom", id = "NH3Image1", src = "NH3-1a.png", style = "width: 100%; background-color: white;")),
                                         conditionalPanel(condition = "input.NH3Image == 'NH3Image2'",
                                                          tags$img(class = "NH3", id = "NH3Image2", src = "NH3-2.png", style = "width: 100%; padding-top: 40px;")),
                                         conditionalPanel(condition = "input.NH3Image == 'NH3Image3'",
                                                          tags$img(class = "NH3", id = "NH3Image3", src = "NH3-3.jpg", style = "width: 100%; padding-top:30px;"))
                                     ),
                                     
                                     #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     div(class = "imgRadio", style = "padding-top: 365px;",
                                         radioGroupButtons(inputId = "NH3Image",
                                                           label = NULL, 
                                                           choiceValues = c("NH3Image1", "NH3Image2", "NH3Image3"), 
                                                           choiceNames = c("", "", ""),
                                                           size = "sm", selected = "NH3Image1", direction = "horizontal", individual = TRUE, width = "100px"))
                                )}, # Image Card
                                {div(class = "captionCard", style = "height:160px;", 
                                     conditionalPanel(condition = "input.NH3Image == 'NH3Image1'",
                                                      p(class = "captionText", 
                                                        strong("Synthesis of Ammonia through the Haber-Bosch Process"), br(),
                                                        "Ammonia is made through the Haber-Bosch process from nitrogen and hydrogen gases. It involves extremely high temperatures and pressure, 
                                                        and is responsible for using 3-5 percent of the world's natural gas consumption and 1-2 percent of the global energy supply.")),
                                     conditionalPanel(condition = "input.NH3Image == 'NH3Image2'",
                                                      p(class = "captionText",
                                                        strong("Potential Application of Ammonia as a Carbon-Free Fuel"), br(),
                                                        "Ammonia as a fuel can be used through either a fuel cell (by converting to hydrogen) or a combustion engine. Gasoline engines must be 
                                                        modified due to different combustion characteristics of ammonia. Advocates promote ammonia as an alternative carbon-free fuel and storage
                                                        medium in vehicles for which batteries are ill-suited, such as cargo ships and air travel.")),
                                     conditionalPanel(condition = "input.NH3Image == 'NH3Image3'",
                                                      p(class = "captionText",
                                                        strong("Ammonia Energy Storage Research at WCROC in Morris, MN"), br(),
                                                        "Researchers at the West Central Research and Outreach Center (WCROC) in Morris, Minnesota work on innovating the production and use of ammonia
                                                        as a fuel and storage medium for agricultural applications. This involves production via a wind-to-ammonia process and use as both a fertilizer and
                                                        fuel for farm equipment."))
                                )}  # Caption Card
                            ) # Right Column with Images and Captions
                        )
                    )}, # Ammonia
                        
                    {hidden(
                        div(class = "row ESTechPanel", id = "coal",
                            div(class = "column textColumn",
                                {div(class = "textCard", style = "overflow-y:scroll;",
                                    p(tags$b("Coal",
                                             tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX5-3")),
                                        hr(style = "border-top:1px solid #999999; margin:5px;"),
                                        tags$b("How does it work?"),
                                            p(class = "cardText",
                                                "Coal is a readily combustible rock with a composition rich in carbon, mostly in the form of complex
                                                hydrocarbons. Energy is stored in the form of the chemical bonds in the hydrocarbon compounds. When
                                                coal is burned, these bonds are broken, and water and carbon dioxide are formed from the disconnected
                                                atoms, releasing the stored energy. Different forms of coal (i.e. Anthracite, Bituminous, Lignite) are 
                                                classified by their carbon composition, which affects their physical properties and energy capacity."), 
                                        tags$b("Common Applications:"),
                                            p(class = "cardText",
                                                "'Baseload' power generation, dispatchable/reserve power, metallurgy/steel production"),
                                        tags$b("State of Development:"),
                                            p(class = "cardText",
                                                "Mature technology"),
                                        tags$b("Advantages:"),
                                            tags$li(class = "cardText", "Dispatchable power resource"),
                                            tags$li(class = "cardText last", "Until recently the cheapest energy resource"),
                                        tags$b("Disadvantages:"),
                                            tags$li(class = "cardText", "Very high in carbon dioxide emissions"),
                                            tags$li(class = "cardText", "Criteria pollutant emissions"), 
                                            tags$li(class = "cardText", "Mercury Emissions"), 
                                            tags$li(class = "cardText", "Land use and extraction environmental concerns (mountaintop removal)"), 
                                            tags$li(class = "cardText", "Coal ash storage and disposal"), 
                                            tags$li(class = "cardText last", "Not a 'rechargeable' storage resource"),
                                        tags$b("Variations/Advances:"),
                                            p(class = "cardText",
                                                "Ongoing efforts have sought to reduce the pollution caused by coal-fired electricity generation. These
                                                include sourcing low-sulfur coal to reduce acid rain formation, installing 'scrubbers' to reduce particulate
                                                matter pollution and other criteria pollutants, and carbon capture and storage (CCS) to sequester carbon 
                                                dioxide before it is released into the atmosphere.")
                                     )
                                )} # Text Card
                            ), # Left Column Text Card
                            div(class = "column imageColumn",
                                {div(class = "imageCard",
                                     div(class = "image_box",
                                         conditionalPanel(condition = "input.coalImage == 'coalImage1'",
                                                          tags$img(class = "coal zoom", id = "coalImage1", src = "coal1.png", style = "width: 100%; margin-top: 40px;")),
                                         conditionalPanel(condition = "input.coalImage == 'coalImage2'",
                                                          tags$img(class = "coal zoom", id = "coalImage2", src = "coal2e.png", style = "width: 100%; background-color: white; margin-top: 20px;")),
                                         conditionalPanel(condition = "input.coalImage == 'coalImage3'",
                                                          tags$img(class = "coal", id = "coalImage3", src = "coal3d.png", style = "width: 100%"))
                                     ),
                                     
                                     #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     div(class = "imgRadio",
                                         radioGroupButtons(inputId = "coalImage",
                                                           label = NULL, 
                                                           choiceValues = c("coalImage1", "coalImage2", "coalImage3"), 
                                                           choiceNames = c("", "", ""),
                                                           size = "sm", selected = "coalImage1", direction = "horizontal", individual = TRUE, width = "100px"))
                                )}, # Image Card
                                {div(class = "captionCard",
                                     conditionalPanel(condition = "input.coalImage == 'coalImage1'",
                                                      p(class = "captionText",
                                                        strong("Map of Coal Resources in the United States"), br(),
                                                        "Coal reserves are distributed unevenly throughout the country in terms of quantity and quality (or type) of coal. It 
                                                        is worth noting that Minnesota does not have any coal reserves within the state's borders. Most coal used in Minnesota
                                                        is imported from Wyoming, while the state also imports electricity from North Dakota generated from coal mined in that state.")),
                                     conditionalPanel(condition = "input.coalImage == 'coalImage2'",
                                                      p(class = "captionText",
                                                        strong("The Four Types of Coal and Relative Characteristics"), br(),
                                                        "Coal can take a number of forms depending on the age and location of the deposit. In terms of energy storage, anthracite
                                                        has the greatest energy density, but bituminous and subbituminous coal are more commonly used for electricity generation. Each
                                                        type of coal differs in hardness, energy density, and carbon content, and has various levels of impurities such as sulfur compounds
                                                        or heavy metals which can pollute air and water resources when the coal is burned.")),
                                     conditionalPanel(condition = "input.coalImage == 'coalImage3'",
                                                      p(class = "captionText",
                                                        strong("Challenges with Disposal of Coal Ash"), br(),
                                                        "An emerging concern with the use of coal (in addition to GHGs and other pollutants) is the treatment and disposal of coal ash.
                                                        The carcinogenic byproduct of coal combustion has high concentrations of toxic metals such as mercury, cadmium, and arsenic, and 
                                                        is often stored in artificial ponds, which can leak and pollute ecologically sensitive waterways."))
                                )}  # Caption Card
                            ) # Right Column with Images and Captions
                        )
                    )}, # Coal
                        
                    {hidden(
                        div(class = "row ESTechPanel", id = "CH4",
                            div(class = "column textColumn",
                                {div(class = "textCard",
                                    p(tags$b("Natural Gas",
                                             tags$i(class = "fa fa-times", style = "font-size:16px;", id = "ESTX5-4")),
                                        hr(style = "border-top:1px solid #999999; margin:5px;"),
                                        tags$b("How does it work?"),
                                            p(class = "cardText",
                                                "Natural gas is made up predominantly of methane, which, like coal, stores energy in the form of
                                                carbon-hydrogen chemical bonds. When methane is burned, carbon dioxide and water are formed, 
                                                releasing energy in the form of heat, which can be converted into electrical energy through the
                                                use of a steam turbine."), 
                                        tags$b("Common Applications:"),
                                            p(class = "cardText",
                                                "Dispatchable energy generation; baseload, intermediate, and peak generation; space heating; natural 
                                                gas-powered vehicles; industrial use"),
                                        tags$b("State of Development:"),
                                            p(class = "cardText",
                                                "Mature Technology"),
                                        tags$b("Advantages:"),
                                            tags$li(class = "cardText", "Lower carbon dioxide emissions than coal"),
                                            tags$li(class = "cardText", "Low particulate matter pollution"),
                                            tags$li(class = "cardText last", "Inexpensive energy resource"),
                                        tags$b("Disadvantages:"),
                                            tags$li(class = "cardText", "Carbon dioxide emissions"),
                                            tags$li(class = "cardText", "Pipeline infrastructure for transportation"),
                                            tags$li(class = "cardText", "Extraction process (i.e. hydraulic fracturing) and land-use concerns"),
                                            tags$li(class = "cardText last", "Methane emissions from natural gas leaks"),
                                        tags$b("Variations/Advances:"),
                                            p(class = "cardText",
                                                "Renewable natural gas (RNG), methane derived primarily from agricultural waste, is emerging as a potential
                                                substitute for extracted natural gas. Natural gas utility CenterPoint Energy has launched a pilot
                                                program in Minnesota to provide renewable natural gas to customers who pay a small fee to cover the
                                                gap in costs between RNG and conventional gas.")
                                     )
                                )} # Text Card
                            ), # Left Column Text Card
                            div(class = "column imageColumn",
                                {div(class = "imageCard",
                                     div(class = "image_box",
                                         conditionalPanel(condition = "input.CH4Image == 'CH4Image1'",
                                                          tags$img(class = "CH4 zoom", id = "CH4Image1", src = "CH4-1.png", style = "width: 100%; margin-top: 15px;")),
                                         conditionalPanel(condition = "input.CH4Image == 'CH4Image2'",
                                                          tags$img(class = "CH4 zoom", id = "CH4Image2", src = "CH4-2a.png", style = "width: 100%; margin-top: 20px;")),
                                         conditionalPanel(condition = "input.CH4Image == 'CH4Image3'",
                                                          tags$img(class = "CH4", id = "CH4Image3", src = "CH4-3b.png", style = "width: 100%; margin-top:25px;"))
                                     ),
                                     
                                     #tags$span(class = "fa fa-angle-left", style = "position: absolute; margin: -150px 0 0 7.5px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     #tags$span(class = "fa fa-angle-right", style = "position: absolute; margin: -150px 0 0 440px; z-index:1; font-size: 30px; font-weight: bold; cursor: pointer;"),
                                     div(class = "imgRadio",
                                         radioGroupButtons(inputId = "CH4Image",
                                                           label = NULL, 
                                                           choiceValues = c("CH4Image1", "CH4Image2", "CH4Image3"), 
                                                           choiceNames = c("", "", ""),
                                                           size = "sm", selected = "CH4Image1", direction = "horizontal", individual = TRUE, width = "100px"))
                                )}, # Image Card
                                {div(class = "captionCard",
                                     conditionalPanel(condition = "input.CH4Image == 'CH4Image1'",
                                                      p(class = "captionText",
                                                        strong("Map of Natural Gas Resources in the United States"), br(),
                                                        "The distribution of natural gas production in the United States is similar to that of coal, since many of the same conditions promote
                                                        their formation. Production is heaviest in Texas, Oklahoma, and Appalachia, while Minnesota does not have any known natural gas reserves.")),
                                     conditionalPanel(condition = "input.CH4Image == 'CH4Image2'",
                                                      p(class = "captionText",
                                                        strong("Price Trends in the Spot Market for Natural Gas"), br(),
                                                        "Domestic natural gas production rose sharply in the 00's as new technological development allowed extraction of shale shale gas through 
                                                        hydraulic fracturing. Natural gas prices initially rose to offset the higher cost of extraction, before falling in the 2010's. Abundant 
                                                        and inexpensive natural gas has spurred a rapid expansion of natural gas-powered electricity generation across the country.")),
                                     conditionalPanel(condition = "input.CH4Image == 'CH4Image3'",
                                                      p(class = "captionText",
                                                        strong("Natural Gas Flaring in the Bakken Oil Fields, North Dakota"), br(),
                                                        "Low natural gas prices have in some cases made collection of the fuel uneconomical. The image above depicts a satellite view of the United 
                                                        States at night, highlighting the Bakken Oil Fields in western North Dakota, which appears similar to major metropolitan areas in terms of light 
                                                        emission. However, this light is produced by flaring or burning off natural gas as it comes of the well, since it would cost more to collect 
                                                        the gas than it would be worth."))
                                )}  # Caption Card
                            ) # Right Column with Images and Captions
                        )
                    )} # Natural Gas
                        
                )}  # Chemical
            )
        )}, # Energy Storage Technologies
        {hidden(
            div(class = "column main intropage", id = "Intro-4",
                {div(
                    p(class = "section-header", 
                        "General Objectives of Energy Storage Use Cases"),
                    hr(style = "margin:10px;"),
                    {div(style = "margin:20px 10px;",
                         
                        {div(class = "row useCaseRow",
                             
                            div(class = "useCaseIntroBox", style = "padding:0 5px;",
                                tags$img(src = "MISOLoad3.png", style = "width: 100%;"),
                                div(class = "bold", style = "position:absolute; width:100%; top:168px; left:325px; color:black; font-size:14px;",
                                    "MISO North Region - Hourly Load Profile, 2016")
                            ),
                                
                            div(class = "useCaseIntroBox",
                                p(class = "center bold", style = "font-size:18px; color: #7a0019;",
                                    tags$i(class = "fa fa-angle-double-left"),
                                    "Efficiency"),
                                p(class = "twelvePt indent",
                                    "Shifting energy use from one time to another allows ratepayers and utilities to mitigate peak load events. This benefits the utility by reducing the
                                    generation fleet required to meet peak demand, and reduces the need for many highly polluting generation resources. For ratepayers, energy storage use
                                    that benefits their utility may be encouraged and rewarded through rate designs such as time-of-use rates or demand charges."),
                                p(class = "twelvePt indent",
                                    "Reducing energy use for just a small fraction of the total hours in the year has the potential to save utilities and ratepayers hundreds of millions 
                                    of dollars. The figure to the left depicts the fraction of yearly peak load that is comprised of just the top five, ten, and fifteen percent of all 
                                    hours in the year, by load. Mitigation may require widespread coordination of energy storage capacity targeting these events.")
                            )
                        )}, # End of First Row - Efficiency
                            br(),   
                        {div(class = "row useCaseRow",     
                            div(class = "useCaseIntroBox",
                                p(class = "center bold", style = "font-size:18px; color: #7a0019;",
                                    "Stability",
                                    tags$i(class = "fa fa-angle-double-right")
                                ),
                                p(class = "twelvePt indent",
                                    "Grid stability refers to the grid's ability to provide customers with consistent, on-demand power with stable voltage and frequency. This involves 
                                    withstanding rapid changes to load and generation, as well as fluctuations to voltage and reactive power. For example, differences between generation
                                    and load can lead to frequency variation, which has the potential to damage equipment and jeopardize electric service to customers. The ability to
                                    properly balance demand with load is required to maintain a consistent frequency and proper grid stability."),
                                p(class = "twelvePt indent",
                                    "Energy storage can be employed to promote grid stability through a number of use cases, including frequency regulation, voltage support, and ramping/peaking.
                                    These are typically provided on the transmission grid level and provide value primarily to the regional grid operator or utility.")
                            ),
                            
                            div(class = "useCaseIntroBox",
                                tags$img(src = "ControlCenter.jpg", style = "width: 100%;"),
                                div(class = "bold", style = "position:absolute; width:100%; top:520px; left:725px; color:white; font-size:16px;", 
                                    "MISO Control Center")
                            )
                        )}, # End of Second Row - Stability
                            br(),
                        {div(class = "row useCaseRow",
                            div(class = "useCaseIntroBox",
                                tags$img(src = "blackoutSat2.png", style = "width: 100%;"),
                                div(class = "bold", style = "position:absolute; width:100%; top:855px; left:360px; color:white; font-size:16px;", 
                                    "Northeast Blackout of 2003")
                            ),
                            
                            div(class = "useCaseIntroBox",
                                p(class = "center bold", style = "font-size:18px; color: #7a0019;",
                                    tags$i(class = "fa fa-angle-double-left"),
                                    "Resiliency"
                                ),
                                p(class = "twelvePt indent",
                                    "Energy storage can also provide resilience to grid interruptions and blackouts and aid recovery after these events. Blackouts are frequently caused 
                                    or exacerbated by transmission congestion during peak load events. The Northeast Blackout of 2003, the largest in American history, affecting 55 
                                    million people, is believed to have been caused in part by overloaded transmission lines which slumped into vegetation and shut down. Power service was 
                                    rerouted through other corridors, which also subsequently shut down due to increased congestion."),
                                p(class = "twelvePt indent",
                                    "Energy storage can mitigate the effects of widespread outages like this blackout by reducing congestion on the transmission grid, continuing
                                    to provide power to customers during the outage, and assisting with grid recovery efforts.")
                            )
                        )}  # End of Third Row - Resiliency
                        
                    )}, # Use Case Objectives Intro
                    
                    br(),
                    p(class = "section-header",
                        "Energy Storage Use Cases"),
                    hr(style = "margin:10px;"),
                    div(style = "width:840px; min-width = 840px; max-width = 840px; margin-top:0; padding-top:0;",
                        p(class = "center",
                            tags$i(class = "fa fa-caret-left"), 
                            "Select a use case from the image below to view more information", 
                            tags$i(class = "fa fa-caret-right")
                        )
                    )
                )}, # Top Half of Use Case Page with Intro
                
                {div(
                    tags$img(style = "margin-left:50px;", src = "RMI-UseCase2.png", style = "min-width: 780px; max-width:780px;"),
                    {div(
                        div(class = "trapezoid", id = "util-2", style = "transform:rotate( 18deg);   top:1797px; left:486px; width:174px; border-left: 20px solid transparent; border-right: 20px solid transparent;"),
                        div(class = "trapezoid", id = "util-1", style = "transform:rotate( 48deg);   top:1730px; left:395px; width:132px; border-left: 16px solid transparent; border-right: 16px solid transparent;"),
                        div(class = "trapezoid", id = "cust-4", style = "transform:rotate( 76deg);   top:1626px; left:336px; width:143px; border-left: 16px solid transparent; border-right: 18px solid transparent;"),
                        div(class = "trapezoid", id = "cust-3", style = "transform:rotate(105deg);   top:1502px; left:336px; width:147px; border-left: 17px solid transparent; border-right: 18px solid transparent;"),
                        div(class = "trapezoid", id = "cust-2", style = "transform:rotate(133deg);   top:1394px; left:398px; width:142px; border-left: 17px solid transparent; border-right: 18px solid transparent;"),
                        div(class = "trapezoid", id = "cust-1", style = "transform:rotate(164deg);   top:1329px; left:499px; width:160px; border-left: 18px solid transparent; border-right: 20px solid transparent;"),
                        div(class = "trapezoid", id = "grid-1", style = "transform:rotate(194deg);   top:1322px; left:635px; width:127px; border-left: 14px solid transparent; border-right: 19px solid transparent;"),
                        div(class = "trapezoid", id = "grid-2", style = "transform:rotate(217deg);   top:1367px; left:736px; width:117px; border-left: 15px solid transparent; border-right: 14px solid transparent;"),
                        div(class = "trapezoid", id = "grid-3", style = "transform:rotate(239deg);   top:1436px; left:808px; width:101px; border-left: 11px solid transparent; border-right: 11px solid transparent;"),
                        div(class = "trapezoid", id = "grid-4", style = "transform:rotate(259deg);   top:1519px; left:839px; width:103px; border-left: 12px solid transparent; border-right: 12px solid transparent;"),
                        div(class = "trapezoid", id = "grid-5", style = "transform:rotate(284.5deg); top:1627px; left:808px; width:149px; border-left: 18px solid transparent; border-right: 18px solid transparent;"),
                        div(class = "trapezoid", id = "util-4", style = "transform:rotate(313deg);   top:1736px; left:754px; width:140px; border-left: 18px solid transparent; border-right: 16px solid transparent;"),
                        div(class = "trapezoid", id = "util-3", style = "transform:rotate(344deg);   top:1801px; left:633px; width:162px; border-left: 21px solid transparent; border-right: 20px solid transparent;")
                    )} # Trapezoid Buttons
                )}, # RMI Use Case Figure with Buttons
                div(
                    {div(
                        {hidden(
                            div(class = "useCasePanel", id = "backupPower",
                                div(class = "useCaseTitle RMI_orange",
                                    "Backup Power / Resiliency",
                                    tags$i(class = "fa fa-times", id = "UCX-1")
                                ),
                                div(class = "row UseCasePanel",
                                    {div(class = "column", style = "padding-left:15px; height:450px;",
                                        div(class = "useCaseImageCard", style = "height:460px;",
                                            div(style = "width:380px; background-color:white; padding: 5px 0;",
                                                p(class = "center bold", "Effects of Power Outages on Customer Power Use")),
                                            tags$img(src = "BackupPower4.png", style = "width: 100%; margin-top:0;")
                                        )
                                    )}, # Left Image Card
                                    {div(class = "column", style = "padding-left:0; height:460px;",
                                        div(class = "useCaseTextCard", style = "height:460px;",
                                            tags$b("Typical User:"),
                                                p(class = "cardText", "Residential, Commercial, and Industrial Customers"),
                                            tags$b("Siting Location:"),
                                                p(class = "cardText","Customer-sited, behind the meter"),
                                            tags$b("Common Technologies:"),
                                                p(class = "cardText", "Batteries (Lead Acid, Lithium Ion, Redox Flow), Gasoline/Diesel Fuel"),
                                            tags$b("Power vs. Energy Favored:"),
                                                p(class = "cardText", "Energy capacity (long duration)"),
                                            tags$b("How Does it Work?"),
                                                p(class = "cardText",
                                                    "Energy storage devices can be employed to provide power in the event of a power outage. This function has
                                                    the potential to replace or reduce the use of petroleum-powered generators, improving carbon and criterion
                                                    pollutant emissions. During outages, homes and businesses with on-site solar generationare unable to continue
                                                    to generate electricity due to power quality and utility line-worker safety concerns. When paired with energy
                                                    storage, however, the panels are able to function if cut off from the grid, powering the home or business and
                                                    recharging the battery, mitigating the effects of the outage (See figure on left)."),
                                            tags$b("Monetization/Value Creation:"),
                                                p(class = "cardText", 
                                                    "No direct monetizable value for residential or commercial customers. However, customers are able to avoid the
                                                    lost value that would have occurred if they were to experience the unmitigated outage, whether that is lost
                                                    revenue or simply comfort and enjoyment.")
                                        )
                                    )}  # Right Text Card
                                )
                            )
                        )}, # Backup Power
                        {hidden(
                            div(class = "useCasePanel", id = "pvFirm",
                                div(class = "useCaseTitle RMI_orange",
                                    "Increasing PV Self-Consumption",
                                    tags$i(class = "fa fa-times", id = "UCX-2")
                                ),
                                div(class = "row UseCasePanel",
                                    {div(class = "column", style = "padding-left:15px; height:530px;",
                                        div(class = "useCaseImageCard", style = "height: 530px; padding-top:10px;",
                                            div(style = "width:380px; background-color:white; padding: 5px 0 0.1px;",
                                                p(class = "center bold", "Solar Optimization")),
                                             tags$img(src = "pvFirm5.png", style = "width: 100%;")
                                        )
                                    )}, # Left Image Card
                                    {div(class = "column", style = "padding-left:0; height:530px;",
                                        div(class = "useCaseTextCard", style = "height:530px;",
                                            tags$b("Typical User:"),
                                                p(class = "cardText", "Residential, Commercial, or Industrial customers with on-site solar generation."),
                                            tags$b("Siting Location:"),
                                                p(class = "cardText", "Customer-sited, behind the meter"),
                                            tags$b("Common Technologies:"),
                                                p(class = "cardText", "Batteries (Lead Acid, Lithium Ion, Redox Flow), Hydrogen Fuel Cells"),
                                            tags$b("Power vs. Energy Favored"),
                                                p(class = "cardText", "Energy"),
                                            tags$b("How does it work?"),
                                                p(class = "cardText",
                                                    "When utility customers with behind-the-meter solar generation are making more electricity than they are
                                                    using, the excess is typically returned to the grid. Alternatively, this energy can be stored on-site
                                                    until the customer is using electricity than they are generating. Then, it can be consumed directly,
                                                    instead of buying power back from the grid. (See 'Optimization of Solar Generation' under 'Use Case
                                                    Examples' for more detail.)"),
                                            tags$b("Monetization/Value Creation:"),
                                                p(class = "cardText",
                                                    "Customers can save money on their electric bills if their rate structure is set up so they sell power
                                                    back to the grid at a lower rate than they buy it at retail. When energy storage owners are able to
                                                    store energy generated by their solar panels and use it rather than selling it to the utility and buying
                                                    it back at a higher rate, their net bill from the utility will decrease.")
                                        )
                                    )}  # Right Text Card
                                )
                            )
                        )}, # PV Self Consumption
                        {hidden(
                            div(class = "useCasePanel", id = "demandMgmt",
                                div(class = "useCaseTitle RMI_orange",
                                    "Demand-Charge Management",
                                    tags$i(class = "fa fa-times", id = "UCX-3")
                                ),
                                div(class = "row UseCasePanel",
                                    {div(class = "column", style = "padding-left:15px; height:400px;",
                                        div(class = "useCaseImageCard",
                                            tags$img(src = "demandMgmt8.png", style = "width: 100%; margin-top:38px; background-color: white;")
                                        )
                                    )}, # Left Image Card
                                    {div(class = "column", style = "padding-left:0; height:400px;",
                                        div(class = "useCaseTextCard", style = "overflow-y:scroll;",
                                            tags$b("Typical User:"),
                                                p(class = "cardText", "Mostly commercial and industrial customers, some residential."),
                                            tags$b("Siting Location"),
                                                p(class = "cardText", "Behind the Meter"),
                                            tags$b("Common Technologies:"),
                                                p(class = "cardText", "Batteries, Flywheels, Supercapacitors"),
                                            tags$b("Power vs. Energy Favored:"),
                                                p(class = "cardText", "Power"),
                                            tags$b("How Does it Work?"),
                                                p(class = "cardText",
                                                    "Most commercial and industrial customers' electric bills are comprised of usage and demand charges.
                                                    Usage charges account for the amount of energy that they have used in each month (measured in kWh).
                                                    Demand charges are assessed on a per-kilowatt-hour basis for the greatest 15-minute sustained load
                                                    throughout each month. Energy storage can smooth the customer's load profile by shifting energy 
                                                    consumption from the grid away from peak times. (See 'Demand Management' under 'Use Case Examples'
                                                    for greater detail and examples.)"),
                                            tags$b("Monetization/Value Creation:"),
                                                p(class = "cardText",
                                                    "Demand-metered customers can reduce their electricity bills by reducing their peak energy use events. 
                                                    Demand charges can make up a significant portion of commercial and industrial customers' total monthly
                                                    bills.")
                                        )
                                    )}  # Right Text Card
                                )
                            )
                        )}, # Demand Management
                        {hidden(
                            div(class = "useCasePanel", id = "touMgmt",
                                div(class = "useCaseTitle RMI_orange",
                                    "Time-of-Use Management",
                                    tags$i(class = "fa fa-times", id = "UCX-4")
                                ),
                                div(class = "row UseCasePanel",
                                    {div(class = "column", style = "padding-left:15px; height:400px;",
                                        div(class = "useCaseImageCard",
                                             tags$img(src = "touMgmt9.png", style = "width: 100%; margin-top:70px;")
                                        )
                                    )}, # Left Image Card
                                    {div(class = "column", style = "padding-left:0; height:400px;",
                                        div(class = "useCaseTextCard", style = "overflow-y:scroll;",
                                            tags$b("Typical User:"),
                                                p(class = "cardText", "Residential, Industrial, or Industrial Customers with Time-of-Use Rate Structures."),
                                            tags$b("Siting Location:"),
                                                p(class = "cardText", "Customer-sited, behind the meter"),
                                            tags$b("Common Technologies:"),
                                                p(class = "cardText", "Batteries (Lithium Ion, Redox Flow), Hot-Water/Ice Storage, Thermal Envelope Insulation"),
                                            tags$b("Power vs. Energy Favored:"),
                                                p(class = "cardText", "Energy"),
                                            tags$b("How Does it Work?"),
                                                p(class = "cardText",
                                                    "When employing time-of-use rate structures, utilities charge customers different rates for electricity
                                                    depending on when it is used. Peak hours in the late afternoon and evenings typically have much higher
                                                    electricity rates than off-peak hours in the early mornings, when demand is low. Customers can employ
                                                    energy storage to shift electricity consumption from high-cost hours to times with lower prices."),
                                            tags$b("Monetization/Value Creation:"),
                                                p(class = "cardText", 
                                                    "Customers can save money for each kilowatt-hour they are able to shift from peak to off-peak hours,
                                                    which they then purchase at a lower rate. The savings for each kilowatt-hour is the difference between
                                                    peak and off-peak prices")
                                        )
                                    )}  # Right Text Card
                                )
                            )
                        )} #  TOU Management
                    )}, # Customer-Serving Use Cases
                    
                    {div(
                        
                        {hidden(
                            div(class = "useCasePanel", id = "deferral",
                                div(class = "useCaseTitle RMI_blue",
                                    "Transmission and Distribution Deferral",
                                    tags$i(class = "fa fa-times", id = "UCX-5")
                                ),
                                div(class = "row UseCasePanel",
                                    {div(class = "column", style = "margin-left:5px; height:400px;",
                                        div(class = "useCaseTextCard",
                                            tags$b("Typical User:"),
                                                p(class = "cardText", "Primarily utilities"),
                                            tags$b("Siting Location:"),
                                                p(class = "cardText", "Transmission grid, Substations"),
                                             tags$b("Common Technologies:"),
                                                p(class = "cardText", "Batteries (Lithium Ion, Redox Flow)"),
                                            tags$b("Power vs. Energy Favored:"),
                                                p(class = "cardText", "Balanced"),
                                            tags$b("How Does it Work?"),
                                                p(class = "cardText", 
                                                    "Utilities must build and maintain transmission and distribution infrastructure with adequate capacity to handle peak load events.
                                                    This equipment must be periodically upgraded to accomodate increasing load and peak size. Energy storage deployed 
                                                    at strategic locations on the transmission and distribution grid can reduce the size and frequency of peak load events by smoothing the regional
                                                    demand curve, reducing strain on this equipment, extending its useful life, and allowing utilities to put off or avoid costly upgrades."),
                                            tags$b("Monetization/Value Creation:"),
                                                p(class = "cardText",
                                                    "If a utility is able to defer or avoid a distribution upgrade, it can potentially save several million dollars.
                                                    These savings and avoided utility expenses can be passed through to ratepayers through reduced electric rates.")
                                         )
                                    )}, # Left Text Card
                                    {div(class = "column", style = "padding-left:0; height:400px;",
                                         div(class = "useCaseImageCard",
                                             tags$img(src = "distDef7.png", style = "width: 100%; margin-top:35px;")
                                         )
                                    )}  # Right Image Card
                                )
                            )
                        )}, # Transmission and Distribution Deferral
                        {hidden(
                            div(class = "useCasePanel", id = "congRlf",
                                div(class = "useCaseTitle RMI_blue",
                                    "Transmission Congestion Relief",
                                    tags$i(class = "fa fa-times", id = "UCX-7")
                                ),
                                div(class = "row UseCasePanel",
                                    {div(class = "column", style = "margin-left:5px; height:400px;",
                                         div(class = "useCaseTextCard",
                                             tags$b("Typical User:"),
                                             p(class = "cardText", "Utilities, Third party energy companies"),
                                             tags$b("Siting Location:"),
                                             p(class = "cardText", "Transmission grid"),
                                             tags$b("Common Technologies:"),
                                             p(class = "cardText", "Batteries (Lithium Ion, Redox Flow)"),
                                             tags$b("Power vs. Energy Favored:"),
                                             p(class = "cardText", "Balanced"),
                                             tags$b("How Does it Work?"),
                                             p(class = "cardText", 
                                               "As more non-dispatchable and location-dependent renewable generation resources are brought online, the flexibility of the grid may be 
                                               negatively impacted. Congestion on transmission infrastructure during times of high renewable generation can jeopardize its operation 
                                               and the stability of the grid. Because renewable resources such as wind and solar are concentrated in the central and southern states respectively,
                                               significant transmission infrastructure is required to bring this power supply to meet load in population centers on the east and west coasts.
                                               Energy Storage can be used to reduce this congestion to ensure more efficient integration of renewable energy generation."),
                                             tags$b("Monetization/Value Creation:"),
                                             p(class = "cardText",
                                               "Congestion relief creates value by reducing the scale of transmission necessary to connect renewable resources while maximizing the resource's
                                               value by ensuring that more power that is generated can be added to the grid and sold to customers.")
                                             )
                                    )}, # Left Text Card
                                    {div(class = "column", style = "padding-left:0; height:400px;",
                                         div(class = "useCaseImageCard",
                                             tags$img(src = "congRlf.png", style = "width: 100%; background-color: white; margin-top: 14%;")
                                         )
                                    )}  # Right Image Card
                                )
                          )
                        )}, # Transmission Congestion Relief
                        {hidden(
                            div(class = "useCasePanel", id = "resAdqcy",
                                div(class = "useCaseTitle RMI_blue",
                                    "Resource Adequacy",
                                    tags$i(class = "fa fa-times", id = "UCX-8")
                                ),
                                div(class = "row UseCasePanel",
                                    {div(class = "column", style = "margin-left:5px; height:400px;",
                                        div(class = "useCaseTextCard",
                                            tags$b("Typical User:"),
                                                p(class = "cardText", "Utilities, Generation and Transmission Companies"),
                                            tags$b("Siting Location:"),
                                                p(class = "cardText", "Transmission Grid, Co-located with Generation"),
                                            tags$b("Common Technologies:"),
                                                p(class = "cardText", "Batteries (Lithium Ion, Flow, Sodium-Sulfur), Molten Salt, Pumped Hydro, CAES"),
                                            tags$b("Key Specifications"),
                                                p(class = "cardText", "Energy-focused, but with significant power capacity."),
                                            tags$b("How Does it Work?"),
                                                p(class = "cardText",
                                                    "As Minnesota's electricity generation resource mix is composed of an increasing proportion of variable renewable energy resources,
                                                    such as wind and solar, there is an increasing probability that these resources will, at times, produce more energy tyhan there is 
                                                    load to consume it. Without energy storage, some resources would have to be curtailed, or intentionally constrained, in order to 
                                                    protect grid frequency and stability. Energy storage would be able to store the energy that otherwise would have been wasted, which
                                                    could then be used when renewable resources are no longer overproducing."),
                                            tags$b("Monetization/Value Creation:"),
                                                p(class = "cardText",
                                                    "Storage can allow utilities to get more useable production out of their generation assets, potentially reducing the need to overbuild 
                                                    generation infrastructure, saving the utility construction costs and preserving the natural capital of the unused land.")
                                         )
                                    )}, # Left Text Card
                                    {div(class = "column", style = "padding-left:0; height:400px;",
                                         div(class = "useCaseImageCard", style = "padding-top:11px;",
                                             tags$img(src = "resAdqcy7.png", style = "width: 100%; background-color:white;")
                                         )
                                    )}  # Right Image Card
                                )
                            )
                        )} #  Resource Adequacy
                      
                    )}, # Utility-Serving Use Cases
                    
                    {div(
                      
                      {hidden(
                        div(class = "useCasePanel", id = "rampPeak",
                            div(class = "useCaseTitle RMI_green",
                                "Ramping and Load-Following",
                                tags$i(class = "fa fa-times", id = "UCX-9")
                            ),
                            div(class = "row UseCasePanel",
                                {div(class = "column", style = "margin-left:5px; height:450px;",
                                    div(class = "useCaseTextCard", style = "min-width:240px; max-width:240px;",
                                        tags$b("Typical User:"),
                                            p(class = "cardText", "Utilities, Third Party Energy Companies, Large Industrials"),
                                        tags$b("Siting Location:"),
                                            p(class = "cardText", "Transmission or Distribution Grid"),
                                        tags$b("Common Technologies:"),
                                            p(class = "cardText", "Lithium-Ion Batteries, Flywheels, Supercapacitors, SMES"),
                                        tags$b("Key Specifications"),
                                            p(class = "cardText", "High Ramp Rate and Fast Response Time, High Power Capacity"),
                                        tags$b("Monetization/Value Creation:"),
                                            p(class = "cardText",
                                                "Utilities can save money by not operating, upgrading, or building natural gas-fired peaker plants in some situations. Can enable
                                                greater use of solar photovoltaic generation without exacerbating the duck curve and threatening grid stability.")
                                     )
                                )}, # Left Text Card
                                {div(class = "column", style = "padding-left:0; height:400px;",
                                     div(class = "useCaseImageCard",
                                         tags$img(src = "rampFollow9.png", style = "width: 100%; background-color:white; margin-top:35px;")
                                     )
                                )}, # Center Image Card
                                {div(class = "column", style = "margin-left:-10px; height:450px;",
                                    div(class = "useCaseTextCard", style = "min-width:240px; max-width:240px; overflow-y:scroll;",
                                        tags$b("How Does it Work?"),
                                            p(class = "cardText",
                                                "Many conventional energy generation resources are limited in terms of the rate at which they can respond to increasing load 
                                                or increase their power output. Other resources, such as wind and solar, are unable to ramp up and down on demand, unless they
                                                are being curtailed. Therefore, when the total load on the grid increases rapidly, utilities often use expensive and heavily
                                                polluting resources like natural gas-fired peakre plants to follow the load. Several forms of energy storage have adequate 
                                                response times and ramp rates to provide this service in the place of natural gas."),
                                        tags$b("Duck Curve Response:"),
                                            p(class = "cardText",
                                                "One emerging area of concern as more solar photovoltaic generation is commissioned is known as the 'Duck Curve.' This occurs
                                                in the evening hours as load generally increases, but solar generation rapidly declines. The load curve that results from this
                                                event has a very steep ramp rate. Energy storage can be employed to mitigate the 'Duck Curve' effect by charging from overproduction
                                                of solar during the day, and discharging in the evening to create a more gradual increase.")
                                     )
                                )}  # Right Text Card
                            )
                        )
                      )}, # Ramping and Load Following
                      {hidden(
                          div(class = "useCasePanel", id = "reserve",
                              div(class = "useCaseTitle RMI_green",
                                  "Spin- and Non-Spin Reserve",
                                  tags$i(class = "fa fa-times", id = "UCX-10")
                              ),
                              div(class = "row UseCasePanel",
                                  {div(class = "column", style = "margin-left:5px; height:485px;",
                                      div(class = "useCaseTextCard", style = "min-width:240px; max-width:240px; height:485px;",
                                          tags$b("Typical User:"),
                                              p(class = "cardText", "Utilities, Generation and Transmission Companies"),
                                          tags$b("Siting Location:"),
                                              p(class = "cardText", "Transmission Grid, Colocated with Generation"),
                                          tags$b("Common Technologies:"),
                                              p(class = "cardText", "Batteries (Lithium Ion, Redox Flow, Sodium-Sulfur), Pumped Hydro, Hydrogen/Ammonia, CAES"),
                                          tags$b("Key Specifications"),
                                              p(class = "cardText", "Power-favored, ability to reach full discharge capacity within ten minutes"),
                                          tags$b("Monetization/Value Creation:"),
                                              p(class = "cardText",
                                                  "Utilities are able to save money by operating power plants more efficently, waste less fuel, and potentially building or expanding
                                                  fewer generation facilities.")
                                       )
                                  )}, # Left Text Card
                                  {div(class = "column", style = "padding-left:0; height:485px;",
                                       div(class = "useCaseImageCard", style = "padding-top:10px; height:485px;",
                                           div(style = "width:380px; background-color:white; padding: 5px 0 0.1px;",
                                              p(class = "center bold", "Response to Loss of Generation Capacity")),
                                           tags$img(src = "Reserve.png", style = "width: 100%")
                                       )
                                  )}, # Center Image Card
                                  {div(class = "column", style = "margin-left:-10px; height:485px;",
                                      div(class = "useCaseTextCard", style = "min-width:240px; max-width:240px; height:485px;",
                                          tags$b("How Does it Work?"),
                                              p(class = "cardText",
                                                  "Utilties are required to hold enough generation capacity in reserve to accommodate the unexpected loss
                                                  of their largest generation resource with minimal disruptions or frequency variations. This is traditionally
                                                  done by witholding some of the generation capacity for all active power plants, so that their capcity can be 
                                                  dialed up to compensate for lost capacity. This practice requires that generation facilities operate at low
                                                  efficiency, wasting fuel, increasing emissions, and raising electricity costs. Employing energy storage to serve 
                                                  as reserve capacity can enable existing generation assets to function more cleanly and effiently."),
                                          tags$b("Spin vs. Non-Spin:"),
                                              p(class = "cardText",
                                                  "Spinning Reserve refers to additional capacity of operating facilities that is held in reserve, while non-spinning
                                                  reserves are facilities which are not currently operating, but can be initiated and reach full capacity within 10 minutes.")
                                       )
                                  )}  # Right Text Card
                              )
                          )
                      )}, # Spin- and Non-Spin Reserve
                      {hidden(
                          div(class = "useCasePanel", id = "freqReg",
                              div(class = "useCaseTitle RMI_green",
                                  "Frequency Regulation",
                                  tags$i(class = "fa fa-times", id = "UCX-11")
                              ),
                              div(class = "row UseCasePanel",
                                  {div(class = "column", style = "margin-left:5px; height:450px;",
                                      div(class = "useCaseTextCard", style = "min-width:240px; max-width:240px;",
                                          tags$b("Typical User:"),
                                              p(class = "cardText", "Utilities, Third Party Energy Companies"),
                                          tags$b("Siting Location:"),
                                              p(class = "cardText", "Transmission Grid"),
                                          tags$b("Common Technologies:"),
                                              p(class = "cardText", "Lithium Ion Batteries, Flywheels, Supercapacitors, SMES"),
                                          tags$b("Power vs. Energy Favored:"),
                                              p(class = "cardText", "Power, Typically very short duration"),
                                          tags$b("Monetization/Value Creation:"),
                                              p(class = "cardText",
                                                  "Frequency regulation is one of several ancillary services, including reserve capacity and voltage support, 
                                                  for which markets have been created by independent system operators (ISOs) to provide compensation to the 
                                                  operators of energy storage systems which provide them.")
                                       )
                                  )}, # Left Text Card
                                  {div(class = "column", style = "padding-left:0; height:400px;",
                                       div(class = "useCaseImageCard", style = "padding-top:12.5px;",
                                           tags$img(src = "freqReg14.png", style = "width: 100%; margin-top:5px;")
                                       )
                                  )}, # Center Image Card
                                  {div(class = "column", style = "margin-left:-10px; height:450px;",
                                      div(class = "useCaseTextCard", style = "min-width:240px; max-width:240px;",
                                          tags$b("How Does it Work?"),
                                              p(class = "cardText",
                                                  "Grid stability relies on maintaining a system frequency of 60 Hz, which requires that generation match load
                                                  as closely as possible. When supply is greater than demand, frequency rises above 60 Hz; and it drops below
                                                  60 Hz when generation declines below load. This latter case is more challenging to correct, since it is easier
                                                  to reduce generation if load drops unexpectedly than it is to increase when a generation asset unexpectedly
                                                  shuts down or reduces generation. Energy storage devices which are capable of rapid response rates can be 
                                                  employed to balance rapid fluctuations to maintain a safe frequency. In the event that longer duration response
                                                  is needed, these devices can arrest the initial change in frequency and stabilize it long enough for longer-duration
                                                  storage devices with slower response times to take over.")
                                       )
                                  )}  # Right Text Card
                              )
                          )
                      )}, # Frequency Regulation
                      {hidden(
                          div(class = "useCasePanel", id = "voltSup",
                              div(class = "useCaseTitle RMI_green",
                                  "Voltage Support",
                                  tags$i(class = "fa fa-times", id = "UCX-12")
                              ),
                              div(class = "row UseCasePanel",
                                  {div(class = "column", style = "margin-left:5px; height:450px;",
                                       div(class = "useCaseTextCard", style = "min-width:240px; max-width:240px;",
                                           tags$b("Typical User:"),
                                           p(class = "cardText", "Utilities, Third Party Energy Companies"),
                                           tags$b("Siting Location:"),
                                           p(class = "cardText", "Transmission and Distribution Grids"),
                                           tags$b("Common Technologies:"),
                                           p(class = "cardText", "Lithium Ion Batteries, Capacitors, Voltage Regulators"),
                                           tags$b("Power vs. Energy Favored:"),
                                           p(class = "cardText", "Power, Typically short duration"),
                                           tags$b("Monetization/Value Creation:"),
                                           p(class = "cardText",
                                             "Voltage Support and Regulation is one of several ancillary services, including reserve capacity and frequency regulation, 
                                             for which markets have been created by independent system operators (ISOs) to provide compensation to the 
                                             operators of energy storage systems which provide them.")
                                           )
                                  )}, # Left Text Card
                                  {div(class = "column", style = "padding-left:0; height:400px;",
                                       div(class = "useCaseImageCard",
                                           tags$img(src = "voltSup2.png", style = "width: 100%; margin-top: 24%;")
                                       )
                                  )}, # Center Image Card
                                  {div(class = "column", style = "margin-left:-10px; height:450px;",
                                       div(class = "useCaseTextCard", style = "min-width:240px; max-width:240px;",
                                           tags$b("How Does it Work?"),
                                           p(class = "cardText",
                                             "Similar to frequency regulation, consumer loads require that incoming power be within a certain voltage range and power quality
                                             standards set by regulators dictate that utilities provide electricity within a certain voltage range. Voltage support, or volt/VAR
                                             optimization (VVO) involves using reactive power to stabilize voltage and minimize voltage drops. A common analogy is of a glass of
                                             beer, where the entire glass is the amount of power that a customer pays for. However, only the beer in the glass is real power, which
                                             is able to do work, while the foam is reactive power which is unable to do work. Voltage regulation aims to maximize the power factor,
                                             or minimize the amount of foam to maximize the portion of the glass that is filled with beer.")
                                           )
                                  )}  # Right Text Card
                              )
                          )
                      )}, # Voltage Support
                      {hidden(
                          div(class = "useCasePanel", id = "blkStart",
                              div(class = "useCaseTitle RMI_green",
                                  "Black Start / System Recovery",
                                  tags$i(class = "fa fa-times", id = "UCX-13")
                              ),
                              div(class = "row UseCasePanel",
                                  {div(class = "column", style = "margin-left:5px; height:450px;",
                                       div(class = "useCaseTextCard", style = "min-width:240px; max-width:240px;",
                                           tags$b("Typical User:"),
                                           p(class = "cardText", "Utilities, Third Party Energy Companies"),
                                           tags$b("Siting Location:"),
                                           p(class = "cardText", "Transmission Grid, Colocated with Generation Resources"),
                                           tags$b("Common Technologies:"),
                                           p(class = "cardText", "Lithium Ion Batteries"),
                                           tags$b("Power vs. Energy Favored:"),
                                           p(class = "cardText", "Power"),
                                           tags$b("Monetization/Value Creation:"),
                                           p(class = "cardText",
                                             "Grid operators (ISOs and RTOs) establish black start tariffs in order to compensate the owners of black start resources. These
                                             tariffs are determined by formulas which account for maintenance, training, and fuel storage costs for the resources.")
                                           )
                                  )}, # Left Text Card
                                  {div(class = "column", style = "padding-left:0; height:400px;",
                                       div(class = "useCaseImageCard",
                                           tags$img(src = "blkStart3.png", style = "width: 95%; margin-left: 10px; margin-top: 15px;")
                                       )
                                  )}, # Center Image Card
                                  {div(class = "column", style = "margin-left:-10px; height:450px;",
                                       div(class = "useCaseTextCard", style = "min-width:240px; max-width:240px;",
                                           tags$b("How Does it Work?"),
                                           p(class = "cardText",
                                             "Black start describes the process of restoring generation resources to proper function after partial or complete outage
                                             events without accessing external power sources. Most power plants require a substantial amount of power to start up and
                                             safely begin generation. This power is often provided by a backup diesel generator, which, itself, is started with the 
                                             assistance of a small lithium-ion battery. Using battery energy storage devices for black start could eliminate the need 
                                             for a diesel generator or other polluting resource and obviate the carbon emissions associated therewith. This approach
                                             could help to restore power more quickly after an outage and with less attributable air pollution.")
                                       )
                                  )}  # Right Text Card
                              )
                          )
                      )}  # Black Start
                      
                    )}  # Grid/ISO-Serving Use Cases
                ) # Use Case Panels
            )
        )}, # Services and Use Case Description
        {hidden(
            div(class = "column main intropage", id = "Intro-5",
                p(class = "section-header", 
                    "Data Description, Limitations, and Sources"),
                hr(),
                {div(style = "width:950px; padding: 20px; background-color: #cedbe8",
                    p(
                        strong(style = "font-size: 16px; color: #7c1717;", "Disclaimer: "),
                        "This tool is intended for explanatory and educational purposes only. It is not meant to be predictive of actual function of an 
                        energy storage device or the energy use and financial impacts thereof. If you are interested in more specific and precise predictive
                        modeling for the use of a battery energy storage device in your home, business, or non-profit organization, please consult one or
                        more of the following resources."
                    ),
                    hr(),
                    div(class = "row", style = "padding: 0 25px;",
                        tags$img(src = "NREL4.png", style = "height: 60px; width: 228px; margin-left: 90px;"),
                        tags$img(src = "EPRI.png", style = "height: 60px; width: 128px; margin-left: 90px;"),
                        tags$img(src = "NextEra3.png", style = "height: 60px; width: 176px; margin-left: 90px;")
                    )
                )}, # Disclaimer and reference to other modeling resources
                br(),
                {tabsetPanel(
                    {tabPanel("Sources and Description",
                        p(class = "section-header", style = "margin-top:10px;",
                            "Sources and Description"),
                        
                        div(class = "row",
                            div(style = "min-width:460px; max-width:460px; padding: 10px; margin: 10px 0 0 14px;",
                                strong("Residential Load and Solar Generation:"),
                                p(class = "indent",
                                  "Data for modeling of residential energy use were acquired from the UMass Trace Repository, created by the University of Minnesota, 
                                  which hosts anonymous load data for 400+ homes. The data sets were selected to represent a range of home sizes and for the year 2016."),
                                strong("Commercial Load Data:"),
                                p(class = "indent",
                                  "Commercial data used in this tool were acquired from OpenEI, a repository for energy data and information. The data selected correspond
                                  to several businesses in Minneapolis for the year 2016, and were narrowed down to organizations that may be likely to be interested in
                                  or benefit from energy storage devices."),
                                strong("Generation Resource Data:"),
                                p(class = "indent",
                                  "Hour-by-hour generation resource data depicted how much electricity is being generated by each generation resource (i.e. coal, wind, 
                                  solar, etc.). These data were acquired from MISO and represent all utilities in the MISO-North region, which includes all of Minnesota,
                                  and Iowa and parts of North Dakota, South Dakota, and Montana.")
                            ),
                            div(style = "margin: 57px 0 0 20px; width: 500px;",
                                tags$img(src = "UMTR.png", style = "height: 60px; width: 468px;"),
                                tags$img(src = "OpenEI.png", style = "height: 60px; width: 191px; margin: 72px 0 0 138px;"),
                                tags$img(src = "MISO1.png", style = "height: 60px; width: 179px; margin: 75px 0 0 145px;")
                            )
                        )
                        
                    )}, # Data Sources and Description
                    
                    {tabPanel("Algorithms and Data Modeling", 
                        
                        p(class = "section-header", style = "margin-top:10px;",
                            "Modeling Energy Storage Use Cases"
                        ),  
                              
                        {div(class = "row",
                            div(style = "margin-left:14px; min-width: 524px; max-width: 524px; height: 552px; padding: 5px 25px;",
                                p(class = "section-subheader", "Time-of-Use Management"),
                                p(class = "indent",
                                    "Time-of-Use rate structures commonly create three time periods throughout each day - Peak, Mid-Peak, and Off-Peak. Peak hours feature the highest per-kilowatt-hour
                                    energy prices, while off-peak hours feature the lowest prices. Generally speaking, the behavior that this rate structure promotes and the way that customers can save
                                    money is to shift their energy use from peak and mid-peak hours to off-peak hours."),
                                p(class = "indent",
                                    "The algorithm used in this tool to model the use of an energy storage device in response to time-of-use rate designs involves three general processes which are shown in the image to
                                    the right. First, the storage device is charged at the maximum rate possible during off-peak hours, increasing energy use when rates are at their lowest. The model then
                                    discharges the device during peak hours as much as the energy capacity of the device allows, prioritizing the reduction of energy use when rates are at their highest. Finally, if
                                    the storage device has any capacity remaining, it is discharged during mid-peak hours."),
                                p(class = "indent",
                                    "It should be noted that this algorithm assumes perfect load forecasting capacity. It calculates the amount of energy used during peak hours and subtracts that from 
                                    the amount charged during off-peak hours. This difference, measured in kilowatt-hours, is then distributed throughout the mid-peak hours.")
                            ),
                            div(style = "width: 425px; height: 552px; background-color: #e3e3e3; border: 1px solid lightgrey; border-radius: 2px; padding:10px;",
                                tags$img(src = "TOU_Algorithm.png", style = "background-color: white; width: 403px;")
                            )
                        )}, # TOU Management
                        hr(),           
                        {div(  
                        div(style = "width: 950px; margin-left: 14px; padding: 0 10px;",
                            p(class = "section-subheader", style = "margin-top:0;",
                                "Demand-Charge Management"),
                            p(class = "indent",
                                "Demand-metered rate structure generally applies to commercial customers and charges customers based on the greatest fifteen-minute sustained
                                load each month. Demand charge management involves more evenly distributing load throughout the day to reduce the prominence, and therefore 
                                the cost, of peak load events. In executing this use case, energy storage devices will charge when energy use is low and discharge when use
                                is high to flatten out the load curve."),
                            p(class = "indent",
                                "The first step in designing an algorithm to model the behavior of an energy storage device engaged in demand-charge management is to estimate
                                the lowest feasable level to which each day's load can be limited. For each day, twenty values are established, representing fractions of that 
                                day's peak load at which that day's maximum load limit can be set (Step 1). For each of these values, the area between the line and the load 
                                curve is calculated, measured in kilowatt-hours (Step 2). The area above the line (in blue) represents the amount that needs to be discharged,
                                while the area below the curve (in grey) represents the amount of energy that can be used to charge the device."),
                            p(class = "indent",
                                "These twenty maximum daily load values will be narrowed down by eliminating those that are not achievable. First, all values which require more
                                discharge of energy than is availeble to be charged are eliminated (corresponding to 5% - 60% in the image below). Then, after considering the
                                characteristics of the battery, any level where the difference between the limit and the maximum load is greater than the power capacity of the
                                battery, or the area between the two lines is greater than the energy capacity of the battery is also eliminated. Of the remaining options, the
                                lowest percentage is selected to be that day's limit at which load will be capped. Any time load is below this value, the storage device will
                                be set to charge, and it will be set to discharge when load is greater than this line. This process is repeated independently for each day of 
                                the year and for each combination of storage device characteristics.")
                        ),      
                        
                        tags$img(src = "PS_Algorithm.png", style = "width: 750px; margin-left:100px;"),
                        br())}, # Peak Shaving
                        hr(),
                        {div(class = "row",
                            div(style = "margin-left:14px; min-width: 470px; max-width: 470px; height: 301px; padding: 10px;",
                                p(class = "section-subheader", style = "margin-top:0;",
                                    "Optimization of On-Site Solar Generation"
                                ),
                                p(class = "indent",
                                  "Solar panels only generate electricity during the day when the sun is shining. In order for solar arrays to provide a significant amount of a home or
                                  business' electricity needs, they have to overgenerate relative to the building's load during daylight hours. Without storage,
                                  customers with solar generation will sell power back to the grid during the day and buy it back at night when their panels are no longer producing."),
                                p(class = "indent",
                                  "The algorithm employed to model energy storage behavior for this use case measures the difference between solar generation and energy use. When generation
                                  is greater than energy use, the storage device is charged, and when generation falls below energy use, it switches to discharge until the energy capacity is
                                  depleted.")
                            ),
                            div(style = "width: 480px; height: 301px; background-color: #e3e3e3; border: 1px solid lightgrey; border-radius: 2px; padding:10px;",
                                tags$img(src = "solarOpt3.png", style = "width: 460px; background-color: white;")
                            )
                        )}, # Solar Optimization
                        br(), br()
                    )}, # Algorithms and Data Modeling
                    
                    {tabPanel("Limitations and Caveats", 
                        p(class = "section-subheader", style = "margin-top:10px;",
                            "Model Limitations and Caveats"),
                        div(style = "width: 950px; padding: 10px; margin-top: 10px;",
                            strong("Use of Sample Data:"),
                            p(class = "indent",
                              "This tool uses sample datasets from anonymous residential and commercial utility customers rather than using user-submitted data. There are 
                              several reasons for this. First, as noted above, this tool is not meant to be predictive, but rather informative of what energy storage can do
                              in general terms. Applying these algorithms to user-submitted data may encourage users to read more into the modeling outcomes than is intended.
                              Additionally, using preformatted data is a much simpler proposition than either requiring user-submitted data to be in a certain format or
                              including formatting processes in the application. Finally, most home and business owners do not have access to hour-by-hour energy use data.
                              These sample data sets allow users to select the option that most closely resembles their situtation, either by business type or size of residence,
                              to get a general idea of their options. If users are interested in more detailed and precise modeling that can be applied in a more predictive
                              capacity, please consult one or more of the resources listed above."),
                            strong("After-the-Fact Modeling:"),
                            p(class = "indent",
                              "The algorithms used to model energy storage behavior have complete information regarding energy consumption. Accordingly, the determination to charge
                              or discharge may be made based on energy use characteristics later in the day. Enacting these use cases in real time requires sophisticated load 
                              forecasting methods to predict these trends and may suffer inneficiencies when predicting trends that do not match actual energy use."),
                            strong("Estimation of Energy Storage Costs:"),
                            p(class = "indent",
                              "Proper estimation of the return on investment (ROI) or the repayment period for an energy storage device requires an accurate estimation of system
                              costs. Battery costs vary significantly on a case-by-case basis depending on a number of factors, making this estimation challenging."),
                            strong("Aggregation of Generation Resources:"),
                            p(class = "indent", 
                              "This tool uses hour-by-hour generation resource data for all of the MISO-North region, encompassing parts of five states and one canadian province
                              and a large number of cooperative, municipal, and investor-owned utilities. Utilities serving customers in Minnesota and the rest of this region vary
                              significantly in their mix of generation resources, and, accordingly, the carbon emission profile of their electricity."),
                            strong("Isolation of Use Cases:"),
                            p(class = "indent",
                              "Often, in order to maximize the value of an energy storage device, multiple use cases will be applied by the same energy storage device (i.e. integration
                              of solar generation and time-of-use management). For the sake of clarity, each use cases is presented here separately and assessed on an individual basis.
                              A more realistic model would likely include two or more use cases. Modeling on this level becomes highly specific to the particular customer and building
                              for which the device is being used, and generalization from these models is much less informative.")
                        )
                    )}  # Limitations and Caveats
                )}  # Data sources, algorithms, and limitations
            )
        )}  # Data Description and Sources
        
      ) # End of Row Section on Intro Page
    )}, # Introduction Page

###  BEGINNING OF RESIDENTIAL PAGE ###

  {hidden(  
    div(id = "Residential", class = "tabcontent",
      div(class = "row",
        div(class = "column left use-case",
            {div(       
                p(class = "button-labels",
                    "Select the Use Case to be Modeled:"),
                div(class = "radioSelect",
                    radioGroupButtons(inputId = "UseCase_res",
                                      label = NULL,
                                      individual = TRUE, justified = TRUE,
                                      choiceNames = c(HTML("Time-of-Use Rate <br/> Management"),
                                                      HTML("Optimization of <br/> Solar Generation")),
                                      choiceValues = c("RTU", "RSF"),
                                      selected = "RTU", size = "sm"
                    )
                ),    
                p(class = "button-labels",
                    "Select the Size of Residence to be Modeled:"),
                div(class = "radioSelect",
                    radioGroupButtons(inputId = "DataSet.res",
                                      label = NULL,
                                      individual = TRUE, justified = TRUE,
                                      choiceNames = c(HTML("Large <br/> 3000-3200 ft<sup>2</sup>"), 
                                                      HTML("Medium <br/> 2300-2500 ft<sup>2</sup>"),
                                                      HTML("Small <br/> 1500-1700 ft<sup>2</sup>")),
                                      choiceValues = c("Lrg_House", "Med_House", "Sml_House"),
                                      selected = "Med_House", size = "sm"
                    )
                )
            
            )}, # Use Case and House Size Selection Buttons
            hr(),
            {div(
                tags$p(class = "slider-labels", 
                    "Battery Characteristics"),
                sliderInput(inputId = "Batt_kW.res",
                    label = "Power Capacity",
                    min = 0, max = 10, 
                    value = 5, step = 1, 
                    width = "100%", 
                    post = " kW"),
                sliderInput(inputId = "Batt_kWh.res",
                    label = "Energy Capacity",
                    min = 0, max = 40, 
                    value = 20, step = 1, 
                    width = "100%",
                    post = " kWh"),
                sliderInput(inputId = "Batt_Efficiency.res",
                    label = "Round-Trip Efficiency",
                    min = 0, max = 100, 
                    value = 80, step = 5, 
                    width = "100%",
                    post = "%"),
                sliderInput(inputId = "Batt_DoD.res",
                    label = "Depth of Discharge",
                    min = 0, max = 100, 
                    value = 95, step = 5, 
                    width = "100%",
                    post = "%"),
                sliderInput(inputId = "Batt_Backup.res",
                    label = "Amount Witheld for Backup Power",
                    min = 0, max = 100, 
                    value = 0, step = 5, 
                    width = "100%",
                    post = "%")
            )}, # Battery Spec Sliders
            hr(),
            {div(
                tags$button(id = "solarAccordion_res", 
                            class = "accordion", 
                    p(class = "slider-labels", 
                        "Solar Characteristics",
                        tags$i(class = "fa fa-caret-down")
                    )
                ),
                hidden(
                    div(id = "solarAccordionPanel_res",
                        sliderInput(inputId = "Solar.res",
                                    label = "Generation Capacity",
                                    min = 0, max = 10, 
                                    value = 5, step = 1, 
                                    width = "100%",
                                    post = " kW"
                        )
                    ) # End of solar accordion panel
                ) # End of hidden accordion panel
            )}  # Solar Slider Accordion
        ), # End of left column
        
        div(class = "column main",
            {div(
                conditionalPanel(condition = "input.UseCase_res == 'RTU'",
                    p(class = "section-header", 
                        "Residential Time-of-Use Rate Design"
                    )
                ),
                conditionalPanel(condition = "input.UseCase_res == 'RSF'",
                    p(class = "section-header", 
                        "Optimization of Residential Solar Generation"
                    )
                )
            )}, # Use Case Main Column Title
            
            tabsetPanel(type = "tabs",
                {tabPanel(style = "width:900px;", "General Information",
                          
                    {conditionalPanel(condition = "input.UseCase_res == 'RTU'",
                        p(class = "column-header", 
                            "What are Time-of-Use Rates?"),
                        p(class = "body-text indent",
                            "Historically, the vast majority of residential utility customers have been assessed electric utility bills with
                            flat, per-kilowatt-hour rate design. This rate design assigns the same cost to each unit of electricity irrespective
                            of how much energy is being used or when it is consumed. Time-of-use rates, on the other hand, assign different rates 
                            depending on the time of day, week, or year in which it is used. Energy used at times of high demand (i.e. summer evenings)
                            is assigned a greater cost, than energy used when demand is typically low (i.e. middle of the night.)"),
                        
                        div(class = "float-right", style = "padding: 5px; height: 510px;",
                            strong(class = "body-text", style = "margin: 0 45.5px;",
                                "Energy Shifting with Time-of-Use Pricing:"), 
                            plotOutput("RTU_Intro1", height = 300, width = 350),
                            p(class = "caption", style = "margin: 3px 5px;",
                                "The top figure above depicts a typical load curve with time-of use pricing.
                                The bottom figure features energy shifting to minimize peak energy use. Move the
                                slider below to adjust energy shifting capacity."),
                            div(style = "margin: 5px 10px 0;",
                                p(class = "center", style = "font-size:13px; font-weight:bold;", 
                                    "Energy Storage Capacity"),
                                div(style = "margin-top:-20px;",
                                    sliderInput(inputId = "RTU_IntroplotSlider",
                                                label = "", 
                                                min = 0, max = 10, 
                                                value = 0, step = 1,
                                                width = "100%")
                                )
                            )
                        ),
                        
                        strong(class = "twelvePt",
                            "Marginal Cost of Electricity"),
                        p(class = "body-text indent",
                            "For Utilities, not all hours of the day, month, and year are equivalent with respect to cost of energy generation or procurement. At times of peak electricity use, 
                            when utilities employ all generation resources available to them, the average cost of generation increases. Low-cost resources like wind, solar, and combined-cycle 
                            natural gas turbines must be supplemented by expensive natural gas or petroleum-fueled peaking plants increasing overall costs to the utilities. When utilities charge 
                            the same rate for each and every kilowatt-hour, they disperse these peak costs throughout the rest of the day by overcharging when generation costs are low and 
                            undercharging when costs are high."),
                        
                        strong(class = "twelvePt",
                            "Promoting Efficient Behavior"),
                        p(class = "body-text indent",
                            "By creating a price differential between electricity consumed during peak times that consumed when demand is low, utilities create incentives for customers to shift
                            their behavior towards using a greater proportion of their electricity during off-peak hours. Common methods for this include using appliances such as washers and 
                            dryers, dishwashers, and ovens more during off-peak times and decreasing their use during peak hours. Additionally, reducing air-conditioner use during summer evenings,
                            whether by improving insulation or allowing household temperatures to rise by a few degrees, can reduce peak energy use and save money on monthly bills"),
                        
                        strong(class = "twelvePt",
                            "Shifting Energy Consumption"),
                        p(class = "body-text indent",
                            "In addition to behavioral changes to reduce peak energy use, employing energy storage to shift electricity consumption from one time to another can allow customers to
                            reduce their energy bills. Customers can charge their storage device during off-peak times or when on-site generation exceeds energy use, and discharge during peak hours. 
                            This practice can reduce the average per-kilowatt-hour electricity cost assessed to the utility customer, saving them money on their energy bill."),
              
                        p(class = "section-header", 
                            "Minnesota Residential Time-of-Use Pilot Program"),
                        p(class = "body-text indent",
                            "In 2019, the Minnesota Public Utilities Commission unanimously approved a proposal for a utility to establish a pilot program for residential time-of-use rates. 
                            The program is set to begin in early 2020 and will take place in Eden Prairie and across several neighborhoods in south Minneapolis. It is an opt-out program, meaning
                            that customers will be automatically enrolled in the program, but they can choose to opt out of it if they so choose. 
                            Weekday peak-hour (3-8pm) rates will be raised from $0.134/kWh in summer months to $0.259/kWh, and from $0.117/kWh in winter months to 
                            $0.224/kWh. The pilot lowers off-peak rates for hours 12-6am to $0.057/kWh and all other hours (mid-peak) are also reduced to $0.121/kWh in the summer and 
                            $0.104/kWh in the winter. These new rates are depicted in the figure below."),
                        p(class = "body-text indent",
                            "A shift to this rate structure could increase a customer’s bill if much of their energy use falls within peak hours and they are unable to adjust their energy 
                            consumption behavior. However, utilizing an energy storage device to charge during off-peak hours and discharge during peak hours to offset peak energy 
                            use represents an opportunity to save money on utility bills and offset the cost of a storage device. ( Note that the time-of-use pilot program is not currently available to 
                            customers with energy storage devices. Potential for savings depends on the future availability of time-of-use rates for all interested customers.)"),
                        tags$img(src="TOU_Introplot2.png", style = "width:850px; margin-left:30px;")
                        )}, # Time-of-Use
                    {conditionalPanel(condition = "input.UseCase_res == 'RSF'",
                        div(class = "float-right", style = "padding: 5px; height:720px; width:420px;",
                            strong(class = "body-text", style = "margin: 0 79px;",
                                "Solar Optimization with Energy Storage:"),
                                plotOutput("RSF_Intro1", height = 200, width = 400),
                                plotOutput("RSF_Intro2", height = 225, width = 400),
                                tags$img(src="RSF_Legend2.png", style = "width:100%; margin-left:5px;"),
                            p(class = "caption", style = "margin: 3px 5px;",
                                "The top figure above depicts a typical load curve for a residence with roof-top solar generation; the figure below shows the same residence with energy storage. 
                                Move the slider below to adjust energy storage capacity and see its effects on energy consumption from the grid."),
                            div(style = "margin: 5px 10px 0;",
                                p(class = "center bold", style = "font-size:13px;", 
                                    "Energy Storage Capacity"),
                                div(style = "margin-top:-20px;",
                                    sliderInput(inputId = "RSF_IntroplotSlider",
                                                label = "", 
                                                min = 0, max = 10, 
                                                value = 0, step = 1,
                                                width = "100%")
                                )
                            )
                        ),
                        p(class = "column-header", 
                            "Services of Solar + Storage"),
                        p(class = "body-text indent",
                            "The last decade has seen a boom in installation of distributed, roof-top solar PV generation. The improving economics of batteries for energy storage have presented
                            battery energy storage systems as an mutually beneficial partner for behind-the-meter solar arrays."),
                        strong(class = "twelvePt",
                            "Energy Shifting"),
                        p(class = "body-text indent",
                            "Solar Generation is in many ways an ideal partner for energy storage. While it only generates electricity during the day, generation patterns are fairly consistent. Often, 
                            solar PV arrays overproduce during the day. Energy storage systems are able to charge during overproduction and discharge in the evenings when demand rises above supply."),
                        strong(class = "twelvePt",
                            "Ramp Rate / Duck Curve"),
                        p(class = "body-text indent",
                            "As distributed solar deployment expands, one potential consequence is an increase in the ramp rate of electricity demand in the afternoon. This occurs due to a sharp decline
                            in solar generation which coincides with an increase in building load in the evening. Energy storage devices which charge from overgeneration during the day and discharge in 
                            the late afternoon and evening. This is demonstrated by the figure to the right when 'Energy Storage Capacity' is set between 1 and 4."),
                        strong(class = "twelvePt",
                            "Islanding and Microgrid Capabilities"),
                        p(class = "body-text indent",
                            "For those wishing to rely exclusively on their own generation, whether connected to the distribution grid or not, solar photovoltaic generation presents both challenges and 
                            opportunities. Solar is the most economically viable means for small-scale generation, but generates well below full capacity for the majority of each day. Long-duration storage
                            can provide the ability to store all excess generation which can then be used when the sun is not shining."),
                        p(class = "section-header",
                            "Net Metering and Service Monetization"),
                        p(class = "body-text indent",
                            "Employing energy storage to store overproduction affects the transactions between the customer and their utility. Without energy storage, this overproduction is typically sold 
                            back to the utility through net metering, while energy storage devices can decrease or eliminate these net-metering transactions."),
                        p(class = "body-text indent",
                            "For customers with retail-rate net metering, each unit of energy returned to the grid is compensated at the same rate at which the customer purchases it. Under this rate structure,
                            which is currently in use across Minnesota, increasing the on-site use of solar generation (rather than selling back to the grid) produces no monetizable value for the device's
                            owner. On the other hand, if, as many states and utilities are interested in implementing, energy returned to the grid is compensated below the retail rate, each unity of energy
                            that is stored for later use rather than being returned to the grid only to be bought back later represents savings for the customer."),
                        tags$img(src = "NEM_Map1.png", style = "width:950px;")
                    )}  # Solar Firming
                    
                   )}, # Residential General Information
                {tabPanel("Daily Load Curve",
                      p(class = "section-subheader", 
                          "Select Date Range:"),
                      div(style = "margin-top: -25px;",
                          dateRangeInput(inputId = "date_res",
                                         label = "",
                                         start = "2016-1-3", end = "2016-1-9",
                                         min = "2016-1-1", max = "2016-12-31",
                                         format = "MM d, yyyy")
                      ),
                      
                      {conditionalPanel(condition = "input.UseCase_res == 'RTU'",
                          div(class = "monthPlotBox",
                              div(class = "monthPlotHead", 
                                  "Energy Consumption Profile"),
                              div(class = "monthPlot", 
                                  div(class = "row",
                                      plotOutput("datePlot_Grid.rtu"),
                                      tags$img(src = "RTU_Grid_Legend.png", style = "height:110px; margin:95px 15px;")
                                  )
                              )
                          ),
                          p(class = "monthPlotCaption indent",
                              "The above plot depicts the energy consumption profile of a residential utility customer with an energy storage device with the characteristics
                              specified on the panel to the left. The red area represents times when the storage device is charging and the rate (in kilowatts) at which it is charging.
                              Conversely, the blue area represents the time and rate of storage device discharge. This transforms the original load curve (represented by the dotted line)
                              into a new load curve with storage, depicted by the solid black line. The result is a new load curve which draws more electricity from the grid during off-peak
                              times, and draws less electricity from the grid during peak and mid-peak hours.",
                              br()
                          ),
                          div(class = "monthPlotBox", 
                              div(class = "monthPlotHead", 
                                  "Battery Use Profile"), 
                              div(class = "monthPlot", 
                                  div(class = "row",
                                      plotOutput("datePlot_Batt.rtu"),
                                      tags$img(src = "RTU_Batt_Legend.png", style = "height:140px; margin:75px 0px 30px 10px;")
                                  )
                              )
                          ),
                          p(class = "monthPlotCaption indent",
                              "This bottom plot depicts the status of the energy storage device throughout its deployment. Similar to the top plot, the red and blue areas represent the times
                              and rates of charging and discharging respectively, measured in kilowatts. The solid black line depicts the state of charge of the battery, that is, the amount of 
                              energy stored in the battery in a given time, measured in kilowatt-hours."
                          )
                         )}, # Time-of-Use
                      {conditionalPanel(condition = "input.UseCase_res == 'RSF'",
                          div(class = "monthPlotBox",
                              div(class = "monthPlotHead", 
                                  "Household Load and Solar Generation"),
                              div(class = "monthPlot",
                                  div(class = "row",
                                      plotOutput("datePlot_One.rsf"),
                                      tags$img(src = "Legend-1.png", style = "height:100px; margin:100px 10px;")
                                  )
                              )
                          ),
                          p(class = "monthPlotCaption indent",
                              "The above plot depicts the household energy use / load curve and solar generation profile for a residential utility customer with a rooftop solar
                              photovoltaic installation. In the absence of energy storage capacity, at times when load exceeds generation, all excess energy needed is purchased
                              from the grid. Meanwhile, when generation is greater than load, excess electricity generated is sold back to the grid, usually through net metering.",
                              br()
                          ),
                          div(class = "monthPlotBox", 
                              div(class = "monthPlotHead", 
                                  "Three Destinations of Solar-Generated Electricity"), 
                              div(class = "monthPlot", 
                                  div(class = "row",
                                      plotOutput("datePlot_Two.rsf"),
                                      tags$img(src = "Legend-2.png", style = "height:175px; margin:60px 10px;")
                                  )
                              )
                          ),
                          p(class = "monthPlotCaption indent",
                              "With an energy storage device in use, electricity generated by the rooftop solar array takes one of three pathways. First, just as is the case without
                              storage capacity, energy is consumed directly from the panels up to 100 percent of load (represented by the blue area on the plot). If energy is generated 
                              to a surplus with respect to load, solar generated electricity is used to charge the energy storage device, as shown by the dark grey area. Finally, 
                              if the storage device is unable to receive all excess solar generation, either due to inadequate power or energy capacity, any remaining electricity
                              is returned to the grid (shown in red).",
                              br()
                          ),
                          div(class = "monthPlotBox", 
                              div(class = "monthPlotHead", 
                                  "New Load Curve with Solar and Storage"), 
                              div(class = "monthPlot", 
                                  div(class = "row",
                                      plotOutput("datePlot_Three.rsf"),
                                      tags$img(src = "Legend-3.png", style = "height:145px; margin:70px 10px;")
                                  )
                              )
                          ),
                          p(class = "monthPlotCaption indent",
                              "After taking into consideration excess solar generation which is stored and consumed later, a new load curve takes shape, as shown above. Herein, the 
                              original load curve is reduced by energy used directly from the panels (dark blue) and by energy that is stored first and consumed later from the battery
                              (light blue). This results in a new load curve which incorporates more of the on-site, solar-generated electricity (solid black line) than a comparable 
                              load curve without energy storage capacity."
                          )
                         )}  # Solar Firming
                      
                   )}, # Residential Daily Load Curve
                {tabPanel("Monthly Load Curve",
                      p(class = "section-subheader", 
                          "Select Month:"),
                      div(style = "margin: 0 10px;",
                      radioGroupButtons(inputId = "Month.res",
                                        label = NULL,
                                        individual = TRUE, justified = TRUE,
                                        choices = c("Jan", "Feb", "Mar",
                                                    "Apr", "May", "Jun",
                                                    "Jul", "Aug", "Sep",
                                                    "Oct", "Nov", "Dec"),
                                        selected = "Jan", size = "xs")),
   
                      {conditionalPanel(condition = "input.UseCase_res == 'RTU'",
                          div(class = "monthPlotBox",
                              div(class = "monthPlotHead", 
                                  "Energy Consumption Profile"), 
                              div(class = "monthPlot", 
                                  div(class = "row",
                                      plotOutput("monthPlot_Grid.rtu"),
                                      tags$img(src = "RTU_Grid_Legend.png", style = "height:110px; margin:95px 30px 0 5px;")
                                  )
                              )
                          ),
                          p(class = "monthPlotCaption indent",
                              "The above plot depicts the energy consumption profile of a residential utility customer with an energy storage device with the characteristics
                              specified on the panel to the left. The red area represents times when the storage device is charging and the rate (in kilowatts) at which it is charging.
                              Conversely, the blue area represents the time and rate of storage device discharge. This transforms the original load curve (represented by the dotted line)
                              into a new load curve with storage, depicted by the solid black line. The result is a new load curve which draws more electricity from the grid during off-peak
                              times, and draws less electricity from the grid during peak and mid-peak hours.",
                              br()
                          ),
                          div(class = "monthPlotBox", 
                              div(class = "monthPlotHead", 
                                  "Battery Use Profile"), 
                              div(class = "monthPlot",
                                  div(class = "row",
                                      plotOutput("monthPlot_Batt.rtu"),
                                      tags$img(src = "RTU_Batt_Legend.png", style = "height:140px; margin:75px 0px 30px 5px;")
                                  )
                              )
                          ),
                          p(class = "monthPlotCaption indent",
                              "This bottom plot depicts the status of the energy storage device throughout its deployment. Similar to the top plot, the red and blue areas represent the times
                              and rates of charging and discharging respectively, measured in kilowatts. The solid black line depicts the state of charge of the battery, that is, the amount of 
                              energy stored in the battery in a given time, measured in kilowatt-hours."
                          )
                         )}, # Time-of-Use
                      {conditionalPanel(condition = "input.UseCase_res == 'RSF'",
                          div(class = "monthPlotBox",
                              div(class = "monthPlotHead",
                                  "Electric Load with Rooftop Solar Generation"), 
                              div(class = "monthPlot", 
                                  div(class = "row",
                                      plotOutput("monthPlot_Solar.rsf"),
                                      tags$img(src = "RSF_Month_Legend.png", style = "height:160px; margin:70px 10px;")
                                  )
                              )
                          ),
                          p(class = "monthPlotCaption indent", 
                              "Without energy storage, solar energy that is generated on-site must be used as it is generated or sold back to the grid. In this image,
                              solar generation is represented by the red line. The blue area represents the average amount of energy generated by solar panels that is
                              able to be used directly, reducing the energy drawn from the grid from the what it would be without solar (grey dotted line) to a new, lower
                              curve (solid black line). Excess energy that is generated by the solar array that cannot be directly consumed must be sold back to the grid.",
                              br()
                          ),
                          div(class = "monthPlotBox", 
                              div(class = "monthPlotHead", 
                                  "Electric Load with Solar and Storage"), 
                              div(class = "monthPlot",
                                  div(class = "row",
                                      plotOutput("monthPlot_Batt.rsf"),
                                      tags$img(src = "RSF_Month_Legend.png", style = "height:160px; margin:70px 10px;")
                                  )
                              )
                          ),
                          p(class = "monthPlotCaption indent", 
                              "Adding energy storage to the situation above allows the user to store excess energy generated by the solar panels that cannot be used as it
                              is generated. This excess energy can then be used later, after solar generation has dipped below energy consumption. Here, the light blue area
                              represents the additional amount of energy that can be used on average when using energy storage, further reducing the amount of energy drawn
                              from the grid (solid black line). This use case can create economic benefit for the user if the rate at which they are paid for exporting excess
                              electricity to the grid is lower than the rate they pay for electricity. If these rates are the same (i.e. net metering), then no financial benefit
                              is achieved."
                          )
                         )}  # Solar Firming
                      
                   )}, # Residential Monthly Load Curve
                {tabPanel(style = "width:900px;", "Bill Comparison", 
                    p(class = "column-header", 
                        "Comparison of Monthly and Yearly Bills:"),
                    
                    {conditionalPanel(condition = "input.UseCase_res == 'RTU'",
                        tableOutput("BillComp.rtu"),
                        hr(),
                        div(class = "row", style = "height:470px; padding: 0 25px;",
                            
                            {div(class = "financeCard", style = "height: 470px; margin: 0 15px 0 20px;",
                                p(class = "section-subheader center",
                                    "Battery Storage System Financial Data"),
                                             
                                div(class = "financeBox",
                                    htmlOutput(class = "center bold", "YearlySavings.rtu")),
                                p("Potential Yearly Savings:"),
                                             
                                div(class = "financeBox",
                                    htmlOutput(class = "center bold", "batteryCost.rtu")),
                                p("Total Upfront Cost:"),
                                sliderInput(inputId = "BattCost.rtu",
                                            label = NULL,
                                            min = 2000, max = 10000,
                                            value = 6000, step = 1000,
                                            width = "100%", pre = "$"),
                                             
                                div(class = "financeBox",
                                    htmlOutput(class = "center bold", "expLife.rtu")),
                                p("Expected Useful Life:"),
                                sliderInput(inputId = "BattLife.rtu",
                                            label = NULL,
                                            min = 5, max = 25,
                                            value = 20, step = 5,
                                            width = "100%", post = " years"),
                                
                                hr(class = "darkGreyLine"),
                                             
                                p(class = "center", 
                                    "Employ a discount rate for savings calculations?"),
                                div(class = "row discRateSwitch",
                                    p("No"),
                                    div(style = "margin:0 10px;",
                                        tags$label(class = "switch",
                                            tags$input(type = "checkbox", id = "toggle-rtu"),
                                            tags$span(class = "slider round")
                                        )
                                    ),
                                    p("Yes")
                                ),
                                             
                                div(class = "financeBox",
                                    htmlOutput(class = "center bold", outputId = "discountRate.rtu")),
                                p("Discount Rate:"),
                                    sliderInput(inputId = "discRate.rtu",
                                                label = NULL,
                                                min = 0, max = 10,
                                                value = 0, step = 0.5,
                                                width = "100%", post = "%")
                                             
                            )}, # Financial Data and Slider Box
                            {div(class = "billCompText", style = "padding: 0 5px;",
                                p(class = "section-subheader",
                                    "Evaluating the Effects of Battery Energy Storage"),
                                p(class = "indent",
                                    "The table above compares the monthly and yearly bills for a sample residential customer with and without energy storage, using both standard,
                                    flat-rate pricing and time-of-use rate design. The two most significant columns to compare are shaded in grey, comparing a standard bill without
                                    energy storage and a time-of-use bill with energy storage. This represents the potential savings of a storage device engaged in time-of-use rate
                                    management. It should be noted that the total energy consumption in kilowatt-hours (two far-right columns) is greater when a storage device is used
                                    because of round-trip inefficiency."
                                ),
                                p(class = "indent",
                                    "The top line in the box to the left shows the estimated yearly savings calculated from the table above. When taken alongside the upfront cost and
                                    the expected useful life of the battery, it is possible to estimate if and when the energy savings can offset the cost and create positive net value.
                                    This is shown graphically below, with green or red vertical bars representing lifetime net savings or cost."
                                )
                            )}  # Text Description Box
                        ),
                        hr(),
                        p(class = "column-header", "Battery Energy Storage Device Break-Even Analysis"),
                        div(style = "margin-left:25px;",
                            plotOutput("PaybackPlot.rtu", width = "850px")
                        )
                        
                    )}, # Time-of-Use
                    {conditionalPanel(condition = "input.UseCase_res == 'RSF'",
                        tableOutput("BillComp.rsf"),
                        
                        {div(class = "row centerBox billCompSliderRow", style = "min-width: 800px; max-width: 800px; height: 165px;",
                             
                            {div(class = "lightGreyBorder", style = "width:520px; margin-left:5px;",
                                p(class = "center BCLabel",
                                    "Net Metering Compensation Rate:"),
                                
                                div(class = "row", style = "margin:2px 10px;",
                                    div(style = "width:16%;",
                                        p(style = "font-size:12px; margin:20px 0 0 15px;", 
                                            "Summer"),
                                        p(style = "font-size:12px; margin:4px 0 0 15px", 
                                            "Winter")
                                    ),
                                    
                                    div(style = "width:28%; border: 1px solid white;",
                                        p(class = "center rateHeaderRsf", 
                                            "Purchase from Grid:"),
                                        div(class = "rateBox centerBox", style = "width: 90px;",
                                            p("13.44¢ per kWh", class = "center bold elevenPt")
                                        ),
                                        div(class = "rateBox centerBox", style = "width: 90px; margin-top:5px;",
                                            p("11.74¢ per kWh", class = "center bold elevenPt")
                                        )
                                    ),
                                    
                                    div(style = "width:28%; border: 1px solid white;",
                                        p(class = "center rateHeaderRsf", 
                                            "Sale Back to Grid:"),
                                        div(class = "rateBox centerBox", style = "width: 90px;",
                                            htmlOutput("NEMRateSummer.rsf", class = "center bold elevenPt")
                                        ),
                                        div(class = "rateBox centerBox", style = "width: 90px; margin-top:5px;",
                                            htmlOutput("NEMRateWinter.rsf", class = "center bold elevenPt")
                                        )
                                    ),
                                    
                                    div(style = "width:28%; border: 1px solid white;",
                                        p(class = "center rateHeaderRsf", 
                                            "Price Difference:"),
                                        div(class = "rateBox centerBox", style = "width: 90px;",
                                            htmlOutput("NEMDiffSummer.rsf", class = "center bold elevenPt")
                                        ),
                                        div(class = "rateBox centerBox", style = "width: 90px; margin-top:5px;",
                                            htmlOutput("NEMDiffWinter.rsf", class = "center bold elevenPt")
                                        )
                                    )
                                ),
                                
                                div(style = "width:90%; margin: 5px 22.5px 0;",
                                    sliderInput(inputId = "NetMeterRate.rsf",
                                                label = NULL,
                                                min = 0, max = 100, 
                                                value = 50, step = 5,
                                                post = "%", width = '100%')
                                )
                            )}, # Net Metering Rate Selection Slider
                            {div(style = "width:240px; margin:5px 0 0 25px;",
                                p(class = "caption",
                                    strong("Note:"),
                                    "Net-Metered Bill refers to the bill that would be assessed if energy returned to the grid were compensated at the full retail rate.",
                                    br(), br(),
                                    "The Adjusted Bill takes into account the reduced compensation for electricity returned to the grid as indicated in the figure to the left."
                                )
                            )}  # Table Caption
                            
                        )}, # Second Row - Rate Selection and Table Caption
                        hr(),
                        {div(class = "row", style = "height:490px; padding: 0 25px;",
                            
                            {div(class = "financeCard", style = "height: 490px; margin: 0 15px 0 20px;",
                                p(class = "section-subheader center",
                                    "Battery Storage System Financial Data"),
                                
                                div(class = "row", style = "margin-left:0px;",
                                    p("Subject of ROI:"),
                                    div(class = "radioPlot", style = "width:270px; margin-top:-4px;",
                                        radioGroupButtons(inputId = "ROI_Subj.rsf",
                                                          label = NULL,
                                                          individual = TRUE, justified = TRUE,
                                                          choiceNames = c("Solar & Storage", "Storage Only"),
                                                          choiceValues = c("Both", "Storage"),
                                                          selected = "Both", size = "sm")
                                    )
                                ),
                                
                                div(class = "financeBox",
                                    htmlOutput(class = "center bold", "YearlySavings.rsf")),
                                p("Potential Yearly Savings:"),
                                
                                div(class = "financeBox",
                                    htmlOutput(class = "center bold", "batteryCost.rsf")),
                                p("Total Upfront Cost:"),
                                sliderInput(inputId = "BattCost.rsf",
                                            label = NULL,
                                            min = 5000, max = 25000,
                                            value = 15000, step = 1000,
                                            width = "100%", pre = "$"),
                                
                                div(class = "financeBox",
                                    htmlOutput(class = "center bold", "expLife.rsf")),
                                p("Expected Useful Life:"),
                                sliderInput(inputId = "BattLife.rsf",
                                            label = NULL,
                                            min = 5, max = 25,
                                            value = 20, step = 5,
                                            width = "100%", post = " years"),
                                hr(class = "darkGreyLine"),
                                
                                p(class = "center", 
                                    "Employ a discount rate for savings calculations?"),
                                div(class = "row discRateSwitch",
                                    p("No"),
                                    div(style = "margin:0 10px;",
                                        tags$label(class = "switch",
                                            tags$input(type = "checkbox", id = "toggle-rsf"),
                                            tags$span(class = "slider round"))),
                                    p("Yes")
                                ),
                                
                                div(class = "financeBox",
                                    htmlOutput(class = "center bold", outputId = "discountRate.rsf")),
                                p("Discount Rate:"),
                                sliderInput(inputId = "discRate.rsf",
                                            label = NULL,
                                            min = 0, max = 10,
                                            value = 0, step = 0.5,
                                            width = "100%", post = "%")
                                
                            )}, # Financial Data and Slider Box
                            {div(class = "billCompText", style = "padding: 0 5px;",
                                 p(class = "section-subheader",
                                   "Evaluating the Effects of Battery Energy Storage"),
                                 p(class = "indent",
                                   "The table above compares the monthly and yearly bills for a sample residential customer without any solar or storage, with roof-top solar,
                                    and with solar and storage. The standard bill in the far left column is calculated with traditional flat-rate pricing. Each of the solar and
                                   solar plus storage examples report the amount of energy overgenerated from the solar panels and returned to the grid through net metering, the electricity
                                   bill if returned electricity is compensated at the full retail rate, and the bill if returned electricity is compensated below the retail rate. The 'Net Metering
                                    Compensation Rate' figure below the table shows the retail and net-metered prices for electricity throughout the year and allows you to adjust the compensation rate."
                                 ),
                                 p(class = "indent",
                                   "The top line in the box to the left shows the estimated yearly savings calculated from the table above. When taken alongside the upfront cost and
                                   the expected useful life of the battery, it is possible to estimate if and when the energy savings can offset the cost and create positive net value.
                                   This is shown graphically below, with green or red vertical bars representing lifetime net savings or cost."
                                 )
                            )}  # Text Description Box
                            
                        )}, # Third Row - Financial Data and Text Card
                        
                        hr(),
                        p(class = "column-header", "Solar and Storage Break Even Analysis"),
                        div(style = "margin-left:25px;",
                            plotOutput("PaybackPlot.rsf", width = "850px")
                        )
                        
                    )}  # Solar Firming
                    
                   )}, # Residential Bill Comparison
                {tabPanel("Generation Resources", 
                      p(class = "column-header", "Generation Resource Use and Carbon Accounting"),
                      {div(class = "row", style = "height:640px; margin:0;",
                          
                          div(class = "column left generation",
                              div(class = "gen-box",
                                  div(class = "box-header", "MISO-North Average Generation Profile:"),
                                  tags$img(src="Gen_Plot3.png", style = "margin: 10px 0px; height:590px;")
                              )
                          ),
                          div(class = "column right generation",
                              div(class = "gen-box",
                                  div(class = "box-header", "Average Household Load Profile:"),
                                  conditionalPanel(condition = "input.UseCase_res == 'RTU'", style = "margin: 5px 10px;",
                                                   plotOutput("GenPlot.rtu", width = "95%", height = "590px")),
                                  conditionalPanel(condition = "input.UseCase_res == 'RSF'", style = "margin: 5px 10px;",
                                                   plotOutput("GenPlot.rsf", width = "95%", height = "590px"))
                              )
                          )
                      )}, # Top row of charts
                      hr(),
                      div(style = "width:815px; height:110px;",
                          p(class = "column-header", 
                              "Carbon Accounting and Social Cost Determination"),
                          p(class = "body-text", style = "text-indent: 40px;",
                              "Two major motivations behind energy storage and other grid innovations include improved system efficiency and the reduction 
                              of greenhouse gas and criterion pollutant emissions from electric generation and service. However, storage represents a much 
                              more complicated path towards decarbonization than does distributed generation, like solar PV.")
                      ),
                      {div(class = "row", style = "height:540px; margin:0;",
                          
                          {div(class = "column left generation",
                              div(style = "height: 540px",
                                  
                                  strong(style = "font-size:12px;",
                                      "Daily Emission Rate Profile"),
                                  p(class = "body-text indent",
                                      "The onset of vast amounts of variable energy resources (mostly wind) in recent years has changed the profile of electric 
                                      generation. As seen above on the left, wind is most productive early in the morning and late at night, and is least 
                                      productive in the middle of the day. Fossil fuel generation is adjusted to compensate for these fluctuations, which leads 
                                      to an emission profile wherein more pollutants are emitted per megawatt during the day than at night."),
                                  #strong(style = "font-size:12px;",
                                  #    "Daily Emission Rate Profile"),
                                  p(class = "body-text indent", style = "text-indent: 40px;",
                                      "Many common energy storage use cases aim to reduce load during peak times. Because peak hours correspond with times of high
                                      emission rates, these use cases have the secondary effect of reshaping the load curve to more closely resemble the renewable
                                      resource generation profile than that of fossil fuels. (See top right)"),
                                  strong(style = "font-size:12px;",
                                      "Effects on Generation Attributes and Impacts"),
                                  p(class = "body-text indent",
                                      "Based on the ability of energy storage to reshape load curves and the coincidence of peak times and high carbon emission rates,
                                      many storage use cases facilitate a greater proportional use of renewable and clean energy resources. Depending on the incorporation
                                      and optimization of new renewable generation resoruces and the efficiency of the storage device, energy storage can have wide-ranging
                                      effects on total energy consumption and overall emissions, as seen in the table to the right.")
                              )
                          )}, # Left Column of Text
                          
                          {div(class = "column right generation",
                              div(style = "border: 1px solid white; height: 540px; background-color: #efeadc;",
                                  p(class = "section-subheader",
                                    "Carbon Accounting and Social Cost Determination:"),
                                  conditionalPanel(condition = "input.UseCase_res == 'RTU'",
                                                   tableOutput("Generation.rtu")),
                                  conditionalPanel(condition = "input.UseCase_res == 'RSF'",
                                                   tableOutput("Generation.rsf")
                                  ),
                                  
                                  div(style = "margin: 25px 10px;",
                                      p(class = "section-subheader", 
                                        "Social Cost of Carbon:"),
                                      sliderInput(inputId = "SCC.res",
                                                  label = NULL,
                                                  min = 0, max = 50,
                                                  value = 15, step = 5, 
                                                  pre = "$", post = " / ton",
                                                  width = "100%")
                                  ),
                                  hr(style = "border-color: darkgrey; margin:0 10px 25px;"),
                                  div(style = "margin: 0 15px;", conditionalPanel(condition = "input.UseCase_res == 'RSF'",
                                      p(class = "caption",
                                          "* Employing distributed solar PV without enough storage capacity to retain 100% of generation typically results in
                                          the sale of some amount of electricity back to the grid. While this contributes 'clean' and renewable energy to the
                                          grid, it is not considered in carbon accounting calculations. Rather, all electricity that is bought from the grid
                                          is considered to have the generation mix and emissions attributes of the local grid as a whole.")
                                  )),
                                  div(style = "margin: 0 15px;", conditionalPanel(condition = "input.UseCase_res == 'RTU'",
                                      p(class = "caption",
                                          "* Employing common energy storage devices for use cases which predominantly shift load and electricity purchases
                                          from one time to another, whether to reduce peak events, reduce costs through time-of-use rate designs, or to shift
                                          load to times when renewable resources make up a greater proportion of overall generation, can often", em("increase"),
                                          "attributed carbon emissions. In these cases, the inefficiency of the battery outweighs the difference in rate of 
                                           carbon emissions from one time to another.")
                                  ))
                              )
                          )}  # Generation Table Output Card 
                      )} # Bottom Row - Text and Gen Table
                  )}  # Residential Resource Use
                
            ) # End of Residential Main Column Tabset Panel
        ) # End of Main Column
      ) # End of Row
    ) # End of Residential Tab
  )}, # Residential Page

### BEGINNING OF COMMERCIAL PAGE ###

  {hidden(  
    div(id = "Commercial", class = "tabcontent",
        div(class = "row",
            div(class = "column left use-case",
                {div(       
                  p(class = "button-labels",
                    "Select the Use Case to be Modeled:"),
                  
                  div(class = "radioSelect",
                      radioGroupButtons(inputId = "UseCase_comm",
                                        label = NULL,
                                        individual = TRUE, justified = TRUE,
                                        choiceNames = c(HTML("Time-of-Use Rate <br/> Management"), 
                                                        HTML("Demand-Charge <br/> Management"),
                                                        HTML("Optimization of <br/> Solar Generation")),
                                        choiceValues = c("CTU", "CPS", "CSF"),
                                        selected = "CTU", size = "sm")
                  ),
                  p(class = "button-labels",
                    "Select the Organization to be Modeled:"),
                  selectInput(inputId = "Comm_Type",
                              label = NULL,
                              choices = c("Primary School" = "Prim_School",
                                          "Office Building" = "Med_Office",
                                          "Retail Store" = "Retail",
                                          "Restaurant" = "Restaurant"),
                              width = "100%")
                )}, # Use Case and Organization Selectors
                hr(),
                {div(
                  tags$p(class = "slider-labels", "Battery Characteristics"),
                  sliderInput(inputId = "Batt_kW.comm",
                              label = "Power Capacity",
                              min = 0, max = 200, value = 50, step = 5, width = "100%", 
                              post = " kW"),
                  sliderInput(inputId = "Batt_kWh.comm",
                              label = "Energy Capacity",
                              min = 0, max = 1000, value = 200, step = 10, width = "100%",
                              post = " kWh"),
                  sliderInput(inputId = "Batt_Efficiency.comm",
                              label = "Round-Trip Efficiency",
                              min = 0, max = 100, value = 80, step = 5, width = "100%",
                              post = "%"),
                  sliderInput(inputId = "Batt_DoD.comm",
                              label = "Depth of Discharge",
                              min = 0, max = 100, value = 95, step = 5, width = "100%",
                              post = "%"),
                  sliderInput(inputId = "Batt_Backup.comm",
                              label = "Amount Witheld for Backup Power",
                              min = 0, max = 100, value = 0, step = 5, width = "100%",
                              post = "%"))}, # Battery Spec Sliders
                hr(),
                {div(
                  tags$button(id = "solarAccordion_comm", class = "accordion", 
                              p(class = "slider-labels", "Solar Characteristics",
                                tags$i(class = "fa fa-caret-down"))),
                  hidden(
                    div(id = "solarAccordionPanel_comm",
                        sliderInput(inputId = "Solar.comm",
                                    label = "Generation Capacity",
                                    min = 0, max = 400, value = 100, step = 25, width = "100%",
                                    post = " kW")
                    ) # End of solar accordion panel
                  )# End of hidden accordion panel
                )} # Solar Slider Accordion
            ),
            
            div(class = "column main",
                {div(
                  conditionalPanel(condition = "input.UseCase_comm == 'CTU'",
                                   p(class = "section-header", 
                                     "Commercial Time-of-Use Rate Design"
                                   )
                  ),
                  conditionalPanel(condition = "input.UseCase_comm == 'CPS'",
                                   p(class = "section-header", 
                                     "Commercial Demand-Charge Management"
                                   )
                  ),
                  conditionalPanel(condition = "input.UseCase_comm == 'CSF'",
                                   p(class = "section-header", 
                                     "Optimization of Commercial Solar Generation"
                                   )
                  )
                )}, # Use Case Main Column Title
                
                tabsetPanel(type = "tabs",
                    {tabPanel(style = "width:900px;", "General Information",
                              
                        {conditionalPanel(condition = "input.UseCase_comm == 'CTU'",
                                          
                                          p(class = "column-header", 
                                            "What are Time-of-Use Rates?"),
                                          p(class = "body-text indent",
                                            "Historically, the vast majority of residential utility customers have been assessed electric utility bills with
                                            flat, per-kilowatt-hour rate design. This rate design assigns the same cost to each unit of electricity irrespective
                                            of how much energy is being used or when it is consumed. Time-of-use rates, on the other hand, assign different rates 
                                            depending on the time of day, week, or year in which it is used. Energy used at times of high demand (i.e. summer evenings)
                                            is assigned a greater cost, than energy used when demand is typically low (i.e. middle of the night.)"),
                                          
                                          div(class = "float-right", style = "padding: 5px; height: 510px;",
                                              strong(class = "body-text", style = "margin: 0 45.5px;",
                                                     "Energy Shifting with Time-of-Use Pricing:"), 
                                              plotOutput("CTU_Intro", height = 300, width = 350),
                                              p(class = "caption", style = "margin: 3px 5px;",
                                                "The top figure above depicts a typical load curve with time-of use pricing.
                                                The bottom figure features energy shifting to minimize peak energy use. Move the
                                                slider below to adjust energy shifting capacity."),
                                              div(style = "margin: 5px 10px 0;",
                                                  p(class = "center", style = "font-size:13px; font-weight:bold;", 
                                                    "Energy Storage Capacity"),
                                                  div(style = "margin-top:-20px;",
                                                      sliderInput(inputId = "CTU_IntroplotSlider",
                                                                  label = "", 
                                                                  min = 0, max = 10, 
                                                                  value = 0, step = 1,
                                                                  width = "100%")
                                                  )
                                              )
                                          ),
                                          
                                          strong(class = "twelvePt",
                                                 "Marginal Cost of Electricity"),
                                          p(class = "body-text indent",
                                            "For Utilities, not all hours of the day, month, and year are equivalent with respect to cost of energy generation or procurement. At times of peak electricity use, 
                                            when utilities employ all generation resources available to them, the average cost of generation increases. Low-cost resources like wind, solar, and combined-cycle 
                                            natural gas turbines must be supplemented by expensive natural gas or petroleum-fueled peaking plants increasing overall costs to the utilities. When utilities charge 
                                            the same rate for each and every kilowatt-hour, they disperse these peak costs throughout the rest of the day by overcharging when generation costs are low and 
                                            undercharging when costs are high."),
                                          
                                          strong(class = "twelvePt",
                                                 "Promoting Efficient Behavior"),
                                          p(class = "body-text indent",
                                            "By creating a price differential between electricity consumed during peak times that consumed when demand is low, utilities create incentives for customers to shift
                                            their behavior towards using a greater proportion of their electricity during off-peak hours. Common methods for this include using appliances such as washers and 
                                            dryers, dishwashers, and ovens more during off-peak times and decreasing their use during peak hours. Additionally, reducing air-conditioner use during summer evenings,
                                            whether by improving insulation or allowing household temperatures to rise by a few degrees, can reduce peak energy use and save money on monthly bills"),
                                          
                                          strong(class = "twelvePt",
                                                 "Shifting Energy Consumption"),
                                          p(class = "body-text indent",
                                            "In addition to behavioral changes to reduce peak energy use, employing energy storage to shift electricity consumption from one time to another can allow customers to
                                            reduce their energy bills. Customers can charge their storage device during off-peak times or when on-site generation exceeds energy use, and discharge during peak hours. 
                                            This practice can reduce the average per-kilowatt-hour electricity cost assessed to the utility customer, saving them money on their energy bill.")                 

                        )}, # Time-of-Use
                        {conditionalPanel(condition = "input.UseCase_comm == 'CPS'",
                            p(class = "column-header", 
                                "What are Demand Charges?"),
                            
                            div(class = "float-right",style = "padding:10px; width:400px; height:680px;",
                                strong(class = "body-text", style = "margin: 0 62.5px; font-size: 14px;",
                                    "Reduction of Peak Energy Use Events"),
                                plotOutput("CPS_Intro1"),
                                tags$img(src = "CPS_Legend4.png", style = "width: 100%;"),
                                p(class = "caption", style = "margin: 10px 5px;",
                                  "Discharging during peak events and charging when load is low reduces daily 
                               peak load. Move the slider below to adjust battery capacity. (The figure may take a few seconds to update.)"),
                                div(style = "margin: 5px 10px 0;",
                                    p(class = "center", style = "font-size:13px; font-weight:bold;", 
                                      "Energy Storage Capacity"),
                                    div(style = "margin-top:-20px;",
                                        sliderInput(inputId = "CPS_IntroplotSlider",
                                                    label = "", 
                                                    min = 0, max = 10, 
                                                    value = 0, step = 1,
                                                    width = "100%")
                                    )
                                )
                            ),

                            p(class = "body-text indent", 
                              "Commercial and industrial utility customers, like residential customers, are 
                                charged for each kWh of energy that they consume. Unlike residential customers, 
                                they are also often assessed demand charges, based on the highest 15-minute 
                                average usage within a given month (measured in kilowatts). For customers who 
                                have an uneven load profile, using a lot of power over short periods of time, 
                                these demand charges can make up a significant portion of their overall electricity 
                                bill."),
                            strong(class = "twelvePt",
                                   "Peak-Shaving"),
                            p(class = "body-text indent",
                                "Demand-metered customers can employ energy storage devices to reduce demand charges
                                by charging when their energy use is low and discharging during their peak energy use times. 
                                This shifts some of the load away from peak events to times of lower energy consumption, effectively smoothing out the 
                                load profile. This can be especially effective for customers who have predictable or 
                                controllable peak use events, such as places of worship or event venues."),
                           p(class = "body-text indent",     
                                "The image below compares
                                a consistent, predictable load on the right to an inconsistent load curve on the left. The ability to predict the
                                time and size of peaks is critical to effectively mitigating them, and this is much easier when energy
                                consumption is consistent on a day-to-day or week-to-week basis. Organizations with predictable peaks
                                can plan ahead to charge their storage device before an expected peak and discharge for the across the full peak,
                                effectively spreading the event's energy consumption out over a longer period."),
                            tags$img(src = "CPS_Intro4.png", style = "width: 475px;"),
                            br(), br(),
                            strong(class = "twelvePt",
                                "Effects on Utility-Wide Load"),
                            p(class = "body-text indent",
                                "Commercial entities, especially industrial and large commercial entities use vast amounts of power compared to most residential
                                and small commercial customers. Accordingly, these organizations can have a sizeable impact on the overall energy use for the area
                                served by a substation or even an entire utility. When these facilities reach their peak consumption events, this can cause significant
                                stress on the utility's distribution infrastructure, particularly if several experience peak events around the same time. Demand charges
                                are both a way for utilities to charge businesses for the excess costs associated with their peak events and to encourage them to reduce
                                the severity of these events. Often, large industrial customers may employ diesel, fuel oil, or natural gas-powered generator to provide
                                a portion of their electricity needs during peak events when the cost of that fuel is less than the marginal cost of increasing their 
                                demand charges. While this reduces the stress on the distribution grid and on the utility, it also has the effect of increasing carbon
                                emissions through the combustion of fossil fuels in the generators.")
                            
                        )}, # Peak Shaving
                        {conditionalPanel(condition = "input.UseCase_comm == 'CSF'",
                            
                                          div(class = "float-right", style = "padding: 5px; height:720px; width:420px;",
                                              strong(class = "body-text", style = "margin: 0 79px;",
                                                     "Solar Optimization with Energy Storage:"),
                                              plotOutput("CSF_Intro1", height = 200, width = 400),
                                              plotOutput("CSF_Intro2", height = 225, width = 400),
                                              tags$img(src="RSF_Legend2.png", style = "width:100%; margin-left:5px;"),
                                              p(class = "caption", style = "margin: 3px 5px;",
                                                "The top figure above depicts a typical load curve for a residence with roof-top solar generation; the figure below shows the same residence with energy storage. 
                                                Move the slider below to adjust energy storage capacity and see its effects on energy consumption from the grid."),
                                              div(style = "margin: 5px 10px 0;",
                                                  p(class = "center bold", style = "font-size:13px;", 
                                                    "Energy Storage Capacity"),
                                                  div(style = "margin-top:-20px;",
                                                      sliderInput(inputId = "CSF_IntroplotSlider",
                                                                  label = "", 
                                                                  min = 0, max = 10, 
                                                                  value = 0, step = 1,
                                                                  width = "100%")
                                                  )
                                              )
                                          ),
                                          p(class = "column-header", 
                                            "Services of Solar + Storage"),
                                          p(class = "body-text indent",
                                            "The last decade has seen a boom in installation of distributed, roof-top solar PV generation. The improving economics of batteries for energy storage have presented
                                            battery energy storage systems as an mutually beneficial partner for behind-the-meter solar arrays."),
                                          strong(class = "twelvePt",
                                                 "Energy Shifting"),
                                          p(class = "body-text indent",
                                            "Solar Generation is in many ways an ideal partner for energy storage. While it only generates electricity during the day, generation patterns are fairly consistent. Often, 
                                            solar PV arrays overproduce during the day. Energy storage systems are able to charge during overproduction and discharge in the evenings when demand rises above supply."),
                                          strong(class = "twelvePt",
                                                 "Ramp Rate / Duck Curve"),
                                          p(class = "body-text indent",
                                            "As distributed solar deployment expands, one potential consequence is an increase in the ramp rate of electricity demand in the afternoon. This occurs due to a sharp decline
                                            in solar generation which coincides with an increase in building load in the evening. Energy storage devices which charge from overgeneration during the day and discharge in 
                                            the late afternoon and evening. This is demonstrated by the figure to the right when 'Energy Storage Capacity' is set between 1 and 4."),
                                          strong(class = "twelvePt",
                                                 "Islanding and Microgrid Capabilities"),
                                          p(class = "body-text indent",
                                            "For those wishing to rely exclusively on their own generation, whether connected to the distribution grid or not, solar photovoltaic generation presents both challenges and 
                                            opportunities. Solar is the most economically viable means for small-scale generation, but generates well below full capacity for the majority of each day. Long-duration storage
                                            can provide the ability to store all excess generation which can then be used when the sun is not shining."),
                                          p(class = "section-header",
                                            "Net Metering and Service Monetization"),
                                          p(class = "body-text indent",
                                            "Employing energy storage to store overproduction affects the transactions between the customer and their utility. Without energy storage, this overproduction is typically sold 
                                            back to the utility through net metering, while energy storage devices can decrease or eliminate these net-metering transactions."),
                                          p(class = "body-text indent",
                                            "For customers with retail-rate net metering, each unit of energy returned to the grid is compensated at the same rate at which the customer purchases it. Under this rate structure,
                                            which is currently in use across Minnesota, increasing the on-site use of solar generation (rather than selling back to the grid) produces no monetizable value for the device's
                                            owner. On the other hand, if, as many states and utilities are interested in implementing, energy returned to the grid is compensated below the retail rate, each unity of energy
                                            that is stored for later use rather than being returned to the grid only to be bought back later represents savings for the customer."),
                                          tags$img(src = "NEM_Map1.png", style = "width:950px;")                  
                                          
                        )}  # Solar Firming
                        
                    )}, # Commercial General Information Pages
                    {tabPanel("Daily Load Curve",
                        p(class = "section-subheader", "Select Date Range:"),
                        div(style = "margin-top: -25px;",
                            dateRangeInput(inputId = "date_comm",
                                           label = "",
                                           min = "2016-1-1", max = "2016-12-31",
                                           start = "2016-1-3", end = "2016-1-9",
                                           format = "MM d, yyyy")
                        ),
                        
                        {conditionalPanel(condition = "input.UseCase_comm == 'CTU'",
                            div(class = "monthPlotBox",
                                div(class = "monthPlotHead", "Energy Consumption Profile"),
                                div(class = "monthPlot", 
                                    div(class = "row",
                                        plotOutput("datePlot_Grid.ctu"),
                                        tags$img(src = "RTU_Grid_Legend.png", style = "height:110px; margin:95px 15px;")
                                    )
                                )
                            ),
                            p(class = "monthPlotCaption indent",
                                "The above plot depicts the energy consumption profile of a commercial utility customer with an energy storage device with the characteristics
                                specified on the panel to the left. The red area represents times when the storage device is charging and the rate (in kilowatts) at which it is charging.
                                Conversely, the blue area represents the time and rate of storage device discharge. This transforms the original load curve (represented by the dotted line)
                                into a new load curve with storage, depicted by the solid black line. The result is a new load curve which draws more electricity from the grid during off-peak
                                times, and draws less electricity from the grid during peak and mid-peak hours.",
                                br()
                            ),
                            div(class = "monthPlotBox", 
                                div(class = "monthPlotHead", "Battery Use Profile"), 
                                div(class = "monthPlot", 
                                    div(class = "row",
                                        plotOutput("datePlot_Batt.ctu"),
                                        tags$img(src = "RTU_Batt_Legend.png", style = "height:140px; margin:75px 0px 30px 10px;")
                                    )
                                )
                            ),
                            p(class = "monthPlotCaption indent",
                                "This bottom plot depicts the status of the energy storage device throughout its deployment. Similar to the top plot, the red and blue areas represent the times
                                and rates of charging and discharging respectively, measured in kilowatts. The solid black line depicts the state of charge of the battery, that is, the amount of 
                                energy stored in the battery in a given time, measured in kilowatt-hours."
                            )
                           )}, # Time-of-Use
                        {conditionalPanel(condition = "input.UseCase_comm == 'CPS'",
                            div(class = "monthPlotBox",
                                div(class = "monthPlotHead", "Energy Consumption Profile"),
                                div(class = "monthPlot", 
                                    div(class = "row",
                                        plotOutput("datePlot_Grid.cps"),
                                        tags$img(src = "RTU_Grid_Legend.png", style = "height:110px; margin:95px 15px;")
                                    )
                                )
                            ),
                            p(class = "monthPlotCaption indent", 
                                "The above plot depicts a commercial utility customer using an energy storage device to reduce their demand charges through peak-shaving.
                                This process involves charging the storage device when energy use is low (red) and discharging when consumption is high (blue), resulting in the smoothing
                                out of the customer's load curve. You may notice that there is a limit on how much each day's peak load can be reduced, since each kilowatt-hour displaced
                                from the peak must be redistributed to the 'valleys' where it represents the storage device being charged. Because the device must be charged at least as
                                much if not more than it discharges (depending on efficiency), the theoretical minimum daily peak load is the average hour-by-hour load throughout the day.",
                                hr()
                            ),
                            div(class = "monthPlotBox", 
                                div(class = "monthPlotHead", "Battery Use Profile"), 
                                div(class = "monthPlot", 
                                    div(class = "row",
                                        plotOutput("datePlot_Batt.cps"),
                                        tags$img(src = "RTU_Batt_Legend.png", style = "height:140px; margin:75px 0px 30px 10px;")
                                    )
                                )
                            ),
                            p(class = "monthPlotCaption indent", 
                                "This bottom plot depicts the status of the energy storage device throughout the selected period. Similar to the top plot, the red and blue areas represent the times 
                                and rates of charging and discharging respectively, measured in kilowatts. The solid black line depicts the state of charge of the battery, that is, the amount 
                                of energy stored in the battery in a given time, measured in kilowatt-hours."
                            )
                           )}, # Peak Shaving
                        {conditionalPanel(condition = "input.UseCase_comm == 'CSF'",
                            div(class = "monthPlotBox",
                                div(class = "monthPlotHead", 
                                    "Household Load and Solar Generation"),
                                div(class = "monthPlot", 
                                    div(class = "row",
                                        plotOutput("datePlot_One.csf"),
                                        tags$img(src = "Legend-1.png", style = "height:100px; margin:100px 10px;")
                                    )
                                )
                            ),
                            p(class = "monthPlotCaption indent",
                              "The above plot depicts the energy use / load curve and solar generation profile for a commercial utility customer with an on-site solar
                              photovoltaic installation. In the absence of energy storage capacity, at times when energy us is greater than generation, all excess energy needed is purchased
                              from the grid. Meanwhile, when generation is greater than load, excess electricity generated is sold back to the grid, often at a price lower than retail.",
                              br()
                            ),
                            div(class = "monthPlotBox", 
                                div(class = "monthPlotHead", 
                                    "Three Destinations of Solar-Generated Electricity"), 
                                div(class = "monthPlot", 
                                    div(class = "row",
                                        plotOutput("datePlot_Two.csf"),
                                        tags$img(src = "Legend-2.png", style = "height:175px; margin:60px 10px;")
                                    )
                                )
                            ),
                            p(class = "monthPlotCaption indent",
                                "With an energy storage device in use, electricity generated by the on-site solar array takes one of three pathways. First, just as is the case without
                                storage capacity, energy is consumed directly from the panels up to 100 percent of load (represented by the blue area on the plot). If energy is generated 
                                to a surplus with respect to load, solar-generated electricity is used to charge the energy storage device, as shown by the dark grey area. Finally, 
                                if the storage device is unable to receive all excess solar generation, either due to inadequate power or energy capacity, any remaining electricity
                                is returned to the grid (shown in red).",
                                br()
                            ),
                            div(class = "monthPlotBox", 
                                div(class = "monthPlotHead", 
                                    "New Load Curve with Solar and Storage"), 
                                div(class = "monthPlot", 
                                    div(class = "row",
                                        plotOutput("datePlot_Three.csf"),
                                        tags$img(src = "Legend-3.png", style = "height:145px; margin:70px 10px;")
                                    )
                                )
                            ),
                            p(class = "monthPlotCaption indent",
                                "After taking into consideration excess solar generation which is stored and consumed later, a new load curve takes shape, as shown above. Herein, the 
                                original load curve is reduced by energy used directly from the panels (dark blue) and by energy that is stored first and consumed later from the battery
                                (light blue). This results in a new load curve which incorporates more of the on-site, solar-generated electricity (solid black line) than a comparable 
                                load curve without energy storage capacity."
                            )
                           )}  # Solar Firming
                   
                       )}, # Commercial Daily Load Curve
                    {tabPanel("Monthly Load Curve", 
                        p(class = "section-subheader", "Select Month:"),
                        div(style = "margin: 0 10px;",
                            radioGroupButtons(inputId = "Month_comm",
                                              label = NULL,
                                              individual = TRUE, justified = TRUE,
                                              choices = c("Jan", "Feb", "Mar",
                                                          "Apr", "May", "Jun",
                                                          "Jul", "Aug", "Sep",
                                                          "Oct", "Nov", "Dec"),
                                              selected = "Jan", size = "xs")),

                        {conditionalPanel(condition = "input.UseCase_comm == 'CTU'",
                            div(class = "monthPlotBox", 
                                div(class = "monthPlotHead", "Energy Consumption Profile"), 
                                div(class = "monthPlot",
                                    div(class = "row",
                                        plotOutput("monthPlot_Grid.ctu"),
                                        tags$img(src = "RTU_Grid_Legend.png", style = "height:110px; margin:95px 30px 0 5px;")
                                    )
                                )
                            ),
                            p(class = "monthPlotCaption", 
                                "The above plot depicts the energy consumption profile of a commercial utility customer using an energy storage device 
                                with the characteristics specified on the panel to the left. The red area represents times when the storage device is 
                                charging and the rate (in kilowatts) at which it is charging. Conversely, the blue area represents the time and rate of 
                                discharge. This transforms the original load curve (represented by the dotted line) into a new load curve with storage, 
                                depicted by the solid black line. The result is a new load curve which draws more electricity from the grid during off-peak 
                                times, and draws less electricity from the grid during peak and mid-peak hours.",
                                hr()
                            ),
                            div(class = "monthPlotBox", 
                                div(class = "monthPlotHead", "Battery Use Profile"), 
                                div(class = "monthPlot", 
                                    div(class = "row",
                                        plotOutput("monthPlot_Batt.ctu"),
                                        tags$img(src = "RTU_Batt_Legend.png", style = "height:140px; margin:75px 0px 30px 5px;")
                                    )
                                )
                            ),
                            p(class = "monthPlotCaption", 
                              "This bottom plot depicts the status of the energy storage device throughout its deployment. Similar to the top plot, the red and 
                              blue areas represent the times and rates of charging and discharging respectively, measured in kilowatts. The solid black line 
                              depicts the state of charge of the battery, that is, the amount of energy stored in the battery in a given time, measured in kilowatt-hours.",
                              hr()
                            )
                           )}, # Time-of-Use
                        {conditionalPanel(condition = "input.UseCase_comm == 'CPS'",
                            div(class = "monthPlotBox CPS", 
                                div(class = "monthPlotHead", 
                                    "Reduction of Monthly Load Peaks"), 
                                div(class = "monthPlot",
                                    plotOutput("monthPlot_Grid.cps")
                                )
                            ),
                            p(class = "monthPlotCaption", 
                                "Demand charges are assessed based on the highest sustained energy consumption (in kW) for each month. The above plot depicts the monthly load curve 
                                with the monthly peaks indicated. Without energy storage, the daily peaks are shown in grey with the corresponding monthly peak value indicated. When
                                energy storage is deployed, it limits the daily peaks to those depicted by the blue line, with the monthly peak value indicated in blue."
                            )
                           )}, # Peak-Shaving
                        {conditionalPanel(condition = "input.UseCase_comm == 'CSF'",
                            div(class = "monthPlotBox", 
                                div(class = "monthPlotHead", 
                                    "Electric Load with Rooftop Solar Generation"), 
                                div(class = "monthPlot",
                                    div(class = "row",
                                        plotOutput("monthPlot_Solar.csf"),
                                        tags$img(src = "RSF_Month_Legend.png", style = "height:160px; margin:70px 10px;")
                                    )
                                )
                            ),
                            p(class = "monthPlotCaption", 
                                "Without energy storage, solar energy that is generated on-site must be used as it is generated or sold back to the grid. In this image,
                                solar generation is represented by the red line. The blue area represents the average amount of energy generated by solar panels that is
                                able to be used directly, reducing the energy drawn from the grid from the what it would be without solar (grey dotted line) to a new, lower
                                curve (solid black line). Excess energy that is generated by the solar array that cannot be directly consumed must be sold back to the grid.",
                                hr()
                            ),
                            div(class = "monthPlotBox", 
                                div(class = "monthPlotHead", 
                                    "Electric Load with Solar and Storage"), 
                                div(class = "monthPlot", 
                                    div(class = "row",
                                        plotOutput("monthPlot_Batt.csf"),
                                        tags$img(src = "RSF_Month_Legend.png", style = "height:160px; margin:70px 10px;")
                                    )
                                )
                            ),
                            p(class = "monthPlotCaption", 
                                "Adding energy storage to the situation above allows the user to store excess energy generated by the solar panels that cannot be used as it
                                is generated. This excess energy can then be used later, after solar generation has dipped below energy consumption. Here, the light blue area
                                represents the additional amount of energy that can be used on average when using energy storage, further reducing the amount of energy drawn
                                from the grid (solid black line). This use case can create economic benefit for the user if the rate at which they are paid for exporting excess
                                electricity to the grid is lower than the rate they pay for electricity. If these rates are the same (i.e. net metering), then no financial benefit
                                is achieved."
                            )
                           )}  # Solar Firming
                        
                       )}, # Commercial Monthly Load Curve
                    {tabPanel(style = "width:900px;", "Bill Comparison", 
                        p(class = "section-subheader", 
                            "Comparison of Monthly and Yearly Bills:"),
                        
                        {conditionalPanel(condition = "input.UseCase_comm == 'CTU'",
                            tableOutput("BillComp.ctu"),
                            
                            hr(),
                            div(class = "row", style = "height:470px; padding: 0 25px;",
                                
                                {div(class = "financeCard", style = "height:470px; margin: 0 15px 0 20px;",
                                     p(class = "section-subheader center",
                                       "Battery Storage System Financial Data"),
                                     
                                     div(class = "financeBox",
                                         htmlOutput(class = "center bold", "YearlySavings.ctu")),
                                     p("Potential Yearly Savings:"),
                                     
                                     div(class = "financeBox",
                                         htmlOutput(class = "center bold", "batteryCost.ctu")),
                                     p("Total Upfront Cost:"),
                                     sliderInput(inputId = "BattCost.ctu",
                                                 label = NULL,
                                                 min = 20000, max = 200000,
                                                 value = 50000, step = 5000,
                                                 width = "100%", pre = "$"),
                                     
                                     div(class = "financeBox",
                                         htmlOutput(class = "center bold", "expLife.ctu")),
                                     p("Expected Useful Life:"),
                                     sliderInput(inputId = "BattLife.ctu",
                                                 label = NULL,
                                                 min = 5, max = 25,
                                                 value = 20, step = 5,
                                                 width = "100%", post = " years"),
                                     
                                     hr(class = "darkGreyLine"),
                                     
                                     p(class = "center", 
                                       "Employ a discount rate for savings calculations?"),
                                     div(class = "row discRateSwitch",
                                         p("No"),
                                         div(style = "margin:0 10px;",
                                             tags$label(class = "switch",
                                                        tags$input(type = "checkbox", id = "toggle-ctu"),
                                                        tags$span(class = "slider round")
                                             )
                                         ),
                                         p("Yes")
                                     ),
                                     
                                     div(class = "financeBox",
                                         htmlOutput(class = "center bold", outputId = "discountRate.ctu")),
                                     p("Discount Rate:"),
                                     sliderInput(inputId = "discRate.ctu",
                                                 label = NULL,
                                                 min = 0, max = 10,
                                                 value = 0, step = 0.5,
                                                 width = "100%", post = "%")
                                     
                                )}, # Financial Data and Slider Box
                                {div(class = "billCompText", style = "padding: 0 5px;",
                                     p(class = "section-subheader",
                                       "Evaluating the Effects of Battery Energy Storage"),
                                     p(class = "indent",
                                       "The table above compares the monthly and yearly bills for a sample commercial customer with and without energy storage, using both flat-rate,
                                       non-demand-metered pricing and time-of-use rate design. The two most significant columns to compare are shaded in grey, comparing a standard bill without
                                       energy storage and a time-of-use bill with energy storage. This represents the potential savings of a storage device engaged in time-of-use rate
                                       management. It should be noted that the total energy consumption in kilowatt-hours (two far-right columns) is greater when a storage device is used
                                       because of round-trip inefficiency."
                                     ),
                                     p(class = "indent",
                                       "The top line in the box to the left shows the estimated yearly savings calculated from the table above. When taken alongside the upfront cost and
                                       the expected useful life of the battery, it is possible to estimate if and when the energy savings can offset the cost and create positive net value.
                                       This is shown graphically below, with green or red vertical bars representing lifetime net savings or cost."
                                     )
                                     )}  # Text Description Box
                            ),
                            
                            hr(),
                            p(class = "column-header", "Break-Even Analysis for Time-of-Use Rate Management"),
                            div(style = "margin-left:25px;",
                                plotOutput("PaybackPlot.ctu", width = "850px")
                            )
                            
                            
                           )}, # Time-of-Use
                        {conditionalPanel(condition = "input.UseCase_comm == 'CPS'",
                            tableOutput("BillComp.cps"),

                            {div(class = "row centerBox billCompSliderRow", style = "min-width: 836px; max-width: 836px; height: 120px;",
                                
                                {div(style = "width:250px; height:100%; border: 1px solid #e3e3e3; border-radius: 2px;",
                                    p(class = "center", style = "font-weight:bold; font-size:14px; margin-top:0px; margin-bottom:0;",
                                        "Per kWh Rate"),
                                    div(class = "row",
                                        p(style = "font-size:12px; margin:5px 0 25px 60px;",
                                            "Year-Round:"),
                                        div(style = "position: relative; background-color: #dddddd; width: 80px; height: 20px; margin:6px 0 2px 10px; padding: 0;",
                                            htmlOutput("Usage_Rate", class = "center", style = "font-weight:bold; font-size:11px;"))),
                                    div(style = "margin:0 5px;",
                                        sliderInput(inputId = "kWh_Rate",
                                                    label = NULL,
                                                    min = 0, max = 20,
                                                    value = 3.5, step = 0.5,
                                                    width = "100%", ticks = FALSE, 
                                                    post = "¢ / kWh")
                                    )
                                   )}, # Per kWh Charge Rate Selection
                                {div(style = "width:250px; border: 1px solid #e3e3e3; border-radius: 2px; height:100%; margin-left:5px;",
                                    p(class = "center", style = "font-weight:bold; font-size:14px; margin-top:0px; margin-bottom:0;",
                                        "Demand Charge Rates"),
                                    div(class = "row",
                                        p(style = "font-size:12px; margin:5px 0 0 30px; lineheight:15px;",
                                            "Summer (June-Sept):"),
                                        div(style = "position: relative; background-color: #dddddd; width: 85px; height: 20px; margin:6px 0 2px 10px; padding: 0;",
                                            htmlOutput("Summer_Rate", class = "center", style = "font-weight:bold; font-size:11px;")
                                        )
                                    ),
                                    div(class = "row",
                                        p(style = "font-size:12px; margin:0 0 2px 30px;",
                                            "Winter (Oct-May):"),
                                        div(style = "position: relative; background-color: #dddddd; width: 85px; height: 20px; margin:2px 0 0 30px; padding: 0;",
                                            htmlOutput("Winter_Rate", class = "center", style = "font-weight:bold; font-size:11px;")
                                        )
                                    ),
                                    div(style = "margin:0 5px;",
                                        sliderInput(inputId = "Demand_Charge_Rate",
                                                    label = NULL,
                                                    min = 0, max = 10,
                                                    value = 5, step = 0.5,
                                                    width = "100%", ticks = FALSE)
                                    )
                                   )}, # Demand Charge Rate Selection
                                {div(style = "width:325px; height:100%; margin-left:15px;",
                                    p(class = "caption",
                                        strong("Note:"),
                                        "Standard Bill column refers to the bill assessed for commercial non-demand metered service at rates of 9.256¢ per kWh
                                        in the summer and 7.757¢ per kWh in the winter.",
                                        br(), br(),
                                        "Total Bill is the sum of the consumption cost assessed per kilowatt-hour and the demand charge assessed per kilowatt.")
                                )}  # Plot Caption
                            )}, # Middle Row - Rate Sliders and Caption
                            
                            hr(),
                            div(class = "row", style = "height:470px; padding: 0 25px;",
                                {div(class = "financeCard", style = "height:470px; margin: 0 15px 0 20px;",
                                     p(class = "section-subheader center",
                                       "Battery Storage System Financial Data"),
                                     
                                     div(class = "financeBox",
                                         htmlOutput(class = "center bold", "YearlySavings.cps")),
                                     p("Potential Yearly Savings:"),
                                     
                                     div(class = "financeBox",
                                         htmlOutput(class = "center bold", "batteryCost.cps")),
                                     p("Total Upfront Cost:"),
                                     sliderInput(inputId = "BattCost.cps",
                                                 label = NULL,
                                                 min = 20000, max = 200000,
                                                 value = 50000, step = 5000,
                                                 width = "100%", pre = "$"),
                                     
                                     div(class = "financeBox",
                                         htmlOutput(class = "center bold", "expLife.cps")),
                                     p("Expected Useful Life:"),
                                     sliderInput(inputId = "BattLife.cps",
                                                 label = NULL,
                                                 min = 5, max = 25,
                                                 value = 20, step = 5,
                                                 width = "100%", post = " years"),
                                     
                                     hr(class = "darkGreyLine"),
                                     
                                     p(class = "center", 
                                       "Employ a discount rate for savings calculations?"),
                                     div(class = "row discRateSwitch",
                                         p("No"),
                                         div(style = "margin:0 10px;",
                                             tags$label(class = "switch",
                                                        tags$input(type = "checkbox", id = "toggle-cps"),
                                                        tags$span(class = "slider round")
                                             )
                                         ),
                                         p("Yes")
                                     ),
                                     
                                     div(class = "financeBox",
                                         htmlOutput(class = "center bold", outputId = "discountRate.cps")),
                                     p("Discount Rate:"),
                                     sliderInput(inputId = "discRate.cps",
                                                 label = NULL,
                                                 min = 0, max = 10,
                                                 value = 0, step = 0.5,
                                                 width = "100%", post = "%")
                                     
                                )}, # Financial Data and Slider Box
                                {div(class = "billCompText", style = "padding: 0 5px;",
                                    p(class = "section-subheader",
                                        "Evaluating the Effects of Battery Energy Storage"),
                                    p(class = "indent",
                                        "The table above depicts the monthly and yearly bills for a sample commercial or industrial utility customer. The far left column calculates the electricity bill
                                        if they were charged on a flat-rate per-kilowatt-hour structure. The 'No Battery' and 'With Battery' sections show bill components for demand-metered
                                        rates with and without a battery performing demand-charge management to reduce peak load events. Each of these sections have 'kWh Charge' and 'Demand Charge' sections
                                        which show the two components that are added together to comprise the total bill, shaded in grey. Note that the kWh charges are greater when a battery is
                                        used because of the increase in total energy use, but the demand charge is reduced by a sizeable amount. Usage and demand charge rates can be adjusted by the sliders
                                        below the table."
                                    ),
                                    p(class = "indent",
                                        "Using the data generated in the able above and additional information provided to the left, it is possible to estimate the total net cost or savings for the lifetime
                                        of the storage device. This information is presented in the break-even analysis figure below."
                                    )
                                )}
                            ),  # Text Description Box
                            
                            hr(),
                            p(class = "column-header", "Break-Even Analysis of Demand-Charge Management Use Case"),
                            div(style = "margin-left:25px;",
                                plotOutput("PaybackPlot.cps", width = "850px")
                            )
                            
                          )}, # Peak Shaving
                        {conditionalPanel(condition = "input.UseCase_comm == 'CSF'",
                                         tableOutput("BillComp.csf"),
                            
                            {div(class = "row centerBox billCompSliderRow", style = "min-width: 810px; max-width: 800px; height: 150px;",
                                {div(class = "lightGreyBorder", style = "width:250px;",
                                    p(class = "center BCLabel",
                                        "Billing Format:"),
                                    div(class = "radioMeter", 
                                        radioGroupButtons(inputId = "MeterType_csf",
                                                          label = NULL,
                                                          individual = TRUE, justified = TRUE,
                                                          choiceNames = c("Demand-Metered", "Non-Demand"),
                                                          choiceValues = c("Demand", "Non_Demand"),
                                                          selected = "Non_Demand", size = "sm")
                                    ),
                                    hr(style = "margin:0 5px;"),
                                    conditionalPanel(condition = "input.MeterType_csf == 'Demand'",
                                        div(class = "row",
                                            p(class = "rateLabelCsf",
                                                "Usage Rate:"),
                                            div(class = "rateBox", style = "margin:3.5px 0 2px 69px;",
                                                p("3.41¢ per kWh", class = "center bold elevenPt"))),
                                        div(class = "row",
                                            p(class = "rateLabelCsf", style = "margin-top:5px;",
                                                "Summer Demand Rate:"),
                                            div(class = "rateBox", style = "margin:4px 0 2px 10px;",
                                                p("$14.79 per kW", class = "center bold elevenPt"))),
                                        div(class = "row",
                                            p(class = "rateLabelCsf", style = "margin-top:5px;",
                                              "Winter Demand Rate:"),
                                            div(class = "rateBox", style = "margin:3px 0 2px 21px;",
                                                p("$10.49 per kW", class = "center bold elevenPt")))
                                    ),
                                    conditionalPanel(condition = "input.MeterType_csf == 'Non_Demand'",
                                        div(class = "row", style = "margin-top: 10px;",
                                            p(class = "rateLabelCsf",
                                                "Summer Rate:"),
                                            div(class = "rateBox", style = "margin:3px 0 2px 59px;",
                                                p("9.26¢ per kWh", class = "center bold elevenPt"))),
                                        div(class = "row", style = "margin-top: 5px;",
                                            p(class = "rateLabelCsf",
                                                "Winter Rate:"),
                                            div(class = "rateBox", style = "margin:3px 0 2px 69px;",
                                                p("7.76¢ per kWh", class = "center bold elevenPt", style = "font-size:11px;")))
                                    )
                                )}, # Rate Type Selection and Rate Displays
                                {div(class = "lightGreyBorder", style = "width:320px; margin-left:5px;",
                                    p(class = "center BCLabel",
                                        "Net Metering Compensation Rate:"),
                                    
                                    conditionalPanel(condition = "input.MeterType_csf == 'Demand'",
                                        div(class = "row", style = "margin:2px;",
                                            div(style = "width:100%;",
                                                p(class = "center rateLabel", 
                                                    "Year-Round Rate:"),
                                                div(class = "rateBox centerBox",
                                                    htmlOutput("NEMRateDemand.csf", class = "center bold elevenPt")
                                                )
                                            )
                                        )
                                    ),
                                        
                                    conditionalPanel(condition = "input.MeterType_csf == 'Non_Demand'",
                                        div(class = "row", style = "margin:2px 10%;",
                                            div(style = "width:50%;",
                                                p(class = "center rateLabel", 
                                                    "Summer Rate:"),
                                                div(class = "rateBox centerBox",
                                                    htmlOutput("NEMRateSummer.csf", class = "center bold elevenPt"))
                                            ),
                                            div(style = "width:50%;",
                                                p(class = "center rateLabel", 
                                                    "Winter Rate:"),
                                                div(class = "rateBox centerBox",
                                                    htmlOutput("NEMRateWinter.csf", class = "center bold elevenPt"))
                                            )
                                        )
                                    ),
                                    div(style = "width:100%; margin: 15px 10px 0;",
                                    sliderInput(inputId = "NetMeterRate.csf",
                                                label = NULL,
                                                min = 0, max = 100, 
                                                value = 50, step = 5,
                                                post = "%")
                                    )
                                )}, # Net Metering Rate Selection Slider
                                {div(style = "width:230px; margin-left:15px;",
                                    p(class = "caption",
                                        strong("Note:"),
                                        "Net-Metered Bill refers to the bill that would be assessed if energy returned to the grid were compensated at the full retail rate.",
                                        br(), br(),
                                        "The Adjusted Bill takes into account the reduced compensation for electricity returned to the grid as indicated in the figure to the left."
                                    )
                                )}  # Table Caption
                            )}, # Second Row - Rate Selection and Caption
                            hr(),
                            {div(class = "row", style = "height:490px; padding: 0 25px;",
                                 
                                 {div(class = "financeCard", style = "height: 490px; margin: 0 15px 0 20px;",
                                      p(class = "section-subheader center",
                                        "Battery Storage System Financial Data"),
                                      
                                      div(class = "row", style = "margin-left:0px;",
                                          p("Subject of ROI:"),
                                          div(class = "radioPlot", style = "width:270px; margin-top:-4px;",
                                              radioGroupButtons(inputId = "ROI_Subj.csf",
                                                                label = NULL,
                                                                individual = TRUE, justified = TRUE,
                                                                choiceNames = c("Solar & Storage", "Storage Only"),
                                                                choiceValues = c("Both", "Storage"),
                                                                selected = "Both", size = "sm")
                                          )
                                      ),
                                      
                                      div(class = "financeBox",
                                          htmlOutput(class = "center bold", "YearlySavings.csf")),
                                      p("Potential Yearly Savings:"),
                                      
                                      div(class = "financeBox",
                                          htmlOutput(class = "center bold", "batteryCost.csf")),
                                      p("Total Upfront Cost:"),
                                      sliderInput(inputId = "BattCost.csf",
                                                  label = NULL,
                                                  min = 20000, max = 200000,
                                                  value = 50000, step = 5000,
                                                  width = "100%", pre = "$"),
                                      
                                      div(class = "financeBox",
                                          htmlOutput(class = "center bold", "expLife.csf")),
                                      p("Expected Useful Life:"),
                                      sliderInput(inputId = "BattLife.csf",
                                                  label = NULL,
                                                  min = 5, max = 25,
                                                  value = 20, step = 5,
                                                  width = "100%", post = " years"),
                                      hr(class = "darkGreyLine"),
                                      
                                      p(class = "center", 
                                        "Employ a discount rate for savings calculations?"),
                                      div(class = "row discRateSwitch",
                                          p("No"),
                                          div(style = "margin:0 10px;",
                                              tags$label(class = "switch",
                                                         tags$input(type = "checkbox", id = "toggle-csf"),
                                                         tags$span(class = "slider round"))),
                                          p("Yes")
                                      ),
                                      
                                      div(class = "financeBox",
                                          htmlOutput(class = "center bold", outputId = "discountRate.csf")),
                                      p("Discount Rate:"),
                                      sliderInput(inputId = "discRate.csf",
                                                  label = NULL,
                                                  min = 0, max = 10,
                                                  value = 0, step = 0.5,
                                                  width = "100%", post = "%")
                                      
                                 )}, # Financial Data and Slider Box
                                 {div(class = "billCompText", style = "padding: 0 5px;",
                                      p(class = "section-subheader",
                                        "Evaluating the Effects of Battery Energy Storage"),
                                      p(class = "indent",
                                        "The table above compares the monthly and yearly bills for a sample commercial or industrial customer without any solar or storage, with on-site solar,
                                        and with solar and storage. The standard bill in the far left column is calculated with traditional flat-rate pricing. Each of the solar and
                                        solar plus storage examples report the amount of energy over-generated from the solar panels and returned to the grid through net metering, the electricity
                                        bill if returned electricity is compensated at the full retail rate, and the bill if returned electricity is compensated below the retail rate. The 'Net Metering
                                        Compensation Rate' figure below the table shows the retail and net-metered prices for electricity throughout the year and allows you to adjust the compensation rate."
                                      ),
                                      p(class = "indent",
                                        "Notice that using a demand-metered rate structure (under 'Billing Format') significantly reduces the savings of the storage device. Organizations with demand-metered 
                                        rates should employ a battery control system that takes this into account when designing device behavior. This underscores the importance of using the right use case 
                                        to get the maximum value from a storage device."
                                      )
                                      )}  # Text Description Box
                                 
                                 
                            )}, # Third Row - Financial Data and Text Card
                            
                            hr(),
                            div(style = "margin-left:25px;",
                                plotOutput("PaybackPlot.csf", width = "850px")
                            )
                            
                          )}  # Solar Firming
                        
                       )}, # Commercial Bill Comparison
                    {tabPanel("Generation Resources", 
                        p(class = "section-subheader", "Generation Resource Use and Carbon Accounting"),
                        {div(class = "row", style = "height:640px; margin:0;",
                            div(class = "column left generation",
                                div(class = "gen-box",
                                    div(class = "box-header", "MISO-North Average Generation Profile:"),
                                    tags$img(src="Gen_Plot3.png", style = "margin: 10px 0px; height:590px;")
                                )
                            ),
                            div(class = "column right generation",
                                div(class = "gen-box",
                                    div(class = "box-header", "Average Load Profile:"),
                                    conditionalPanel(condition = "input.UseCase_comm == 'CTU'", style = "margin: 5px 10px;",
                                        plotOutput("GenPlot.ctu", width = "95%", height = "590px")),
                                    conditionalPanel(condition = "input.UseCase_comm == 'CPS'", style = "margin: 5px 10px;",
                                        plotOutput("GenPlot.cps", width = "95%", height = "590px")),
                                    conditionalPanel(condition = "input.UseCase_comm == 'CSF'", style = "margin: 5px 10px;",
                                        plotOutput("GenPlot.csf", width = "95%", height = "590px")
                                    )
                                )
                            )
                        )}, # Top Row of Plots
                        hr(),
                        {div(style = "width:815px; height:110px;",
                            p(class = "column-header", 
                                "Carbon Accounting and Social Cost Determination"),
                            p(class = "body-text", style = "text-indent: 40px;",
                                "Two major motivations behind energy storage and other grid innovations include improved system efficiency and the reduction 
                                of greenhouse gas and criterion pollutant emissions from electric generation and service. However, storage represents a much 
                                more complicated path towards decarbonization than does distributed generation, like solar PV.")
                        )}, # Middle Row of Text
                        {div(class = "row", style = "height:540px; margin:0;",
                             
                            {div(class = "column left generation",
                                div(style = "height: 540px",
                                    strong(style = "font-size:12px;",
                                        "Daily Emission Rate Profile"),
                                    p(class = "body-text indent",
                                        "The onset of vast amounts of variable energy resources (mostly wind) in recent years has changed the profile of electric 
                                        generation. As seen above on the left, wind is most productive early in the morning and late at night, and is least 
                                        productive in the middle of the day. Fossil fuel generation is adjusted to compensate for these fluctuations, which leads 
                                        to an emission profile wherein more pollutants are emitted per megawatt during the day than at night."),
                                    #strong(style = "font-size:12px;",
                                    #    "Subtitle"),
                                    p(class = "body-text indent", style = "text-indent: 40px;",
                                        "Many common energy storage use cases aim to reduce load during peak times. Because peak hours correspond with times of high
                                        emission rates, these use cases have the secondary effect of reshaping the load curve to more closely resemble the renewable
                                        resource generation profile than that of fossil fuels. (See top right)"),
                                    strong(style = "font-size:12px;",
                                        "Effects on Generation Attributes and Impacts"),
                                    p(class = "body-text indent",
                                        "Based on the ability of energy storage to reshape load curves and the coincidence of peak times and high carbon emission rates,
                                        many storage use cases facilitate a greater proportional use of renewable and clean energy resources. Depending on the incorporation
                                        and optimization of new renewable generation resoruces and the efficiency of the storage device, energy storage can have wide-ranging
                                        effects on total energy consumption and overall emissions, as seen in the table to the right.")
                                )
                            )}, # Left Column of Text
                             
                            {div(class = "column right generation",
                                div(style = "border: 1px solid white; height: 540px; background-color: #efeadc;",
                                    p(class = "section-subheader",
                                        "Carbon Accounting and Social Cost Determination:"),
                                    conditionalPanel(condition = "input.UseCase_comm == 'CTU'",
                                                      tableOutput("Generation.ctu")),
                                    conditionalPanel(condition = "input.UseCase_comm == 'CPS'",
                                                      tableOutput("Generation.cps")),
                                    conditionalPanel(condition = "input.UseCase_comm == 'CSF'",
                                                      tableOutput("Generation.csf")
                                    ),
                                     
                                    div(style = "margin: 25px 10px;",
                                        p(class = "section-subheader", 
                                            "Social Cost of Carbon:"),
                                        sliderInput(inputId = "SCC.comm",
                                                    label = NULL,
                                                    min = 0, max = 50,
                                                    value = 15, step = 5, 
                                                    pre = "$", post = " / ton",
                                                    width = "100%")
                                    ),
                                    hr(style = "border-color: darkgrey; margin:0 10px 25px;"),
                                    div(style = "margin: 0 15px;", 
                                        conditionalPanel(condition = "input.UseCase_comm != 'CSF'",
                                            p(class = "caption",
                                                "* Employing common energy storage devices for use cases which predominantly shift load and electricity purchases
                                                from one time to another, whether to reduce peak events, reduce costs through time-of-use rate designs, or to shift
                                                load to times when renewable resources make up a greater proportion of overall generation, can often", em("increase"),
                                                "attributed carbon emissions. In these cases, the inefficiency of the battery outweighs the difference in rate of 
                                                carbon emissions from one time to another.")
                                        ),
                                        conditionalPanel(condition = "input.UseCase_comm == 'CSF'",
                                            p(class = "caption",
                                                "* Employing distributed solar PV without enough storage capacity to retain 100% of generation typically results in
                                                the sale of some amount of electricity back to the grid. While this contributes 'clean' and renewable energy to the
                                                grid, it is not considered in carbon accounting calculations. Rather, all electricity that is bought from the grid
                                                is considered to have the generation mix and emissions attributes of the local grid as a whole.")
                                        )
                                    )
                                )
                            )}  # Generation Table Output Card 
                        )} # Bottom Row - Text and Gen Table

                       )}  # Commercial Generation Resources
                    
                ) # End of Commercial Main Column Tabset Panel
            ) # End of Main Column
        ) # End of Row
    ) # End of Commercial Tab
  )}, # Commercial Page

### BEGINNING OF GUIDEBOOK PAGE ###

  {hidden(  
    div(id = "Guidebook", class = "tabcontent",
        div(class = "row",
            {div(class = "column left intro",
                div(class = "sidenav", style = "position: absolute;",
                    tags$a(class = "tablink3 activeSidebar", id = "tablink3-1",
                        "Purpose and Use Case"),
                    tags$a(class = "tablink3", id = "tablink3-2",
                        "Device Type and Capacity Needs"),
                    tags$a(class = "tablink3", id = "tablink3-3",
                        "Auxiliary Equipment Requirements"),
                    tags$a(class = "tablink3", id = "tablink3-4",
                        "Warranty Availability"),
                    tags$a(class = "tablink3", id = "tablink3-5",
                        "Financing Options"),
                    tags$a(class = "tablink3", id = "tablink3-6",
                        "Operations and Maintenance Costs")
                ) # End of Guidebook Page Sidenav
            )}, # Guidebook Page Left Index Column
            
            {div(class = "column main guidebook", id = "Guide-1", style = "min-width:950px; max-width:950px;",
                p(class = "section-header", 
                    "Identifying the Purpose and Selecting the Use Case"),
                hr(),
                div(style = "padding: 0 25px;",
                    p(class = "body-text indent",
                        "The starting point for any energy storage device installation should be to clarify the purpose or purposes it is meant to serve.
                        Subsequent decisions regarding technology/chemistry selection, battery capacity, auxilliary equipment, etc. all depend on the general
                        purpose of the device. It is important to note that in some cases, multiple use cases can be employed, but this may hinder the effectiveness
                        of the device in performing each individual application, depending on battery capacity and other characteristics.", br()),
                    strong("Considering the following questions may help with this process. Click on an arrow for follow-up questions and more information.")),
                
                {div(class = "row", style = "padding-left: 40px; margin-top:30px;",
                    {div(style = "background-color: #d6dce5; width: 31%; padding:10px 20px; height: 260px; border-radius:10px;",
                        p(class = "center", style = "font-size: 14px;",
                            "Do you want to save money on energy bills by shifting when electricity is being drawn from the grid?"),
                        div(style = "margin: 10px 0 0; width: 247px; height: 149px;",
                            tags$img(src = "EnergyShift.png", height = "149px", width = "247px")
                        ),
                        tags$i(id = "down_timeshift", class = "fa fa-chevron-down", style = "position: absolute; font-size: 22px; left: 395px;"),
                        hidden(tags$i(id = "up_timeshift", class = "fa fa-chevron-up", style = "position: absolute; font-size: 22px; left: 395px;"))
                    )}, # Time-Shifting
                    {div(style = "background-color: #d6dce5; width: 31%; padding:10px 20px; height: 260px; border-radius:10px; margin-left: 10px;",
                        p(class = "center", style = "font-size: 14px;", 
                          "Do you have a renewable energy system such as solar panels and want to get more value from them?"),
                        div(style = "margin: 10px 0 0; width: 247px; height: 149px;",
                            tags$img(src = "Solar_Array.jpg", height = "149px", width = "247px")
                        ),
                        tags$i(id = "down_solar", class = "fa fa-chevron-down", style = "position: absolute; font-size: 22px; left: 690px;"),
                        hidden(tags$i(id = "up_solar", class = "fa fa-chevron-up", style = "position: absolute; font-size: 22px; left: 690px;"))
                    )}, # Solar Optimization
                    {div(style = "background-color: #d6dce5; width: 31%; padding:10px 20px; height: 260px; border-radius:10px; margin-left: 10px;",
                        p(class = "center", style = "font-size: 14px;",
                          "Are you hoping to improve the reliability of your electric service in the event of power outages?"),
                        div(style = "margin: 10px 0 0; width: 247px; height: 149px;",
                            tags$img(src = "PowerOutage.png", height = "149px", width = "247px")
                        ),
                        tags$i(id = "down_resil", class = "fa fa-chevron-down", style = "position: absolute; font-size: 22px; left: 985px;"),
                        hidden(tags$i(id = "up_resil", class = "fa fa-chevron-up", style = "position: absolute; font-size: 22px; left: 985px;"))
                    )}  # Resiliency
                )}, # Top Row
                
                {div(class = "row", style = "padding-left: 40px; margin-top:10px;",
                    {hidden(div(id = "timeshift_box", style = "width: 31%; padding:10px 20px; border-radius:10px; box-shadow:0 4px 8px 0 rgba(0,0,0,0.2);",
                        p(class = "center", style = "font-size: 14px;",
                            strong("Time-Shifting:"),
                            tags$li("Do you have a demand-metered or time-of-use rate structure?"),
                            tags$li("Do demand charges make up a significant portion of your bill?"),
                            tags$li("Does your electricity use follow predictable patterns or trends?")
                        ),
                        hr(),
                        p(class = "body-text",
                            "Employing time-shifting to create value for energy storage relies on a customer having a rate structure which accomodates it. This generally means having 
                            time-of-use or demand-metered rate structures. Customers whose demand charges make up a large portion of their bill and whose electricity use follows predictable
                            daily or weekly trends are good candidates for", tags$b("demand-charge management"), ". For customers who have time-of-use rate structures and have a significant
                            portion of their overall electricity consumption during peak hours, ", strong("time-of-use management"), "may be a good option.")
                    ))}, # Question 1 - Time-Shifting
                    hidden(div(class = "solar_box", style = "width: 284.5px; height:565.4px;")),
                    {hidden(div(class = "solar_box", style = "width: 284.5px; height:565.4px; padding:10px 20px; border-radius:10px; box-shadow:0 4px 8px 0 rgba(0,0,0,0.2); position: absolute; left: 557.4px; top: 604.4px;",
                        p(class = "center", style = "font-size: 14px;",
                            strong("Solar Optimization:"),
                            tags$li("Does your solar array overproduce relative to building energy use and export electricity to the grid?"),
                            tags$li("When you return electricity to the grid, is it net-metered at or near the retail rate or significantly below it?")
                        ),
                        hr(),
                        p(class = "body-text",
                            "Many customers who have installed solar arrays on their property want to use as much of the power they generate as possible.
                            Energy storage devices are capable of optimizing solar resources by storing excess generation and using it later when the sun is no
                            longer shining. However, the economic and energy efficiency of solar-plus-storage depends on rate structures. If your net-metering rate
                            is at or near the retail rate, there is no financial incentive, but for customers who have solar arrays larger than 40 kW and/or have low net-metering
                            rates, ", strong("solar firming"), "can reduce energy costs.")
                        ))}, # Question 2 - Solar-Firming
                    hidden(div(class = "resil_box", style = "width: 284.5px; height:565.4px;")),
                    {hidden(div(class = "resil_box", style = "width: 284.5px; height:565.4px; padding:10px 20px; border-radius:10px; box-shadow:0 4px 8px 0 rgba(0,0,0,0.2); position: absolute; left: 852.4px; top: 604.4px;",
                        p(class = "center", style = "font-size: 14px;",
                            strong("Resiliency:"),
                            tags$li("Do you experience frequent power outages or power quality problems?"),
                            tags$li("Do power outages result in a loss of revenue or other financial cost?"),
                            tags$li("Do you have a fossil fuel-powered generator for backup power?")
                        ),
                        hr(),
                        p(class = "body-text",
                            "If you experience frequent power outages which result in financial losses or hinder the provision of services, employing energy storage for",
                            strong("backup power and resiliency"), "may be beneficial. Energy storage can reserve some charged capacity, which can be discharged during power outages
                            to serve 'critical load,' or a selection of electricity uses in a building which are deemed critically important. This can replace the need to
                            use a gas- or diesel-powered generator for backup power, and reduces the emission of carbon dioxide and other pollutants from those generators.")
                    ))}  # Question 3 - Resiliency
                )}, # Description Boxes for Top Row
                
                {div(class = "row", style = "padding-left: 40px; margin-top: 10px;",
                    {div(style = "background-color: #d6dce5; width: 47%; padding:9px 20px; height: 187px; border-radius:10px;",
                        div(class = "row",
                            p(class = "center", style = "font-size: 14px; width: 170px; padding: 5px 10px 0 15px;",
                                "Do you want to reduce your greenhouse gas emissions or contribute to the decarbonization of Minnesota's energy sector?"),
                            div(style = "margin: 10px 0; width: 237px; height: 149px;",
                                tags$img(src = "CO2_Emissions.png", height = "149px", width = "237px")
                            )
                        ),
                        tags$i(id = "down_emissions", class = "fa fa-chevron-down", style = "position: absolute; font-size: 22px; left: 345px; margin-top: -20px;"),
                        hidden(tags$i(id = "up_emissions", class = "fa fa-chevron-up", style = "position: absolute; font-size: 22px; left: 345px; margin-top: -20px;"))
                    )}, # Carbon Emissions
                    {div(style = "background-color: #d6dce5; width: 47%; padding:9px 20px; height: 187px; border-radius:10px; margin-left: 10px;",
                        div(class = "row",
                            div(style = "margin: 10px 0 0 10px; width: 240px; height: 156px;",
                                tags$img(src = "Microgrid7.png", height = "156px", width = "240px")
                            ),
                            p(class = "center", style = "font-size: 14px; width: 170px; padding: 5px 10px 0 15px;",
                                "Is the goal of the storage installationt to disconnect from the grid entirely and/or to create a local microgrid?")
                        ),
                        tags$i(id = "down_microgrid", class = "fa fa-chevron-down", style = "position: absolute; font-size: 22px; left: 1035px; margin-top: -20px;"),
                        hidden(tags$i(id = "up_microgrid", class = "fa fa-chevron-up", style = "position: absolute; font-size: 22px; left: 1035px; margin-top: -20px;"))
                    )}  # Microgrids
                )}, # Bottom Row
                
                {div(class = "row", style = "padding-left: 40px; margin-top: 10px;",
                    {hidden(div(id = "emissions_box", style = "background-color: white; width: 47%; padding:10px 20px; border-radius:10px; box-shadow:0 4px 8px 0 rgba(0,0,0,0.2);",
                        p(class = "center", style = "font-size: 14px;",
                            strong("Pollutant Emissions:"),
                            tags$li("Do you have solar panels or some other renewable generation resource?"),
                            tags$li("What is the emission profile of your utility's mix of generation resources?"),
                            tags$li("Will the storage device replace a fossil fuel-powered resource such as a backup generator?")
                            ),
                            hr(),
                        p(class = "body-text",
                            "Determining the effect of energy storage use on greenhouse gas emissions is not straightforward and", strong("depends on how the
                            device is used."), "Using storage devices with imperfect round-trip efficiency causes customers to consume more electricity than they otherwise would have. 
                            Even if you charge the device at night when use of fossil fuels is at its lowest and renewable penetration is at its highest, the inefficiency of the
                            battery typically adds more emissions than the time-shifting saves. For most storage applications to decrease net carbon emissions, it will require
                            more efficient storage devices and cleaner electricity from the grid."),
                        p(class = "body-text",    
                            "On the other hand, if the storage device replaces a fossil-fuel resource, it can represent a significant reduction of 
                            emissions. For example, replacing a diesel-powered backup generator with a battery typically reduces emissions because the generation mix used to charge
                            the battery (either from the grid or from solar panels) creates fewer emissions than diesel. For larger-scale installations, battery storage devices can replace
                            inefficient and expensive natural gas peaker plants.")
                    ))}, # Question 4 - Emissions
                    hidden(div(class = "microgrid_box", style = "width: 47%; height: 641.4px;")),
                    {hidden(div(class = "microgrid_box", style = "background-color: white; width: 432.2px; padding:10px 20px; border-radius:10px; box-shadow:0 4px 8px 0 rgba(0,0,0,0.2); position:absolute; left: 704.4px;",
                        p(class = "center", style = "font-size: 14px;",
                            strong("Off-Grid Applications:"),
                            tags$li("What generation resources do you have and what is their general reliability/capacity factor?"),
                            tags$li("What type of facility are you powering (i.e. one building vs. large complex)?"),
                            tags$li("What auxiliary equipment are you planning to or have the capacity to use to create a microgrid?")
                        ),
                        hr(),
                        p(class = "body-text",
                            "Creating a microgrid that enables you to disconnect a building or group of buildings from the grid entirely is one of the more complex uses
                            of energy storage, but it is also one of the applications that creates the most interest and has great potential to revolutionize the energy
                            industry. Successful microgrids require reliable generation resources, backup generation if the main resource is inadequate for an extended 
                            period, and quite a bit of auxiliary equipment to manage energy generation, storage, and consumption, as well as controlling the connection to 
                            the grid, if there is such a connection."),
                        p(class = "body-text",
                            "Having an energy storage device that is the proper technology and size is one of the most important features of a successful microgrid. In these
                            instances, storage devices (typically batteries) are used similarly to", strong("optimizing solar generation,"), "in that it they charge when excess
                            energy is generated and discharge when the sun goes down or the wind stops blowing. However, energy produced from the distributed generation
                            resources is meant to provide", tags$i("all"), "of the electricity needed by the microgrid rather than just supplementing energy drawn from the grid.")
                    ))}, # Question 5 - Microgrids
                    br()
                )} # Description Boxes for Bottom Row
                
            )}, # Purpose and Use Case
            {hidden(
                div(class = "column main guidebook", id = "Guide-2", style = "min-width:950px; max-width:950px;",
                    p(class = "section-header", 
                        "Determining the Ideal Energy Storage Technology and Capacity Requirements"),
                    hr(),
                    p(class = "body-text indent",
                        "The type of storage device employed can have significant impact on its ability to perform the selected use case and to fulfill its intended purpose.
                        For a detailed description of several storage technologies, see the", 
                        strong(style = "font-style:italic;", "Energy Storage Technologies"),
                        "page under the",
                        strong(style = "font-style:italic;", "Introduction"), "tab."),
                    p(class = "section-subheader", "Battery Type Selection"),
                    p(class = "body-text indent",
                        "Often, the most cost-effective investment in energy storage is in the improvement of building envelope insulation. More efficient thermal storage
                        in a building reduces energy use for heating and cooling, corresponding to lower carbon and other pollutant emissions. Energy use is typically avoided
                        during times of high energy demand, such as summer afternoons when most buildings are running air conditioning equipment. This provides value by reducing
                        a building's peak energy use and its contribution to system-wide peak load events, since energy use reduction is typically greatest during times of high 
                        energy demand."),
                    div(class = "float-right", style = "padding: 10px; height: 540px; width: 420px;",
                        strong(style = "padding: 0 8px;", "Relative pros and cons of common battery chemistries:"),
                        tags$img(src = "BattComp.png", height = "500px", width = "400px")
                    ),
                    p(class = "body-text indent",
                        "For more active energy storage applications achievable for community-scale or residential customers, the most commonly used energy storage technology in
                        residential and community-scale applications is electrochemical battery energy storage systems. Selection of a particular battery chemistry can come down 
                        to a number of factors. Lead acid batteries are by far the least expensive option, but may require ongoing monitoring to ensure optimal function, and may 
                        need to be replaced after a few years of use. If funds available for an energy storage project are limited, or the device is only needed or wanted for a few 
                        years, then lead acid may be a good choice - particular one of the newer “advanced” lead acid battery designs. Additionally, if circular material flow and 
                        recyclability are significant concerns for you or your organization, lead-acid has a long history of recycling and reuse of battery materials. Lead acid batteries 
                        have long been used for off-grid operation or emergency backup power and would also fit well with an application that does not require frequent cycling or deep 
                        discharging, such as demand-charge management, potentially extending the battery’s useful life."),
                    p(class = "body-text indent",
                        "Lithium ion technology is currently the most common battery chemistry for stationary energy storage installations. This can be attributed to its advantageous mix 
                        of modest cost, high energy density (small footprint), and moderately long functional life. These balanced properties make lithium ion batteries suited to a wide 
                        range of use cases and applications, including all four described herein. Continued research and development in the electric vehicle industry have greatly contributed 
                        to the declining costs of lithium ion batteries and are expected to continue to drive lower costs and improved performance."),
                    p(class = "body-text indent",
                        "Redox flow batteries are a much newer technology than others in widespread use. As such, they make up a much smaller share of the energy storage market and typically 
                        have higher costs per unit of battery capacity. One particular advantage of flow batteries is the ability to select the power and energy capacities independently of 
                        each other. This enables batteries of longer duration than other technologies can typically achieve, which makes flow batteries advantageous for application in cases 
                        which benefit from long duration storage, such as integration of distributed renewable generation resources, backup power, or time-of use management.
                      "),
                    p(class = "section-subheader", "Determination of Battery Capacity"),
                    p(class = "body-text indent",
                      "In addition to the selection of battery chemistry, determining an appropriate battery capacity to meet the requirements of the selected use case(s) is critical in achieving 
                      the objectives of the storage application in an efficient, cost-effective manner. A device which is sized too small would be unable to provide the level of services necessary 
                      to meet project goals; meanwhile, one that is too large would be more expensive than necessary and likely would not generate the value necessary to offset the capital expense 
                      of the installation."),
                    div(class = "float-left", style = "float: left; width: 360px; height: 550px;",
                        strong(style = "margin: 0 60px;", "Marginal Value Estimation Analysis"),
                        tags$img(src = "BattCap.png", width = "360px", height = "530px")),
                    p(class = "body-text indent",
                      "Additionally, the ratio of power capacity to energy capacity can greatly influence the effectiveness of the battery in executing a particular use case. The figure to the left depicts a 
                      value estimation analysis of a theoretical battery engaged in demand-charge management on a particular load curve. The shade of each colored tile represents the relative 
                      marginal value for each added unit of battery capacity. Darker shades represent greater marginal value for each additional unit, while the black dashed lines represents fixed battery
                      durations or the ratio of power and energy capacity."),
                    div(style = "width: 400px; margin: -10px 500px -2px;", 
                        p(style = "font-size: 13px; font-style: italic", "Duration  =  Energy Capacity / Power Capacity")
                    ),
                    p(class = "body-text indent",
                      "The grey region of the plot represents 
                      ranges of power to energy ratios in which additional units of either power or energy capacity represent no added value. The shape of this plot is highly dependent on the 
                      characteristics of each individual load curve and on the use case being applied. Based on these factors, it is crucial to select a battery with characteristics that suit 
                      the particular application by achieving proper balance and magnitude of these specifications for efficient provision of the chosen services. Most vendors of energy storage 
                      devices or battery management systems are able to provide detailed analysis to assist in the selection of a use case or use cases and to size a battery storage system 
                      appropriately to maximize the potential value of the installation."),
                    p(class = "body-text indent",
                      "Batteries which are intended to optimize solar generation should be sized with consideration for the size of the solar array and the typical amount of energy that is 
                      generated in excess of building demand. If the battery is intended to charge only from the solar array, any energy over and above the expected exvess generation is unlikely 
                      to be used. Likewise, power capacity should be determined with an eye toward the largest amount of overgeneration expected, in order to ensure that the battery can use as much 
                      overgenerated electricity as possible, rather than exporting it to the grid.")
                    
                )
            )}, # Tech and Capacity
            {hidden(
                div(class = "column main guidebook", id = "Guide-3", style = "min-width:950px; max-width:950px;",
                    p(class = "section-header", 
                        "Auxiliary Equipment Requirements and Considerations"),
                    hr(),
                    p(class = "body-text indent",
                      "In addition to the battery or other storage device itself, there are a few additional requirements for the device to function properly. Selection of these 
                      components can have profound effects on the overall performance of the storage device. These auxiliary equipment requirements include the following:"),
                    hr(),
                    p(class = "section-subheader", 
                      "Power Inverter"),
                    p(class = "body-text indent",
                      "In addition to a battery management system, battery devices typically need to be connected through a power inverter to function. Load centers such as homes 
                      and businesses operate on AC power, while batteries use DC power to charge and discharge. An inverter converts between these two formats, allowing power to 
                      flow back and forth. Batteries typically do not include an inverter, and a compatible device must be purchased separately. Some systems, typically designed 
                      for small, residential installations, do come with built-in inverters. (Tesla’s Powerwall has a built-in inverter while the LG Chem RESU battery does not.)"),
                    p(class = "body-text indent",
                      "If the energy storage device is paired with a generation resource such as solar photovoltaic, the storage device can often be installed in one of two general 
                      ways: DC-coupled or AC-coupled. When AC-coupled, the battery storage device and the generation resource are each connected to an inverter to convert output to 
                      AC, before joining the two and connecting to the targeted source of load. DC-coupled devices on the other hand, are connected while still in DC 
                      state, before passing through an inverter to the building load. While AC-coupled systems allow more versatility in terms of placement of the storage 
                      and generation devices, DC coupled systems tend to be more efficient as they have less energy loss from electricity passing through inverters."),
                    tags$img(style = "margin-left: 80px;", src = "ACDC_Coupling.png", height = "275px", width = "782px"),
                    hr(),
                    p(class = "section-subheader", 
                      "Battery Management System (BMS)"),
                    p(class = "body-text indent",
                      "Batteries typically contain basic control systems which maintain key measurements and processes of the device within a safe operating range, preventing it from 
                      inflicting damage on itself through overcharging, overheating, or some other detrimental behavior. However, these systems usually are not designed to operate 
                      the storage device in the execution of any particular use case. A BMS is required to interface with the load and/or generation resource to enable use case 
                      execution. Some batteries (typically residential, such as the Tesla Powerwall) are purchased and installed with a BMS as part of the product package, while 
                      others require the purchase of a compatible management device. The BMS is in many ways the most important piece of an energy storage installation because 
                      without it, the device is unable to provide the desired services."),
                    tags$img(style = "margin-left: 150px;", src = "BMS.png", height = "300px", width = "600px"),
                    hr(),
                    p(class = "section-subheader", 
                      "Fire Safety Equipment"),
                    p(class = "body-text indent",
                      "Unfortunately, lithium ion batteries can be extremely flammable, due to the flammability of the lithium material and the high concentration of energy stored in
                      the cell. This combination has led to a range of outcomes from cell phone batteries burning up to utility-scale battery systems producing violent explosions.
                      However, these risks can be effectively mitigated using proper fire prevention strategies. These strategies typically entail four key aspects:", 
                      strong("Failure Prevention, Fire Detection, Fire Suppression, and Compartmentation.")),
                    p(class = "body-text indent",
                      "Fire prevention is simply the process of designing the battery cell to minimize the risk of thermal runaway events that are often the cause of overheating
                      and fires. During the information gathering stage of purchasing a lithium ion battery it is important to ask potential vendors about design and construction
                      features that serve as fire prevention measures. Fire detection involves rapid recognition of conditions that could lead to fires or the early stages of a fire.
                      The nature of thermal runaway events is that they escalate extremely rapidly as one exothermic reaction creates heat which accelerates another exothermic reaction,
                      which continues this cycle to disastrous effect. Early detection of these events is critical in minimizing risk of severe fires and explosions. Fire suppression
                      systems receive signals from detection systems and respond quickly to cool the battery and suppress the fire if it exists. Water mist is a common way to achieve
                      both of these aims. Finally, compartmentation is the design aspect of the battery that seals off each of the individual cells from each other so that if one cell
                      catches fire, it will not spread rapidly to each of the other cells in the unit.")
                )
            )}, # Auxiliary Equipment
            {hidden(
                div(class = "column main guidebook", id = "Guide-4", style = "min-width:950px; max-width:950px;",
                    p(class = "section-header", 
                        "Warranty Availability and Considerations"),
                    hr(),
                    p(class = "body-text indent",
                      "There are a number of different warranty and insurance options available from battery manufacturers to ensure battery storage devices operate properly for as 
                      long as possible. The simplest form is a", strong("product warranty,"), "which guarantees repairs in the event of defects in the device. There are also", strong("performance warranties,"), " 
                      which ensures that one or more of the four key attributes (energy and power capacity, availability, and round-trip efficiency) maintain certain levels of 
                      performance over time (i.e. 70 percent of the original capacity). Finally, there may also be an option of an", strong("energy throughput warranty,"), "which guarantees that 
                      the storage device delivers or discharges a certain amount of energy over the product’s lifespan."),
                    p(class = "body-text indent",
                      "Depending on the specifics of the storage system and the warranty options available, manufacturers may offer self-insurance, where the company itself bears the 
                      risks of the warranty they have offered. Manufacturers may also oversize the battery relative to the capacity specified in the sale. For example, a battery sold 
                      with 100 kilowatt-hours of nominal capacity may be built with 110 kilowatt-hours of actual capacity, so that as the battery experiences degradation over time, 
                      the apparent degradation relative to the nominal, purchased capacity appears less significant than the actual capacity degradation. This practice reduces the 
                      level of risk for performance and throughput warranties. Warranties are often contingent on certain battery use stipulations, such as use case(s) and/or 
                      cycle limits per day, month, or year. These conditions are often set because the frequency and depth of cycling, which can vary significantly depending on the 
                      use case(s) employed, have a significant impact on the degradation rate of battery capacities.")
                )
            )}, # Warranties Available
            {hidden(
                div(class = "column main guidebook", id = "Guide-5", style = "min-width:950px; max-width:950px;",
                    p(class = "section-header", 
                        "Financing Options and Challenges"),
                    hr(),
                    p(class = "body-text indent",
                      "Historically, developers and other purchasers of energy storage devices have relied on upfront self-funding of projects or captive lending arrangements with 
                      manufacturers to finance them. Banks and other lending institutions are typically hesitant to fund storage installations. They are unfamiliar with the 
                      technology and it has yet to establish a consistent record of cost-recovery and profitability. This is slowly changing with advances in modeling capabilities 
                      and an expanding record of implementation; however, this is largely on a large commercial or utility scale. Community-scale, small commercial, and residential 
                      energy storage have a far less extensive track record and often face challenges to cost-recovery, such as market access, rate design, economies of scale, and 
                      volatile tariff structures."),
                    p(class = "body-text indent",
                      "Furthermore, the availability of financing is highly dependent on the use case(s) employed by the device. At this point in time, due in part to limited value 
                      streams, demand-charge management is the primary means for cost-recovery among commercial installations and the main justification for approval of financing. 
                      This justification is strongest when demand charges are high, improving the ability to save money, which improves one’s ability to finance the installation. 
                      Storage installations for other uses such as backup power and resiliency, or in load centers with low demand charges or peak-hour consumption rates may have 
                      challenges securing financing for an energy storage installation."),
                    hr(),
                    p(class = "section-subheader", "Available Tax Incentives"),
                    p(class = "body-text indent",
                      "Under current law, there are generally two incentive mechanisms for energy storage installations. These include the federal Investment Tax Credit (ITC) 
                      and Modified Accelerated Cost Recovery System (MACRS). The ITC is typically used for renewable generation resources such as solar panels and allows owners 
                      to deduct a portion of the cost from their taxes. Up to 2019, this deduction was set at 30 percent, but this declined to 26 percent in 2020, 22 percent 
                      in 2021, and will drop to 10 percent from 2022 onward (for non-residential installations). If an energy storage device is charged with renewable energy from a 
                      solar array or other renewable generation resource, it may be eligible for the same ITC rebate amount. Energy Storage systems which are charged 75 percent 
                      or more from renewable resources are eligible for a portion of the full ITC equal to the fraction of renewable energy that they use."),
                    p(class = "body-text indent",
                      "While securing the ITC can represent significant savings on a costly storage system, committing to charge from solar generation has the potential to complicate 
                      the execution of certain use cases. For example, if a battery system is engaged in demand-charge management but experiences an extended period of dense cloud 
                      cover during key times, it may miss a peak that it is mean to be shaving, missing out on the savings that the battery is meant to be delivering. For this 
                      reason, some owners eschew the ITC altogether to focus on use case execution."),
                    p(class = "body-text indent",
                      "Energy storage devices both paired with and in the absence of renewable generation resources are eligible for MACRS unless they are owned by a public 
                      institution or other non-profit organization. This accounting mechanism allows owners to recover some of the capital cost of the device over time. Systems 
                      eligible for the ITC may employ a 5-year MACRS schedule, equivalent to savings of approximately 21 percent of the cost of the system. Those which are ineligible 
                      for the ITC can qualify for a 7-year MACRS timeframe, corresponding to 20 percent savings over those seven years.")
                )
            )}, # Financing Options
            {hidden(
                div(class = "column main guidebook", id = "Guide-6", style = "min-width:950px; max-width:950px;",
                    p(class = "section-header", 
                        "Operations and Maintenance Costs and Considerations"),
                    hr(),
                    p(class = "body-text indent",
                      "As with modeling and use case selection, operation and maintenance is much more complex for energy storage systems than it is for solar photovoltaic arrays. 
                      There are several reasons that contribute to this trend. First, storage devices are very complex systems with many moving parts. Maintenance involves the 
                      management of electrical, electromechanical, electrochemical, and thermal systems. Depending on battery chemistry and scale, maintenance may involve monitoring 
                      fluid levels, chemical concentrations, hosing and pump manifolds, and/or fire suppression systems. Additionally, control systems, firmware, and software are 
                      more complex because storage systems have more complex operational needs than solar arrays, which are designed primarily to convert light into electrical energy 
                      in the most efficient way possible."),
                    p(class = "body-text indent",
                      "Furthermore, the repercussions of maintenance practices vary between the two technologies. Poor maintenance may cause solar PV systems to lose efficiency or 
                      generation capacity. Often, any damage or detriment incurred from poor maintenance practices can be fixed by subsequent repairs or the replacement of a panel. 
                      On the other hand, poor maintenance of battery systems, especially lithium ion batteries, can lead to chemical leaks and contamination or thermal runaway events, 
                      which can either destroy the battery altogether or render it unable to function."),
                    hr(),
                    p(class = "section-subheader",
                      "Vendor-Performed Maintenance and Self-Maintenance Options"),
                    p(class = "body-text indent",
                      "Most vendors offer service contracts along with their battery systems in which they will send an employee or authorized representative to perform periodic 
                      maintenance of the battery system. This typically includes routine maintenance such as monitoring key systems like those described above, replacing equipment 
                      such as pumps when they reach the end of their service lifespan, and checking for malfunctioning equipment. Depending on the location of the battery device 
                      and the capabilities of the vendor, service contracts may cost around 1 to 3 percent of the total capital cost on a yearly basis. If this routine service 
                      discovers a problem with the battery that is covered by the warranty, the vendor will fix it at their expense, and if the problem is not covered under the 
                      warranty or if the warranty has expired, the vendor will fix it and bill the device’s owner."),
                    p(class = "body-text indent",
                      "Depending on the battery technology used, many of the available vendors are relatively small organizations and have limited capacity for on-site maintenance, 
                      particularly for small- to medium-scale installations. For this reason, vendors may offer self-maintenance options. When the vendor is on-site during battery 
                      installation, they can train employees or members of the host site to do much of the basic, routine maintenance. If a larger issue arises that may need more 
                      specialized attention, the vendor can come to the site to do incidental maintenance, but the majority of the regular maintenance can be done in-house by the 
                      host site. This may be of particular interest or relevance to battery owners or hosts with an educational interest or mission or with particular skill with 
                      electrical equipment, such as job training facilities, educational institutions, or certain industrial businesses.")
                )
            )}  # O & M Costs
        )
    )
  )} # Guidebook Page
    
  ) # End of tags$body
)) # End of shinyUI and fluidPage