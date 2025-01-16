# Basic Flowchart
```mermaid
graph TD
    A[Start] --> B[Process]
    B --> C[End]
```

# Adding Multiple Nodes and Connections
```mermaid
graph LR
    A[Start] --> B{Decision}
    B -->|Yes| C[Do Something]
    B -->|No| D[Do Nothing]
    C --> E[End]
    D --> E
```

# Different Node Shapes
```mermaid
graph TD
    A[Square Box] --> B(Rounded Box)
    B --> C{Diamond}
    C --> D((Circle))
    C --> E[\Slanted\]
    C --> F[/Other Slanted/]
```

# Subgraphs (Grouping)
```mermaid
graph TD
    subgraph Group1
        A[A] --> B[B]
    end
    subgraph Group2
        C[C] --> D[D]
    end
    B --> C
```

# Sequence Diagram Example
```mermaid
sequenceDiagram
    participant Client
    participant Server
    Client->>Server: Request Data
    Server-->>Client: Send Response
    Client->>Server: Another Request
    Server-->>Client: Another Response
```

# Class Diagram Example
```mermaid
classDiagram
    Animal <|-- Duck
    Animal <|-- Fish
    Animal : +int age
    Animal : +String gender
    Animal: +mate()
    class Duck{
      +String beakColor
      +swim()
      +quack()
    }
```

# Gantt Chart Example
```mermaid
gantt
    title Project Schedule
    dateFormat  YYYY-MM-DD
    section Planning
    Design           :2024-01-01, 5d
    section Development
    Coding          :2024-01-06, 10d
    Testing         :2024-01-16, 5d
```

```mermaid
graph TD
    A[Clone Repository] --> B[Install Dependencies]
    B --> C[Run Tests]
    C --> D[Start Development]
    D --> E[Make Changes]
    E --> F[Commit]
    F --> G[Push]

### Bug Report Flow
```
```mermaid
graph LR
    A[Bug Found] --> B{Reproducible?}
    B -->|Yes| C[Create Issue]
    B -->|No| D[Gather More Info]
    C --> E[Add Labels]
    E --> F[Assign Developer]
