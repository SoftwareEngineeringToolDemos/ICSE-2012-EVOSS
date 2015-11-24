How to get started ? 

link to youtube video :  https://youtu.be/FkngAzdoPRI 
Please refer installation.txt before running these. This tool runs on the Terminal so please run the terminal for this. 
If at any point you get permission denied and need to do a sudo , the password is "esha"

There are two modules in this tool : 
1. Simulator : 
When an upgrade is to be made to the system , this module takes the package model and configuration model of the system
as input and simulates the upgardes before actual deployment of the upgrade. It consequently tells whether or not 
the upgrade will be successful or not . Steps to follow : 

cd /home/mancoosi/mancoosi/evoss/simulator

java -jar upgenerator.jar "apt-get install --simulate amule" upgradePlan.xml

java -jar simulator.jar

You will see a simulation succeeded message.

2. Fault detection : This is a client/server infrastructure that takes up the configuration model of the system 
and checks for potential faults . Steps to follow : 

cd /home/mancoosi/mancoosi/evoss/faultdetector/fdserver

do a
java -jar fdserver.jar

you will see a message : " listening for connection request on port ...." 

Open a new terminal : 

do a 

cd /home/mancoosi/mancoosi/evoss/faultdetector/fdclient

do a
java -jar fdclient.jar

You will see the error report generated. 









