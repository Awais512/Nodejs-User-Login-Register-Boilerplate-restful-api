# Nodejs-User-Login-Register-Boilerplate-restful-api
It is a boilerplate Node js Mongo db and Expressjs Restful api. User can register, Login and Update their profile. It has two types of users. One is Admin and other is simple user. Admin can view all the users. User can only update their profile. Use two middlewares one for protected users and another for protecting the admin routes. Give it a try.
It is a boilerplate Node js Mongo db and Expressjs Restful api. User can register, Login and Update their profile. It has two types of users. One is Admin and other is simple user. Admin can view all the users. User can only update their profile. Use two middlewares one for protected users and another for protecting the admin routes. Give it a try.

1)Clone the Repo

2)Run npm install

3)Run npm start

Open Postman and hit the route for registering the users at localhost://5000/api/users/register with name email and password.
Then login with your email and password at localhost://5000/api/users/login

Make sure you have mongoDb installed or you can use mongoDb Atlas just edit the environment variable MONGO_URI with the url of your atlas database
