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


3. pom.xml - this is main file used by maven , when you run mvn clean install , it uses this file to download the plugings from maven  we site.

4. server folder -  project related contain its own pom.xml and few other files and folders

5. webapp folder  - project related contain its own pom.xml and  src/main/webapp/index.js is location of index file
