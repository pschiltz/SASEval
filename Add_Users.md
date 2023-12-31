### Adding new users to your server 

To allow more user-specific testing, you may want to create individual accounts on the SAS-Server.  Follow these steps to create the user, add them to the SAS Server Users group, and also add them to the SAS Metadata.
*Remember*, by default, with Windows 2022 Server, only two users can be remotely logged in (RDP) at a time.

1.  In your Command Prompt windows, create the user and add it to the SAS Server Users group with the commands below, altering the USERID, PASSWORD, and NAME values:
```
net user USERID PASSWORD /add /expires:never /passwordchg:no /fullname:"NAME"
```
```
net localgroup "SAS Server Users" USERID /add
net localgroup "Remote Desktop Users" USERID /add
```
2.  Add the new user to SAS metadata:
	- Open **SAS Management Console** from Start > SAS
	- Login with:
		- User: sasadm@saspw
		- Password:  Orion123
  	- Click **User Manager** from within the **Plugins** tab	
	- Click **Actions > New > User** from the menu
	- Type the name on the **General** tab
	- Go to the **Accounts** tab and click **New**
	- Type the User ID in the form **SAS-Server\USERID** and click **OK** (you do not need to specify the password)
	- Click **OK** to complete

If you would like to enable Windows Terminal Server, which allows more user concurrency, you can utilize a 120-day trial following the instructions on [this video](https://www.youtube.com/watch?app=desktop&v=FPDm64sFJMo) (only watch until 3:40)
