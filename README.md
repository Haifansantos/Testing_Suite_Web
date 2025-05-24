# Test Plan: DemoQA Web Application Testing

## 1. Test Plan Overview

**Project Name:** DemoQA Automation Testing Suite  
**Application Under Test:** https://demoqa.com/  
**Test Type:** Functional & UI Automation Testing  
**Testing Framework:** Selenium WebDriver + Python + Pytest  
**Test Environment:** Chrome Browser   
**Test Duration:** 1 weeks  
**Tester:** Haifan Santos

## 2. Test Objectives

- Validate core functionalities of DemoQA web application
- Ensure UI elements work as expected across different scenarios
- Verify form validations and user interactions
- Test responsive behavior and error handling
- Create reusable automation framework for future testing

## 3. Test Scope

### In Scope:
- Elements section testing (Text Box, Check Box, Radio Button, Web Tables, Buttons, Links)
- Forms section testing (Practice Form)
- Alerts, Frame & Windows testing
- Interactions testing (Drag & Drop, Sortable)
- Basic responsive testing

### Out of Scope:
- Performance testing
- Security testing
- Cross-browser compatibility (focus on Chrome only)
- Mobile testing

## 4. Test Strategy

**Automation Approach:**
- Page Object Model (POM) design pattern
- Data-driven testing where applicable
- Parameterized test cases
- Screenshot capture on failures
- HTML reports generation

**Test Execution:**
- Smoke testing first
- Functional testing
- Regression testing

## 5. Detailed Test Cases

### 5.1 Elements Section

#### TC001: Text Box Functionality
**Priority:** High  
**Objective:** Verify text box input and output functionality

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to Text Box page | Page loads successfully |
| 2 | Enter "John Doe" in Full Name field | Text is entered correctly |
| 3 | Enter "john@example.com" in Email field | Valid email format accepted |
| 4 | Enter "123 Main St" in Current Address | Text is entered correctly |
| 5 | Enter "456 Oak Ave" in Permanent Address | Text is entered correctly |
| 6 | Click Submit button | Output box displays all entered information |

**Test Data:**
- Valid Name: "John Doe", "Jane Smith", "Alex Johnson"
- Valid Email: "test@gmail.com", "user@yahoo.com"
- Invalid Email: "invalid-email", "test@", "@domain.com"

#### TC002: Check Box Functionality
**Priority:** High  
**Objective:** Verify checkbox selection and tree structure

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to Check Box page | Tree structure displayed |
| 2 | Click on Home checkbox | All child checkboxes selected |
| 3 | Expand Desktop folder | Desktop items visible |
| 4 | Select only Notes checkbox | Only Notes selected, partial selection for parent |
| 5 | Verify result display | Selected items shown in result section |

#### TC003: Radio Button Selection
**Priority:** Medium  
**Objective:** Verify radio button selection behavior

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to Radio Button page | Three radio options visible |
| 2 | Click "Yes" radio button | "Yes" selected, success message displayed |
| 3 | Click "Impressive" radio button | "Impressive" selected, previous selection cleared |
| 4 | Verify "No" button state | "No" button should be disabled |

#### TC004: Web Tables Operations
**Priority:** High  
**Objective:** Verify CRUD operations on web table

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to Web Tables page | Default table with 3 records displayed |
| 2 | Click "Add" button | Registration form modal opens |
| 3 | Fill form with valid data | All fields accept input |
| 4 | Click Submit | New record added to table |
| 5 | Edit existing record | Edit form opens with current data |
| 6 | Update information | Record updated successfully |
| 7 | Delete a record | Record removed from table |
| 8 | Search for specific record | Filter functionality works |

**Test Data for Web Tables:**
```json
{
  "valid_user": {
    "firstName": "Test",
    "lastName": "User",
    "email": "test@example.com",
    "age": "25",
    "salary": "50000",
    "department": "Engineering"
  }
}
```

#### TC005: Buttons Interaction
**Priority:** Medium  
**Objective:** Verify different button click events

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to Buttons page | Three buttons visible |
| 2 | Double-click "Double Click Me" | Success message for double-click |
| 3 | Right-click "Right Click Me" | Context menu or success message |
| 4 | Single-click dynamic button | Success message for single-click |

#### TC006: Links Navigation
**Priority:** Medium  
**Objective:** Verify internal and external link functionality

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to Links page | All links visible |
| 2 | Click "Home" link | Opens in same tab |
| 3 | Click external link | Opens in new tab |
| 4 | Test API call links | Check network response |

### 5.2 Forms Section

