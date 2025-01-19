# Dabank

My first large native Android project (spent 150h+). [Source code here](https://github.com/jani-heinikoski/dabank/tree/main/DaBank/app/src/main/java/com/jhprog/dabank). It is an imaginary mobile banking application which features four imaginary banks which have their own customers, bank accounts, cards etc. Users are able to make payments to other accounts, transfer funds between their own accounts, view transaction history, make recurring payments, and much more.

Some of the most notable features:
* Features four banks which have their own accounts and customers.
* Three types of bank accounts: current account, fixed-term account, savings account.
* Bank cards can be created and tied to accounts which can be used in the simulation to make transactions.
* Transaction history can be viewed indefinitely.
* Customers can make various transactions to other accounts: normal transactions, recurring payments, and pending transactions (set to be payed in the future).
* The application uses fragments instead of multiple activity architecture.
* SQLite is used as a local database to store information. Passwords are hashed and salted.
* UI-components have been styled from scratch instead of defaults. Material design has been followed.
* Each bank has test users with the following log-in credentials:
```
  username: username
  password: password
```
* Each bank has admin accounts with the following log-in credentials:
```
  username: admin
  password: Administrator123!
```

Drawbacks:
* Architecture and implementation are not great given what I have learned since creating this project. A much better approach would be to follow [MVVM-architecture as suggested by Google](https://developer.android.com/topic/architecture/intro). Notably, the structure is not as layered, clear, and testable as I would like it to be.
* Application's lifecycle has not been considered properly and as such suffers from bugs when certain lifecycle events are triggered.
* Data-access should use an object-relation mapper (ORM) such as [Room](https://developer.android.com/training/data-storage/room) instead of the SQLite APIs within the Android core libraries.
* Styles and theming should be better abstracted into common resources to make changes much easier.
* Documentation is not very comprehensive to say the least.

In conclusion, this project was intended to be a learning journey to native Android development, and should not be taken as a guide for best practices.

# Source code files

[See the relevant source code here](https://github.com/jani-heinikoski/viewmodel-demo/tree/main/app/src/main/java/com/lut/jh/viewmodeldemo)

