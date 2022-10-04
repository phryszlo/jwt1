### CALL THIS FIRST
(use requests.rest with REST Client extension)
```
POST http://localhost:4040/login
Content-Type: application/json

{
  "username": "jonas"
} 
```

### then paste the resulting refreshToken into here:

``` POST http://localhost:4040/token
Content-Type: application/json

{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1lIjoiam9uYXMiLCJpYXQiOjE2NjQ4OTQyMjh9.SGezde52ereg6tnp-ALaSglk8t4x2ittrCC4whSCZvw"
} 
```

### and here 

``` DELETE http://localhost:4040/logout
Content-Type: application/json

{
  "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1lIjoiam9uYXMiLCJpYXQiOjE2NjQ4OTQyMjh9.SGezde52ereg6tnp-ALaSglk8t4x2ittrCC4whSCZvw"
} 
```


### finally this should work until timeout.

```
GET http://localhost:4000/posts
Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1lIjoiam9uYXMiLCJpYXQiOjE2NjQ4OTQyMjgsImV4cCI6MTY2NDg5NDUyOH0.bWmq5XClQRcEMO3gyHMTM8l4Klm3yw_Yc_cxUwoiq2c
```
