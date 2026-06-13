This formative assessment is designed based on the provided sources to evaluate your understanding of data engineering fundamentals, the lifecycle, and stakeholder management.

### Part 1: Fill-in-the-Gaps

1.  Data engineering is defined as the intersection of Security, Data Management, DataOps, Data Architecture, **Orchestration**, and Software Engineering.
2.  The stage of the data engineering lifecycle responsible for getting data from source systems is called **Ingestion**.
3.  **Storage** is unique because it is an integral part of and spans across all other stages of the data engineering lifecycle.
4.  Unlike lifecycle stages, **undercurrents** are critical ideas that span and are relevant to every stage of the lifecycle.
5.  **Non-functional** requirements describe the "how" of a system, such as its performance, security, and reliability constraints.
6.  According to the Shared Responsibility Model, a cloud provider like AWS is responsible for security **of** the cloud, while the customer is responsible for security **in** the cloud.
7.  In the early days of software engineering, data was often treated as a **byproduct** or "exhaust" rather than a primary asset.
8.  A **Type A** data engineer focuses on abstraction and prefers using off-the-shelf, managed services to avoid "undifferentiated heavy lifting".
9.  A data engineer acts as a **hub** (or nexus) between data producers, such as software engineers, and data consumers, such as data scientists.
10. The modern era of data engineering was largely triggered by Google’s publications in the early 2000s on the **Google File System** and MapReduce.

***

### Part 2: Short Questions

1.  **What are the five stages of the data engineering lifecycle?**
    The stages are Generation, Ingestion, Storage, Transformation, and Serving.
2.  **What is the difference between a functional and a non-functional requirement?**
    Functional requirements define **what** the system must do (e.g., alerting a user to an anomaly), while non-functional requirements define **how** it should perform (e.g., scalability and security constraints).
3.  **Name three "undercurrents" that span the data engineering lifecycle.**
    Any three of the following: Security, Data Management, DataOps, Data Architecture, Orchestration, or Software Engineering.
4.  **How does a Type B data engineer differ from a Type A data engineer?**
    While Type A focuses on abstraction and off-the-shelf tools, a Type B data engineer focuses on **building** custom tools and systems that scale to serve a company's specific competitive advantage.
5.  **What does it mean for a data engineer to "stand on the shoulders of giants"?**
    It means using proven, scalable tools and technologies developed by others to build powerful data systems rather than trying to build everything from scratch.

***

### Part 3: Analytical Questions

1.  **Analyze how the shift from on-premises systems to the cloud has changed the relationship between data architecture and data engineering.**
    In traditional on-premises environments, architecture decisions involved long lead times, hardware installation, and rigid contracts. In the cloud, architecture is much more **fluid**. Decisions are often made during the implementation process itself. This shift has blurred the boundaries, often requiring data engineers to assume responsibilities traditionally held by data architects, such as designing blueprints for data management during a cloud migration.
2.  **Explain why the data engineering lifecycle is considered "cyclical" rather than linear.**
    Although presented in stages, the process is cyclical because **business goals evolve and stakeholder needs change**. As new tools emerge or performance evaluations reveal flaws, the data engineer must iterate on the system. This requires continuous communication with stakeholders to re-evaluate requirements and evolve the system accordingly.

***

### Part 4: Design Questions

1.  **A data scientist informs you that the marketing team needs real-time sales analysis, but they currently only receive a daily batch data dump. Outline your first three steps for designing a solution based on the "Thinking Like a Data Engineer" framework.**
    *   **Step 1:** Identify business goals and stakeholder needs by asking exactly what actions the marketing team will take with the real-time data.
    *   **Step 2:** Define system requirements, specifically the **functional** requirement of real-time ingestion and the **non-functional** requirements like latency and cost.
    *   **Step 3:** Choose tools and technologies by performing a **cost-benefit analysis** between comparable streaming technologies (e.g., comparing managed services like Amazon Kinesis vs. custom-built solutions).
2.  **You are designing a data system for a highly regulated industry (e.g., healthcare). How would this impact your approach to "Requirements Gathering" and "Security" undercurrents?**
    During requirements gathering, you must identify **regulatory concerns** as a primary non-functional requirement. In terms of security, you would apply the **Shared Responsibility Model**, ensuring that while the cloud provider secures the infrastructure, you design robust systems for data encryption, identity management, and access control ("security IN the cloud") to meet compliance standards.