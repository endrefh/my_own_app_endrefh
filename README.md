# emissions-calculator-group3
## Section 1 - Questions for Gabriel :)
Our Group is a bit unclear on your expectations each week. We hope to use this preliminary section of our README file to outline some of our questions. To start, I've listed our group's understanding of the weekly tasks. Could you verify or correct our understnading?

### Methodology
Each week, the methodology team is tasked with researching methods to calculate emissions for different polluting entities. The findings each week will then be built out below in this README file to outline our strategy for calculations.
### Diary
The Diary team will outline tasks each week under the Projects tab on github and follow along to make sure that each task is completed or on its path to completion. 
### App Development
Those working on app development will complete the application related exercises included in each week's youtube tutorial found on canvas under its associated [Task page](https://nhh.instructure.com/courses/1359/pages/emissions-app-calculator-module)


Emissions DB collector for ENE425

[Emission calculator](http://ene425.gabrielfuentes.org)

## Section 2 - Emissions Methodology Introduction

### Within this section we are gathering information on emissions calculation method for transport sources:
A basic understanding requires having a classification of transport as urban transport or industrial transport (e.g maritime, air).
A more segregated classification of "vehicles" under EC standards can be found at this [link](https://www.eafo.eu/knowledge-center/european-vehicle-categories), which is connected to the last study of ["Determining the environmental impacts of conventional
and alternatively fuelled vehicles through LCA"](https://ec.europa.eu/clima/sites/clima/files/transport/vehicles/docs/2020_study_main_report_en.pdf) by Ricardo Energy and Environment for the European Comission. Our observation of this study is that the segregation is practical for our purpouses, but the methodology is on a higher scale than what we are intending to do with the app (local direct emission per km rather than Life Cycle Analysis (LCA)).

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