#### TC007: Practice Form Validation
**Priority:** High  
**Objective:** Verify form validation and submission

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to Practice Form | Form loads with all fields |
| 2 | Submit empty form | Required field validations shown |
| 3 | Fill all required fields | No validation errors |
| 4 | Upload a file | File selected successfully |
| 5 | Select state and city | Dropdown cascading works |
| 6 | Submit complete form | Success modal displayed |

**Test Data Sets:**
- **Valid Data:** Complete form with all fields
- **Invalid Data:** Missing required fields, invalid email, invalid phone
- **Boundary Data:** Max length testing for text fields

### 5.3 Alerts, Frame & Windows

#### TC008: Alert Handling
**Priority:** High  
**Objective:** Verify different types of alerts

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to Alerts page | Alert buttons visible |
| 2 | Click simple alert | Alert appears with OK button |
| 3 | Click timer alert | Alert appears after 5 seconds |
| 4 | Click confirm alert | Accept/Cancel options work |
| 5 | Click prompt alert | Text input in alert works |

#### TC009: Frame Handling
**Priority:** Medium  
**Objective:** Verify frame switching and interaction

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to Frames page | Frames are loaded |
| 2 | Switch to large frame | Can interact with frame content |
| 3 | Switch to small frame | Frame content accessible |
| 4 | Switch back to main content | Can access main page elements |

#### TC010: Window Handling
**Priority:** High  
**Objective:** Verify new window/tab operations

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to Browser Windows | Window buttons visible |
| 2 | Click "New Tab" | New tab opens |
| 3 | Switch to new tab | Can interact with new tab |
| 4 | Close new tab | Return to original tab |
| 5 | Click "New Window" | New window opens |

### 5.4 Interactions Section

#### TC011: Drag and Drop
**Priority:** Medium  
**Objective:** Verify drag and drop functionality

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to Dragabble page | Draggable elements visible |
| 2 | Drag element to new position | Element moves successfully |
| 3 | Navigate to Droppable page | Source and target areas visible |
| 4 | Drag from source to target | Drop zone accepts element |
| 5 | Verify state change | Target area shows "Dropped!" |

#### TC012: Sortable Lists
**Priority:** Low  
**Objective:** Verify list reordering functionality

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to Sortable page | List items visible |
| 2 | Drag item to different position | Item reorders successfully |
| 3 | Verify new order | List maintains new sequence |

## 6. Test Environment Requirements

**Browser:** Chrome (Latest Version)  
**Operating System:** Windows 10/11 or macOS  
**Screen Resolution:** 1920x1080  
**Internet Connection:** Stable broadband  

**Required Tools:**
- Python 3.8+
- Selenium WebDriver
- ChromeDriver (managed by webdriver-manager)
- Pytest framework
- pytest-html for reporting

## 7. Test Data Management

**Data Storage:** JSON files and Python dictionaries  
**Test Data Categories:**
- Valid input data
- Invalid input data  
- Boundary value data
- Special characters data

## 8. Defect Management

**Defect Severity Levels:**
- **Critical:** Application crash, major functionality broken
- **High:** Important feature not working as expected  
- **Medium:** Minor feature issues, UI problems
- **Low:** Cosmetic issues, typos

**Defect Reporting:** GitHub Issues with detailed steps, screenshots, and environment info

## 9. Entry and Exit Criteria

**Entry Criteria:**
- Test environment is set up and accessible
- All required tools are installed and configured
- Test data is prepared
- Application under test is stable

**Exit Criteria:**
- All high and critical priority test cases executed
- 90% test cases passed
- All critical and high severity defects resolved
- Test execution report generated
- Code coverage meets minimum threshold

## 10. Risk Assessment

**Technical Risks:**
- Website downtime during testing
- Browser compatibility issues
- Element locator changes

**Mitigation Strategies:**
- Implement robust wait strategies
- Use multiple locator strategies
- Regular framework maintenance

## 11. Deliverables

1. **Test Automation Framework**
2. **Test Execution Reports**
3. **Defect Reports**
4. **Test Data Files**
5. **Documentation (README, Setup Guide)**
6. **Video Demo of Test Execution**

## 12. Timeline

| Phase | Duration | Activities |
|-------|----------|------------|
| Week 1 | 5 days | Setup, Framework development, Core test cases |
| Week 2 | 5 days | Advanced scenarios, Reporting, Documentation |

## 13. Success Criteria

- All planned test cases automated and executable
- Clean, maintainable code following best practices
- Comprehensive test reports generated
- Zero critical defects in automation framework
- Professional documentation ready for portfolio

---

**Document Version:** 1.0  
**Last Updated:** [Current Date]  
**Approved By:** [Your Name]
