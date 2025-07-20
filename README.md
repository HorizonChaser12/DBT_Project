This is a DBT Project based upon the tutorial made by Mark Freeman on LinkedIn Learning. As a fresher who is new into Data related work, this project drives me the productional level knowledge one should gain before going to actual coding/Production Environement. 
I will be attaching notes as well as the necessary points that can keep me handy while working and learning DBT.

<hr>

This is the project architecture as of now.
![alt text]<img width="913" height="470" alt="image" src="https://github.com/user-attachments/assets/bd256029-5cc1-4160-9359-dd94916a55dd" />

<hr>

These are all the DBT Commands that are used in the whole tutorial.

**dbt init** - to initalize a dbt project(makes the whole dbt project's folder which contains multiple folder like models,macros,seeds etc by itself without you creating one by one.)

**dbt debug** - to check the whole dbt project of any issue or errors in syntax. You need to be in the dbt project folder to execute this and the below commands.

**dbt compile** - this is used to compile all the available code in the dbt project. It says about the issues that will happen after the code is executed. Comes in handy when there are lots of code in your project and cross-references too, compiling this helps to check all the issues rather than running all the codse.

**dbt run** - runs all the code available in the models section of the dbt project. Should be run with cautions as this is critical process that can affect multiple files in database.

**dbt docs generate** - looks for all the metadata present in the project adn then it will create the files in JSON format.

**dbt docs serve** - this will take all the files from created by the bt docs generate and will open up a webpage describing you project and everything in your project. You can get details for all your models as well as what does the data contain. There is a pictorial graph too to visualize your whole dbt project.

