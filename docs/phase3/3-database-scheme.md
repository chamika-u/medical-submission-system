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