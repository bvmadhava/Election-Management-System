# Digital Election Management System

##  Project Overview

This project is a **Digital Election Management System** that allows users to:

- Register and log in as a voter or election commissioner.
- View candidates based on the voter's constituency.
- Cast votes for candidates (only one vote per user is allowed).
- View live vote counts (commissioner role).
- Store data using a mock backend (JSON Server).

It is primarily designed for **front-end demonstration** and uses `JSON Server` as a mock REST API backend.

---

## Setup Instructions

### 1. Clone the Repository
```bash
git clone <repository-url>
cd digital-election-system
```

### 2. Install JSON Server
Make sure Node.js is installed. Then install JSON Server globally:
```bash
npm install -g json-server
```

### 3. Start JSON Server
Navigate to the folder containing `db.json` (provided in the project folder):
```bash
json-server --watch db.json --port 3000
```

### 4. Run the Frontend
You can open the HTML files (`login.html`, `signup.html`, `candidates.html`, etc.) in your browser using Live Server (VS Code extension) or simply by double-clicking.

---

##  Features Implemented

###  Authentication
- User signup with constituency selection
- Login validation against registered users
- User role detection (voter or commissioner)

### Voting System
- Voters can view candidates **only in their constituency**
- Vote for **only one** candidate
- Local storage tracks voter status to prevent multiple votes

###  Commissioner View
- View total votes for each candidate
- View constituency-wise details

###  Data Management (Mock Backend)
- Data stored in `db.json` using JSON Server
- Includes:
  - `users` (voters & commissioners)
  - `candidates` (with name, party, votes, constituency)
  - `votes` (to track if a user has voted)
