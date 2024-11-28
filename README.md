# TASK 1 Write shell script to install jenkins
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


This shell script automates the installation of a specified Jenkins version on Debian-based (Ubuntu/Debian) or Red Hat-based systems. It installs necessary dependencies (Java, wget), adds the official Jenkins repository, and installs the user-specified Jenkins version. After installation, the script starts and enables the Jenkins service. Simply run the script, enter the desired Jenkins version (e.g., 2.414.3), and it handles the rest, ensuring a smooth setup process.



![task1real](https://github.com/user-attachments/assets/5ef9cead-1fe1-4470-8564-124be5e81e2e)

________________________________________________________________________________________________________________________________________________________________________________________________________________________

# TASK 2 Setup Master-slave architecture
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


Created a node to setup the master-slave architecture, using a private ssh key and the ip address (username) of the other node, which in this case is an EC2 instance.


![image](https://github.com/user-attachments/assets/92a6ffa9-ee78-48d8-b8d3-bdfb103e0511)

It is also configured to run 5 different tasks at one time.

![image](https://github.com/user-attachments/assets/b43172f5-b44e-4f52-b255-2489fbc3f344)


________________________________________________________________________________________________________________________________________________________________________________________________________________________


# TASK 3 Setup Role based authorization
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


3 User ids are created namely: devops1 devp-1 testing1

![image](https://github.com/user-attachments/assets/89847df7-9e1a-4f3c-8ca1-d751e0844afc)


Dev, DevOps, and Test roles with respective authorizations are set. Global Admin and Reader roles provide read access for all.


![image](https://github.com/user-attachments/assets/a58f480b-9c67-4308-a50e-75167e86f743)
![image](https://github.com/user-attachments/assets/592fbaa5-baf8-4502-af49-b97e390d2228)

Global Reader is assigned to all roles, and Global Admin to the admin user, as shown below.


![image](https://github.com/user-attachments/assets/dcce6b5a-f924-4c55-bb4f-3eca077f5556)

________________________________________________________________________________________________________________________________________________________________________________________________________________________


# TASK 4  A Pipeline for Disk Usage And Process Management
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


The script monitors root (/) disk usage, warns if it exceeds 80%, and exits with an error; otherwise, it confirms normal usage.

![image](https://github.com/user-attachments/assets/7cd1ae46-a016-4f60-b72c-f73c55fdad2c)


The script lists the top 5 CPU and memory-consuming processes and detects zombie processes for troubleshooting.


![image](https://github.com/user-attachments/assets/0400a0ca-49b7-4df2-b253-3cba8b0c2233)


This Jenkins pipeline automates Git cloning, disk usage monitoring, and process management via custom scripts on an hourly schedule, with email notifications on failure.


![image](https://github.com/user-attachments/assets/d2629a92-8144-4ad5-a4ea-43fcb47866ba)


______________________________________________________________________________________________________________________________________________________________________________________________________________________


# TASK 5 Backup Process
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


The script accepts command-line arguments for source "-s", destination "-d" directories, and optional compression "-c". It logs timestamps for tracking and exits with a message if mandatory requirements are unmet.The script also checks if the source and destination 
directories exist. If they do, it proceeds; if not, it creates the destination directory. In case of failure during directory creation, an error message is shown, and the log is updated before exiting. The script then performs a backup of the source directory to the 
destination, generating a timestamped backup name. If the compression option is enabled, it backs up the directory as a .tar.gz file using `tar`; otherwise, it simply copies the source directory. Logs are updated at each step, whether successful or not. A cleanup 
function removes backup files older than 7 days.


![image](https://github.com/user-attachments/assets/3dccf4bd-248f-4c19-954b-56d7fff04adc)
![image](https://github.com/user-attachments/assets/79302993-cb8f-4015-97f4-37c27f1edace)


________________________________________________________________________________________________________________________________________________________________________________________________________________________


# TASK 6 Building a Java App
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Tools like JDK 17 and Maven 3.9.9 have been implemented to build the Java app.

![image](https://github.com/user-attachments/assets/4c0ce687-74bc-47fb-a7d3-c8bbb04b2ce3)


This Jenkins pipeline builds, tests, and delivers a project using Maven and Java. Triggered by githubPush(), it checks out code from https://github.com/Syndrizzle/devops-stuff.git (main branch by default), runs `mvn clean package -DskipTests` to compile and package the code into a .jar file, and executes `deliver.sh` to
deploy the app after a successful build.

![image](https://github.com/user-attachments/assets/f700260b-27fa-430d-b474-a926d0914b42)

![image](https://github.com/user-attachments/assets/971f4ed2-a0f8-47cd-a27e-192ea73326c5)




______________________________________________# END OF THE FILE ____________________________________________________







