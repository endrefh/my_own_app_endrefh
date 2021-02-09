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
The app dev team will dive into App Design this week as we start to learn the basics of customizing our Emissions Calculator. 

  ## Section 3
## Emissions Methodology Introduction

### Within this section we are gathering information on emissions calculation method for transport sources:
A basic understanding requires having a classification of transport as urban transport or industrial transport (e.g maritime, air).
A more segregated classification of "vehicles" under EC standards can be found at this [link](https://www.eafo.eu/knowledge-center/european-vehicle-categories), which is connected to the last study of ["Determining the environmental impacts of conventional
and alternatively fuelled vehicles through LCA"](https://ec.europa.eu/clima/sites/clima/files/transport/vehicles/docs/2020_study_main_report_en.pdf) by Ricardo Energy and Environment for the European Comission. Our observation of this study is that the segregation is practical for our purpouses, but the methodology is on a higher scale than what we are intending to do with the app (local direct emission per km rather than Life Cycle Analysis (LCA)).

## List of References
[Global Footprint Network](https://www.footprintnetwork.org/resources/data/)
