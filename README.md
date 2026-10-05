# 🎬 Movie Review App

A full-stack movie review application with a **React.js** frontend, a **Spring Boot** REST API backend, and **MongoDB Atlas** for data storage.


---

## ✨ Features

- Browse movies served by a Spring Boot REST API
- Read and add reviews for movies **[CONFIRM: add or remove features to match your app]**
- Client-side routing with React Router
- Responsive UI built with React Bootstrap
- Movie and review data stored in MongoDB Atlas

## 🛠️ Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React.js, React Router, Axios, React Bootstrap |
| Backend | Java, Spring Boot, REST APIs |
| Database | MongoDB Atlas |

## 📁 Project Structure

```
Movie_Review_App/
├── MovieClient/
│   └── movie-gold-v1/   # React frontend
├── movies/
│   └── movies/          # Spring Boot backend
└── movies.json          # Movie dataset
```

## 🔌 API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| `GET` | `/api/v1/movies` | Get all movies |
| `GET` | `/api/v1/movies/{id}` | Get a single movie |
| `POST` | `/api/v1/reviews` | Add a review |

## 🚀 Run Locally

### Prerequisites

- Java **[CONFIRM: version, for example 17]** and Maven
- Node.js and npm
- A MongoDB Atlas account (free tier works)

### 1. Clone the repository

```bash
git clone https://github.com/KatariTrivikram/Movie_Review_App.git
cd Movie_Review_App
```

### 2. Set up the database

1. Create a free cluster on [MongoDB Atlas](https://www.mongodb.com/atlas).
2. Create a database user and allow your IP address under **Network Access**.
3. Import the sample data from `movies.json` **[CONFIRM: database and collection names]**:

```bash
mongoimport --uri "<your-atlas-connection-string>" --db <database-name> --collection movies --file movies.json --jsonArray
```

### 3. Start the backend

```bash
cd movies/movies
```

Set your connection string without committing it, for example as an environment variable **[CONFIRM: property name used in your application.properties]**:

```bash
export SPRING_DATA_MONGODB_URI="<your-atlas-connection-string>"
./mvnw spring-boot:run
```

The API runs on 'http://localhost:8080'.

### 4. Start the frontend

```bash
cd MovieClient/movie-gold-v1
npm install
npm start
```

The app opens at `http://localhost:3000` **[CONFIRM: port and start command]**.



## 🔮 Future Improvements

- User authentication for posting reviews
- Search and filter movies by genre and rating
- Deploy the frontend and backend and add a live demo link

## 👤 Author

**Trivikram Katari**

- GitHub: [KatariTrivikram](https://github.com/KatariTrivikram)
- LinkedIn: [trivikramkatari](https://www.linkedin.com/in/trivikramkatari/)
- Email: trivikramkatari@gmail.com
