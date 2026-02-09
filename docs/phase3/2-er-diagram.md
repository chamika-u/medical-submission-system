# Entity-Relationship Diagram (ERD)
```
+------------------+           +-------------------------+
|     USERS        |           |  MEDICAL_SUBMISSIONS   |
|------------------|           |-------------------------|
| id (PK)          |1-------N  | id (PK)                 |
| username         |           | user_id (FK)            |
| password         |           | submission_date         |
| full_name        |           | medical_date            |
| email            |           | reason                  |
| role             |           | medical_type            |
| student_id       |           | description             |
| created_at       |           | status                  |
+------------------+           | reviewed_by (FK)        |
       |                       | reviewed_at             |
       | 1                     | review_notes            |
       |                       +-------------------------+
       |                                |
       +--------------------------------+
         (reviewed_by references Users.id)
```

## Explanation:
- **USERS**: This entity represents all users of the system, including both students and medical officers. It contains fields for user identification, authentication, and role management.
- **MEDICAL_SUBMISSIONS**: This entity represents the medical certificate submissions made by students. It includes details about the submission, such as the date of submission, medical date, reason for absence, type of medical issue, and the current status of the submission. It also has fields to track who reviewed the submission and any notes from the review process.
- The relationship between USERS and MEDICAL_SUBMISSIONS is a one-to-many relationship, where one user (student) can have multiple medical submissions, and each submission is associated with one user. Additionally, the reviewed_by field in MEDICAL_SUBMISSIONS references the id of a user (medical officer) who reviewed the submission.