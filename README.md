# SaltyLead
This is my mini project for my Configuration Management Systems course in Haaga-Helia. The idea of the assignment is that I'm supposed to have a real life "issue" that I can resolve with the Salt Master Minion Managment tool.

The assignment in total is found on: https://terokarvinen.com/2022/palvelinten-hallinta-2022p2/

The idea of the assignment is based n the needs I have found in my everyday job. Sometimes ppl that work with the app isin't the most Technical and this sometimes requre a lot of work to get them to download the application and the troubleshooting tools.
The idea is that the salt master can distribute the folders to new workers, make sure they have the tools and updates that they need to run the program and if issues areise they can download the troubleshooting tools. 

I have created the folder in salt and one bash file that I have tried locally on my VM. 
I have also created a init.sls where is an apache update and the folder that I want to run. 
I also made a pkg.installed for ssh which sould be useful incase the client dont know how to do anything.
I decided to make all the .sh files first, run them locally and on tomorrows lesson get answers why I do not get it to work. 
