<hr>

These are all the DBT Commands that are used in the whole tutorial.

**dbt init** - to initalize a dbt project(makes the whole dbt project's folder by itself without you creating one by one.)

**dbt debug** - to check the whole dbt project of any issue or errors in syntax. You need to be in the dbt project folder to execute this and the below commands.

**dbt compile** - this is used to compile all the available code in the dbt project. It says about the issues that will happen after the code is executed. Comes in handy when there are lots of code in your project and cross-references too, compiling this helps to check all the issues rather than running all the codse.

**dbt run** - runs all the code available in the models section of the dbt project. Should be run with cautions as this is critical process that can affect multiple files in database.

**dbt docs generate** - looks for all the metadata present in the project adn then it will create the files in JSON format.

**dbt docs serve** - this will take all the files from created by the bt docs generate and will open up a webpage describing you project and everything in your project. You can get details for all your models as well as what does the data contain. There is a pictorial graph too to visualize your whole dbt project.

