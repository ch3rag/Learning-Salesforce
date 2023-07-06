# Salesforce Notes
### Introduction
* Salesforce is CRM software.
* It helps to stream-line the process of customer acquisition, customer relationship management and interaction with company's current and potential customers.
* It has various functional capabilities for complete CRM process such as Marketing, Sales & E-Commerce, Services, Incident Management, Community, Analytics (Tableau), IoT & AI (Einstein), Apps EcoSystem(AppExchange) and Support.
---
### Architecture
#### Front-End
* Salesforce has two user interfaces:
    1. Salesforce Classic UI
    2. Salesforce Lightning UI
* Salesforce Classic UI is an old salesforce user interface which uses __VisualForce__ Pages.
* Salesforce Lighting UI was introduced in 2014 and is more modern UI that uses either __Aura Component__ or __Lighting Web Component__ for front-end development.
* Lightning Web Component is faster than Aura Component. Also, the Salesforce Classic UI is soon will be discontinued.
#### Back-End
* Salesforce uses __Oracle Database__ in the backend to store data. However, the developers cannot directly interact with the database, and rather, they interact with the __Salesforce Objects__.
* Salesforce Objects are similar to database tables where data is stored in a tabular format. The columns are known as __Fields__ and the rows of data are called __Records__.
* At the back-end, salesforce uses it's proprietary language called __Apex__ for development, which is similar to Java.
* Apex can be used to interact with the objects(database tables) using __Salesforce Object Query Language__ or __SOQL__.
* There are some declarative tools that can be used to interact with the salesforce objects such as:
    1. Workflow Rules
    2. Process Builder
    3. Visual Flows
    4. Approval Process

![Declarative Tools](images/declarative-tools.png)
---
### Code Editors
1. __Salesforce Setup__: Salesforce's internal code editor. Supports Apex Classes, Apex Triggers, and VisualForce pages. Does not support Aura Component and Lightning Component.
2. __Developer Console__: Better than Salesforce Setup. Can view logs, run test classes and anonymous code. 
3. __VSCode__: Best code editor for salesforce out there.
---
### HeapSize
* There is hard limit that each Apex Program can have up to a Heap Size of 6MB. Exceeding this, can lead to an error.
---
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

__Note: If a value is not assigned, its NULL.__

