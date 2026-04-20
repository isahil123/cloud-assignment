AWS EC2 Static Website Deployment
This is my submission for the AWS assignment where I had to launch an EC2 instance, host a static website, and create IAM users with different permission levels.

🌐 Deployed Project Link
http://51.20.204.0

📋 What I Did
I launched an EC2 instance on AWS, set up Apache web server on it, and hosted a static website. I also assigned an Elastic IP so the site stays accessible on a fixed address. On top of that, I created two IAM users — one with no permissions and one with EC2 access — to understand how AWS access control works.

🛠️ Tech Stack

AWS EC2 (t3.micro, Amazon Linux 2023)
Apache (httpd) Web Server
HTML, CSS, JavaScript
AWS IAM
Elastic IP


📸 Screenshots
EC2 Instance (AWS Console)
Show Image
User 1 Login - No Permissions
Show Image
User 2 Login - EC2 Access
Show Image

👥 IAM Users
I created two IAM users to demonstrate different access levels:

user1-no-access — This user has zero permissions. When they try to access EC2, they get an "Unauthorized" error.
user2-ec2-access — This user has the AmazonEC2FullAccess policy attached, so they can view and interact with EC2 instances.


⚙️ Steps I Followed

Launched an EC2 instance (Amazon Linux 2023, t3.micro) from AWS Console
Created a key pair and downloaded the .pem file for SSH access
Allocated an Elastic IP and associated it with the instance
Connected to the instance via SSH using Windows Command Prompt
Installed and started Apache (httpd) web server
Uploaded my static website using SCP and copied it to /var/www/html/
Created 2 IAM users with different permission levels


🚧 Challenges I Faced

The nano editor kept showing "log file support is not available" and wasn't saving the file properly, so I had to use SCP to upload the file directly from my local machine instead.
While logging in as User 2, the region was set to Asia Pacific (Sydney) by default instead of Europe (Stockholm) where my instance is. The console access still worked fine though.
Getting the key pair permissions right on Windows took a bit of trial and error.


🖥️ Instance Details

Instance ID: i-03b156c29cec00774
Instance Type: t3.micro
Region: Europe (Stockholm)
Elastic IP: 51.20.204.0
Web Server: Apache (httpd)
OS: Amazon Linux 2023
