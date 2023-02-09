# Header - README Template.
![Github Logo](https://github.githubassets.com/images/modules/logos_page/Octocat.png "Github logo - markdown")

>## Table of Contents Example
* [About the Project](#about_the_project)
* [Tools](#tools)
* [Installation Instructions](#installation)
* [Contact Information](#contact)

<a class="anchor" id="about_the_project"></a>
>## About the Project
In this project I am pulling data from MIT's course catalog with Python's urllib library. The data being pulled  is unstructured and will need to be cleaned after extraction. Data analysis on the cleaned data is performed to find words that appear most often in course titles. The analysis is stored with the JSON format to be used with a D3 web application which will also visualize this data. An Airflow web server will be instantiated in Docker to run Python tasks to automate this pipeline.

<a class="anchor" id="tools"></a>
>## Tools
Include a list of the tools used in the project:
1. Python
2. urllib
3. Docker
4. Airflow

<a class="anchor" id="installation"></a>
>## Installation Instructions
In a terminal window, inside the airflow-docker folder, run the docker-compose up command to create and run the containers.

You can now navigate to https://localhost:8080/ to login to Airflow. By default username and password are 'airflow'.

Run each task to generate the JSON file.

The files created by airflow will need to be extracted from the worker_1 airflow server. 

Open a terminal to this server through the docker desktop app and copy the words.json file to your local machine. See the commands for opening a terminal and copying a file from a container below.

<code>
docker exec -it airflow_docker_airflow-worker_1 /bin/bash
</code>

<code>
docker cp airflow_docker_airflow-worker_1:/opt/airflow/words.json YOUR_PATH_HERE
</code>

To visualize the JSON file extracted from our airflow server we will need to save it as words.js.

Finally, you can visualize the results of our sensemaking pipline by visiting the web page listed below.

file://YOUR_PATH_HERE/project-23/code_visualization/mitcourses_graph.html

<a class="anchor" id="contact"></a>
>## Contact Information
[Cristian Garcia](https://www.linkedin.com/in/cristiangarcia2636)