# Design Documents
## Context Diagram
```
                     +---------------------------+
                     |                           |
    Students ------->|   Medical Submission      |-----> Submission Records
                     |   Management System       |
Medical Officer ---->|   (Sabaragamuwa Univ)    |-----> Statistics Reports
                     |                           |
                     +---------------------------+
```

## Level-0 Data Flow Diagram (DFD)
```
                 +---------------------+
                 |                     |
Student Login -->| 1.0                 |
                 | User Authentication |---> Auth Token
Officer Login -->|                     |
                 +---------------------+
                         |
                         v
                  [D1: Users]
                         |
                         v
                 +---------------------+
                 |                     |
Medical Info --->| 2.0                 |---> Submission Record
                 | Submit Medical      |
                 | Certificate         |
                 +---------------------+
                         |
                         v
                [D2: Medical_Submissions]
                         |
                         v
                 +---------------------+
                 |                     |
Review Request ->| 3.0                 |---> Updated Status
                 | Review Submission   |
                 | (Approve/Reject)    |
                 +---------------------+
                         |
                         v
                [D2: Medical_Submissions]
                         |
                         v
                 +---------------------+
                 |                     |
Stats Request -->| 4.0                 |---> Statistics Report
                 | Generate Statistics |
                 |                     |
                 +---------------------+


### Explanation:
- The context diagram illustrates the high-level interactions between the main actors (Students and Medical Officers) and the Medical Submission Management System. Students can submit medical certificates, while medical officers can review submissions and generate statistics.
- The Level-0 DFD breaks down the system into its main processes: User Authentication, Submitting Medical Certificates, Reviewing Submissions, and Generating Statistics. It also shows the data stores (Users and Medical_Submissions) that hold user information and submission records. Each process interacts with the relevant data stores to perform its function.




