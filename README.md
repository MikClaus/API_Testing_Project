# API Testing Project – Trello REST API

##  Description
This is a pet project for practicing API testing using Trello's real REST API. I tested how to create, get, and delete a Trello board using Postman.

##  Tools
- Postman
- Trello Developer API
- JSON
- GitHub

 ## How to run this Postman collection
Create a Postman Environment (or a .env file for local use) and define the following variables:

- apiKey — your Trello API Key

- apiToken — your Trello API Token

- boardId — the ID of the test board (used for deleting or creating lists)

Fill these variables with your actual keys, which you can get from the Trello developer console.

In Postman, select this environment before running the requests.

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
  ![GetBoards](https://github.com/MikClaus/API_Testing_Project/blob/e4809648571c9b2d46517fa22675552553c8efca/Screenschoots/Getboards_tests.jpg)

  ### 📍 Create Board – POST /boards/
- Status: `200 OK`
- Screenshot: ![create-board](https://github.com/MikClaus/API_Testing_Project/blob/f3a7d187408727d0e6ac179c9066de0432ba1ad0/Screenschoots/createaboard.jpg)

- 
 ### 📍 Create a new list – POST /lists/

- ✅ **Status Code**: `200 OK` — _passed_
- ⏱ **Response Time**: `< 600 ms` — _passed_
- 🔤 **Field Validation**: `name is a string` — _passed_

#### 🖼 Screenshot:
![create-board](https://github.com/MikClaus/API_Testing_Project/blob/467b794c25c53070cb5750f22250ed51f71cadd8/Screenschoots/Createanewlist.jpg)

### 📍 Create a new Card – POST /cards/

- ❌ **Status Code**: `Expected 200` — _passed_  
  
- ⚠️ **Response Time**: `Expected < 200ms`, got `647ms` — _failed_  
  > 🐢 Server was slower than expected.

- ✅ **Field Validation**: `ID is a string` — _passed_

#### 🖼 Screenshot:
![create-board](https://github.com/MikClaus/API_Testing_Project/blob/a918ee6b6a5b3f79f8ff3a39c6e5e6c7d74e5a52/Screenschoots/createanewcard.jpg)

### 🗑️ Delete Board – DELETE /boards/{id}

- ✅ **Status Code**: 200 OK
- 🧪 **Test Result**: Passed

#### 🖼 Screenshot:
![delete-board](https://github.com/MikClaus/API_Testing_Project/blob/bc16aa2e87941c7d59494a9bac1e6c5427cd670a/Screenschoots/Deleteaboard.jpg)

### 📦 Postman Collection
- [Trello API Test Collection]([postman/trello_api_collection.json](https://github.com/MikClaus/API_Testing_Project/blob/3af60ca9da3bebadfada75250d1d0c5454d33163/postman/Trello%20HW.postman_collectionn.json))


