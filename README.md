# :strawberry:Team-Strawberries:strawberry:
**:handshake:Team Members:handshake:**
| Name | Email |
| ------------- | ------------- |
| Andrew Bromwich | andrew.bromwich@students.fhnw.ch |
| Alise Garsina | alise.garsina@students.fhnw.ch |
| Karolina Paulauskaite | karolina.paulauskaite@students.fhnw.ch |
| Addhe Vehapi | addhe.vehapi@students.fhnw.ch |


**Coach of the Project: Charuta Pande/Maja Spahic** 

# Introduction
The selection of the supplier might be a quite tought process to go through, however it is a crucial one, since it has a significant impact on the success or losses of a company. That said a strategic approach of choosing the right supplier is important. The supplier selection process involves many different steps, which has a direct effect on company's resourses such as human, financial, time, as well as the quality and reliability of it all. In addition, supplier selection also plays a key role in managing risk and ensuring compliance. It requires careful planning, evaluation and communication, where introduction of digitalization and automation can improve supply process, enhance sustainability and reduce costs. Our project team is dedicted to help the SMEs to chose the right supplier efficienlty and without investing too much time in the due dilligence process. 

## Background
Our project's primary objective is to transform and enhance the supplier selection process by leveraging digitalization and automation technologies. The case presented further, shall be used for best practice cases for other SMEs. By integrating these cutting-edge solutions, we aim to significantly improve the efficiency and effectiveness of the decision-making process for choosing suppliers. To achieve this, we plan to develop sophisticated decision models that incorporate clearly defined rules and criteria, ensuring a consistent and transparent evaluation process.

Our project team will create Application Programming Interfaces (APIs) that facilitate seamless integration with existing systems and enable a user-friendly platform for effortless operation. This platform will empower stakeholders to access essential information, streamline workflows, and make informed decisions in a timely manner. The combination of advanced decision models and an intuitive digital platform will not only simplify the supplier selection process but also promote a more collaborative and data-driven approach to strategic procurement management.

## 🚀 Deliverables for the project: 
* Link to GitHub repositories containing:
* Modelling artefacts (such as BPMN, DMN, CMMN, etc.) and, if required, other project artefacts (such as configuration files, source code, etc.)
* Documentation about project and processes (as GitHub markdown files (e.g., Readme and interlinked .md files)).


# The 'As-Is-Process':

