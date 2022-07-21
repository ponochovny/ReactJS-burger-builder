<h3 align="center">:sandwich:<a href="https://react-my-burger-d86a3.firebaseapp.com/">DEMO</a>
  </h3>

## About the project

Project loads available ingredients for Your burger from Firebase, allows user to sign in and sign up, and to build own burger with ingredients, fill form with own contact information and send to the server all collected data of an order.

* Firebase api requests with axios
* Form validation
* Lazy load components
* Load indicator
* Error pop-up
* Prop Types
* Redirect
* Authentication check with middlware
* Check orders by current user
* Redux, Redux Thunk

## Installation

1. Clone repo

` git clone https://github.com/ponochovny/ReactJS-burger-builder.git `

2. Install NPM packages

` npm install `

3. Start

` npm start `

## Firebase settings
### Realtime database rules:
```
{
  "rules": {
    "ingredients": {
      ".read": "true",
      ".write": "true",
    },
    "orders": {
      ".read": "auth != null",
      ".write": "auth != null",
        ".indexOn": ["userId"]
    }
  }
}
```
### Add object into realtime Firebase:
```
{
ingredients:
  {
    bacon: 0,
    cheese: 0,
    meat: 0,
    salad: 0
  }
}
```
