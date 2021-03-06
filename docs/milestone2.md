# ctrl-alt-elite

# UMass Job Board

# Team Overview

* Aditya Pothanaboyina: apothanaboyina
* Amanda Katt: akatt1221

# Innovative Idea

We would like to create a web application similar to that of the UMass Student Job Board. The current web page for the Student Job Board gets the job done, but navigating through the jobs, and filtering based on multiple criteria becomes a difficult task given the layout of the web page. Likewise, users have to rely on their UMass email address to apply for jobs, leaving a lot of uncertainty in the status of their applications. 
As a group, we would like to address these obstacles and create a web application similar to that of the existing application, but with the capability for users to create user profiles to apply faster and more efficiently. We also want to make the job search process more flexible to candidates by allowing them to filter jobs based on their availability, job field, etc.

# Important Data

* Login for applicants / login for employer
    * This allows for applicants and employers to maintain a profile as well as ensure that only UMass students/staff are applying to jobs
* Jobs being posted
    * Allowing employers to post various jobs within their profiles allows for easy access to see which applicants applied for which job
* A personal user profile that contains resume, cover letter, etc
    * With a user profile, applicants can personalize their profile to showcase their strengths and skills through uploading documents as well as editing their profile.
* Number of applicants for a particular job(for employers)
    * Allows for employers to easily review applicants and their profiles as opposed to checking emails for application
* History of jobs applicant has previously applied to(for candidates)
    * Allows for applicants to quickly check on the status of their application if they have multiple applications.

# Objects:
* User
    * Email
    * Password
    * Name
    * Resume
    * List of Jobs applied
* Employer
    * Email
    * Password
    * Name
    * List of Jobs posted
* Job
    * jobID   //6 digit unique number randomly generated to represent specific job
    * Email //email of employer who created
    * Name
    * Location
    * Date created
    * List of applicants*

# API Endpoints:
* /user/login: logs user profiles in
* /employer/login: logs employer profiles in
* /user/create/:email/:name : creates new user
* /employer/create/:email/:name : creates new employer
* /employer/job/create/:email/:name/:location/:date : creates new job
* /jobs : response will be JSON object representing all jobs
* /users : response will be JSON object representing all users
* /employers: response will be JSON object representing all employers
* /employer/job/:jobID: response will be JSON object of specified job
* /employer/:email: response will be JSON object of specified employer
* /user/:email: response will be JSON object of specified user
* /user/:email/apply/:jobID : Specified user applies to specified job. Adds jobID to list of applied jobs for user, adds email to list of applicants for specific jobs
* /employer/jobs/delete/:jobID: deletes specified job
* /employer/delete/:email : deletes specified employer
* /user/delete/:email : deletes specified user

# Work Distribution
* Amanda:
    * Created jobDescription html and css
    * Created Index.html and index.css
    * Initialized server.js
    * API Endpoints
    * Utilities.js functions (CRUD functions)
    * Routes to html pages
    * Created js files for all of the pages and heavily worked on search.js, login.js, index.js, and jobDescription.js
* Aditya:
    * Worked on applicants.js and employerinterface.js on employer side
    * Created CRUD operations for jobs
    * Created milestone2 markdown file

