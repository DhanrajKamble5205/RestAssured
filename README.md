## Framework From Scratch (Rest Assured)
1. Payload (Serialization (Java to JSON)), Deserialization (JSON to Java)
    1. GSON
    2. Jackson API 
2. Allure Reports
3. POJO
4. Custom Hybrid Framework
5. Data Driven Testing
6. Log4j
7. Folder Structure to keep the data. 
8. TestNG listeners
9. JSON schema validation

### What is Framework?
**Framework**  - Organising your code in such a manner, where we can achieve the Maintenance., Reusability.

### Why we use framework in Rest Assured?
- Maintenance
- Reusability
- Structured way
- Organize 
- Readability

## Good API Automation Framework **

- Proper Folder structure.
- Payload Mangement.
- Flexibility and Scalability
- Data-Driven Testing
- Integration with CI/CD
    - Email Report
    - Enhanced Reporting (logs)
- Support different Envs QA, Stage, Preprod, Prod.
- Credentials should be hidden. 
- Utilities - REST ( APIs) - Generic in nature. 
- Linting - Best Coding Practices - SolarLint

## Custom Hybrid API Automation Framework 
1. Mixture of Data Driven + Module Driven + Payload -> Generic Framework
    1. REST API - we will automate - JIRA API, GITHUB API, 
    2. SOAP

## **Tech Stack**
1. Java
2. Rest Assured 
3. Maven & TestNG , Assert J.
4. Payload Management - POJO 
    1. GSON
    2. Jackson API
5. Allure Report
6. Logs - log4j
7. Test - Data JSON Files
8. Excel 
    1. Apache POI
9. Linting - Sonarlint 
10.  JDK > 22-24 , 
11. GIT & GITHUB
12. Jenkins.

### API Framework Components

![image.png](https://eraser.imgix.net/workspaces/kmE7FXkcgw31ToHKQANL/WWS31TdyovhjTB1TVo9v2jWpPei1/c4YBRvI99ARBbh-1a996A.png?ixlib=js-3.7.0 "image.png")

![image.png](https://eraser.imgix.net/workspaces/kmE7FXkcgw31ToHKQANL/WWS31TdyovhjTB1TVo9v2jWpPei1/yvfNm85qdKKQ5eQphghyo.png?ixlib=js-3.7.0 "image.png")

### Folder structure  API Automation
**src**

- **main -> **folder which will contain all files **which are not tests**
    - endpoints - auth, booking, booking/:id:
    - modules - payload manager 
    - pojos 
- **test -> **files which are tests cases
- tests - all your Testcases
    - crud
    - integration 
    - **sample**
- asserts - assertion files - assertActions
- base - > common to all Testcase file
- **resources **
    - TestData.xlsx.
    - data.properties - url, credentials

[﻿github.com/PramodDutta/APIAutomationFramworkATB11x/blob/main/README.md?plain=1](https://github.com/PramodDutta/APIAutomationFramworkATB11x/blob/main/README.md?plain=1) 

### Framework
- Individual Testcases (more assertions)
    - Positive
    - Negative
        - e.g -> testCreateBooking ( TC)
- E2E Integration / Testcases
    - Combine multiple of the TC
    - Less Assertions
        - e.g -> TestIntegrationFlow1

# How to change the Allure Report?

[﻿allurereport.org/docs/gettingstarted-readability/](https://allurereport.org/docs/gettingstarted-readability/) 

Foler Structure Ready - Part 2
[﻿github.com/PramodDutta/APIAutomationFramworkATB11x/tree/main/src/main/java/com/thetestingacademy](https://github.com/PramodDutta/APIAutomationFramworkATB11x/tree/main/src/main/java/com/thetestingacademy) 

## API Automation Framework with Rest ASSURED

![image.png](https://eraser.imgix.net/workspaces/kmE7FXkcgw31ToHKQANL/WWS31TdyovhjTB1TVo9v2jWpPei1/o9ENVhI3qz0i-Q2o-XV_A.png?ixlib=js-3.7.0 "image.png")

Java Object -> JSON
## Serialization (Java Object to JSON)
- Why we are doing the serialization  Suppose we want to transfer the lightweight data, which is JSON, from client to server. So, it is always advisable to convert your Java object to JSON to transfer the data from client to server over the network. The process is called as serialization. 
- `Please remember you can always use two types of library: JSON and Jackson API to serialize the data. The syntax is given below for JSON.` 


```
Gson gson = new Gson();
String jsonStringBooking = gson.toJson(booking);
System.out.println(jsonStringBooking);
```


## Deserialization (JSON to Java Object)
```
BookingResponse bookingResponse = gson.fromJson(jsonResponseString1,BookingResponse.class);
[﻿github.com/DiUS/java-faker](https://github.com/DiUS/java-faker) 

** How do you handle SSL in REST Assured?**

- relaxedHTTPSValidation()

## TestNG Listeners
TestNG listeners in Java are powerful tools that allow you to modify and enhance the default behavior of TestNG during test execution.

## Types of TestNG Listeners
TestNG offers several listener interfaces, including:

1. **ITestListener**
2. ISuiteListener
3. IReporter
4. IAnnotationTransformer
5. IInvokedMethodListener
6. **IExecutionListener**
7. IHookable
8. IMethodInterceptor


**NEED to learn, How to Pass the value of the Token, Booking ID from one Test to another Test. **

ITestContext - TestNG listener - 

ITestContext **iTestContext**  -> setAttribute(), getAttribute()

iTestContext.setAttribute("bookingid",bookingResponse.getBookingid());

Integer bookingid = (Integer) iTestContext.getAttribute("bookingid");

# API Automation Framework - Last Part 

[﻿github.com/PramodDutta/APIAutomationFramworkATB11x/tree/main/src/test/java/com/thetestingacademy/tests/e2e_integration](https://github.com/PramodDutta/APIAutomationFramworkATB11x/tree/main/src/test/java/com/thetestingacademy/tests/e2e_integration) 

1. Run this Framework via the Jenkins + Github. -> 85%
2. Another way to create a jar file and Run it via the Jenkins  -> jar creation , old technology


