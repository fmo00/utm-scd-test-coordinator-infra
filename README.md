# BR-UTM Lab mock servers

This repository provides mocked dependencies for the execution of BR-UTM Lab.

### Why

To create an effective sandbox environment for testing USSP integration, the environment must contain a controlled setup in which you conduct software testing. This way, it prevents instability caused by updates, patches or changes and maintain consistency making it is easier to simulate real-life situations that USSP will encounter when deployed.

#### Available resources

-   **Authentication server**:

    -   GET /token

-   **DSS server**

    -   POST /dss/v1/constraint_references/query
    -   GET /dss/v1/constraint_references/{entityid}
    -   PUT /dss/v1/constraint_references/{entityid}
    -   PUT /dss/v1/constraint_references/{entityid}/{ovn}
    -   DELETE /dss/v1/constraint_references/{entityid}/{ovn}

-   **USS server**:
    -   GET /uss/v1/operational_intents/{entityid}
    -   GET /uss/v1/constraints/{entityid}
    -   POST /uss/v1/operational_intents
    -   POST /uss/v1/constraints

### Getting started

```
docker compose up --build
```
