# fitnesse
This Docker images extends the baseimage.
Installs php5.6, java jdk 1.8 update 111 and fitnesse

to run docker run -d -p <port>:8070 -v <local_fitnesse_project_path>:/prj  lawcab/fitnesse java -jar /usr/local/fitnesse/fitnesse-standalone.jar -e 0 -p 8070 -d /prj

the <local_fitnesse_project_path> is where you want to save the fitnesse project files.

to see the Fitnesse Page go to localhost:<port>

Just one step you need to do before you can start using fitnesse with php slim. 
Go to : localhost:<port>/root
Edit the page and put

!define TEST_RUNNER (/opt/phpslim.phar)
!path /prj
!define COMMAND_PATTERN (php %m %p)
!define TEST_SYSTEM (slim)

You are ready to go. For more samples you can go to : http://ggramlich.github.io/phpslim/tutorials.html for some tutorial.