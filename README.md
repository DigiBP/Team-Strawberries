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
Currently the As-Is-Process is very manual and user task driven. That said, the process is prone to error and is not efficient. The main issue with the As-Is process is that there is no automation, and most of the process steps are formed with user tasks, which consumes a lot of time to be reviewed and manually forwarded futher within the process. 

### ⌛ Following tasks shall be automated/digitilized: 
* The market research
* Sending of the RFI & RFQ to the chosen suppliers 
* Update of the data base with the answers from the potential suppliers 
* Evaluation of the supplier with the scoring system corresponding to their responses  

### Steps to be taken
1. Set up Google account
2. Connect to Google Sheet
3. Define Criteria for Suppliers
4. Create Supplier Search/RFI & RFQ Forms
5. Generate data base
6. Evaluate the Results from Input Data
7. Connect it with MAKE
8. Connect MAKE with Camunda
9. Execute the Process

# The 'To-Be-Process':

After evaluating the As-Is-Process our team found a few tasks that had a potential for automization and digitization decreasing its complexity, saving time and improving overall process performance. In this way the tasks are going to be user-friendly and also transparent. Following are the steps taken from our team, to automize/digitize the process.

### Process Digitization & Automation

To improve the overall process of supplier selection we have implemented:
* Structured definition of evaluation criteria. The main factors that we took into consideration are location, quality grade, price, minimum and maximum order quantity and obtained certifications. 
* Set up of Google Forms. This will help to initiate the process and to better evaluate the supplier. For this step we are using a Google Forms. It includes, the request from the customer, and request for information and qouta with all of the questions and areas that correspond to the defined criteria for the supplier. 
* Automation of data collection. Data collection will be automated by sending the RFI & RFQ form to the suppliers via email. Then the supplier can fill out the form and submit the answers electronically.
* Integration of supplier data. After receiving filled out forms, the provided information, using data connectors, is then integrated as the supplier data that is stored in the database, which in our case is Google Sheets.
* Automation of data analysis. According to the answers provided by the suppliers in the forms they will be given certain number of points, which will be displayed and ranked in the decision table providing a clear overview of the supplier suitability. It helps to sort the suppliers into the list of the potential candidates and a definite declines.

Process is triggered by the product order request and ends once the best supplier(s) is chosen for the order fulfillment :arrow_down:.

![Supplier Selection To-Be new (2)](https://github.com/DigiBP/Team-Strawberries/assets/5271595/a2a3a3dc-7b42-454e-973b-49f658783835)

The purpose of implementing the "To Be" supplier selection process is to increase decision-making accuracy and efficiency of the overall process. It provides the advantage of technology capabilities while taking into account the special insights and experience from different stakeholders. 

### Goals 

As mentioned before there are certain expectations for this process partial automation. The goals of it are as follows: 

* Automate time-consuming, repetitive tasks to streamline the entire supplier selection process. 
* Enable internal and external stakeholders’ engagement in supplier evaluation and selection to collaborate and communicate more effectively. 
* For thorough supplier research automate the collection of pertinent data from databases and industry publications.
* Keep the process flexible by continuing to use manual tasks for judgment calls and decision-making. 
* Automated release of RFI and RFQ forms to supplier.
* Maintenance and completion of current list of potential suppliers (supplier file) using both automatic and human inputs. 

It is important to note that while some of the steps can be automated, there will still remain manual tasks to guarantee awareness and full comprehension of the outcome and other qualitative factors that could be involved in the selection process.

### Assumptions

There must be certain assumptions made for the fluent implementation of the "To Be" process for supplier selection. For the sake of the exercise, we must assume that: 

* :one: Access to the industry publications, databases, and other relevant research sources is available. 
* :two: Consultation with external and internal stakeholders are available and they are willing to share their recommendations. 
* :three: The automated system can efficiently collect and exhibit data from sources. 
* :four: The RFI and RFQ are sent to all relevant existing players within the industry and the answers are populating the database for the n amount of times (unlimited submissions). 
* :five: The business - Strawberry Inc., has well predefined criteria and guidelines to aid on the evaluation and the official documentation is attainable to all in the decision included members. 

Keeping in mind these indicated assumptions we can proceed to each step evaluation. 

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


## Steps in Process Automation using MAKE scenarios and Camunda

To implement the automation and to guarantee process flow efficiency MAKE scenarios were used. To set up this environment first step was to create a common Gmail account, from which all of interactions would be conducted, such as: receiving order request, sending/receiving the RFI & RFQ forms, communication with suppliers, as well as the access to Google Sheet and Google Form.

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/838c8b79-80a4-446e-affe-e9e13e63f624)

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/6bd3dbd6-538e-4a37-adfb-1b6df1fbfbad) 

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/af29c7ad-e471-4ab1-aefe-4de2cce0deed)
 
