# emissions-calculator-group3
Emissions DB collector for ENE425
[Emission calculator](http://ene425.gabrielfuentes.org)

Directory Tree:

                
                +--- Emissions_App
                |   app.py
                |   LICENSE
                |   Procfile
                |   python-app.yml
                |   requirements.txt
                |   tree_output.doc
                |   
                +---notes
                |       .gitkeep
                |       module_design_v2.png
                |       
                +---static
                |       favicon.png
                |       
                \---templates
                        add_record.html
                        edit_or_delete.html
                        error.html
                        index.html
                        list.html
                        login.html
                        result.html
                        select_record.html
                        
  ## Section 1
## Ask Gabriel
Group 3 had our first all team meeting this week and is hoping to verify your expectations from us each week. We hope to use this preliminary section of our README file to outline these questions in an effort to familiarize the team with using Github and editing the README. To start, I've listed our group's understanding of the weekly tasks. Could you verify or correct our understnading?

> Great job so far, I can see a very well organized group in here. I am addressing your questions at the next section. You can erase this blocks before delivering the app.
### Question 1
#### Methodology
Each week, the methodology team is tasked with researching methods to calculate emissions for different polluting entities. The findings each week will then be built out below in this README file to outline our strategy for calculations.
> Yes. Note that on this project, assuming is a first stage of our app, we are only focusing on transport emissions.
#### Diary
The Diary team will outline tasks each week under the Projects tab on github and follow along to make sure that each task is completed or on its path to completion.
> I would add that the diary team is also gathering overall information of the app development and posting it in here e.g posting what you have achieved every week and what is pending for the next week. By doing this, the next team would know from where to take over.

#### App Development
Those working on app development will complete the application related exercises included in each week's youtube tutorial found on canvas under its associated [Task page](https://nhh.instructure.com/courses/1359/pages/emissions-app-calculator-module)
> Yes

### Question 2
Our group consists of 23 people on the groups excel document, but we are currently identifying only 13 people who plan to continue with the course. Is there a plan to remedy the descrepancy or something we should do on our end?
> Good observation and it brought an unexpected challenge to us. As you might have noticed, some new comers have enrolled to the course and assigned to either of the groups. Also, we have noticed and been adressed by some groups that there are some enrolled students which are not going to follow up the course. To help in adressing that, we are establishing the end of the week (Feb 14th) as the deadline for enrolling into the module (task 1 and engagement within the group). So, short answer, nothing is needed on your side. Perhaps helping us spreading the info to those colleages that haven't enrolled but are expecting to continue the course. Your engagement and managing strategy have being great, so we do believe it is fair to establish some deadlines.

  ## Section 2
## App Development Journal
### Week 1 (Calendar Week 5)
In Week 1 of development, we did our best to get everybody set up with Github and Heroku accounts as well as develop a group chat forum where we could stay connected and strategize around each week's tasks. 

### Week 2 (Calendar Week 6)
This week, the app development team copied and uploaded repository files taken from Gabriel's example repository to structure our own repository. The team also created a directory tree for our repository that is located in this README file. 

### Week 3 (Calendar Week 7)
The app dev team have worked with the design of the app and changed colors and text in the right files within the template folders.

#### Design suggestions and proposals:

**Color suggestions:**

    05B384 (Mint)
    388697 (Metallic Seaweed)
    E9EDEB (Platinum)

Another suggestion is to apply colors from the UN Sustainable Development Goals, especially from the relevant goals:

    #7 Affordable and clean energy: fbc412
    #11 Sustainable cities and communities: f89d2a
    #13 Climate action: 407f46
    #14 Life under water: 1f97d4
    #15 Life on land: 59ba47

<img src="notes/UN SDG colors.png" width="400" height="150"/>

**Design proposals:**

Below are some screenshots from a website that calculates people's overall carbon footprint. The website, called 
Ducky, contains great inspirations for our website when it comes to colors, design and layput.


<img src="notes/Example Ducky home page.png" width="500" height="300"/>

Above: Screenshot of Ducky's start page. Very minimalistic and clean.

<img src="notes/Example Ducky 1.png" width="400" height="400"/>

<img src="notes/Example Ducky graph.png" width="500" height="250"/>

### Week 4 (Calendar Week 8)

### Week 5 (Calendar Week 9)

### Week 6 (Calendar Week 10)


  ## Section 3
## Emissions Methodology Introduction

### Within this section we are gathering information on emissions calculation method for transport sources:
A basic understanding requires having a classification of transport as urban transport or industrial transport (e.g maritime, air).
A more segregated classification of "vehicles" under EC standards can be found at this [link](https://www.eafo.eu/knowledge-center/european-vehicle-categories), which is connected to the last study of ["Determining the environmental impacts of conventional
and alternatively fuelled vehicles through LCA"](https://ec.europa.eu/clima/sites/clima/files/transport/vehicles/docs/2020_study_main_report_en.pdf) by Ricardo Energy and Environment for the European Comission. Our observation of this study is that the segregation is practical for our purpouses, but the methodology is on a higher scale than what we are intending to do with the app (local direct emission per km rather than Life Cycle Analysis (LCA)).

### NTM Method for Emissions Calculation
This method is developed by The Network for Transport and Environment (NTM) which is a non profit organization, initiated in 1993 and aiming at establishing a common base of values on how to calculate the environmental performance for various modes of transport[link](https://www.transportmeasures.org/en/about-ntm/). NTM is involved with the European Committee for Standardization (CEN) in developing the European standard for emission calculation. NTM method specifies emission calculations for four types of transport: air, rail, road and water.

#### Air Transport
The total emission of a vessel is determined by the emission factor (constant and variable) and the distance. 

The emission factor consists of (1) the constant emission factor (CEF in kg) which is for emissions during take-off and landing, and (2) the variable emission factor (VEF in kg/km) which is linear in the flight distance. The emission factors are specific for the aircraft type, engine type and maximum load. The load factor is defined as the actual weight of the load versus the maximum load.

Distance is calculated by the same method used by the International Civil Aviation Organization (ICAO). The flight distance (D<sub>a</sub> in km) is calculated by using the great-circle distance formula which calculates the shortest distance between two locations by taking the bend of the earth into account. 

Total emissions for an aircraft is then given by:

EM<sub>total</sub> = CEF + VEF * D<sub>a</sub>

The unit emissions (e<sub>a</sub> in kg) is calculated by multiplying EM<sub>total</sub> with the physical weight of the load (w<sub>d</sub>) and divide it by the maximum load (LO<sub>max</sub>) of the aircraft times the average load factor (LF): 

e<sub>a</sub> = EM<sub>total</sub> * w<sub>d</sub> / LO<sub>max</sub> * LF

#### Rail Transport
Railway transport is distinguished into two types (1) electrical and (2) diesel. The unit emissions (e<sub>e</sub> and e<sub>d</sub>) depend on three main factors: the emission factor, the distance and the weight of the product.

The emission factor in country z (EF<sub>e</sub><sup>z</sup>  or EF<sub>d</sub><sup>z</sup>) is defined as the amount of CO<sub>2</sub> emitted when transporting 1 net tonne over 1km. It depends on the gross weight of the train, an emission constant, a correcting factor for the terrain, the load factor, energy efficiency factor, and a transfer loss (for electronical only).

Distance traveled in country z, D<sup>z</sup>, can be calculated from the EcoTransIT webpage [link](https://www.ecotransit.org/calculation.en.html).

Unit emissions e<sub>e</sub> and e<sub>d</sub> (in kg) are a function of the weight of the product (w in tonne) and are calculated per country and then summed over the countries traversed:

e<sub>e</sub> = ∑<sub>z∈Z</sub> EF<sup>z</sup> * D<sup>z</sup> * w

e<sub>d</sub> = ∑<sub>z∈Z</sub> EF<sup>z</sup> * D<sup>z</sup> * w

#### Road Transport
The total emissions of the vehicle are determined by the fuel consumption of that vehicle, the fuel emissions and the distance.

Fuel consumption (FC in l/km) depends on the load factor (LF) and the type of vehicle.

The Fuel Emissions factor (FE) is defined as gram of CO<sub>2</sub> emitted per liter of fuel (diesel).

Distance (D in km) is the distance between two terminals. 

Total emissions are then (in gram):

EM<sub>total</sub> = FE + FC x D

The unit emissions (er in g) is calculated by multiplying EM<sub>total</sub> with the physical weight of the load (w<sub>d</sub>) and divide it by the maximum load (LO<sub>max</sub>) of the vehicle times the average load factor (LF)of the vehicle:

e<sub>r</sub> = EMe<sub>total</sub> * w<sub>d</sub> / LO<sub>max</sub> * LF

#### Water Transport
Covers short-sea transport and inland transport with diesel oil-powered vessels. The calculation of emissions for vessels is dependent on the type of vessel.

Total emissions (EM<sub>total</sub> in kg) depend on three factors: fuel consumption (FC), the distance (D<sub>w</sub>) and the fuel emissions (FE). 

Fuel consumption (l per km) is dependent on vessel type in NTM Water for a given average load factor. 

Distance (D<sub>w</sub>) in km can be retrieved for example from the World Port Distances.
The fuel emissions factor (FE) (kg of CO<sub>2</sub> emitted when 1l of diesel is burnt) is also required. 

Total emissions (EM<sub>total</sub> in kg) is the three mentioned factors multiplied:

EM<sub>total</sub> = FC * D<sub>w</sub> * FE

Unit emissions. Allocation fraction is defined as follows:

α = unit capacity / total capacity

The unit emissions (e<sub>w</sub> in kg) are then calculated with the following formula:

e<sub>w</sub> = α * FC * D<sub>w</sub> * FE

#### Assessment of the NTM Method
The NTM method has a high level of detail and focuses on transport in Europe. The method defines four different types of transport and the calculations for each transport mode seem to be based on relevant factors and assumptions. However, NTM aim to create "a common base of values" on how to calculate transport emissions but is doing so mainly by taking European transport into account.

### ARTEMIS method
The ARTEMIS tools are the result of a large European co-operation around the pollutant emissions and energy consumption of the transports. The ARTEMIS project resulted in many important scientific results and in a unique state of the art on the topic in Europe. The main lines of the project and its results: emission measurements, principles of the modelling, street-scale approach based on the definition of traffic situations, and the resulting tools. The tools application requires detailed and reliable data describing the traffic (vehicle fleets and activity, driving conditions, etc.). [link](https://www3.epa.gov/ttnchie1/conference/ei18/session6/andre.pdf)

#### Assessment of the ARTEMIS Method
The ARTEMIS Method is probably to advanced for the type of app we are aiming to create. 

#### A specific method to calculate air traveling emissions
ICAO is a UN specialised agency. They have among other things created a flight emissions calculator. 
Summary of the methodology the use:
CO2 Emissions per passenger take into consideration the load factor and are based only on passenger operations (i.e. fuel burn associated with belly freight is not considered). The steps for the estimation of CO2 emissions per passenger:

Step 1: Estimation of the aircraft fuel burn

Step 2: Calculation of the passengers' fuel burn based on a passenger/freight factor which is derived from RTK data

Step 3: Calculation of seats occupied (assumption: all aircraft are entirely configured with economic seats). Seat occupied = Total seats * Load Factor

Step 4: CO2 emissions per passenger = (Passengers' fuel burn * 3.16) / Seat occupied

Note: for flights above 3000 km, CO2 emissions per passenger in premium cabin = 2 x CO2 emissions per passenger in economy [link](https://www.icao.int/environmental-protection/Carbonoffset/Pages/default.aspx)

### GHG Protocol
GHG Protocol establishes comprehensive global standardized frameworks to measure and manage greenhouse gas (GHG) emissions from private and public sector operations, value chains and mitigation actions. GHG protocol is mainly used by private subjects such as companies and organization as well as by public entities countries and cities. The idea of establishing an international standard for global accounting was born in the late 1990s, but it is only in 2001 that the first edition of the Corporate Standard was published. The GHG protocol was additionally updated after the Paris Agreement in 2015. The GHG protocol provides tools as well as standardized guidelines for emission accounting.

#### Corporate standard
The standard covers the accounting and reporting of seven greenhouse gases covered by the Kyoto Protocol – carbon dioxide (CO2), methane (CH4), nitrous oxide (N2O), hydrofluorocarbons (HFCs), perfluorocarbons (PCFs), sulphur hexafluoride (SF6) and nitrogen trifluoride (NF3). It was updated in 2015 with the Scope 2 Guidance, which allows companies to credibly measure and report emissions from purchased or acquired electricity, steam, heat, and cooling. There are two categories of tool used:

  ##### Cross-sector tools
  Applicable to many industries and businesses regardless of sector. The one useful for our research topic could be the Mobile Combustion tool that calculates direct and  
  indirect CO2 emissions from fuel combustion in mobile sources. It also provides calculations and emission factors for road, air, water, and rail transport. Excel tables for
  using a certain tool are available on GHG Protocol website.
  
  ##### Sector specific tools
  Principally designed for the specific sector or industry listed, though they may be applicable to other situations.

#### Protocol for cities
GHG Protocol is working to give cities the standards and tools they need to measure their emissions, build more effective emissions reduction strategies, set measurable and more ambitious emission reduction goals, and to track their progress more accurately and comprehensively.

The GHG Protocol seems not to be the best choice for our research because it focus on private or public actors, it is designed for corporate and national emission accounting.
  
### EcoTransIT
EcoTransIT World is the most widely used software worldwide to automate the calculation and analysis of energy consumption and freight emissions.ETW allows calculation of complete transport chains across all modes of transport (truck, train, ocean vessel, inland waterways, aircraft) including transhipments / warehousing worldwide on the basis of a scientific and neutral methodology. This makes ETW equally usable for logistics service providers (LSP), carriers, shippers as well as software providers, consulting companies and other related organisations. ETW calculates the transport distances, energy consumption, greenhouse gases CO2 and CO2 equivalents as well as air pollutants SOx , NOx, NMHC and PM10 for any global transport chain.

#### Methodology
The ETW considers all emissions directly caused by the operation of vehicles and the final energy consumption are taken into account. Additionally, all emissions and the energy consumption of the generation of final energy (fuels electricity) are included. Two process steps and the sum of both are distinguished.

  + Upstream energy consumption and upstream emissions (= energy provision, production and distribution; Well-to-Tank WTT)
  It includes energy provision, production and distribution: extraction and generation, refineries and power plants and energy distribution. 
  + Final energy consumption and vehicle emissions (= operation; Tank-toWheels TTW)
  It accounts for the actual consumption of energy for transport operations.
  + Total energy consumption and total emissions: Sum of operation and upstream figures (Well-to-Wheels WTW).
  It is basically a sum of the the two previous steps, accounting for the entire process.
  
The ETW does not account for energy related to the construction of infrastructer and vehicles.

#### Which transports are calculated?
Basically, all modes of transports are calculated, clustered into:
+ Air freight – different aircraft types and sizes
+ Ocean freight – container shipping, bulk shipping and liquids
+ Inland ship freight – different ship types
+ Road freight – truck types aggregated into size classes and emission standards, including/excluding ferry shares
+ Rail freight – different rail sizes and types and emission standards 

#### Energy consumption allocated and calculated for a single shipment
The basic principle of calculation relies on the metric weight of the shipment and the distance travelled (tkm).

The principal calculation rule for the calculation of vehicle emissions is
WTW energy consumption or emissions per transport = Transport Distance * mass of freight transported * (TTW energy consumption or vehicle emissions per net tonne km +WTT energy consumption or emissions per net tonne km)

The corresponding formulas are

+ EMTi = Di* M* (EMVtkm,i + EMUtkm,i)
+ ECTi = Di* M* (ECFtkm,i + ECUtkm,i) 

ETW is mainly used to account emissions for commercial transportation, but it could be also used to account for emissions produced by a single consumer.

## List of References
[Global Footprint Network](https://www.footprintnetwork.org/resources/data/)

[Effect of Carbon Emission Regulations on Transport Mode Selection in Supply Chains](https://pdfs.semanticscholar.org/a96a/9108170e8e5f3e6b23ac990a89834248af56.pdf?fbclid=IwAR2-aMr7AEeU8UZ1XI2i08Sy5AtgsXtfu3KZHh_k4n8fFb0mNt23PZ-DZjE)

[GHG Protocol](https://ghgprotocol.org/)

[EcoTransIT](https://www.ecotransit.org/methodology.en.html)
