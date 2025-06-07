# API Testing Project – Trello REST API

##  Description
This is a pet project for practicing API testing using Trello's real REST API. I tested how to create, get, and delete a Trello board using Postman.

##  Tools
- Postman
- Trello Developer API
- JSON
- GitHub

##  Authorization
To send requests to Trello API, you need an `API Key` and `Token`.  
How to get them: [Trello API Authorization Guide](https://developer.atlassian.com/cloud/trello/guides/rest-api/authorization/)

## 📋 Tested Requests

| request | Endpoint                 | Description          |
|--------|--------------------------|----------------------|
| GET   | boards                  | Get all existing boards|
| Create| board                  | create a new board   |
| Create | Create a new List      | Create a new list    |
| Create| Create a new card       | Create a new card on a list|
| Delete | Delete a board         | Delete one of boards |

##  Test Results

### 📍 Get Boards – Get /boards/

-  **Status Code**: `200 OK`
- 🚀 **Response Time**: `< 400 ms`
- 🗂 **Content-Type**: `application/json`
- 🧪 **Test Result**: Passed; Failed 
- 🖼 **Screenshot**:  
  [GetBoards](https://github.com/MikClaus/API_Testing_Project/blob/e4809648571c9b2d46517fa22675552553c8efca/Screenschoots/Getboards_tests.jpg)
