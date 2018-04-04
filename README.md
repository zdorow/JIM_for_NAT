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
![Image of URL](https://github.com/zdorow/JIM_for_NAT/blob/master/JIMscreenshots/URL_Entry.png)

Second prompt has changes to more accurately describe the privileges needed and re-branding.
![Image of UserName](https://github.com/zdorow/JIM_for_NAT/blob/master/JIMscreenshots/UserEntry.png)

Third prompt changes are solely for re-branding. 
![Image of Password](https://github.com/zdorow/JIM_for_NAT/blob/master/JIMscreenshots/PasswordEntry.png)

Fourth prompt added more accurate language for the information being requested and re-branding.
![Image of FQDN](https://github.com/zdorow/JIM_for_NAT/blob/master/JIMscreenshots/FQDN.png)

Fifth and final prompt to account for NAT by editing the /etc/hosts file. Users can input none to bypass.
![Image of NAT](https://github.com/zdorow/JIM_for_NAT/blob/master/JIMscreenshots/NATentry.png)

Addition to the success message informing the user of the change.
![Image of success](https://github.com/zdorow/JIM_for_NAT/blob/master/JIMscreenshots/Successful_Install.png)

This shows how it would look in Jamf Pro once the changes are applied.
![Image of JamfEntry](https://github.com/zdorow/JIM_for_NAT/blob/master/JIMscreenshots/JamfEntry.png)

Once we connect it to LDAP this will show on the server when running Netstat -ntlp (Provided the network routing is place).
![Image of Netstat](https://github.com/zdorow/JIM_for_NAT/blob/master/JIMscreenshots/Netstat.png)

That is it! Thanks for reading! Any suggestions are welcomed! 
