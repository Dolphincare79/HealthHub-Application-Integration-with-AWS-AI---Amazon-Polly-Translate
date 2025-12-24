# HealthHub-Application-Solution-Integration-with-AWS-AI---Amazon-Polly-Translate
Implementation of Functionality for Converting Medical Information into Natural Speech in Multiple Languages using AWS AI Services (Amazon Polly and Amazon Translate)


Implementation of Functionality for Converting Medical Information into Natural Speech in Multiple Languages using AWS AI Services (Amazon Polly and Amazon Translate)

This project implements a serverless solution on AWS to convert medical information into natural speech in multiple languages using Amazon Polly and Amazon Translate.
It features secure authentication with Amazon Cognito, data hosting on Amazon S3, backend processing with API Gateway and AWS Lambda, and storage in DynamoDB.
The architecture is fully monitored with CloudWatch, ensuring scalability, security, and real-time processing, making it ideal for multilingual healthcare applications.

## Step 01 - HealthHub Backend Implementation

# Downloading and Unzipping Project Files

wget https://tcb-bootcamps.s3.us-east-1.amazonaws.com/aicloud-bootcamp/v1/module4/healthhub-module-4.zip
unzip healthhub-module-4.zip

cd healthhub-module-4/
ls
cd health-hub-backend/

cat package.json
cat serverless-compose.yml 
tree -L 3 src/

npm install  

 
# Installing Dependencies For Each Service's Project

for service in src/services/*; do (cd "$service" && npm install) done


# Deploying HealthHub Backend

npm run deploy

cat .serverless/compose.log
cat .serverless/compose.log | grep -i error



## Step 02 - Validating AWS Service's Created

- CloudFormation
- AWS Lambda | Function
    - `hh-ai-interaction-dev-getInteraction



## Step 03 - Code Explanation for “AI-Interaction-Service”
- Let’s use `vi` command or `VS Code` over these files:

`health-hub-backend/src/services/ai-interaction-service/serverless.yml`

`health-hub-backend/src/services/ai-interaction-service/src/services/aiInteractionService.ts`



## Step 04 - HealthHub Frontend Implementation

cd ../health-hub-frontend
cat package.json
tree -L 3 src/

npm install

# Defining the API Base URL for VITE
cp .env.example .env && nano .env



## Step 05 - Running HealthHub Serverless Application

# You can use this command line bellow to get your EC2 Workstation Instance Public IP Address:
aws ec2 describe-instances | grep -i PublicIpAddress

mv tailwind.config.js tailwind.config.cjs

# Running HealthHub Serverless Application:
	npm run dev -- --host



## Step 06 - Accessing HealthHub Serverless Application

- EC2 Security Group: `5173`
- **`HTTP**://Your_EC2_Public_IP:5173`


## Step 07 - Adding a Doctor and a Patient

- **Doctor**:
    - Email: `david.lee@hh.com`
    - Password: `123456`
    - Role: `Doctor`
    - First Name: `David`
    - Last Name: `Lee`
    - Date of Birth: `01/01/2001`
    - Gender: `Male`
    - Contact Number: `11111111`
    - Specialization: `Radiology`
    - License Number: `111111`
    
- **Patient**:
    - Email: `ava.brown@tcb.com`
    - Password: `123456`
    - Role: `Patient`
    - First Name: `Ava`
    - Last Name: `Brown`
    - Date of Birth: `01/01/2001`
    - Gender: `Female`
    - Contact Number: `11111111`

## Step 08 - Testing HealthHub AI Speech Feature

🇺🇸 Examples of medical information or instructions you could enter:

1. **Patient Allergy Warning**:
    
    "Patient is allergic to penicillin. Avoid prescribing any medications containing penicillin derivatives."
    
2. **Post-Surgery Care**:
    
    "Administer pain relief every 6 hours. Keep the wound area clean and dry. Schedule follow-up for stitch removal in 7 days."
    
3. **Medication Instructions**:
    
    "Prescribe 10mg of Atorvastatin once daily at bedtime to manage high cholesterol levels."
    
4. **Physical Therapy Plan**:
    
    "Recommend physical therapy sessions twice a week for 6 weeks to rehabilitate the right knee after surgery."



