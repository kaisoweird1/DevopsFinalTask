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



