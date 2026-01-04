# IBM.DAY4

# 📚 Library Management System (Node.js + MongoDB)

A simple **Library Management System REST API** built using **Node.js, Express, and MongoDB (Mongoose)**.
This project demonstrates CRUD operations on books with proper validations.



 🚀 Features

* Add multiple books at once
* View all books
* Filter books by category
* Get books published after a specific year
* Update available copies of a book
* Change book category
* Delete a book only when available copies are `0`
* MongoDB database integration using Mongoose



 🛠️ Tech Stack

* **Backend:** Node.js, Express.js
* **Database:** MongoDB
* **ODM:** Mongoose
* **Tools:** Postman / Thunder Client (for API testing)


## 📁 Project Structure
├── app.js            # Main server file
├── bookmodel.js      # Book schema & model
├── db.js             # MongoDB connection
├── package.json
├── package-lock.json

 ⚙️ Installation & Setup

 1️⃣ Clone the repository
git clone https://github.com/your-username/library-management-system.git
cd library-management-system


 2️⃣ Install dependencies
npm install


 3️⃣ Start MongoDB

Make sure MongoDB is running locally:
mongod


4️⃣ Run the server
node app.js


Server will start at:
http://localhost:3000


📌 API Endpoints

➕ Add Books (Insert 7 books)

**POST**

/addBooks


 📖 Get All Books
**GET**
/books

 📂 Get Books by Category

**GET**
/books/category/:category

Example:
/books/category/AI


 📅 Get Books Published After 2015

**GET**
/books/year/after2015


 🔄 Update Available Copies

**PUT**
/books/updateCopies/:id

**Request Body**
json
{
  "change": 2
}

> Use negative values to reduce copies.


🏷️ Change Book Category

**PUT**
/books/changeCategory/:id

**Request Body**

json
{
  "category": "Programming"
}


 🗑️ Delete Book (Only if copies = 0)

**DELETE**
/books/delete/:id

 ❗ Validations

* Available copies cannot be negative
* Book cannot be deleted if copies > 0
* Proper error handling for invalid IDs

📌 Future Improvements

* User authentication
* Pagination & search
* Environment variables (`.env`)
* Deployment to cloud (Render / Railway)

👩‍💻 Author

**Devi Priyanka**
Beginner-friendly backend project for learning Express & MongoDB 🌱
