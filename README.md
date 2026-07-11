# 🎲 EJS Roll Dice Project

## 📌 Project Overview

This is a simple backend project developed using **Node.js**, **Express.js**, and **EJS**. The project demonstrates how to use the EJS template engine to render dynamic HTML pages. A random dice number is generated on the server and displayed on the webpage.

---

# 🛠️ Technologies Used

* Node.js
* Express.js
* EJS
* HTML

---

# 📂 Development Process

### Step 1: Create the Project Folder

Create a new project folder.

```
EJS_Project
```

---

### Step 2: Initialize Node.js

Initialize the project using:

```bash
npm init -y
```

This command creates the **package.json** file, which stores the project's information and dependencies.

---

### Step 3: Install Express

Install Express.js using:

```bash
npm install express
```

Express is used to create the web server and handle routing.

---

### Step 4: Install EJS

Install the EJS template engine:

```bash
npm install ejs
```

EJS allows us to render dynamic HTML pages from the server.

---

### Step 5: Create the Main Server File

Create an **index.js** file.

In this file:

* Import Express and Path modules.
* Create the Express application.
* Set the server port.
* Configure EJS as the view engine.
* Configure the Views directory.
* Create application routes.
* Render EJS templates.
* Start the Express server.

The application contains:

* `/` → Renders the Home page.
* `/rolldice` → Generates a random dice value (1–6) and passes it to the EJS template.

---

### Step 6: Create the Views Folder

Create a folder named:

```
views
```

Inside the folder, create two EJS files:

* `home.ejs`
* `rolldice.ejs`

These files are responsible for displaying the user interface.

---

### Step 7: Configure the View Engine

Configure Express to use EJS as the template engine:

```javascript
app.set("view engine", "ejs");
```

This allows Express to render `.ejs` files without specifying the file extension every time.

---

### Step 8: Configure the Views Directory

Specify the location of the Views folder:

```javascript
app.set("views", path.join(__dirname, "views"));
```

This tells Express where all EJS templates are stored.

---

### Step 9: Dynamic Data Rendering

The `/rolldice` route generates a random number using JavaScript.

That value is passed to the EJS template using:

```javascript
res.render("rolldice.ejs", { num: diceval });
```

The template receives the value and displays the generated dice number on the webpage.

---

# 📁 Project Structure

```
EJS_Project
│
├── node_modules
├── views
│   ├── home.ejs
│   └── rolldice.ejs
├── index.js
├── package.json
├── package-lock.json
└── README.md
```

---

# ▶️ How to Run the Project

Install dependencies:

```bash
npm install
```

Start the server:

```bash
node index.js
```

Open your browser and visit:

```
http://localhost:8080/
```

To generate a random dice value:

```
http://localhost:8080/rolldice
```

---

# 🎯 Learning Outcomes

Through this project, I learned:

* Setting up a Node.js project
* Installing and managing npm packages
* Creating an Express server
* Configuring the EJS template engine
* Rendering dynamic web pages
* Passing data from the backend to the frontend
* Organizing project files using the Views folder
* Creating routes in Express.js

---

# 👩‍💻 Author

**Dipanjali Gupta**
