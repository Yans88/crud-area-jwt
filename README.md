# crud-area with jwt
Jum'at, 26 Agustus 2022

Crud data provinsi dan kota menggunakan JWT.

## Arsitektur
1. Database PostgreSQL
2. Java SpringBoot untuk REST API

Soal : https://docs.google.com/document/d/12Hu5l12vAXf6fm7jPgQ_i-RMk3q6P8lEUyNz0nuZWWk
<br/>
Dokumentasi API : https://documenter.getpostman.com/view/624374/VUxKSoof

## HTTP Request Sample
### Signup(POST)
<pre>
curl --location --request POST 'http://localhost/crud-jwt/v2/auth/signup' \
--header 'Content-Type: application/json' \
--data-raw '{
    "phone": "012345678911234",
    "name" : "yansen",
    "email" : "test@mail.com",
    "password": "123456"
}'
</pre>

### Signin(POST)
<pre>
curl --location --request POST 'http://localhost/crud-jwt/v2/auth/signin' \
--header 'Content-Type: application/json' \
--data-raw '{
    "phone": "012345678911234", 
    "password": "123456"
}'
</pre>

### Get Phone number by JWT(GET)
<pre>
curl --location --request GET 'http://localhost/crud-jwt/v2/auth/info' \
--header 'Authorization: Bearer eyJhbGciOiJIUzUxMiJ9.eyJzdWIiOiIxIiwiaWF0IjoxNjYxNjcxNTkwLCJleHAiOjE2NjIyNzYzOTB9.JdVltuyMd3y0-6wg7hkazkF_-5ixRoItSYnGBg7d4O_1ZxVB3UUHzRP2eColBPhclpMgjD2SnE95EIJmQ0yvBQ'
</pre>