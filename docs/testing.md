# System Testing

FikaMarket uses a structured test case register containing **250+ documented test cases** to ensure full traceability between system requirements and implementation.

 info "Test Case Classification"
    Every test case tracks essential metadata: Test ID, Linked Requirement, User Story, Severity, Preconditions, Test Data, and Expected Results. Tests are executed using three methodologies:
    
    **Automated:** Executed via automated test runners and API scripts.
    **Manual:** Human-verified edge cases and network interruptions.
    **Hybrid:** Combined manual setup with automated verification.

---

## Test Coverage Overview

Our test suite guarantees complete coverage across all core system channels and components:

* **User Channels:** Farmer USSD Flow & Buyer/Lead Farmer PWA interfaces.
* **Core Marketplace:** Produce listing, real-time market price feeds, and order placement.
* **Backend Processing:** Payment processing, secure escrow splitting, and webhook handlers.
* **External Integration:** Gateway SMS notifications and third-party API connectivity.

---

## API Testing with Postman

We leverage **Postman** to validate backend business logic, response payloads, status codes, and input validation schemas.

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
    For bulk testing or regression runs, use the **Postman Collection Runner** to execute entire test folders sequentially, inject test iterations, and view real-time assertion graphs.
