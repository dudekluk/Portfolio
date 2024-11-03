
<h1 id="Test-plan">Test plan for skleptest.pl</h2>

### Description
The main objective is to ensure the quality and reliability of the e-commerce website [https://skleptest.pl/](https://skleptest.pl/) functionalities, including login, registration, product browsing, and shopping cart. The tests will focus on ensuring proper functionality and expand into different types of tests, including performance, security, and UX. The main tests performed will be manual tests, that will cover various aspects of these functionalities, and should later expand into automation.


### Scope of Testing

**Registration**
- Successful registration with valid credentials
- Failed registration with invalid data (empty fields, invalid email, weak password)
- Email verification process
- Password reset functionality
- Social media login 
- Terms and conditions acceptance
- Data privacy policy acceptance

**Login**
- Successful login with valid credentials
- Failed login with invalid credentials
- Password strength requirements
- Forgotten password functionality
- Security vulnerabilities
- Accessibility for users with disabilities
- Performance under load

**Product Browsing**
- Product listing display (name, price, image, description)
- Product sorting
- Product filtering (category, brand, price range)
- Product search functionality (keyword, phrase)
- Detailed product information display

**Shopping Cart**
- Adding products to the cart
- Updating product quantities in the cart
- Removing products from the cart
- Viewing the cart and its contents
- Calculating the total cart amount 
- Proceeding to checkout
- Guest checkout 
- Order confirmation and email notification

### Testing Environment

- **Operating System**: Windows 11
- **Browser**: Google Chrome

### Types of Tests

1. **Functional Tests**: To verify that the functionalities work according to the requirements.
2.  **Performance Tests**: To verify that min 10,000 user can login and use app at the same time.
3.  **Security Testing**: To verify that no 3rd party can access user accounts. 
4.  **Accessibility Tests**: To verify that the application passes all requirements from EU Accessibility Act 2025.
5.  **UX Tests**:  To verify positive user response to the features.

### Test Schedule
* **Start Date**: Beginning of Sprint 7
* **End Date**: End of Sprint 7 or continuous testing until all test cases are executed and critical issues are resolved.

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
- The all features code is stable for testing.
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

<h1 id="Qase-Main">Example test cases in full details using Qase.</h2>



### 1. Verify successful login with valid data

![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC1.png "Test Case 1")

### 2. Verify failed login with invalid data

![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC2.png "Test Case 2")

### 3. Check login with empty fields

![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC3.png "Test Case 3")

### 4. Test password reset functionality

![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC4.png "Test Case 4")

### 5. Check two-factor authentication

![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC5.png "Test Case 5")
 
### 6. Check login using social media
![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC6.png "Test Case 6")

### 7. Test logout functionality
![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC7.png "Test Case 7")

### 8. Validate session timeout
![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/TC8.png "Test Case 8")

<h1 id="Test-report">Test summary report for skleptest functionalitys and bugs report.</h2>

## Test Summary Report
1. **Descripton**: Tests were conducted to ensure the quality and reliability of the web application functionalitys.
2. **Test Period**: Beginning of Sprint 7 - End of Sprint 7
3. **Test Coverage** : 95% test coverage, remaining 5% contained edge cases with low risk
4. **Test Execution Summary:** 
* Total Test Cases: 110
* Passed: 30
* Failed: 3
* Blocked: 0
* Not Executed: 6

5. **Key Findings**:
* The login functionality is generally reliable, with a high pass rate of test cases.
* 2 critical defects and 1 bloker were identified.
* All defects are now fixed and re-tested.
* The remaining 5% of uncovered test cases involve low-risk edge scenarios.
* 6 performance tests were not executed due to a lack of a performance tester.

6. **Recommendations**:
To address the remaining performance tests and ensure comprehensive testing coverage I recomend to hire a performance tester or upskill an existing tester.
The login functionality is ready for deployment, it is crucial to closely monitor its performance in the production environment, especially given the lack of extensive performance testing.

7. **List of reported bugs:**
   
#### 1. User can't login using correct two-factor authentication.
![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/2FA.png "2FA")


#### 2. User didn't receive mail with reset password.
![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/Reset.png "Reset")


#### 3. User remain login after 15 min without activity.
![Alt text](https://github.com/dudekluk/Portfolio/blob/main/img/Session.png "Session")

