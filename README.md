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

