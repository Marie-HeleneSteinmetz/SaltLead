#SaltyLead
This is the last assignment for Tero Karvinens Haaga-Helia Configuration Management Systems.
You can visit the whole assignment and course info on: 
https://terokarvinen.com/2022/palvelinten-hallinta-2022p2/#comments

I have used Ubuntu on Virtual Mmchine and have installed from before Salt-Master and minion on the same Machine.

I work as a Technical Support Specialist at a SaaS company that offer VoIP(Voice over IP) in an Applikation and on an browser.
The once using the applikation is from coldcalling sales ppl to inbound call using instanses (banks, healthdare etc. )
The idea of the assignment is based on the needs I have found in my everyday work. Sometimes ppl that work with the app isin't the most Technical and this sometimescasues a lot of extra work to give instrucrions on how to help me help them.
This requre a lot of work to get them to download the application, right brower and the troubleshooting tools. Espesially if the person cannot even write in English.

The idea is that the salt master from the company side, or if they have an internal IT, can distribute the folders to new workers, make sure they have the tools and updates that they need to run the program and if issues areise they can download the troubleshooting tools. 

I have created the folder in salt and one bash file that I have tried locally on my VM. 
I have made the following so far.
1. A script where the Admin can ask the Master to add a salesspeesh. In mine there is only a link to a salesspeech. 
2. A link with the link to download the applikation 
3. A link with the link to download the troubleshooting tool and ping plotter tool
4. A init.sls file that makes these scripts possible to give minions and where they would copy with a pkg.installed and apache plus ssh. SSH is that if the client/minion don't know how to do anything the master/Internal IT can connect to the client computer. 

I get the to apply the files locally and it shows as expected: 
![image](https://user-images.githubusercontent.com/117899860/207680524-b06fc912-c624-46d4-b738-ccbd56aaf144.png)
The time it takes is really long tho. 

Earlier whe I ran the states to my slaves there was not problem. Now I get Keyerror: retcode
![image](https://user-images.githubusercontent.com/117899860/207681187-b984d295-31ee-4610-ae6a-bd0631bbe0e7.png)
This I need to look into. 

I would still like to add the Chrome download to the init.sls(chome is the supported browser for the web page) file and make differernt programs running if the user is an Admin or an Agent. Unfortunatly for this I would need to dive deeper in Salt stack and thats what I will do next. I have found some great readings regarding the matter: 
https://docs.vmware.com/en/VMware-vRealize-Automation-SaltStack-Config/6.4/SaltStack_Config_Installation_and_Upgrade_v6_4.pdf
https://github.com/harkx/saltstack-cheatsheet
https://docs.saltproject.io/en/latest/ref/states/all/salt.states.pkg.html

There could be more in the instructions on logs and error logs to send over in case that issues arise. Possibility to make a automation that gathers ping, pipes them to a file that then is send to the Master if there is too much packet loss. 

Unfortunatly while updateing the Git my VM ran into problems and did not get a connection to the internet not anything else. 
![image](https://user-images.githubusercontent.com/117899860/207681732-d0220cea-e1e2-41a6-9f96-62750996ea7d.png)
I found that it might have to do that my VM is not up to date: 
 https://stackoverflow.com/questions/18099144/clone-from-github-com-temporary-failure-in-name-resolution-error
 The connection issue seems to effect most of the prosess I'm trying to do: 
 
 ![image](https://user-images.githubusercontent.com/117899860/207682316-0087c6ed-f7e5-4987-be16-fdc5ceaa74e4.png)
Because I by accident in the creation made many direcoties the git add ., commit, push and pull did not work in the directory that I had intended for it and I though that this first casues the issue. 

Now It does seem like I need to start troubleshooting the issues that arised during this project.
I will upload all the scripts when the issue has been resolved. At this moment they exist in the salt master direktory. 
 ![image](https://user-images.githubusercontent.com/117899860/207682468-5e1a5e4e-45fe-49b7-8919-26a1181f5ba6.png)
 
 And in the Git on mu VM: 
 ![image](https://user-images.githubusercontent.com/117899860/207685917-bb160283-1076-43f8-b66b-990340418b47.png)
 I managed to get the Git to work with updating the VM.



 
