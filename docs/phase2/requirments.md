## Requirements Document

## Functional Requirements

### FR1: User Authentication
- FR1.1: System shall allow students to login with username and password
- FR1.2: System shall allow medical officers to login with username and password
- FR1.3: System shall use JWT tokens for session management
- FR1.4: System shall provide role-based access control Requirements Document

### FR2: Medical Certificate Submission (Student)
- FR2.1: Students shall be able to submit medical certificates with date, type, and reason
- FR2.2: System shall support three types: Examination, Assessment, and Other
- FR2.3: Students shall be able to add additional description to submissions
- FR2.4: System shall record submission date and time automatically
- FR2.5: Students shall be able to view their submission history

### FR3: Submission Management (Medical Officer)
- FR3.1: Medical officers shall view all medical submissions
- FR3.2: System shall allow filtering by status (pending, approved, rejected, hold)
- FR3.3: System shall allow filtering by medical type
- FR3.4: Medical officers shall be able to approve submissions
- FR3.5: Medical officers shall be able to reject submissions
- FR3.6: Medical officers shall be able to put submissions on hold
- FR3.7: Medical officers shall be able to add review notes to decisions

### FR4: Statistics and Reporting
- FR4.1: System shall display total number of submissions
- FR4.2: System shall show count by status (pending, approved, rejected, hold)
- FR4.3: System shall show breakdown by medical type
- FR4.4: Statistics shall update in real-time