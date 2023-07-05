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
![Declarative Tools](images/declarative-tools.png)
### Code Editors
1. __Salesforce Setup__: Salesforce's internal code editor. Supports Apex Classes, Apex Triggers, VisualForce pages. Does not support Aura Component and Lightning Component.
2. __Developer Console__: Better than Salesforce Setup. Can view logs, run test classes and anonymous code. 
3. __VSCode__: Best code editor to salesforce out there.
### HeapSize
* There is hard limit that each Apex Program can have up to a Heap Size of 6MB. Exceeding this, can lead to error.
### Data-Types
* Boolean (True, False, NULL)
```apex
Boolean flag = false;
System.debug(flag);
```
* String ("Hello World")
```apex
String greeting = 'Hello World!';
System.debug(greeting);
```
* Integer (1, 123)
```apex
Integer age = 18;
System.debug(age);
```
* Long (Long Integer 64 Bit)
```apex
Long reallyLongNumber = 123456789L;
System.debug(reallyLongNumber);
```
* Decimal (Floats)
```apex
Decimal pi = 3.14;
System.debug(pi);
```
* Double (Long Floats)
```apex
Double price = 1.67632456;
System.debug(price);
```
* Date
```apex
Date tday = Date.newInstance(2023, 07, 05);
System.debug(tday);
```
* Time
```apex
Time currentTime = Time.newInstance(11, 01, 0, 0);
System.debug(currentTime);
```
* Datetime
```apex
DateTime currentDateTime = DateTime.newInstance(2023, 07, 05, 11, 01, 0);
System.debug(currentDateTime);
```
* Blob (Binary Data: Images, Files)
* ID (Record ID, Object ID, Metadata ID)
    1. 15 Digit ID: Case Sensitive ID
    2. 18 Digit ID: Case Insensitive ID
