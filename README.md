Devops Project
--------------




Important IP
-----------
10.0.0.4  nat
10.0.0.68 jenkinsmaster
10.0.0.69 docker01
10.0.0.70 ns1
10.0.0.71 ansible


1. README.md - its readme file for this project.


2. Dockerfile - this file need to be copied to ansible server and from ansible server to docker server to create aan image. Docker file contain instructions to build the image, then you will use ansible jon to create container from image and run it . while creating image we are copying war file into the image.
#
FROM tomcat:latest
COPY ./webapp.war /usr/local/tomcat/webapps
RUN cp -r /usr/local/tomcat/webapps.dist/* /usr/local/tomcat/webapps
#


3. cpWarAndDockerFile2Ansible.yml - this ansible-playbook will copy war file and Dockerfile to ansible server. So that it can be further copied from ansible server to number of docker servers(where we will be running number of containers)

4. createWebServer.yml - this ansible-playbook will copy dockerfile and war file from ansible server to docker server.
then it will use docker file to create image and finally it will run container


5. pom.xml - this is main file used by maven , when you run mvn clean install , it uses this file to download the plugings from maven  we site.

6. server folder -  project related contain its own pom.xml and few other files and folders

7. webapp folder  - project related contain its own pom.xml and  src/main/webapp/index.js is location of index file




8. ansible_inventory.txt - we created this file manually in ansible server , if you are coping this project then please create this file manually.
[amitadmin@ansible ~]$ pwd
/home/amitadmin
[amitadmin@ansible ~]$ cat ansible_inventory.txt
[jenkins]
jenkinsMaster
[amitadmin@ansible ~]$

