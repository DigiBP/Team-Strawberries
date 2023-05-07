# :strawberry:Team-Strawberries:strawberry:
**:handshake:Team Members:handshake:**
 * Andrew Bromwich
 * Alise Garsina 
 * Karolina Paulauskaite 
 * Addhe Vehapi 

**Coach of the Project: Charuta Pande** 

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

### Process Digiization & Automation

For this we have implemented:
* Structured definition of evaluation criteria. The main factors that we took into consideration are: location, qualitz grade, price, minimum and maximum order quantity, obtained certifications, shipping method and lead time.
* Set up of an evaluation form. For this step we are using a web-based form builder JotForm. It includes all the questions and areas that correspond to the defined criteria. 
* Integration with supplier data. After receiving filled out forms, the evaluation results then are integrated with the supplier data that is stored in a database, which is in our case google sheets using data connectors.
* Automation of data collection. Data collection will be automated by sending the evaluation for to suppliers via email. Then the supplier can then fill out the form and submit it electronically.
* Automation of data analysis. According to the answers provided by the suppliers in the form they will be given certain amount of points and then it will be summed providing a clear overview of the supplier ranking, and sorts it into the list of the potential candidates and a definit declines. 
* Signing the contract. Based on the evaluation data and outcomes, companies can decide, which suppliers are the best to choose for their business colloboration. After the desicion is taken and final negotiation is completed supplier will receive el. contract using automated workflows which can be signed and submited electorincally, and can be stored in the data base as well. 

### Steps to be taken

1. Define Criteria for Suppliers
2. Create data base
3. Connect it with MAKE
3. Create Information Request Form
4. Connect it with data base
5. Prepare Supplier Scorecard
6. Evaluate the Report from Input Data
7. Create a Digital Contract
8. Execute the Process

## The 'To-Be-Process':


