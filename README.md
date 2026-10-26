# AWS-EC2-SSH-Connection-For-Windows-10
Guide to connect AWS EC2 instances using SSH from a Windows 10 system

For this demonstration, run the SSH command in either Windows PowerShell or the Command Prompt to verify it's available for this demonstration

<img width="1109" height="328" alt="image" src="https://github.com/user-attachments/assets/edbcbe49-a7ec-4e04-809e-b1b6e54788cf" />

<img width="985" height="322" alt="image" src="https://github.com/user-attachments/assets/23e5ecc0-e14c-4109-9e3d-25a30d62c4e9" />

Moving forward, I will be using Windows PowerShell

To begin, I first need to connect to the directory that is holding my .pem file

After running the list command, I still won't see my .pem file because it is under Desktop directory

<img width="986" height="777" alt="image" src="https://github.com/user-attachments/assets/2471dc82-2d72-443b-b8eb-c47f6d518da4" />

So I now have to run the change directory command and switch from the user directory to the Desktop

<img width="985" height="777" alt="image" src="https://github.com/user-attachments/assets/e19c8ad5-e6c7-4bb7-9b29-adcc069af4f6" />

After switching to the Desktop folder, use the clear command to declutter your prompt take a look at the screenshot below for reference

<img width="959" height="768" alt="image" src="https://github.com/user-attachments/assets/f343f0f7-a254-4455-bbbf-ecaa18da4ddb" />

Now, executing the list command once more should reveal the .pem file in the directory

<img width="987" height="363" alt="image" src="https://github.com/user-attachments/assets/fed31b15-9d01-4ab8-bf45-6ecd88417704" />

Before continuing, we need to make sure that Port 22 is open for SSH on the security group of my EC2 instance

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/09ca36e1-2c07-4347-9dd0-6e0a0fc2780e" />

Then, to connect to my AWS EC2 instance using PowerShell, I will use the following command structure

<img width="981" height="771" alt="image" src="https://github.com/user-attachments/assets/483751fb-2551-44aa-a7d5-b320f4f7997c" />

Type yes and press Enter to continue 

<img width="984" height="172" alt="image" src="https://github.com/user-attachments/assets/b90fdc27-5c36-4e50-a3f0-bcbff2913768" />

<img width="982" height="206" alt="image" src="https://github.com/user-attachments/assets/d18663bf-9e87-4cd9-baaa-f66e1eebbdb7" />

Your SSH authentication succeeded, and you are now remotely connected to your Linux server

<img width="987" height="505" alt="image" src="https://github.com/user-attachments/assets/10b92c40-566d-452a-88a0-1482b4354511" />

To disconnect from your remote AWS server at any time, run "exit" in the terminal. This terminates the SSH session and brings you back to your local command prompt

<img width="975" height="505" alt="image" src="https://github.com/user-attachments/assets/7f04d757-109a-429a-8e7d-23a8a6db71a1" />

<img width="975" height="544" alt="image" src="https://github.com/user-attachments/assets/4bd08c3b-baf7-4077-9c59-195b3ff07520" />

If a permission error occurs during execution, follow these troubleshooting steps below:

Find your key, right-click it, and select Properties

<img width="921" height="762" alt="image" src="https://github.com/user-attachments/assets/f8b33989-d19c-41c3-b18b-191b5ae2f4b9" />

Select the Security tab at the top of the pop-up

<img width="489" height="635" alt="image" src="https://github.com/user-attachments/assets/f499fcfb-6eb9-402b-b8ad-5af2aad630de" />

At the bottom of the pop-up, click Advanced to access special permissions and advanced settings

<img width="1059" height="791" alt="image" src="https://github.com/user-attachments/assets/ab607a7b-ec13-4b77-9ced-43f1cac28899" />

As highlighted in blue, this confirms that I am the owner of the file

<img width="1026" height="643" alt="image" src="https://github.com/user-attachments/assets/ec384cfd-ff33-499b-9ba2-488dd30d1499" />

If a different user is listed as the owner, click Change, search for your user account, and assign yourself as the new owner

<img width="830" height="447" alt="image" src="https://github.com/user-attachments/assets/a2e4419a-f96d-4d46-b0f0-e3cf6a8b0b88" />

To follow the principle of least privilege, remove the SYSTEM and Administrators permission entries so that only your user account has access to the private key, but before doing this, you must disable inheritance 

Click Disable inheritance

<img width="1019" height="640" alt="image" src="https://github.com/user-attachments/assets/48cafb09-0a2a-47a1-ad85-6e8bd8c14f10" />

Then select "Remove all inherited permissions from this object". 

<img width="1020" height="637" alt="image" src="https://github.com/user-attachments/assets/f21e8d95-dafd-4645-b85d-9b930b519523" />

Your pop-up should now look like this after the removal:

<img width="1020" height="637" alt="image" src="https://github.com/user-attachments/assets/5796c8bf-3fd5-45a3-9585-c8576fd019ac" />

Now I need to add a principal. I'll do this by right-clicking Add at the bottom of the display on of the pop-up

<img width="653" height="387" alt="image" src="https://github.com/user-attachments/assets/55d57118-cc5b-41ca-adae-415afd41b957" />

Right-click "Select a principal" and search for your user account, then click Check Names, which will execute my principal name, which I can quickly verify, and select OK

<img width="653" height="387" alt="image" src="https://github.com/user-attachments/assets/33dc9ce2-647e-4aa2-adef-8c3f0de9767b" />

Next, I will need to give myself Full control of this .pem file and press OK

<img width="1215" height="722" alt="image" src="https://github.com/user-attachments/assets/3d8b0e3e-203f-4295-be0b-ff99b43b9ee6" />

Now I am the owner and the principal of the .pem file

<img width="1023" height="641" alt="image" src="https://github.com/user-attachments/assets/3aa07e7b-18e3-47b3-a095-542109c4f874" />
