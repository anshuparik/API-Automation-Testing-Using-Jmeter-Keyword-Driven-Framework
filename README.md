# API-Automation-Testing-Using-Jmeter-Keyword-Driven-Framework
Keyword-Driven Framework for API Automation Testing Using Jmeter
![image](https://github.com/user-attachments/assets/4f9b24ea-8e6f-4f47-81ae-4081df01f801)
 
User-Defined Global Variables – Put variables that apply to all the environments, you can also add multiple user-defined variables.

![image](https://github.com/user-attachments/assets/db9041c0-4e88-462d-81b1-17fc0c99d3e8)
You can add multiple include controller as per requirements.
Whatever name you provide include controller same name needs to be put in CSV.
All the JMX are available under Test_Files folder. You can put path as shown in picture else you can use absolute path.

![image](https://github.com/user-attachments/assets/dd852191-f15f-4cd9-a832-d09089e8df2c)

To add more cases or debug existing cases open JMX under include controller do changes in this JMX and save.
You can add multiple API calls in the same JMX
You can also add multiple transaction controllers. 
Note - You can’t add a thread group besides that, there are no restrictions.

![image](https://github.com/user-attachments/assets/f7c0866b-d1be-44f1-8fca-06d6c9e7c799)

CSV is available at this path. No need to change the path if you clone the project. but if it does not work you can put an absolute path.

![image](https://github.com/user-attachments/assets/d84d3217-8540-4b09-883c-c73c8041a955)

Jmeter will execute the include controller based on how you put the include controller name in CSV, not under the switch controller. 
E.g. – If you put Get call at last in include controller but in CSV if it is at first then Get call will execute at first.

![image](https://github.com/user-attachments/assets/eaba7ead-0b6a-4f5e-a8bd-cfb533fcb411)
![image](https://github.com/user-attachments/assets/a082196b-2f8c-4921-b25d-6ad6d42b981b)

Whatever names you provide for include controller same should be put in the B column in the CSV
Also, the jmeter will follow the execution order of CSV, not the switch controller.

![image](https://github.com/user-attachments/assets/b0ede5d7-4147-4ff7-a73b-01bf5ad2d4d3)

You can add environment-specific variables under the IF controller.
You can also add multiple user-defined variables under the IF controller. 
Just make sure the key is be same in all environments and values can be different.

![image](https://github.com/user-attachments/assets/a6301af2-0311-429c-9f8e-41333b398ec4)

To execute on a specific environment just enable only that environment and disable the other two
Like In this case PROD is enabled to execute on the PROD environment and Dev, QA is disabled.

![image](https://github.com/user-attachments/assets/249f1002-fce7-4db3-bb58-df90d2b8d8ba)

Reports will be available in the Test result folder. 
No need to change the path. Most probably it will work but if this do not work you can put an absolute path.
You can also put multiple view result trees for different kinds of formats like JTL and XML.

![image](https://github.com/user-attachments/assets/a8578c84-0c0f-4856-a8c4-86eef7dc8208)

These are debug samplers for debugging.
Even if you disable a few test cases (include controller) as shown in the picture.
Still, debug sampler will execute but do not worry cases under them won’t execute.
So, there is flexibility to execute only those cases which are required.














