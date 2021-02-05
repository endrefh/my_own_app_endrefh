# emissions-calculator-group3
## Welcome Group 3

Emissions DB collector for ENE425

[Emission calculator](http://ene425.gabrielfuentes.org)

## Emissions Methodology

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
