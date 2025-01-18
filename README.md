
```mermaid
flowchart TD
    classDef challenge fill:#4B0082,stroke:#2d7de6,color:#ffffff
    classDef impact fill:#F0E6FF,stroke:#7A4E97,color:#000000
    classDef solution fill:#D0E4FF,stroke:#6A5ACD,color:#000000

    A[TURBULENCE AHEAD:<br>IndiGo's Financial Setbacks]

    %% Branch 1: Operational Challenges
    A --> B[Operational Challenges]
    B --> B1[ATF Cost Rise]
    B --> B2[Non-Reliable GTF Engines]
    
    B1 --> B1A[Geopolitical factors<br>Russia-Ukraine conflict]
    B1A --> B1B[ATF: 40-50% operational expenses<br>20% YoY surge in fuel prices<br>Fuel costs exceed ₹7,000 crore]
    
    B2 --> B2A[Grounding of Over 70 Aircraft]
    B2A --> B2B[15% fleet grounded<br>Reduced flight capacity<br>₹1,200 crore replacement cost]

    %% Branch 2: Financial Challenges
    A --> C[Financial Challenges]
    C --> C1[High Lease and Maintenance Cost]
    C --> C2[Higher Dollar Denominated Cost]
    
    C1 --> C1A[Increased fixed costs<br>20-22% hike in leasing rates]
    C1A --> C1B[80% leased aircraft<br>Higher ticket prices<br>Reduced service quality]
    
    C2 --> C2A[4% depreciation of INR vs USD]
    C2A --> C2B[$1.3B annual payments<br>₹500 crore forex loss]

    %% Branch 3: Growth Challenges
    A --> D[Growth Challenges]
    D --> D1[Less Revenue Growth]
    D1 --> D1A[Increased operational costs<br>outpace revenue growth]
    D1A --> D1B[2.8% growth in RASK<br>Stagnant passenger yields]

    %% Branch 4: Regulatory Challenges
    A --> E[Regulatory Challenges]
    E --> E1[Aviation Compliance Issues]
    E --> E2[Slot Allocation and Restrictions]
    
    E1 --> E1A[Stricter safety norms<br>Increased oversight]
    E1A --> E1B[Higher compliance costs<br>Operational disruptions]
    
    E2 --> E2A[Limited peak-time slots<br>Route restrictions]
    E2A --> E2B[Reduced revenue potential<br>Challenges in expansion]

    %% Solutions Layer
    B1B --> S1[Short-term Solutions]
    B2B --> S1
    S1 --> S1A[Fuel Hedging Program<br>Fleet Maintenance Optimization<br>Target: 15-20% cost reduction]

    C1B --> S2[Medium-term Solutions]
    C2B --> S2
    S2 --> S2A[Lease Restructuring<br>Currency Risk Management<br>Target: 10-15% cost saving]

    D1B --> S3[Long-term Solutions]
    S3 --> S3A[Revenue Enhancement Program<br>Network Optimization<br>Target: 10% yield growth]

    E2B --> S4[Policy Solutions]
    E1B --> S4
    S4 --> S4A[Lobbying for policy reforms<br>Improved compliance frameworks<br>Target: Enhance regulatory alignment]

    class A challenge
    class B,C,D,E challenge
    class B1,B2,C1,C2,D1,E1,E2 challenge
    class B1A,B2A,C1A,C2A,D1A,E1A,E2A impact
    class B1B,B2B,C1B,C2B,D1B,E1B,E2B impact
    class S1,S2,S3,S4 solution
    class S1A,S2A,S3A,S4A solution
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

```
### Bug Report Flow

```mermaid
graph LR
    A[Bug Found] --> B{Reproducible?}
    B -->|Yes| C[Create Issue]
    B -->|No| D[Gather More Info]
    C --> E[Add Labels]
    E --> F[Assign Developer]
