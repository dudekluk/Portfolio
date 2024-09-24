# Example of Login test cases

## Table of Contents
* [Test plan for login functionality.](#Test-plan)
* [List of all test cases created in Jira and Xray.](#Jira-Main)
* [Example test cases in full details using Qase.](#Qase-Main)
    * [1. Verify successful login with valid data](#Qase-1)
    * [2. Verify failed login with invalid data ](#Qase-2)
    * [3. Check login with empty fields](#Qase-3)
    * [4. Test password reset functionality ](#Qase-4)
    * [5. Check two-factor authentication](#Qase-5)
    * [6. Check login using social media](#Qase-6)
    * [7. Test logout functionality](#Qase-7)
    * [8. Validate session timeout](#Qase-8)

 

<h1 id="Test-plan">Test plan for login functionality.</h2>

### Description
The main objective is to ensure the quality and reliability of the testing web application's login functionality. The tests will focus on ensuring proper login functionality and expand into different types of tests, including performance, security, and UX. A combination of manual and automated testing will be used to cover various aspects of the login functionality.


### Scope of Testing

1. Verify successful login with valid credentials.
2. Test failed login attempts with invalid credentials.
3. Validate password strength requirements.
4. Ensure proper handling of forgotten password functionality.
5. Check for security vulnerabilities.
6. Verify login page accessibility for users with disabilities.
7. Assess login performance under different load conditions.
8. Check user experience.


### Testing Environment

- **Operating System**: Windows 11
- **Browser**: Google Chrome

### Types of Tests

1. **Functional Tests**: To verify that loign page works according to the requirements.
2.  **Performance Tests**: To verify that min 10,000 user can login and use app at the same time.
3.  **Security Testing**: To verify that no 3rd party can access user accounts. 
4.  **Accessibility Tests**: To verify that loign page passes all requirements from EU Accessibility Act 2025.
5.  **UX Tests**:  To verify positive user response to the login feature.

### Test Schedule
* **Start Date**: Beginning of Sprint 7
* **End Date**: End of Sprint 7 or Continuous testing until all test cases are executed and critical issues are resolved.

### Resources

- **Manual tester**: Responsible for creating and executing test cases.
- **Automation testers**: 
  *  **Performance tester**: Responsible for creating and executing automated permformance testing.
  * **Automation tester**: Responsible for creating and executing automated API and E2E testing
- **Tools**:
   * Jira for team management.  
   * Xray for test management.
   * Confluence for documentation.
   * JMeter for performance testing.
   * Postman for API testing.

### Entry Criteria
- The login feature code is stable for testing.
- Test environment is set up and ready.
- Test cases are designed, reviewed, and approved.
- Test data is designed
  
  

### Exit Criteria

- All test cases are executed.
- All critical and major defects should be fixed or have a solution plan.
- Test coverage should be at least 80%.
- Test summary report is ready.

### Risks and Mitigations
- **Risk**: Changes in requirements or specifications during testing.
  - **Mitigation**: Maintain constant contact with the product owner and monitor documentation changes.
- **Risk**: Lack of testers knowledge.
  - **Mitigation**: Ensure proper training and development to improve testing skills of team members.
- **Risk**: Delays in test execution.
  - **Mitigation**:  Prioritize critical test cases and conduct proper time estimation to avoid delays.



<h1 id="Jira-Main">List of all test cases created in Jira and Xray</h2>

![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/Login_Test_Cases.png "a title")
<br>
<br>
<br>
<br>
<h1 id="Qase-Main">Example test cases in full details using Qase.</h2>

 <a name="Qase-1">1. Verify successful login with valid data</a>  
 
 ---
![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC1.png "Test Case 1")
 <a name="Qase-2">2. Verify failed login with invalid data </a>
 
 ---
![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC2.png "Test Case 2")
 <a name="Qase-3">3. Check login with empty fields</a>
 
 ---
![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC3.png "Test Case 3")
 <a name="Qase-4">4. Test password reset functionality</a>
 
 ---
![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC4.png "Test Case 4")
 <a name="Qase-5">5. Check two-factor authentication</a>
 
 ---
![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC5.png "Test Case 5")
 <a name="Qase-6">6. Check login using social media</a>
 
 ---
![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC6.png "Test Case 6")
 <a name="Qase-7">7. Test logout functionality</a>
 
 ---
![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC7.png "Test Case 7")
 <a name="Qase-8">8. Validate session timeout </a>
 
 ---
![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC8.png "Test Case 8")


