# Execution Flowchart

This flowchart shows how user data flows through the AI Financial Copilot system at runtime.

```mermaid
flowchart TD

    START([Start])

    LOGIN[User Login or Signup]

    INPUT[Add or Upload Transactions]

    VALIDATE{Is Data Valid?}

    STORE[Store Transactions in Database]

    ANALYZE[Analyze Monthly Spending]

    DECIDE[Decision Engine\nRules and ML Models]

    INSIGHT{Insight Detected?}

    EXPLAIN[Generate Explanation\nUsing LLM]

    DISPLAY[Display Dashboard and Insights]

    END([End])

    START --> LOGIN
    LOGIN --> INPUT
    INPUT --> VALIDATE

    VALIDATE -- No --> INPUT
    VALIDATE -- Yes --> STORE

    STORE --> ANALYZE
    ANALYZE --> DECIDE
    DECIDE --> INSIGHT

    INSIGHT -- Yes --> EXPLAIN
    INSIGHT -- No --> DISPLAY

    EXPLAIN --> DISPLAY
    DISPLAY --> END
