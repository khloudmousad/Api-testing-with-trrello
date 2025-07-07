Trello API Testing Project
This project demonstrates comprehensive API testing with Trello using Trello's REST API and includes automated tests for:

Creating boards

Updating boards

Getting board data

Creating lists

Creating cards

Adding items/checklists

Adding labels

Authentication is handled via API Key and Token provided by Trello.

🔧 Tech Stack
Language: Python (can be adapted for Postman, JavaScript, etc.)

Testing Framework: \Postman / custom test suite

HTTP Client: requests (or Postman built-in runner)

Assertions: Response code, response schema, content validations

🔑 Authentication
Trello uses API key and token for authentication.

📋 Features & Test Cases
1. ✅ Create Board
Method: POST

Endpoint: /1/boards/

Params: name, defaultLists, key, token

Assertions:

Status code == 200

Response contains id, name

response time

2. ✏️ Update Board
Method: PUT

Endpoint: /1/boards/{id}

Params: name, desc, key, token

Assertions:

Status code == 200

Board name and description updated

3. 📥 Get Board Data
Method: GET

Endpoint: /1/boards/{id}

Assertions:

Status code == 200

Response contains full board metadata

4. 🗂️ Create Lists
Method: POST

Endpoint: /1/lists

Params: name, idBoard, key, token

Assertions:

List created under correct board

Status == 200

5. 🗃️ Create Cards
Method: POST

Endpoint: /1/cards

Params: name, desc, idList, key, token

Assertions:

Card created with correct name and description

6. ✅ Add Items (Checklists)
Method: POST

Endpoint: /1/checklists

Params: idCard, name, key, token

Assertions:

Checklist created under card

7. 🏷️ Add Labels
Method: POST

Endpoint: /1/labels

Params: name, color, idBoard, key, token

Assertions:

Label created on board

Status == 200


This video show the run of the collection

https://github.com/user-attachments/assets/c9b7fa89-b2b8-4deb-868b-51dbec4f40dd

