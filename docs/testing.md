# Quality Assurance & System Testing

FikaMarket uses a structured test case register containing **250+ documented test cases**. This ensures every part of the system works exactly as planned before deployment.

### Test Case Classification

Every test case tracks essential details: Test ID, Linked Requirement, User Story, Severity, Preconditions, Test Data, and Expected Results. 

We test the system using three simple methods:

*   **Automated:** Computer-run scripts that check code and APIs automatically.
*   **Manual:** Human testers checking visual screens and real-world problems.
*   **Hybrid:** A human sets up the test, and an automated script verifies the result.

---

###  Test Coverage Matrix

Our test suite splits coverage across the three core parts of the FikaMarket ecosystem:

The test case register provides traceability between system requirements and the corresponding tests, helping the team verify that implemented functionality meets the defined acceptance criteria.

[Click here to view the FikaMarket Test Cases](https://docs.google.com/spreadsheets/d/1Z7QTRuLElVkaJlTu9hEQ14aoNn1bm8R_li0ZLvcrXw0/edit?gid=0#gid=0){ .md-button target="_blank" rel="noopener" }

### 1. Mobile Application (Flutter)
Testers check the buyer-facing app on real smartphones and emulators to ensure a smooth user experience.
*   **Authentication:** Testing login, signup, and forgot password flows.
*   **Marketplace & Cart:** Verifying adding crops to the cart, counting price subtotals, and checking out.
*   **Offline Caching:** Making sure the app handles weak or disconnected internet gracefully.

### 2. Management Dashboard (Web Portal)
Testers verify the web-based admin panel used for monitoring market listings and platform activities.
*   **Data Accuracy:** Ensuring sales charts, farmer registers, and buyer order histories update correctly.
*   **Access Control:** Checking that admins, staff, and partners only see the data they are allowed to see.
*   **Responsiveness:** Verifying that the layout looks clean on both laptop screens and tablets.

### 3. Backend Processing & Integrations (FastAPI & USSD)
Automated scripts test core business logic, database queries, and third-party systems.
*   **API Security:** Guarding database tables from direct internet exposure using secure tokens.
*   **USSD Flow:** Testing step-by-step menu interactions for farmers using basic feature phones.
*   **Webhooks:** Verifying that SMS gateways (Africa's Talking) and order notification pipelines trigger properly.

---

##  API Testing with Postman

We leverage **Postman** to validate backend business logic, response payloads, status codes, and data verification rules.

### Execution Workflow

```text
Open Postman ──> Select FikaMarket Collection ──> Set Environment ──> Send Request ──> Run Scripts ──> Pass/Fail
```

### Postman Test Scripts

Automated test scripts verify API responses instantly. For example, to validate a successful endpoint response:

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

### Running Test Batches

!!! success "Collection Runner"
    For bulk testing or regression runs, we use the **Postman Collection Runner** to execute entire test folders sequentially, inject data variables, and view real-time pass/fail reports.
