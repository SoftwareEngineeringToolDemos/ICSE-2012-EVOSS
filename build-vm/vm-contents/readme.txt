Link to youtube video :  https://youtu.be/FkngAzdoPRI 
Please refer installation.txt before running these. If at any point you get permission denied and need to do a sudo , the password is "vagrant"

There are two modules in this tool : 

1) Simulator : When an upgrade is to be made to the system , this module takes the package model and configuration model of the system
as input and simulates the upgardes before actual deployment of the upgrade. It consequently tells whether or not 
the upgrade will be successful or not . Steps to follow : 

	1. cd /home/mancoosi/mancoosi/evoss/simulator
	2. sudo java -jar upgenerator.jar "apt-get install --simulate amule" upgradePlan.xml
	3. sudo java -jar simulator.jar

You will see a simulation succeeded message.

2) Fault detection : This is a client/server infrastructure that takes up the configuration model of the system 
and checks for potential faults . Steps to follow : 

	1. cd /home/mancoosi/mancoosi/evoss/faultdetector/fdserver
	2. java -jar fdserver.jar

you will see a message : " listening for connection request on port ...." 

Open a new terminal and run these commands: 

	3. cd /home/mancoosi/mancoosi/evoss/faultdetector/fdclient
	4. java -jar fdclient.jar

You will see the error report generated. 









