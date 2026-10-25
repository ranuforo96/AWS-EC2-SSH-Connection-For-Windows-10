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

1

<img width="981" height="771" alt="image" src="https://github.com/user-attachments/assets/483751fb-2551-44aa-a7d5-b320f4f7997c" />

2

<img width="984" height="172" alt="image" src="https://github.com/user-attachments/assets/b90fdc27-5c36-4e50-a3f0-bcbff2913768" />

3

<img width="982" height="206" alt="image" src="https://github.com/user-attachments/assets/d18663bf-9e87-4cd9-baaa-f66e1eebbdb7" />

4

<img width="987" height="505" alt="image" src="https://github.com/user-attachments/assets/10b92c40-566d-452a-88a0-1482b4354511" />

5

<img width="975" height="505" alt="image" src="https://github.com/user-attachments/assets/7f04d757-109a-429a-8e7d-23a8a6db71a1" />

6

<img width="975" height="544" alt="image" src="https://github.com/user-attachments/assets/4bd08c3b-baf7-4077-9c59-195b3ff07520" />
