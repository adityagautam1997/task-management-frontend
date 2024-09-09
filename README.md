
<h2 align="center">Task Management App</h2>

<h3>Backend Setup (NestJS)</h3>

<h4>Prerequisites</h4>
<ul>
  <li>Node.js: Ensure you have Node.js installed. You can download it from <a href="https://nodejs.org/" target="_blank">here</a>.</li>
  <li>MS SQL Server: A running instance of MS SQL Server.</li>
  <li>Git: To clone the project from the repository using Git.</li>
</ul>

<h4>Getting Started</h4>
<ol>
  <li><strong>Clone the Repository</strong>
    <pre><code>git clone &lt;backend-repo-url&gt;
cd task-management-backend</code></pre>
  </li>
  <li><strong>Install Dependencies</strong>
    <pre><code>npm install</code></pre>
  </li>
  <li><strong>Database Setup</strong>
    <ul>
      <li>Ensure your MS SQL Server is running.</li>
      <li>Create a database for the app.</li>
    </ul>
    <pre><code>CREATE DATABASE TaskManagmentDB;
    CREATE TABLE Tasks (
  id INT PRIMARY KEY IDENTITY(1,1),
  description NVARCHAR(255) NOT NULL,
  created_at DATETIME DEFAULT GETDATE()
);</code></pre>
  </li>
  <li><strong>Configure the Environment</strong>
    <p>Create a <code>.env</code> file in the root of the <code>task-management-backend</code> folder with the following content:</p>
    <pre><code>DB_HOST=localhost
DB_PORT=1433
DB_USERNAME=your_username
DB_PASSWORD=your_password
DB_DATABASE=TaskManagmentDB</code></pre>
  </li>
  <li><strong>Run the Application</strong>
    <pre><code>npm run start:dev</code></pre>
  </li>
</ol>

<h3>Frontend Setup (React)</h3>

<h4>Getting Started</h4>
<ol>
  <li><strong>Clone the Repository</strong>
    <pre><code>git clone &lt;frontend-repo-url&gt;
cd task-management-frontend</code></pre>
  </li>
  <li><strong>Install Dependencies</strong>
    <pre><code>npm install</code></pre>
  </li>
  <li><strong>Run the Application</strong>
    <pre><code>npm start</code></pre>
    <p>This will run the app at <code>http://localhost:3001</code>.</p>
  </li>
</ol>

<h4>Running Both Applications</h4>
<ol>
  <li>Start Backend: <code>npm run start:dev</code> in the <code>task-management-backend</code> folder.</li>
  <li>Start Frontend: <code>npm start</code> in the <code>task-management-frontend</code> folder.</li>
  <li>Access the frontend at <code>http://localhost:3001</code>, and the frontend will interact with the backend to manage tasks.</li>
</ol>

<h3>API Endpoints</h3>
<ul>
  <li><strong>GET</strong> <code>/tasks</code>: Fetch all tasks.</li>
  <li><strong>POST</strong> <code>/tasks</code>: Add a new task. (Send JSON with <code>description</code>).</li>
  <li><strong>DELETE</strong> <code>/tasks/:id</code>: Remove a task by ID.</li>
</ul>
