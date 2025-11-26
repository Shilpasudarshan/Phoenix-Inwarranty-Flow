# Postman API Automation Integration with Github Actions #

This repository is the POC for integrating Postman Tests with github actions. The tests are written in postman and they are executed on the vertual machine with the help of newman and newman-reporter-htmlextra.
Github actions will trigger the project execution on every push to the main branch. you can also execute the project manually using workflow_dispatch. The projects runs on the scheduled time with the help of cron job.

The HTML reports archived and kept in the artifact section for the team to download it. Along with that they can view the report directly from the github page : https://shilpasudarshan.github.io/Phoenix-Inwarranty-Flow/.
The latest reports is mailed to the team members using GMAIL SMTP.

## About Me ##
Hi My Name is Shilpa Gururajaiah. I have 4 years of experience in Automation Testing and Devops. My Skillset Include UI Automation with Selenium Webdriver, Cypress, 
Playwright and API Testing I use Rest Assured and Postman. You can connect with me over : [Linked In](https://www.linkedin.com/in/shilpa-gururajaiah-883a3b322/)

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing and Edge Case Testing
3. Token Testing
4. Data Driven Testing with CSV
5. Schema Validation
6. Secrets Management with Github Secrets  

## Tech-Stack ##
1. Postman
2. Nodejs 22
3. Newman
4. Newman-reporter-htmlextra
5. Github Actions
6. Gmail SMTP
7. Github Pages
8. CSV for Data Driven Testing
9. AWS-EC2 for self hosted github runner

## Github Pages ##
You can directly view the latest test report of the postman test at the Github page link : https://shilpasudarshan.github.io/Phoenix-Inwarranty-Flow/

## HTML Report ##
The Report will be created in the newman folder
![Postman Report](https://github.com/Shilpasudarshan/Phoenix-Inwarranty-Flow/blob/static-content/newman-report.png)

## Project Structure ##
```
Phoenix Inwarranty Flow
├─ Inwarranty-flow collection.postman_collection.json
├─ QA.postman_environment.json
└─ TestData.csv

```

## How to run the project ##
You can the project on your local system for that:
1. Clone the project on local system: https://github.com/Shilpasudarshan/Phoenix-Inwarranty-Flow.git 
2. Install the Nodejs and NPM: https://nodejs.org/en
3. Install Newman using: ``` npm install -g newman ```
4. Install Newman-reporter-htmlextra: ``` npm install -g newman-reporter-htmlextra ```
5. Run the Neman Command:
   ```
              newman run 'Inwarranty-flow Collection_CLI.postman_collection.json' \
             -e QA.postman_environment.json \
             -d testdata.csv \
             -r cli,htmlextra \
             --reporter-htmlextra-export ./newman/index.html
   ```


 

   
