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
### Explanation:

#### Processes:
- **1.0 User Authentication**: Validates login credentials for both students and medical officers. Generates authentication tokens for secure session management.
- **2.0 Submit Medical Certificate**: Allows students to upload and submit medical certificates with required information. Validates file format and stores submission details in the Medical_Submissions data store.
- **3.0 Review Submission**: Enables medical officers to review submitted certificates, add comments, and update approval status (Approved, Rejected, or On Hold). Updates are logged in Medical_Submissions.
- **4.0 Generate Statistics**: Compiles submission data into comprehensive reports showing submission rates, approval ratios, processing times, and status distributions for administrative analysis.

#### Data Stores:
- **D1: Users**: Stores user credentials, roles (Student/Medical Officer), and authentication profiles.
- **D2: Medical_Submissions**: Maintains all submitted certificates, timestamps, review comments, approval status, and audit trails.

#### External Entities:
- **Students**: Users who submit medical certificates for approval.
- **Medical Officers**: Users who review and approve/reject submissions.

#### Data Flows:
- Authentication tokens enable secure access to system functions.
- Submission records flow to the data store for persistent storage and retrieval.
- Updated statuses reflect review decisions and communicate outcomes to users.
- Statistics reports provide administrative insights derived from submission data.

## Authentication Flow
```
┌─────────┐     Login      ┌──────────┐     Validate     ┌────────┐
│  Login  │ ─────────────> │   App    │ ──────────────> │ Success│
│  Page   │                │  Logic   │                  │        │
└─────────┘                └──────────┘                  └────────┘
                                 │                             │
                                 │ Invalid                     │
                                 ▼                             ▼
                           ┌──────────┐                 ┌──────────┐
                           │  Error   │                 │ Redirect │
                           │ Message  │                 │Dashboard │
                           └──────────┘                 └──────────┘
```
# Explanation:
1. **Login Page**: The user (student or medical officer) accesses the login page and submits their credentials (username and password).
2. **App Logic**: The application receives the login request and validates the credentials against the user database. If the credentials are correct, the user is authenticated successfully.
3. **Success**: Upon successful authentication, the user is redirected to their respective dashboard (student or medical officer).
4. **Error Message**: If the credentials are invalid, an error message is displayed on the login page, prompting the user to try again.

### Student Submission Flow
```
┌─────────┐   Click Submit  ┌──────────┐   Fill Form   ┌────────┐
│ Student │ ──────────────> │  Submit  │ ────────────> │ Submit │
│Dashboard│                 │  Modal   │               │ Button │
└─────────┘                 └──────────┘               └────────┘
                                 ▲                           │
                                 │ Cancel                    │
                                 │                           ▼
                                 └────────────────────  ┌────────┐
                                                         │  Save  │
                                                         │  Data  │
                                                         └────────┘
                                                              │
                                                              ▼
                                                        ┌──────────┐
                                                        │  Close   │
                                                        │  Modal   │
                                                        └──────────┘
                                                              │
                                                              ▼
                                                        ┌──────────┐
                                                        │ Refresh  │
                                                        │   List   │
                                                        └──────────┘
```
# Explanation:
1. **Student Dashboard**: The student accesses their dashboard where they can view their submission history and click the "Submit Medical Certificate" button.
2. **Submit Modal**: A modal form appears where the student fills in the required information (medical date, reason, type, description) and uploads the medical certificate file.
3. **Submit Button**: The student clicks the "Submit" button to save the data. The system validates the input and saves the submission to the database.
4. **Cancel**: If the student decides not to submit, they can click "Cancel" to close the modal without saving.
5. **Refresh List**: After a successful submission, the system refreshes the submission list on the dashboard to show the new entry with its status (initially "Pending").      

### Officer Review Flow
```
┌─────────┐   Click Review  ┌──────────┐   Make Decision ┌────────┐
│ Officer │ ──────────────> │  Review  │ ──────────────> │ Submit │
│Dashboard│                 │  Modal   │                 │ Review │
└─────────┘                 └──────────┘                 └────────┘
     ▲                           │                             │
     │                           │ Cancel                      │
     │                           ▼                             ▼
     │                      ┌─────────┐                   ┌────────┐
     │                      │  Close  │                   │ Update │
     │                      │  Modal  │                   │ Status │
     │                      └─────────┘                   └────────┘
     │                                                          │
     │                                                          │
     └──────────────────────────────────────────────────────────┘
                            Refresh List
```
# Explanation:
1. **Officer Dashboard**: The medical officer accesses their dashboard where they can see a list of all pending submissions. They click the "Review" button next to a specific submission to open the review modal.
2. **Review Modal**: The modal displays the details of the submission, including the student's information, medical date, reason, type, description, and the uploaded certificate. The officer can make a decision to approve, reject, or hold the submission and add review notes if necessary.
3. **Submit Review**: The officer clicks the "Submit Review" button to save their decision. The system updates the submission status in the database accordingly.
4. **Cancel**: If the officer decides not to review at that moment, they can click "Cancel" to close the modal without making any changes.
5. **Refresh List**: After submitting the review, the system refreshes the list of submissions on the dashboard to reflect the updated status of the reviewed submission.







