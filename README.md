<h1 style="text-align:center; color: #4CAF50;">Smart Attendance Management System</h1>

<p style="text-align:center; font-style:italic;">A Flask-based backend for managing employees, shifts, and attendance logs, complete with JWT authentication, Celery tasks, and Swagger API documentation.</p>

<hr style="border:1px solid #ddd;">

<h2 style="color:#2196F3;">🌟 Features</h2>
<ul>
  <li>Manage <strong>Employees</strong> – Add, Edit, Delete, View with filters and pagination.</li>
  <li>Manage <strong>Shifts</strong> – Create, Edit, Delete, and Display shifts.</li>
  <li>Assign <strong>Shifts</strong> to employees on specific dates.</li>
  <li>Track <strong>Attendance Logs</strong> – Entry and Exit records with timestamp validation.</li>
  <li>User management with <strong>JWT authentication</strong> – Register, Login, Secure endpoints.</li>
  <li><strong>Swagger Documentation</strong> for all APIs using Flask-RESTX.</li>
  <li>Background tasks with <strong>Celery + Redis</strong> for sending emails asynchronously.</li>
  <li>Database handled by <strong>SQLAlchemy</strong> with relationships between employees, shifts, and logs.</li>
</ul>

<h2 style="color:#2196F3;">🚀 Technologies Used</h2>
<ul>
  <li>Python 3.10+</li>
  <li>Flask, Flask-RESTX (Swagger), Flask-JWT-Extended, Flask-Bcrypt</li>
  <li>SQLAlchemy (ORM)</li>
  <li>Celery + Redis for async tasks</li>
  <li>Flask-Mail / smtplib for email notifications</li>
  <li>Marshmallow for input validation</li>
</ul>

<h2 style="color:#2196F3;">💻 Project Structure</h2>
<ul>
  <li><code>api/models/</code> – Database models</li>
  <li><code>api/routes/</code> – API endpoints per namespace (Employees, Shifts, Attendance, Users)</li>
  <li><code>api/fields/</code> – Request schemas for validation</li>
  <li><code>celery_config.py</code> – Celery initialization</li>
  <li><code>config.cfg</code> – Configuration for database, JWT, email, and Celery</li>
</ul>

<h2 style="color:#2196F3;">⚙️ Setup Instructions</h2>
<ol>
  <li>Clone the repository: <code>git clone https://github.com/yourusername/Smart-Attendance-System-Backend.git</code></li>
  <li>Create a virtual environment:
    <pre><code>python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows
</code></pre>
  </li>
  <li>Install dependencies: <code>pip install -r requirements.txt</code></li>
  <li>Update <code>config.cfg</code> with your database URI, JWT secret key, email credentials, and Redis config.</li>
  <li>Run the Flask app: <code>python run.py</code></li>
  <li>Access Swagger docs at: <a href="http://localhost:5000/">http://localhost:5000/</a></li>
  <li>Start Celery worker: <code>celery -A api.celery worker --loglevel=info</code></li>
</ol>

<h2 style="color:#2196F3;">📌 Usage</h2>
<ul>
  <li>Register a user and login to get the JWT token.</li>
  <li>Use the JWT token to authenticate API requests.</li>
  <li>Add employees, shifts, assign shifts, and log attendance.</li>
  <li>Check attendance and employee data via paginated endpoints.</li>
  <li>Send notification emails via Celery tasks asynchronously.</li>
</ul>

<h2 style="color:#2196F3;">🎨 Design Philosophy</h2>
<p>This project focuses on:</p>
<ul>
  <li>Clean, modular code using Flask Blueprints and RESTX namespaces.</li>
  <li>Secure APIs with JWT and password hashing.</li>
  <li>Async task handling for scalability.</li>
  <li>Ease of testing via Swagger documentation.</li>
</ul>

<h2 style="color:#2196F3;">📝 Notes</h2>
<ul>
  <li>Ensure Redis server is running for Celery tasks.</li>
  <li>Email sending requires valid SMTP credentials.</li>
  <li>Database must exist and URI must be correctly set in <code>config.cfg</code>.</li>
</ul>

<hr style="border:1px solid #ddd;">
