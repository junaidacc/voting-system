# Online Voting System
### Secure Election Management and Relational Data Architecture

This project is a full-stack system designed to handle the complexities of digital balloting. Developed over a multi-phase engineering lifecycle, it focuses on data consistency, secure session management, and a structured relational database back-end.

---

## 1. System Specifications and Requirements
The following environment was used for development and testing to ensure system stability:

| Component | Specification |
| :--- | :--- |
| **Language** | PHP 7.4+ (Core Logic) / Hack |
| **Database** | MySQL 5.7 (Relational Storage) |
| **Frontend** | HTML5, CSS3 (Responsive Design) |
| **Local Server** | XAMPP / Apache Environment |

---

## 2. Database Schema Design
A major portion of the engineering effort went into designing a relational schema that ensures integrity.

| Table Name | Primary Key | Key Columns | Purpose |
| :--- | :--- | :--- | :--- |
| **Users** | `user_id` | `username`, `password`, `status` | Stores encrypted voter credentials. |
| **Candidates** | `candidate_id` | `name`, `party`, `total_votes` | Manages candidate profiles and counts. |
| **Votes** | `vote_id` | `user_id`, `candidate_id` | Prevents double-voting via unique links. |

---

## 3. Key Engineering Features
* **Session-State Persistence:** Uses server-side sessions to track voter progress.
* **Atomic Transactions:** Logic ensures a vote is either fully recorded or not recorded at all.
* **Input Sanitization:** Filters all user data to protect against SQL injection.

---

## 4. Local Installation
1. Move the project folder into your `htdocs` directory.
2. Create a new MySQL database in **phpMyAdmin**.
3. Import the included `.sql` file to initialize the tables.
4. Update `db_connect.php` with your local credentials.
5. Access via `localhost/OnlineVotingSystem`.
