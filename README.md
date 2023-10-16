# Postman_Demoqa.com
**API testing example**  
This project implemets JS Postman API autotests for https://demoqa.com/swagger   
A tech stack: Postman + JS + Jenkins + Newman + Allure 
For "Account" section were made:  
- Autotests — [ссылка](https://www.postman.com/badboy5555/workspace/pub/request/21209626-ac151384-eead-4c63-ba9c-359d351f7947)
- Pipeline for neman + Jenkins — [ссылка](https://github.com/Badboy5555/Postman_Demoqa.com/blob/main/Jenkins_cfg_demoqa.yml)

# Installation
1. Install Postman [Postman home page tutorial](https://www.postman.com/downloads)
2. Install NodeJs v18.16.0 [NodeJS home page tutorial](https://nodejs.org/en/download/current)
3. Install Newman v5.3.2:
 using CLI, run command: `npm install -g newman@5.3.2`
5. Install Allure v2.22.1: 
 using CLI, run command: `npm install -g newman-reporter-allure`
6. Install Jenkins v2.375.4 [Jenlins home page tutorial](https://www.jenkins.io/download/)   
7. Clone the project `git clone https://github.com/Badboy5555/Postman_Demoqa.com.git`

# Tests runnig
To run all test:
- Newman run command: using CLI, navigate to project directory and run command: `newman run Demoqa.postman_collection.json -e Demoqa.postman_environment.json -r allure --reporter-allure-export allure-results`
- automatic Jenkins pipeline: New Item -> Pipeline -> put content of Jenkins_cfg_demoqa.yml in csript-field -> Build

# Report 
To generate testrun report: 
- after Newman run command: using CLI, navigate to project directory and run command: `allure serve allure-results`
- after automatic Jenkins pipeline: click Allure icon 
  