Google Sheet is serving as a data base for the purpose of this assignment.

### 1. Integration of Google Sheets

Everytime the process is trigged by the request, new row in Google Sheet is added, which helps to collect inputs for data base and send the tocken to the following process. 

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/bd1c11c7-2562-410c-8459-9c9fec2d052d)

To identify seperate suppliers and facilitate further processing, a unique identifier called BKey (Business Key) for each supplier is created, which essentially helps to pull and connect the required data to Camunda later on in the process. 

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/028589ff-3bc7-4dfe-b6db-8fc32cdf99bf)

This helps to retain the data and recognize it within the different steps. 

### 2. Process trigger - Request for the Order

The process starts once internal supplier search request is received from Order Product Process. This form contains Requester details (name, surname), Requester e-mail (work e-mail) and required Product Name. 

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/34474438-776d-48d1-8018-8639aec73708)

Once the request been sent, e-mail at redsweetberries@gmail.com account is received stating that this specific form has a new response, and it is populated in the internal supplier data base. 

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/11fd561b-eb37-4528-a232-9c29a36e93c2)
 
![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/1994b9d8-cb7a-4286-bfbe-7454021fce10)

The token in Camunda is created after Message Start Event is initiated and transferred to the first user task of Input Supplier Search, which has to be claimed and completed. 

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/36692fa7-c367-4936-a709-f1a0992aace2)
 
![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/6cb7e3d8-c11d-4b23-b5cf-abc00aa69459)
 
After the Input Supplier Search is completed the token moves forward to the next Service task.
 
![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/e6918da4-c424-4cd9-8218-eb3db9263e2c) 

### 3. Conduct Market Research

Market research is conducted by using OpenAI's model capabilities, along wiht the integration of Google Tools. 
Depending on the incoming request the form is submited by specifying search for supplier and the product. For example requesting certain amount of strawberry suppliers, the country of origin and the suppliers email address. 
 
![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/24ee66d2-63a3-4cb7-aced-7b422affb3ce)
 
By submiting this form the process is moving its token further to the following User Task. 
 
![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/41255956-2a9c-4339-8c8b-0d5144bf6a89)
 
By claiming this task we receive AI generated inputs for the request, which then has to be reviewd and recorded in supplier database in order to send RFI & RFQ form. 

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/5d9b766c-70c0-4cf8-8f7c-037bd9730159)

 
![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/4be70530-245f-4881-8afa-d835f9118c35)

After the task is completed token with two instances (for two different suppliers) moves once more to the next Service Task, and the inputs are saved in the supplier file. 
 
![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/b14d3ab7-75c9-41b2-bd60-951e19167c5a)

### 4. Send RFI & RFQ Form to the List of Suppliers

To sufficiently evaluate the supplier we need to inquire more information. Therefore, Request for Information (RFI) and for Request for Quota (RFQ) form is sent out to each new supplier.

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/003846cd-2d17-42b6-8728-b1c4d1b5d773)

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/e2c6e2ea-3190-4609-aac0-37c8ea43bc19)
 
