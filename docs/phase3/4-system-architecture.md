# System Architecture and API Design
## System Architecture

### Technology Stack
- **Backend:** Node.js with Express.js framework
- **Database:** SQLite3 (lightweight, embedded database)
- **Authentication:** JWT (JSON Web Tokens)
- **Password Security:** bcryptjs for hashing
- **Frontend:** HTML5, CSS3, Vanilla JavaScript
- **API:** RESTful API architecture

### Application Layers
1. **Presentation Layer:** HTML pages with CSS styling and JavaScript
2. **API Layer:** Express.js routes and middleware
3. **Business Logic Layer:** Controllers and service functions
4. **Data Access Layer:** SQLite database queries
5. **Security Layer:** JWT authentication and bcrypt hashing

## API Endpoints Design

### Authentication
- `POST /api/login` - Authenticate user and return JWT token

### Medical Submissions
- `POST /api/submissions` - Create new submission (Student)
- `GET /api/submissions/my` - Get current user's submissions (Student)
- `GET /api/submissions` - Get all submissions with filters (Medical Officer)
- `GET /api/submissions/:id` - Get specific submission details
- `PUT /api/submissions/:id` - Update submission status (Medical Officer)

### Statistics
- `GET /api/stats` - Get submission statistics (Medical Officer)

## Security Design

### Authentication Flow
1. User submits credentials
2. System verifies against database
3. System generates JWT token (24-hour expiration)
4. Token included in subsequent requests
5. Middleware validates token before processing

### Authorization
- Role-based access control
- Students can only access their own submissions
- Medical officers can access all submissions
- Status updates restricted to medical officers

### Data Security
- All passwords hashed with bcrypt (10 salt rounds)
- SQL injection prevention through parameterized queries
- CORS enabled for cross-origin requests
- JWT secret key for token signing