## Auto Run Project
Welcome to the Auto Run Project! This project is designed to showcase a simple Python script that runs indefinitely. The Dockerfile provided allows you to containerize this project using Docker. The script (run.py) prints a welcome message in an infinite loop.

## Prerequisites
Docker installed on your machine

## Getting Started
1. **Clone this repository to your local machine:**

 <code> git clone https://github.com/your-username/auto-run-project.git</code>

 <code> cd <em> auto-run-project</em> </code>

2. **Build the Docker image:**

 **docker build -t auto-run-project .**

3. Run the Docker container:

 **docker run auto-run-project**

That's it! The Python script will start running, and you'll see the "Welcome in auto_run_project" message printed continuously.

## Dockerfile
 
 The **'Dockerfile'** sets up an Ubuntu 18.04 base image, installs Python 3 and required dependencies (**'numpy"** and **'pandas'**), and copies the **'run.py'** script into the container. The **CMD** instruction specifies the command to run when the container starts.

#dockerfile

<code>**FROM ubuntu:18.04**</code>

RUN apt-get update && apt-get install -y python3-pip
RUN pip3 install numpy
RUN pip3 install pandas
COPY run.py run.py

CMD ["python3", "run.py"]
run.py
The run.py file contains a simple Python script with an infinite loop that prints the welcome message.

python
Copy code
# python code

while True:
    print("Welcome in auto_run_project")
Feel free to customize the run.py script or modify the Dockerfile to suit your project's needs. Happy coding!





