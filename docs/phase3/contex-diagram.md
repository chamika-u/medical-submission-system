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
### Explanation:
- **Students**: The primary users of the system who will submit their medical certificates for approval.
- **Medical Officers**: The users responsible for reviewing and approving/rejecting submitted medical certificates.
- **Medical Submission Management System**: The central system that facilitates submission, review, and management of medical certificates.
- **Submission Records**: The database where all submitted medical certificates and their statuses are stored.
- **Statistics Reports**: The output that provides insights into submissions, statuses, and relevant statistics for administrative purposes. 



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
```







