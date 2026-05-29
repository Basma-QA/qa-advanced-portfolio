## GET Users API Test

### Objective
Verify that the API returns a list of users.

### Endpoint
GET /users

### Preconditions
API is available

### Steps
1. Send GET request to /users
2. Check response

### Expected Result
- Status code 200
- List of users returned

### Actual Result
- Users returned successfully

### Status
Passed
----------------------------------------------------------------------------------------------------

# 🧪 Test Case: Get Single User API

**ID:** TC_GET_SINGLE_USER_01  
**Module:** Users API  
**Priority:** High  
**Type:** Functional Test  
**Method:** GET  


## 🎯 Objective
Vérifier que l’API retourne correctement les informations d’un utilisateur spécifique.


## 🔗 Endpoint
GET https://api.example.com/users/2  


## 🔧 Pre-conditions
- API disponible  
- User ID existe  
- Postman configuré  


## 🚀 Steps
1. Ouvrir Postman  
2. Envoyer requête GET  
3. Vérifier response status  
4. Vérifier response body  


## ✅ Expected Result
- Status = 200  
- Données utilisateur correctes  


## 📸 Evidence
![Get Single User](images/get-single-user.png)

-----------------------------------------------------------------------------------------------------
































