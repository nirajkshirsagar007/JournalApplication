# JournalApplication

A backend journal management application built with **Spring Boot** by [nirajkshirsagar007](https://github.com/nirajkshirsagar007).

This project provides RESTful APIs to create, manage, and organize journal entries.  
**Note:** This application does not include a user interface (UI)—it is intended to be used as a backend API and uses an in-memory data structure (HashMap) for storage. No external database is required.

## Features

- Add, update, and delete journal entries via REST endpoints
- Organize entries by id, title, or content
- Uses an in-memory HashMap as a temporary database (all data is lost on server restart)
- Easily extensible for additional features

## Getting Started

### Prerequisites

- Java 17 or higher
- Maven 3.6.x or higher

### Building and Running

1. **Clone the repository:**
    ```bash
    git clone https://github.com/nirajkshirsagar007/JournalApplication.git
    cd JournalApplication
    ```

2. **Build the project:**
    ```bash
    mvn clean install
    ```

3. **Run the application:**
    ```bash
    mvn spring-boot:run
    ```

    By default, the server will start at `http://localhost:8080`.

### API Usage

You can interact with the API using tools like [Postman](https://www.postman.com/) or `curl`.

Example endpoints (these may vary based on your implementation):

| Method | Endpoint            | Description                 |
|--------|---------------------|-----------------------------|
| GET    | `/journals`         | List all journal entries    |
| POST   | `/journals`         | Create a new journal entry  |
| GET    | `/journals/{id}`    | Get a specific entry        |
| PUT    | `/journals/{id}`    | Update an entry             |
| DELETE | `/journals/{id}`    | Delete an entry             |

All request and response formats are typically JSON.

#### Example: Create a Journal Entry

```bash
curl -X POST http://localhost:8080/journals \
  -H "Content-Type: application/json" \
  -d '{"title": "My Day", "content": "Today I learned Spring Boot.", "date": "2025-09-08"}'
```

## Notes

- **No persistent storage:** All data is stored in-memory using a Java HashMap and will be lost when the application stops or restarts.
- **No user interface:** This project exposes only REST APIs and does not provide a front-end.

## Contributing

Contributions, bug reports, and feature requests are welcome!  
Feel free to open an issue or submit a pull request.


## Author

- [nirajkshirsagar007](https://github.com/nirajkshirsagar007)

---
> *Happy journaling—API style!*
