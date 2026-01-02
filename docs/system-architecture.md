# System Architecture

The AI Financial Copilot follows a layered architecture separating presentation, application logic, intelligence, and data layers.

```mermaid
flowchart TB

    subgraph Presentation_Layer
        UI[Web Dashboard]
    end

    subgraph Application_Layer
        API[API Gateway]
        SVC[Application Services]
    end

    subgraph Intelligence_Layer
        DEC[Decision Engine]
        RULES[Rules Engine]
        ML[ML Models]
        METRICS[Metrics Engine]
    end

    subgraph AI_Explanation_Layer
        LLM[LLM Explainer]
    end

    subgraph Data_Layer
        DB[(PostgreSQL Database)]
        CACHE[(Redis Cache)]
    end

    UI --> API
    API --> SVC

    SVC --> DB
    SVC --> CACHE

    SVC --> DEC
    DEC --> RULES
    DEC --> ML
    DEC --> METRICS

    DEC --> LLM
    LLM --> SVC

    SVC --> API
    API --> UI
