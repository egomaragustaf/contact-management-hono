# User API Spec

## Register User

Endpoint: POST /api/users

Request Body: 

```json
{
    "username": "egomaragustaf",
    "password": "secret",
    "name": "Ego Maragustaf"
}
```

Response Body (Success):

```json
{
    "data": {
        "username": "egomaragustaf",
        "name": "Ego Maragustaf"
    }
}
```

Response Body (Success):

```json
{
    "errors": "Username must not blank, ..."
}
```

## Login User

Endpoint : POST /api/users/login

Request Body :

```json
{
    "username": "egomaragustaf",
    "password": "secret",
}
```

Response Body (Success):

```json
{
    "data": {
        "username": "egomaragustaf",
        "name": "Ego Maragustaf",
        "token": "token"
    }
}
```

## Get User

Endpoint: GET /api/users/current

Request Header:
 - Authorization: token

Response Body (Success):

```json
{
    "data": {
        "username": "egomaragustaf",
        "name": "Ego Maragustaf",
    }
}
```

## Update User

Endpoint: PATCH /api/users/current

Request Header:
 - Authorization: token

```json
{
    "name": "When update name.",
    "password": "When update password.",
}
```

Response Body (Success):

```json
{
    "data": {
        "username": "egomaragustaf",
        "name": "Ego Maragustaf",
    }
}
```

## Logout User

Endpoint: DELETE /api/users/current

Request Header:
 - Authorization: token

```json
{
    "data": true
}
```