![Supplier Selection As-Is v2 (1)](https://github.com/DigiBP/Team-Strawberries/assets/5271595/d608035f-aa73-4cd7-b05f-3dc1338ea342)

A typical supplier selection process should involve the following steps: 
* Identifying suppliers
* Soliciting information from suppliers
* Setting contract terms
* Negotiating with suppliers
* Evaluating suppliers

The process model beginns with an internal request for a new supplier. As soon as the procurement team receives the request via e-mail, three parallel tasks are exectued from user: 
* review industry publications and databases
* internal and external stakeholder consulting 
* conduct the market research

As soon as all steps are completed, the user is creating a list of potential suppliers with the help of excel ("supplier file"). As soon as the list is complete, the user is sending the Request for Information (RFI) or Request for Proposal (RFP), and reviewing responses. If the information received from the supplier, the user is updating the supplier file. If within 7 days there is no answer, the answers are not received, the supplier on the list is not consiered.

After 7 days, suppliers are evaluated based on criteria such as company characteristics, product quality, financial stability, geographical location, and sustainability practices. Initial screening of suppliers is performed using these criteria, and if there are enough pre-qualified suppliers, the process proceeds to soliciting information from suppliers. The evaluation stage consists of developing a weighted scoring system, scoring and ranking suppliers based on their RFI/RFP responses, and conducting site visits or audits if necessary. If the supplier meets performance expectations, the relationship continue and the department which requested the research, receives an e-mail with the perferred supplier

### ⚡ Problem of As-Is-Process: 
Currently the As-Is-Prozess is very manual and user task driven. That said, the process is prone to error and is not efficient. The main issue with the As-Is process is that there is little to no automation, and most of the process steps are formed with user tasks, which consumes a lot of time to be reviewed and manually forwarded futher within the process. 

### ⌛ Following tasks shall be automated/digitilized: 
* The market research
* Sending of the RFI & RFQ to the chosen suppliers 
* Update of the excel files with the answers from the potential suppliers 
* Evaluation of the supplier responses  

### Steps to be taken
1. Define Criteria for Suppliers
2. Create data base
3. Create Information Request Form
4. Connect it with data base
5. Create a Decision Table
6. Prepare Supplier Scorecard
7. Evaluate the Results from Input Data
8. Connect it with MAKE
9. Connect MAKE with Camunda
10. Execute the Process


# The 'To-Be-Process':

There is a high need to improve process.  After evaluating the As-Is-Process our team found a lot of potential of automizing and ditilizing some processes in a non-complex way. The tasks are going to be user-friendly and also transparent. Following are the steps taken from our team, to automize/digitize the process: 

### Process Digitization & Automation

For this we have implemented:
* Structured definition of evaluation criteria. The main factors that we took into consideration are: location, qualitz grade, price, minimum and maximum order quantity, obtained certifications, shipping method and lead time.
* Set up of an evaluation form. For this step we are using a Google Forms. It includes all the questions and areas that correspond to the defined criteria. 
* Integration with supplier data. After receiving filled out forms, the evaluation results then are integrated with the supplier data that is stored in a database, which is in our case google sheets using data connectors.
* Automation of data collection. Data collection will be automated by sending the evaluation for to suppliers via email. Then the supplier can then fill out the form and submit it electronically.
* Automation of data analysis. According to the answers provided by the suppliers in the form and they will be given certain amount of points, which will be displayed and ranked in the desicion table providing a clear overview of the supplier suitability. It helps to sort the suppliers into the list of the potential candidates and a definit declines. 


## 1) Create a decision model for the supplier evaluation (TO BE DONE!!) 
### Task: Conduct Supplier Evaluation

The team has defined a dedicated point system, which helps us to decide, which supplier should be chosen, considering our criterias set.

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


## 2) Automatically send the RFI & RFQ
### Service Task: Send RFI & RFQ to suppliers 

The Supplier Selection has a high priority and imporatance in our fictive business operations calling for effective decision-making and collaboration. To achieve its best potential, it is crucial for business to implement effective and standardized approach when choosing suppliers. To optimize As-Is process, it is essential to establish fine balance between automation and manual tasks. Automated tasks in streamlining of this process helps to get rid of, as much as possible, manual errors as well provide cost/time-efficiency. The "To Be" process for supplier selection described below in more details combines automated steps with manual tasks and aims to improve decision-making, optimize supplier evaluation, and ensure consistency in the selection criteria. 

Process is triggered by the product order and ends once the right supplier is chosen for the order fulfillment :arrow_down:.

![Supplier Selection To-Be new (2)](https://github.com/DigiBP/Team-Strawberries/assets/5271595/a2a3a3dc-7b42-454e-973b-49f658783835)

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

* :one: Access to the industry publications, databases, and other relevant research sources is available. 
* :two: Consultation with external and internal stakeholders are available and they are willing to share their recommendations. 
* :three: The automated system can efficiently collect and exhibit data from sources. 
* :four: The RFI and RFQ are sent to all relevant existing players within the industry and the answers are populating the database for the n amount of times (unlimited submissions). 
* :five: The business - Redsweetberries, has well predefined criteria and guidlines to aid on the evaluation and the official documentaion is attainable to all in the decision included members. 

Keeping in mind these indicated assumptions we can proceed to each step evaluaition. 

## Steps in Process Automation using MAKE scenarios

To implement the automation and to guarantee process flow effeciency MAKE scenarios were used. To set up this environment first step was to create a common Gmail account, from which all of interactions would be conducted, such as sending/receiving the RFI froms, communication with suppliers, as well as the access to Google Sheet and Google Form.

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/838c8b79-80a4-446e-affe-e9e13e63f624)
 
Google Sheet is serving as a data base for the purpose of this assigment.

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/af29c7ad-e471-4ab1-aefe-4de2cce0deed)

### 1. Intgration of Google Sheets

Everytime process is trigged by the request, new row in Google Sheet is added, which helps to collect inputs for data base and send the tocken to following process. Furthermore, in order to connect the received and registred data with our created BPMN model in Camunda, business key needs to be defined, that generates a random number, which is unique for every input variable, so it could be correctly identified by the process. 

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/bd1c11c7-2562-410c-8459-9c9fec2d052d)

