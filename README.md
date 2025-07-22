# Intro and why I am doing it?
This is a DBT Project based upon the tutorial made by Mark Freeman on LinkedIn Learning. As a fresher who is new into Data related work, this project drives me the productional level knowledge one should gain before going to actual coding/Production Environement. 
I will be attaching notes as well as the necessary points that can keep me handy while working and learning DBT.

<hr>

## Architecture of the Project.

<img width="913" height="470" alt="image" src="https://github.com/user-attachments/assets/71e19848-1db5-4212-a403-3045aedf41f5" />


<img width="913" height="470" alt="image" src="https://github.com/user-attachments/assets/bd256029-5cc1-4160-9359-dd94916a55dd" />

<hr>

# Notes
## DBT : 

- **dbt init** - to initalize a dbt project(makes the whole dbt project's folder which contains multiple folder like models,macros,seeds etc by itself without you creating one by one.)

- **dbt debug** - to check the whole dbt project of any issue or errors in syntax. You need to be in the dbt project folder to execute this and the below commands.

- **dbt compile** - this is used to compile all the available code in the dbt project. It says about the issues that will happen after the code is executed. Comes in handy when there are lots of code in your project and cross-references too, compiling this helps to check all the issues rather than running all the codse.

- **dbt run** - runs all the code available in the models section of the dbt project. Should be run with cautions as this is critical process that can affect multiple files in database.

- **dbt docs generate** - looks for all the metadata present in the project adn then it will create the files in JSON format.

- **dbt docs serve** - this will take all the files from created by the bt docs generate and will open up a webpage describing you project and everything in your project. You can get details for all your models as well as what does the data contain. There is a pictorial graph too to visualize your whole dbt project.

- **Materialization** - controls how your models within your database are viewed and created. This is done mostly to limit what tables can be viewed by database users, Reduce costs of data storage or to speed up certaion data pipelines(For example dashboards, where the need for the data needs to be fast to get the UI going good.) <br>
Five different materialization methods within dbt:
    - table : Creates a fully rebuilt physical table that stores data persistently for fast querying.
    - view : Defines a database view that dynamically reflects up-to-date data without storing results.
    - incremental : Builds or updates a table by processing only new or changed data since the last run, improving efficiency.
    - ephemeral : Does not create any database object; the model is inlined as a CTE in downstream queries at runtime.
    - materialized view : Creates a database-managed object that stores precomputed results like a table but refreshes automatically like a view

You need to define all these materialization in the dbt_project.yml file under the models section.

# Others :
**ref** - this is not a dbt command, its more of a SQL command that helps reference sql files inside another SQL file. For the SQL files which are present in model folder, the first one doesnt need to have any refs in it as it isnt referring to anything but it can refer to files from other folders too.
for example - {{ref('bronze_parking_violations')}} , which is written in the silver_parking_violation_codes file to get a reference from the bronze_parking_violations.

# Acknowledgments

This project was solely made for educational purposes and my will to learn DBT. This project is a practical part of the series by [Mark Freeman](https://www.linkedin.com/in/mafreeman2/) on [LinkedIn](https://www.linkedin.com/learning-login/share?account=2154233&forceAccount=false&redirect=https%3A%2F%2Fwww.linkedin.com%2Flearning%2Fdata-engineering-with-dbt%3Ftrk%3Dshare_ent_url%26shareId%3DbVDhiv1CQfWyoe6ipZnG5w%253D%253D).
