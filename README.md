# Postman API Automation Collection

This project demonstrates API testing and automation using Postman, including dynamic variables, scripting, and request chaining.

---

## Features

-  Created and tested REST API requests using Postman
-  Used collection variables for dynamic request handling
-  Implemented Post-response scripts using JavaScript (pm object)
-  Extracted data from API responses and reused it in subsequent requests
-  Configured API Key authentication
-  Structured requests with query parameters and JSON body

---

## Tech Stack

- Postman (API Testing)
- JavaScript (Postman scripting)
- REST APIs

---

## Key Implementation

### Dynamic Variable Handling
Used collection variables like:
```
{{skillcheckBaseUrl}}
{{favoriteActor}}
```

---

### Post-response Script Example
```javascript
const actorName = pm.response.json().data.actorName;
pm.collectionVariables.set("favoriteActor", actorName);
```

Request Configuration
- Method: POST
- Query Params: movieName
- Authorization: API Key
- Body:
{
  "actorName": "Tom Holland"
}

Project Structure
```
Postman Collection (JSON export)
README.md
```

## What this project demonstrates
- API request building
- Automation using scripts
- Handling real-world API responses
- Debugging JSON structures
- Variable-driven workflows

## How to Use
- Import the Postman collection JSON file
- Set up collection variables
- Run requests in sequence
- View variable updates in Postman

## Learning Outcome

Through this project, I gained hands-on experience in:

- API automation workflows
- Writing scripts in Postman
- Debugging and handling API responses
- Using variables to chain requests
