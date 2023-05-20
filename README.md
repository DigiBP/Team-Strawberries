# :strawberry:Team-Strawberries:strawberry:
**:handshake:Team Members:handshake:**
| Name | Email |
| ------------- | ------------- |
| Andrew Bromwich | andrew.bromwich@students.fhnw.ch |
| Alise Garsina | alise.garsina@students.fhnw.ch |
| Karolina Paulauskaite | karolina.paulauskaite@students.fhnw.ch |
| Addhe Vehapi | addhe.vehapi@students.fhnw.ch |


**Coach of the Project: Charuta Pande/Maja Spahic** 

## Introduction
The selection of the supplier might be a quite tought process to go through, however it is a crucial one, since it has a significant impact on the success or losses of a company. That said a strategic approach of choosing the right supplier is important. The supplier selection process involves many different steps, which has a direct effect on company's resourses such as human, financial, time, as well as the quality and reliability of it all. In addition, supplier selection also plays a key role in managing risk and ensuring compliance. It requires careful planning, evaluation and communication, where introduction of digitalization and automation can improve supply process, enhance sustainability and reduce costs.  Our project team is dedicted to help the SMEs to chose the right supplier efficienlty and without investing too much time in the due dilligence process. 

### 🚀 Deliverables for the project: 
* Link to GitHub repositories containing:
* Modelling artefacts (such as BPMN, DMN, CMMN, etc.) and, if required, other project artefacts (such as configuration files, source code, etc.)
* Documentation about project and processes (as GitHub markdown files (e.g., Readme and interlinked .md files)).


## Background
Our project's primary objective is to transform and enhance the supplier selection process by leveraging digitalization and automation technologies. By integrating these cutting-edge solutions, we aim to significantly improve the efficiency and effectiveness of the decision-making process for choosing suppliers. To achieve this, we plan to develop sophisticated decision models that incorporate clearly defined rules and criteria, ensuring a consistent and transparent evaluation process.

Additionally, we will create Application Programming Interfaces (APIs) that facilitate seamless integration with existing systems and enable a user-friendly platform for effortless operation. This platform will empower stakeholders to access essential information, streamline workflows, and make informed decisions in a timely manner. The combination of advanced decision models and an intuitive digital platform will not only simplify the supplier selection process but also promote a more collaborative and data-driven approach to strategic procurement management.


### The 'As-Is-Process':

