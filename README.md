# Deploy-a-Node.js-app-on-AWS
![node](https://github.com/uvalentino/Deploy-a-Node.js-app-on-AWS/assets/125161023/4b164ef1-6b46-4a5b-be11-1d9bc0a5a529)

## Step1: Setup an AWS EC2 instance
1. Launch an EC2 instance.
2. Choose an Ubuntu OS image.
3. Generate a new key pair and save the .pem file.
4. Select instance type t2.micro.
5. Create an Elastic IP and associate with your instance
6. Connect to the instance using SSH.
## Step2: Configure your instance 
1. Update the outdated packages and dependencies with "sudo apt update"
2. Install git with "sudo apt install git"
3. Install node.js with "sudo apt install nodejs"
4. Install npm package with "sudo apt install npm" 
## Step3: Deploy the project on AWS 
1. Clone your repository for example "git clone https://github.com/verma-kunal/AWS-Session.git" 
2. Setup the following environment variables - (.env) file
   ```bash
    DOMAIN= "your-ec2-ip-address"
   PORT=3000
   STATIC_DIR="./client"
   PUBLISHABLE_KEY=""
   SECRET_KEY="" 
    ```
3. Initialise and start the project with the following commands
  - npm install
  - npm run start
## Step4: Edit Security group inbound rule 
1. Select Security Groups: From the EC2 Dashboard, click on "Security Groups" in the navigation pane on the left.
2. Locate the Security Group: Find the security group associated with your EC2 instance. Click on the security group name to select it.
3. Edit Inbound Rules: In the "Inbound rules" tab, you'll see a list of existing inbound rules. Click on the "Edit inbound rules" button.
4. Add a New Rule: Click on the "Add rule" button to add a new inbound rule. Configure it as follows.
![rule](https://github.com/uvalentino/Deploy-a-Node.js-app-on-AWS/assets/125161023/3cc83d81-506e-45c2-836d-5152e27b9580)

5. Save the Rule: Click on the "Save rules" button to apply the changes.

## Project is deployed on AWS 🎉 
To access your application, open your web browser and enter the following URL in the address bar: http://your-ec2-ip-address:3000. You should get the following result
