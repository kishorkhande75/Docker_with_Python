\# Docker with Python Auto Run Project
   Welcome to the Auto Run Project! This project is designed to showcase a simple Python script that runs indefinitely. The Dockerfile provided allows you to containerize this project using Docker. The script (run.py) prints a welcome message in an infinite loop.

# Prerequisites
   Docker installed on your machine

# Getting Started
1. **Clone this repository to your local machine:**

   <code> git clone https://github.com/your-username/auto-run-project.git</code>

   <code> cd <em> auto-run-project</em> </code>

2. **Build the Docker image:**

      <code>**docker build -t auto-run-project .**</code>
	
3. Run the Docker container:

      <code>**docker run auto-run-project**</code>

That's it! The Python script will start running, and you'll see the "Welcome in auto_run_project" message printed continuously.

## Dockerfile
 
The 'Dockerfile' sets up an Ubuntu 18.04 base image, installs Python 3 and required dependencies (**'numpy"** and **'pandas'**), and copies the **'run.py'** script into the container. The **CMD** instruction specifies the command to run when the container starts.


## Dockerfile

    <code>**FROM ubuntu:18.04**</code>

    <code>**RUN apt-get update && apt-get install -y python3-pip**</code>

    <code>**RUN pip3 install numpy**</code>

    <code>**RUN pip3 install pandas**</code>

    <code>**COPY run.py run.py**</code>

    <code>**CMD ["python3", "run.py"]**</code>

## Run.py file
  The **'run.py'** file contains a simple Python script with an infinite loop that prints the welcome message.

## Python file

    <code>**# python code</code>**

    <code>**while True:
       print("Welcome in auto_run_project")</code>**

Feel free to customize the run.py script or modify the Dockerfile to suit your project's needs. Happy coding!