To identify seperate suppliers and facilitate further processing, a unique identifier called BKey (Business Key) for each supplier is created, by using a formula {{pi * random * 1000}}, which essentially helps to pull and connect the required data to Camunda later on in the process. This helps to retain the data and recognize it within the different steps. 

### 2. Conduct Market Research

The process starts once Supplier Search Request is received. This form contains Requester details (name, surname), Requester e-mail (work e-mail) and Product Name. 

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/6bd3dbd6-538e-4a37-adfb-1b6df1fbfbad)

Request for the order initiates the market research. This research is conducted by using OpenAI's model capabilities, along wiht the integration of Google Sheets. 

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/53fd9c93-0ae1-4918-bcb3-b2ca416fd73a)

Depending on the incoming request the market research is activated by specifying search for supplier and the product. For example requesting certain amount of strawberry suppliers, the country of origin and the suppliers email address. 

After the list of suffient amount of suppliers is generated, it sent directly to the Gmail. The output of the request is then transferred into supplier data base in Google Sheet. 

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/06d4cfeb-19be-4adb-8e98-2a42882cc4d8)

From where following processes are executed. 

### 3. Send RFI & RFQ to the List of Suppliers

To sufficiently evaluate the supplier we need to inquire more information. Therefore, Request for Information (RFI) and for Request for Quota (RFQ) form is sent out to each new supplier that is created as a new row from an output of conducted market research.

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/e2c6e2ea-3190-4609-aac0-37c8ea43bc19)

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/484ff213-3924-4bf3-8ab2-22e16bbaa84d)

The form includes criteria on which the final supplier evalutation score is concluded. The required field of input from the supplier side includes: Email, Business Key provided in subject of the e-mail, Company Name, Contact Person, Address, Zip Code & City, Country, Phone Number, Contact Person Email, Quality grade, Certificate. The second half of the form is more directed towards quantitative metrics, that gives more insights into suppliers competitiveness such as: Request for Quote, Price per KG, Minimum Order (in kg), Maximum Order (in kg), and Total Lead Time (days). 

Answers from the supplier are automatically populated within the Google Sheet that can be accessed by any internal process participants.

### 4. Supplier Evaluation

After the RFI & RFQ Form is sent the process token moves forward either when the information is received, or when the time event expires, which is set to be 7 days from the sent out request for information. 

From there on answers given by suppliers are evaluated according to: 
*Points
:exclamation: *Scorecard (do we use??)

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/eff14d44-7771-4bf6-ac9f-cbb3df918394)

Each supplier is appointed certain amount of points regarding different evaluation criteria: 
* Country: Allows to estimate total lead time, delivery time, transportation method and costs.
* Quality: A - highest level of quality, AB - good level of quality, B - average level of quality. 
* Price: Provides view on the price competitiveness of the supplier.
* Min. Order: defines limits of the Minimum Order Quantity
* Max. Order: defines limits of the Maximum Order Quantity.
* Certification: Proves suppliers reliability, legitimacy and compliance with respective regulations, bodies or organizations. 

***Scoring System***

:globe_with_meridians: Coutry Point Scale: 0 - 50; 
:straight_ruler: Quality Point Scale: 0 - 50;
:moneybag: Price Point Scale: ?
:arrow_down: Min. Order Point: if minimum order < 200, appoint -1000 (=unacceptable). if > 200, keep 0.
:arrow_up: Max. Order Point: if minimum order < 500, appoint -1000 (=unacceptable). if > 500, keep 0.
:scroll: Certification Points: Each certification is worth 50 points. 

At the end **Total Score** is summed providing the list of selections for the decision. 

### 5. The Final Supplier Selection

Based on the evaluation score assigned to each considered supplier clear desicion can be made between choosing the right supplier(s) to fullfil the intial customer request. 

After selecting the best match for the order request the E-mail is then sent to the requestor with the **Company's Name** followed by its **Total Score**. In addition the link to Google Sheet is shared, to get more detailed view about the supplier, its capabilities and the criteria that was taken into consideration during the evaluation process. 

On the other hand suppliers that lacked in scoring, or were deemed not sufficient for one or another reason to fullfil the customers request, provided inormation is automatically updated and stored in the internal data base for the future references. 

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/15442fdb-cf89-4bb0-821a-7ca23557f628)

With this step the supplier selection process is closed!
