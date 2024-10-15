# API Automation Testing Using JMeter Keyword-Driven Framework

## Overview
This framework is designed for API automation testing using JMeter with a keyword-driven approach. It allows for flexible test execution by using data-driven inputs, making it easier to manage and scale API tests across multiple environments.

## Features
- **Keyword-Driven**: Executes test scenarios based on keywords provided in a CSV file, allowing for easy modifications.
- **Environment-Specific Setup**: Supports multiple environments (e.g., DEV, QA, PROD) with custom configurations.
- **Flexible Execution Order**: The test execution order is driven by the CSV file, not by the sequence in the JMeter test plan.

## Framework Structure

### 1. Global Variables
- Use **User-Defined Global Variables** for values that apply across all environments.
- You can easily add or modify variables as needed.
- You can add multiple user-defined variables.

![Global Variables](https://github.com/user-attachments/assets/db9041c0-4e88-462d-81b1-17fc0c99d3e8)

### 2. Include Controllers
- Include multiple controllers in the test plan based on your requirements.
- Ensure that the name of the include controller matches the name specified in the CSV file.
- The JMX files for these controllers are stored in the `Test_Files` folder.

![Include Controller Setup](https://github.com/user-attachments/assets/dd852191-f15f-4cd9-a832-d09089e8df2c)

### 3. Test Case Management
- To add or modify test cases, update the JMX file under the relevant include controller.
- You can include multiple API calls and transaction controllers in a single JMX file.
- **Note**: Do not add thread groups to the include controllers, as they are not supported.

![Test Case Management](https://github.com/user-attachments/assets/f7c0866b-d1be-44f1-8fca-06d6c9e7c799)

### 4. CSV Data File
- The CSV file that drives test execution is located in the Keyword_CSV_File folder.
- It contains the mapping of include controller names to the order of execution.
- **Execution Order**: JMeter will follow the order specified in the CSV file, not the order in the switch controller.

![CSV File Path](https://github.com/user-attachments/assets/d84d3217-8540-4b09-883c-c73c8041a955)

### 5. Environment-Specific Variables
- Add environment-specific variables under the IF controller for different configurations.
- Ensure that the keys are the same across all environments, with values adjusted according to each environment's needs.

![Environment-Specific Variables](https://github.com/user-attachments/assets/a6301af2-0311-429c-9f8e-41333b398ec4)

### 6. Execution Control
- To run tests in a specific environment, enable only that environment in the IF controller and disable the others.
- For example, enable PROD to execute tests in the PROD environment while keeping DEV and QA disabled.

![Execution Control](https://github.com/user-attachments/assets/249f1002-fce7-4db3-bb58-df90d2b8d8ba)

### 7. Reporting
- Test results are automatically saved in the Test result folder.
- No need to change the path. Most probably it will work but if this do not work you can put an absolute path.
- You can also put multiple view result trees for different kinds of report formats like JTL and XML.

![image](https://github.com/user-attachments/assets/249f1002-fce7-4db3-bb58-df90d2b8d8ba)

### 7. Debugging
- The framework includes debug samplers to help identify and resolve issues during test execution.
- Even if specific test cases are disabled, the debug samplers will still execute to assist with troubleshooting.
- This flexibility allows you to focus on debugging specific parts of your test plan without affecting the overall execution.

![Debugging](https://github.com/user-attachments/assets/a8578c84-0c0f-4856-a8c4-86eef7dc8208)




