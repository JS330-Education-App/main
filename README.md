EDUCATION REPORT README

Students, Teachers, and Parents need to be in communication about grades.  Using JavaScript, it is possible to create a portal for up-to-date assignment reports.  By creating this as a web application, these three groups can have a better time engaging in the learning process.
Teachers should be able to monitor their various classes and assignments.  Students should be able to see their grades as well as upcoming/ungraded assignments.  Parents should be able to see their students’ grades and assignments.
To solve this we will create an MVC style JavaScript Application, using React, MongoDB, Express, and Node.js.  There will be four views: login/registration, parent, teacher, and student.  Mongoose will be used to create models for our data collections in MongoDB.  Express will control the state of the application’s data through routing and connect the Views to the Models.  By using each of the listed technologies, we utilize JavaScript as the only language and convention needed to create this application.  Each technology is complimentary, empowering the application to quickly render changes in data state.
MongoDB is both scalable and fast.  It stores data as a binary value.  Through Node.js, it is able to quickly translate JSON objects to binary data and search for schema-less collections.  Mongoose is an Object Relational Mapping layer that helps provide schemas for MongoDB.  Here, we will utilize these technologies to create three separate schema objects to be stored in MongoDB collections.  User.js, Assignment.js, and AssignmentGrades.js will be the three mongoose schemas to be used as our models.
Assignment mode has a title, body, and index to be used for performance.  This will allow aggregations to be made as a total grade viewable by the Parent/Student.
React is 


We built this application based off the idea from Tamara Trefilova.  She suggested this idea as a way to showcase our abilities in MongoDB, Mongoose, Express and Node.js from what we have learned in JS330.  

By discussing this project, we came up with a model of having

React-Router, React-Bootstrap, and MaterialUI will be used to help .  Axios will be used 
