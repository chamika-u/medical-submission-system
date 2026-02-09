# Database Schema

##Users Table
```sql
CREATE TABLE users (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  username TEXT UNIQUE NOT NULL,
  password TEXT NOT NULL,
  full_name TEXT NOT NULL,
  email TEXT,
  role TEXT NOT NULL CHECK(role IN ('student', 'medical_officer')),
  student_id TEXT,
  created_at DATETIME DEFAULT CURRENT_TIMESTAMP
)
```

## Medical_Submissions Table
```sql
CREATE TABLE medical_submissions (
  id INTEGER PRIMARY KEY AUTOINCREMENT,
  user_id INTEGER NOT NULL,
  submission_date DATETIME DEFAULT CURRENT_TIMESTAMP,
  medical_date DATE NOT NULL,
  reason TEXT NOT NULL,
  medical_type TEXT NOT NULL CHECK(medical_type IN ('examination', 'assessment', 'other')),
  description TEXT,
  status TEXT NOT NULL DEFAULT 'pending' CHECK(status IN ('pending', 'approved', 'rejected', 'hold')),
  reviewed_by INTEGER,
  reviewed_at DATETIME,
  review_notes TEXT,
  FOREIGN KEY (user_id) REFERENCES users(id),
  FOREIGN KEY (reviewed_by) REFERENCES users(id)
)
```

## Explanation:
- The `users` table stores information about all users of the system, including their username, password, full name, email, role (student or medical officer), and an optional student ID for students. The `created_at` field automatically records when a user account is created.    

- The `medical_submissions` table captures all details related to medical certificate submissions. It includes a foreign key `user_id` that references the `users` table to link each submission to a specific user. The `submission_date` records when the submission was made, while `medical_date`, `reason`, `medical_type`, and `description` capture the details of the medical issue. The `status` field tracks the current state of the submission, and the `reviewed_by` and `reviewed_at` fields log who reviewed the submission and when, along with any review notes.

