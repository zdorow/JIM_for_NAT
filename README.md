# JIM installer adjusted for for NAT

Hello and welcome to the JIM fix page!

***The reason for the fix:***
Currently the most prevalent issue setting up the JIM is usually due to the lack of support for IPv4 NAT built into the JIM. In reality IPv6 or split-DNS would be ideal, however an overwhelming majority of Admins use IPv4 with NAT and do not want to setup split-DNS. This installer accounts for that by editing the /etc/hosts file of the server to make sure the JIM is listening on an IP address it can control and not the FQDN IP before NAT is applied changing the IP address. Without access to the source code this is the best fix to ensure it is setup and working on the first run through.

Main changes are:
1. Additional prompt to account for IPv4 NAT
2. More accurate descriptions
3. Additional examples
4. Adjustments for Jamf re-branding

First prompt is minor changes for re-branding and examples for local and cloud hosted.
![Image of URL](https://github.com/zdorow/JIM_for_NAT/blob/master/JIM%20screenshots/URL%20Entry.png)

Second prompt has changes to more accurately describe the privileges needed and re-branding.
![Image of User](https://github.com/zdorow/JIM_for_NAT/blob/master/JIM%20screenshots/UserEntry.png)

Third prompt changes are solely for re-branding. 
![Image of Password](https://github.com/zdorow/JIM_for_NAT/blob/master/JIM%20screenshots/Password%20Entry.png)

Fourth prompt added more accurate language for the information being requested and re-branding.
![Image of FQDN](https://github.com/zdorow/JIM_for_NAT/blob/master/JIM%20screenshots/FQDN.PNG)

Fifth and final prompt to account for NAT by editing the /etc/hosts file. Users can input none to bypass.
![Image of NAT](https://github.com/zdorow/JIM_for_NAT/blob/master/JIM%20screenshots/NATentry.PNG)

Addition to the success message informing the user of the change.
![Image of success](https://github.com/zdorow/JIM_for_NAT/blob/master/JIM%20screenshots/Successful_Install.PNG)

This shows how it would look in Jamf Pro once the changes are applied.
![Image of JamfEntry](https://github.com/zdorow/JIM_for_NAT/blob/master/JIM%20screenshots/Jamf%20Entry.png)

Once we connect it to LDAP this will show on the server when running Netstat -ntlp (Provided the network routing is place).
![Image of Netstat](https://github.com/zdorow/JIM_for_NAT/blob/master/JIM%20screenshots/Netstat.PNG)

That is it! Thanks for reading! Any suggestions are welcomed! 