![Supplier Selection As-Is v2](https://user-images.githubusercontent.com/127504098/232316079-b0c1c2c4-e8f4-43ec-a95d-307f15135c94.png)


### Description-of-the-Workflow-Steps
The process model begins with identifying potential suppliers through market research, consulting stakeholders, reviewing industry publications, and creating a list of potential suppliers. If enough suppliers are identified, the process moves to the pre-qualification stage. In this stage, suppliers are evaluated based on criteria such as company characteristics, product quality, financial stability, geographical location, and sustainability practices. Initial screening of suppliers is performed using these criteria, and if there are enough pre-qualified suppliers, the process proceeds to soliciting information from suppliers. This involves developing and distributing a Request for Information (RFI) or Request for Proposal (RFP), and reviewing responses. Based on the satisfactory nature of the responses, the process either continues to the evaluation stage or returns to earlier steps.

The evaluation stage consists of developing a weighted scoring system, scoring and ranking suppliers based on their RFI/RFP responses, and conducting site visits or audits if necessary. If top-ranked suppliers are suitable, the process moves to negotiating and setting contract terms, which includes developing negotiation strategies, negotiating with top-ranked suppliers, finalizing contract terms, and signing contracts. Once negotiations are successful, the process enters the monitoring and review stage. This involves establishing Key Performance Indicators (KPIs), monitoring supplier performance, conducting periodic reviews, providing feedback, and identifying improvement opportunities. If the supplier meets performance expectations, the relationship continues; otherwise, contract terms are revisited or alternative suppliers are considered.


### Task: Conduct Supplier Evaluation

![Screenshot 2023-05-03 at 21 22 44](https://user-images.githubusercontent.com/5271595/236023068-54cb2977-5202-4f3f-96d5-82a766b806ef.png)


The group has defined a point system, which helps us to decide, which supplier should be chosen, considering our criterias set.

The following criterias were defined with the possible inputs in the brackets:

* Country (Switzerland, Germany, Italy, France etc.)
* Quality Grade ("A", "B", "AB")
* Price per kg (">=5", "<5", "<=4") 
* Minimum order ("<=200")
* Maximum order ("<=500")
* Certification ("HACCP", "Bio Suisse")
* Shipping Method ("Air", "Ground", "Sea")
* Lead Time (">=5")

![Screenshot 2023-05-03 at 21 25 06](https://user-images.githubusercontent.com/5271595/236023525-c1bbd31c-9ff3-4d4f-9e65-03b2e34509e6.png)


Here is our longlist grading:

A, this is the highest grade. The supplier fullfills all necessary criterias.
B, this is the medium grade. The supplier is placed on the waiting list, in case the perferred supplier is not fullfilling his deliverables.
R, this is the lowest grade. The supplier is rejected directly, since the criterias set are not fullfilled.

![Screenshot 2023-05-03 at 21 25 45](https://user-images.githubusercontent.com/5271595/236023789-f3c7cc5c-49d4-49e6-a084-be2c909b3fe6.png)


## Process Improvement

* The steps of the evaluation can be automized 
* The request of information and price can be automized

The main issue with the As-Is process is that there is little to no automation, and most of the process steps are formed with user tasks, which consumes a lot of time to be reviewed and manually forwarded futher within the process. 

### Process Digitization & Automation

For this we have implemented:
* Structured definition of evaluation criteria. The main factors that we took into consideration are: location, qualitz grade, price, minimum and maximum order quantity, obtained certifications, shipping method and lead time.
* Set up of an evaluation form. For this step we are using a web-based form builder JotForm. It includes all the questions and areas that correspond to the defined criteria. 
* Integration with supplier data. After receiving filled out forms, the evaluation results then are integrated with the supplier data that is stored in a database, which is in our case google sheets using data connectors.
* Automation of data collection. Data collection will be automated by sending the evaluation for to suppliers via email. Then the supplier can then fill out the form and submit it electronically.
* Automation of data analysis. According to the answers provided by the suppliers in the form and they will be given certain amount of points, which will be displayed and ranked in the desicion table providing a clear overview of the supplier suitability. It helps to sort the suppliers into the list of the potential candidates and a definit declines. 
* Signing the contract. Based on the evaluation data and outcomes, companies can decide, which suppliers are the best to choose for their business colloboration. After the desicion is taken and final negotiation is completed supplier will receive el. contract using automated workflows which can be signed and submited electorincally, and can be stored in the data base as well. 

### Steps to be taken

1. Define Criteria for Suppliers
2. Create data base
3. Connect it with MAKE
3. Create Information Request Form
4. Connect it with data base
5. Create a Decision Table
6. Prepare Supplier Scorecard
7. Evaluate the Report from Input Data
8. Create a Digital Contract
9. Execute the Process

## :soon: The 'To-Be-Process':

### Overview

The Supplier Selection has a high priority and imporatance in our fictive business operations calling for effective decision-making and collaboration. To achieve its best potential, it is crucial for business to implement effective and standardized approach when choosing suppliers. To optimize As-Is process, it is essential to establish fine balance between automation and manual tasks. Automated tasks in streamlining of this process helps to get rid of, as much as possible, manual errors as well provide cost/time-efficiency. The "To Be" process for supplier selection described below in more details combines automated steps with manual tasks and aims to improve decision-making, optimize supplier evaluation, and ensure consistency in the selection criteria. 

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/e081f2f6-c543-407c-8b6c-653cb355484d)

The purpose of implementing the "To Be" supplier selection process is to increase decision-making accuracy and efficiency og the overall process. It creates and advantage of technology capabilities while taking into account the special insights and experience from different stakeholders. 

### Goals 

As mentioned before there are certain expectations for this partial process automation. The goals of it are as follows: 

* Automate time-consuming, repetitive tasks to streamline the entire supplier selection process. 
* Enable internal and external stakeholders engagement in supplier evaluation and selection to collaborate and communicate more effectively. 
* For thorough supplier research automate the collection of pertinent data from databases and industry publications.
* Keep the process flexible by continuing to use manual tasks for judgment calls and decision-making. 
* Automated release of RFI and RFQ forms to supplier
* Maintainace and completion of current list of potential suppliers (supplier file) using both automatic and human inputs. 

It is imporant to note that while some steps such as reviewing publications and databases, and reviewing a list of potential suppliers can be austomated, the final supplier selection will remain as a manual task to guarantee awarness and full understandment of the outcome and other qualitative factors that could be involved in the selection process. 

### Assumptions

There must be certain assumptions made for the fluent implementation of the "To Be" process for supplier selection. For the sake of the exercise we must assume that: 

:one: Access to the industry publications, databases, and other relevant research sources is available. 
:two: Consultation with external and internal stakeholders are available and they are willing to share their recommendations. 
:three: The automated system can efficiently collect and exhibit data from sources. 
:four: The RFI and RFQ are sent to all relevant existing players within the industry and the answers are populating the database for the n amount of times (unlimited submissions). 
:five: The business - Redsweetberries, has well predefined criteria and guidlines to aid on the evaluation and the official documentaion is attainable to all in the decision included members. 

Keeping in mind these indicated assumptions we can proceed to each step evaluaition. 

### Conduct Market Research

- Describe more in detail the automation of the step. 

### Send RFI & RFQ to Suppliers

- Describe more in detail the automation of the step. 

### Update supplier file

- Describe more in detail the automation of the step. 

### Analyze Supplier Response 

### Select Supplier 