---
### String Class
```apex
String str = 'i am a string variable';
System.debug('Actual String: ' + str);
//Actual String: i am a string variable

// Capitalize String
System.debug('Capitalized String: ' + str.capitalize());
// Capitalized String: I am a string variable

// Contains
System.debug('Contains ring?: ' + str.contains('ring'));
// Contains ring?: true

// Convert To Uppercase
System.debug('Upper Case: ' + str.toUpperCase());
// Upper Case: I AM A STRING VARIABLE

// Convert To Lowercase
System.debug('Lower Case: ' + str.toLowerCase());
// Lower Case: i am a string variable

// Equals & EqualsIgnoreCase
System.debug('IsEqual to "ring"?: ' + str.equals('ring'));
// IsEqual to "ring"?: false
String name1 = 'Chirag';
String name2 = 'chirag';
System.debug('Name1 equals Name2?: ' + name1.equals(name2));
// Name1 equals Name2?: false
System.debug('Name1 equals Name2?: ' + name1.equalsIgnoreCase(name2));
// Name1 equals Name2?: true

// Remove
System.debug('Remove "ring": ' + str.remove('ring'));
// Remove "ring": i am a st variable

// Replace
System.debug('Replace "ring": ' + str.replace('ring', 'rong'));
// Replace "ring": i am a strong variable

// Split
System.debug('Split by Space: ' + str.split(' '));
// Split by Space: (i, am, a, string, variable)

// Escaping Characters
string str2 = 'My name is \'chirag\'\nI am learning Salesforce!';
System.debug(str2);
// My name is 'chirag'
// I am learning Salesforce!
```
---
### Lists (Ordered List)
```apex
// Declaration
// Empty List
List<Integer> emptyList = new List<Integer>();
System.debug(emptyList);
// ()

// Populated List
List<Integer> numbers = new List<Integer> {1, 2, 3, 4, 5};
System.debug(numbers);
// (1, 2, 3, 4, 5)

// Appending/Inserting
numbers.add(6);
numbers.add(7);
System.debug(numbers);
// (1, 2, 3, 4, 5, 6, 7)

numbers.add(1, 99);
System.debug(numbers);
// (1, 99, 2, 3, 4, 5, 6, 7)

// Indexing
System.debug(numbers[1]);
System.debug(numbers.get(1));
// 99

// Size Of The List
System.debug(numbers.size());
// 8

// Remove An Item
// Remove Excepts An Index
numbers.remove(1);
System.debug(numbers);
// (1, 2, 3, 4, 5, 6, 7)

// Update An Item
numbers[0] = -1; 
// OR numbers.set(0, -1);
System.debug(numbers);
// (-1, 2, 3, 4, 5, 6, 7)

// Remove All Items
numbers.clear();
System.debug(numbers);
// ()
```
### Sets (Unordered Lists)
```apex
// Declaration
// Empty Set
Set<Integer> emptySet = new Set<Integer>();
System.debug(emptySet);
// {}

// Populated List
Set<Integer> numbers = new Set<Integer> {1, 2, 3, 4, 5};
System.debug(numbers);
// {1, 2, 3, 4, 5}

// Adding Items To Set
// Duplicate
numbers.add(5);
numbers.add(6);
numbers.add(7);
System.debug(numbers);
// {1, 2, 3, 4, 5, 6, 7}

// Check If Set Contains An Item
System.debug(numbers.contains(7));
// True
System.debug(numbers.contains(-1));
// False

// Size Of The Set
System.debug(numbers.size());
// 7

// Remove An Item
// Remove Excepts An Item
numbers.remove(1);
System.debug(numbers);
// {2, 3, 4, 5, 6, 7}

// Check If The Set Is Empty
System.debug(numbers.isEmpty());
// False

// Remove All Items
numbers.clear();
System.debug(numbers);
// {}
System.debug(numbers.isEmpty());
// True
```
---
### Maps (K-V Pairs)
```apex
// Maps Declaration
Map<Integer, String> persons = new Map<Integer, String>();

// Add New Item In The Map
persons.put(101, 'Chirag');
System.debug(persons);
// {101=Chirag}

persons.put(102, 'Alex');
persons.put(103, 'Jane');
persons.put(104, 'Smith');
System.debug(persons);
// {101=Chirag, 102=Alex, 103=Jane, 104=Smith}

// Update Values
persons.put(104, 'Ryan');
System.debug(persons);
// {101=Chirag, 102=Alex, 103=Jane, 104=Ryan}

// Getting Values
System.debug(persons.get(101));
// Chirag

// Removing Items From The Map
persons.remove(104);
System.debug(persons);
// {101=Chirag, 102=Alex, 103=Jane}

// Getting All The Keys As Set
Set<Integer> personIds = persons.keySet();
System.debug(personIds);
// {101, 102, 103}

// Getting All The Values In The Set As List
List<String> personNames = persons.values();
System.debug(personNames);
// (Chirag, Alex, Jane)

// Check If A Key Exists
System.debug(persons.containsKey(101));
// True
System.debug(persons.containsKey(105));
// False
```
---
### Constants
```apex
// Constants Using Final
final Decimal PI = 3.14159;
// Can Be Assigned Later, But Only Once!
final Decimal GRAVITY;
GRAVITY = 9.8;
// Print
System.debug(PI);
// 3.14159
System.debug(GRAVITY);
// 9.8
```
### Operators
```apex
// Assignment Operator
Integer x = 5;

// Arithmetic Operators
// Addition
x = x + 5;
System.debug(x); // 10

// Subtraction
x = x - 5;
System.debug(x); // 5

// Multiplication
x = x * 5;
System.debug(x); // 25

// Division
x = x / 5;
System.debug(x); // 5

// Increment And Decrement Operators
x++;
System.debug(x); // 6
x--;
System.debug(x); // 5

// Addition, Multiplication, Subtraction, Division Assignment Operators
x += 5; // 10
x -= 5; // 5
x *= 5; // 25
x /= 5; // 5

// Boolean Operators
Boolean a = true;
Boolean b = false;

System.debug(a && b); // False
System.debug(a || b); // True
System.debug(!a); // False

// Equality Operators
System.debug(a == b); // False
System.debug(a == !b); // True
System.debug('Hello' == 'Hello'); // True
System.debug('Hello' == 'heLlO'); // True
System.debug('Hello' == 'World'); // False

// LT, GT, LTE, GTE
System.debug(5 < 5); // False
System.debug(5 <= 5); // True
System.debug(6 > 5); // True
System.debug(6 >= 5); // True

// Ternary Operator
Integer age = 19;
Boolean isAdult = age > 18? true : false;
System.debug('IsAdult?: ' + isAdult);
```

__Note: == String comparison results in case insensitive character comparison (Hello == heLLo).__