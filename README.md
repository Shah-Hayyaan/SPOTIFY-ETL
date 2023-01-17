This Project is about scheduling a Job that runs ETL process for  Spotify Data. So firstly I'm Setting the airflow home variable to a sub folder in the home folder through VS Code. Here all the airflow data gets saved. Make sure that you've installed airflow with the necessary constraints or you need to reinstall it after uninstalling it. Airflow documentation is there for Guidance. Then I've Addressed airflow with the Location of the dags directory and after pointing the location Variable to the location of the created Dags subfolder I've started the airflow webserver and then we need to run the virtual Environment again to run the airflow scheduler. So when the Airflow Webserver and Scheduler are running we can Run the airflow UI through a webbrowser by accessing the Localhost. Now I've created a new Dag in the airflow window where dags are defined by a python script. A Dag stands for Directed Acyclic Graph. Here the Graph task flow is going in a single direction  and there is no coming back or there can't be a Formation of a cycle. Then I've mentioned and created the parameters which are needed to be passed through Airflow. Now the start date has to be mentioned as the current date and I've defined an operator and then after running the run-etl = PythonOperator {

task_id= 'whole_Spotify_etl',

python _ callable=just _a_function,

dag=dag

}

run_etl 

so after defining thr order of execution of the tasks I've run the file to start the new dag and acces the log file after getting it successfully created the after checking the logs multiple times I've created a function named -

def run_spotify_etl 

Now I've Pasted all the code from  the main File to the Function and deleted the main function & renamed the file as spotify_etl.py
from main.py then. I've imported the newly created function to the renamed  Python file and then to check if the Data has gotten downloaded and The ETL process is running, I've accessed it through a database by running th query to get the table and the data will get downloaded everyday when the airflow is running successfully.