The form includes criteria on which the final supplier evalutation score is concluded. The required field of input from the supplier side includes: Email, Business Key provided in subject of the e-mail, Company Name, Contact Person, Address, Zip Code & City, Country, Phone Number, Contact Person Email, Quality grade, Certificate. The second half of the form is more directed towards quantitative metrics, that gives more insights into suppliers competitiveness such as: Request for Quote, Price per KG, Minimum Order (in kg), Maximum Order (in kg), and Total Lead Time (days). 
 
This form is sent automatically to the provided supplier email, by running this scenario in MAKE.
 
![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/484ff213-3924-4bf3-8ab2-22e16bbaa84d)
 
This service task have an Exclusive Gateway (or XOR Gateway) meaning that the token instances can be directed to take different paths:
 
![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/b9fc0e51-9896-4568-bc78-20035ff6a227)
 
Path 1: Update Supplier File: When the supplier submits RFI & RFQ form, and it is not meeting specified criteria or other options scored better, the token proceeds directly to the update supplier file service task, that the collected information could be stored anf if needed be shortlisted, or used for the future reference. With the Supplier File Update the process of this path is complete. 
 
Path 2: Wait 7 Days and to proceed to Select Supplier User task: It means that after the service task, the token waits for a period of 7 days (Timer Intermediate Catch Event) before proceeding to the next step, which involves selecting a supplier. 

### 5. Supplier Evaluation

After the RFI & RFQ Form is sent the process token moves forward either when the information is received, or when the time event expires, which is set to be 7 days from the sent out request for information. 

From there on answers given by suppliers are evaluated according to: 
*Points

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/eff14d44-7771-4bf6-ac9f-cbb3df918394)

Each supplier is appointed certain amount of points regarding different evaluation criteria: 
* Country: Allows to estimate total lead time, delivery time, transportation method and costs.
* Quality: A - highest level of quality, AB - good level of quality, B - average level of quality. 
* Price: Provides view on the price competitiveness of the supplier.
* Min. Order: defines limits of the Minimum Order Quantity
* Max. Order: defines limits of the Maximum Order Quantity.
* Certification: Proves suppliers reliability, legitimacy and compliance with respective regulations, bodies or organizations. 

***Scoring System***

<p> :globe_with_meridians: Coutry Point Scale: 0 - 50;  <br>
<p> :straight_ruler: Quality Point Scale: 0 - 50;  <br>
<p> :moneybag: Price Point Scale: The lower price per kilo the higher the score supplier gets: price < 4 awarded 30 points, < 5 awarded 5 points, = 5 awarded 0 points. 
<p> :arrow_down: Min. Order Point: if minimum order < 200, appoint -1000 (=unacceptable). if > 200, keep 0.  <br>
<p> :arrow_up: Max. Order Point: if minimum order < 500, appoint -1000 (=unacceptable). if > 500, keep 0.  <br>
<p> :scroll: Certification Points: Each certification is worth 50 points. <br>

At the end **Total Score** is summed providing the list of selections for the decision. <br>

### 6. The Final Supplier Selection

Based on the evaluation score assigned to each considered supplier clear desicion can be made between choosing the right supplier(s) to fullfil the intial customer request. Automated email is sent to the initial requester with the chosen supplier and its score and the link to the supplier details on Google Sheet.

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/3b63483b-d67a-44ab-9489-d7e0f95c3271)

![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/962e59fa-d0a6-416e-88e8-84e949074ea4)
 
![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/ffd79cb9-528e-4c71-883a-a5c6eceec220)

After selecting the best match for the order request the E-mail is then sent to the requestor with the **Company's Name** followed by its **Total Score**. In addition the link to Google Sheet is shared, to get more detailed view about the supplier, its capabilities and the criteria that was taken into consideration during the evaluation process. 
 
![image](https://github.com/DigiBP/Team-Strawberries/assets/97253646/37476ed3-4eae-4120-8b44-87c9e847f3ae)

On the other hand suppliers that lacked in scoring, or were deemed not sufficient for one or another reason to fullfil the customers request, provided inormation is automatically updated and stored in the internal data base for the future references. 

With this step the supplier selection process is closed!
