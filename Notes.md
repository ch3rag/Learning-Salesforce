# Salesforce Notes
### Introduction
* Salesforce is CRM software.
* It helps to stream-line the processes of customer acquisition, customer relationship management and interaction with company's current and potential customers.
* It has various functional capabilities for complete CRM process such as Marketing, Sales & E-Commerce, Services, Community, Analytics, IoT & AI, Apps EcoSystem(AppExchange) and Support.
### Architecture
#### Front-End
* Salesforce has two user interfaces:
 1. Salesforce Classic UI
 2. Salesforce Lightning UI
* Salesforce Classic UI is an old salesforce user interface which uses __VisualForce__ for the development.
* Salesforce Lighting UI was introduced in 2014 and is more modern UI that uses either __Aura Component__ or __Lighting Web Component__ for front-end development.
* Lightning Web Component is faster than Aura Component. Also, the Salesforce Classic UI is soon will be discontinued.
#### Back-End
* Salesforce uses __Oracle Database__ in the backend to store the data. However, the developers cannot directly interact with the database, rather, they interact with the __Salesforce Objects__.
* Salesforce Objects are similar to database tables where data is stored in the tabular format. The columns are known as __Fields__ and the rows of data are called __Records__.
* At the back-end, salesforce uses it's proprietary language called __Apex__ for development, which is similar to Java.
* Apex can be used to interact with the objects(database tables) using __Salesforce Object Query Language__ or __SOQL__.
* There are some declarative tools that can be used to interact with the salesforce objects such as:
 1. Workflow Rules
 2. Process Builder
 3. Visual Flows
 4. Approval Process

