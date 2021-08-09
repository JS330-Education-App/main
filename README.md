EDUCATION REPORT README

Students, Teachers, and Parents need to be in communication about grades.  Using JavaScript, it is possible to create a portal for up-to-date assignment reports.  By creating this as a web application, these three groups can have a better time engaging in the learning process.
Teachers should be able to monitor their various classes and assignments.  Students should be able to see their grades as well as upcoming/ungraded assignments.  Parents should be able to see their students’ grades and assignments.
To solve this, we will create an MVC style JavaScript Application, using React, MongoDB, Express, and Node.js.  There will be four views: login/registration, parent, teacher, and student.  Mongoose will be used to create models for our data collections in MongoDB.  Express will control the state of the application’s data through routing and connect the Views to the Models.  By using each of the listed technologies, we utilize JavaScript as the only language and convention needed to create this application.  Each technology is complimentary, empowering the application to quickly render changes in data state.
MongoDB is both scalable and fast.  It stores data as a binary value.  Through Node.js, JSON objects are quickly translated to binary data and search for schema-less collections.  Mongoose is an Object Relational Mapping layer that helps provide schemas for MongoDB.  Here, we will utilize these technologies to create three separate schema objects to be stored in MongoDB collections.  User.js, Assignment.js, and AssignmentGrades.js will be the three mongoose schemas to be used as our models.
Express.js is a framework that makes it easier to write a web server on Node.js.  This is accomplished by defining routes.  Express parses the URL, headers, and parameters.  The route determines what to do with the received HTTP request matching a specific pattern.  For this project we will have three routes: Login.js, Assignment.js, AssignmentGrades.js.  
For Login.js there will be three routes: Signup, Login, and Change Password.
Signup POST /login/signup, Login POST /login, and Change Password POST/login/password.  The sign-up page will offer a field for First/Last name, a dropdown for role of teacher, student, or parent, and a specification for what grade level the student.  When signing up, all fields will be verified determined by selected role.  When logging in, email/password will be verified as well.
Assignment.js will require authentication and authorization.  To create a new assignment, a POST /assignment route will be made, restricted to the teacher role.  The assignment is placed into the JSON body.  To assign an assignment to a student, the route of : POST/assignment/:id, will be made and restricted to the “teacher” role.  The “id” = student email.  To update the assignment, the route of PUT/assignment/:id is used.  Only the teacher and student can update these assignments.  All assignments must also be displayed for the teacher/student.  GET/assignment/:id will resolve this, with “id” = teacher’s last name.  To get a particular assignment, the route GET/assignment/:id will be used.  Teacher and student roles can only access this route if and only if the student id matches the student’s id found in the specific homework object.
To get grades, AssignmentGrades.js routes will be used.  GET/studentAssignments/:id will be displayed both to the Student and Parent, and show the student’s grades, where “id”= student.  GET/studentAssignments will display grades for all students for only the Teacher role.
With Express allowing to define routes, Express can also be written as middleware.  Middleware gives web servers the ability to insert custom code into any request/response processing path.  In addition to routing, we have written Express middleware to handle authentication and authorization.
With MongoDB, we will be utilizing indexes for performance using the userId, and Assignment title.  We will also be making two text searches, searching Assignment by title, and the other searching Students by name/grade level.  We will have three aggregations: assignment by title, assignment by grade level, and by teacher.  There will be one lookup for a specific assignment for a student.
React-Router, React-Bootstrap, and MaterialUI will be used to help render data and provide a simple front-end to demonstrate the API.  Axios will potentially be used to help handle headers.
Jest is a testing framework that will be used to test login routes and assignment routes.
We built this application based off the idea from Tamara Trefilova.  She suggested this idea to showcase our abilities in MongoDB, Mongoose, Express and Node.js from what we have learned in JS330.  Kateryna helped provide UI design and an overall framework for us to develop around.  Surry provided user stories and outlined the site’s architecture.






Copyright (c) 2021 Patrick Gronstal, Tamara Trefilova, Surry Mowery, Kateryna Masiuk

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
