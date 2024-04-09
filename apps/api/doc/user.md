# User API Spec

## Register User
Endpoint : POST /api/auth/register

Request Body:

```json
{
  "username": "rayhansoe",
  "email": "rayhan@gmail.com",
  "password": "inipassword",
  "display_name": "Rayhan Hanif"
}
```

Response Body ( Success ):

```json
{
  "status": "OK",
  "data": {
    "username": "rayhansoe",
    "email": "rayhan@gmail.com",
    "display_name": "Rayhan Hanif"
  }
}
```

Response Body ( Fail ):

```json
{
  "status": "Not OK!",
  "errors": "Username must not be blank, ..."
}
```

## Login User
Endpoint : POST /api/auth/login

Request Body:

```json
{
  "username": "rayhansoe",
  "email": "rayhan@gmail.com",
  "password": "inipassword"
}
```

Response Body ( Success ):

```json
{
  "status": "OK",
  "data": {
    "username": "rayhansoe",
    "email": "rayhan@gmail.com",
    "display_name": "Rayhan Hanif",
    "token": "qwerty"
  }
}
```

Response Body ( Fail ):

```json
{
  "status": "Not OK!",
  "errors": "Username or password wrong, ..."
}
```


## Get User
Endpoint : GET /api/users

Response Body ( Success ):

```json
{
  "status": "OK",
  "data": {
    "username": "rayhansoe",
    "email": "rayhan@gmail.com",
    "display_name": "Rayhan Hanif"
  }
}
````

Response Body ( Fail ):

```json
{
  "status": "Not OK!",
  "errors": "Unauthorized, ..."
}
```

## Update User
Endpoint : PATCH /api/users

Request Body:

```json
{
  "username": "rayhansoe", // tidak wajib
  "email": "rayhan@gmail.com",  // tidak wajib
  "password": "inipassword",  // tidak wajib
  "display_name": "Rayhan Hanif",  // tidak wajib
  "avatar_url": "avatar.png", // tidak wajib
  "bio": "Yuhuuuu"  // tidak wajib
}
```

Response Body ( Success ):

```json
{
  "status": "OK",
  "data": {
    "username": "rayhansoe",
    "email": "rayhan@gmail.com",
    "display_name": "Rayhan Hanif",
    "avatar_url": "avatar.png",
    "bio": "Yuhuuuu"
  }
}
```

Response Body ( Fail ):

```json
{
  "status": "Not OK!",
  "errors": "Unauthorized, ..."
}
```


## Logout User
Endpoint : DELETE /api/users

Response Body ( Success ):

```json
{
  "status": "OK",
}
```

Response Body ( Fail ):

```json
{
  "status": "Not OK!",
  "errors": "Unauthorized, ..."
}
```