# yoga-app

#Yoga-client(front-end)

I have implemented UI using react-bootstrap and added notification functionality using react-toastify. I have also implemented form validation using regular expressions, including a validation to ensure that the age of the person must be between 18 and 65, all the fields have been filled, and the person must pay the 500/- rs fee for the month and select a particular batch for classes. I have managed the form fields using the useState hook in React and used axios to send HTTP requests.

also I have implemented a mock function called CompletePayment() that accepts the details of a user and payment, processes the payment for students, and displays a success notification using React Toastify."



I have deployed the app on Netlify. Here is the live link:

https://yoga-client-app.netlify.app/

I have Dockerized the front-end(client-side) by creating a Docker container for it.


if you want to see the backend code and documentation (ER diagram)
please visit this link:-
https://github.com/batman005/yoga-server


Shots:
registerform UI
![registerform](https://user-images.githubusercontent.com/51878340/208254883-87e00fa6-09ac-4d3d-94a3-c73b4efc4191.png)

CompletePayment and Succesfull registraion UI 
![completepaymentandregistered](https://user-images.githubusercontent.com/51878340/208254902-de8bce4a-d501-449c-8db2-3bc15266b0bc.png)

If email or mobileno  already exist in database then it show a popup error 
![emailnumberexist](https://user-images.githubusercontent.com/51878340/208254919-55a93205-2c02-40ac-8a0d-ca014f174d09.png)

Update batch of a person by email id
![updateform](https://user-images.githubusercontent.com/51878340/208254955-ca2ecb7a-1250-49ef-a4bc-f47817ad7453.png)

In the API, I have implemented a condition that checks if the CURRENT_DATE is less than the expiration date of the student's enrollment. If this is the case, a popup message is displayed indicating that the student must stay in their current batch for the current month. If the CURRENT_DATE is greater than the expiration date, the student's batch is updated. This allows the API to enforce the rule that a student must complete their current enrollment period before switching to a new batch.

## Available Scripts

In the project directory, you can run:
for running locally in your system

### `npm install`

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

#BACKEND(sever)
# Yoga-Server
This is the server-side component of a Yoga application. It is a RESTful API built using Node.js and Express. The API enables clients to perform various operations such as creating, reading, updating, and deleting Yoga classes and appointments.

Prerequisites
Before you begin, make sure you have the following installed on your local machine:

-Node.js
-npm

Installation
Clone the repository to your local machine:
Copy code
```
git clone https://github.com/batman005/yoga-server.git
```
Navigate to the project directory:
Copy code
```
cd yoga-server

```
Install the project dependencies:
Copy code
```
npm install
```
Start the server:
Copy code
```
npm start 
nodemon index.js
```

This Entity Relationship (ER) diagram shows the relationships between several entities in a Yoga class  Registration form.

![ERDiagram](https://user-images.githubusercontent.com/51878340/208255937-22a0a463-f376-491b-8c3a-cdc2a310aef5.png)


I have implemented the database for this application using PostgreSQL and the backend using Node.js and Express. To serve the database, I have used the render and to host the server, I have used cyclic. These technologies enable me to create a robust and scalable RESTful API for the Yoga class scheduling system.

About my Yogatable Schema
This schema defines a table called yoga in a PostgreSQL database. The table has the following columns:

- yoga_id: A unique serial identifier for each row in the table.
* batch: A string representing the batch in which the student is enrolled.
+ dob: A date representing the student's date of birth.
- email: A string representing the student's email address, which is also used as the primary key for the table.
* gender: A string representing the student's gender.
+ name: A string representing the student's name.
- status: A string representing the student's payment status.
* number: A unique big integer representing the student's phone number.
+ date_of_joining: A date representing the date on which the student joined the program.
- date_of_expiry: A date representing the date on which the student's enrollment expires.

This table is used to store information about Yoga students, including their personal details, enrollment information, and contact details. The yoga_id column is used as a unique identifier for each student, and the email column is used as the primary key for the table. The date_of_joining and date_of_expiry columns are used to track the student's enrollment period.





