# Milestone 3 Submission

1. [Introduction](#introducton)
2. [Setting Up](#setting-up)
3. [User Stories](#user-stories)
4. [Components](#components)
    4.1. [Main Components](#main-components)
    4.2. [Features](###4.2-Features)
        4.2.1. [Milestone 2](####Features-implemented-in-Milestone-2)
        4.2.2. 
    
## <a name="introducton"></a>1. Introduction
**Proposed Level of Achievement:**

Artemis

![](RackMultipart20200726-4-6pxwre_html_a7b3e8ca1a96a4b9.png)

**Motivation**

Have you ever needed to deliver a parcel somewhere but you are too busy to hand deliver it? Have you ever noticed that your trip from point to point can be more meaningful? Ever wanted to make use of the empty space in your vehicle?

Normal delivery services usually require at least a few days to deliver your parcel. With the advent of technology, we see companies like Grab and Uber making use of people&#39;s vehicles to provide carpool services to ferry people to locations near their destination. So why not we implement a parcel delivery service where people can help deliver parcels to locations that are near to their end destination?

**Aim**

We hope to make parcel delivery more efficient by providing a platform for commuters to help with deliveries.


## <a name="setting-up"></a>2.1 Setting Up
### Setting up the project on local machine **(example using Mac OSX):**

**Prerequisites:**

- An IDE, eg. Visual Studio Code
- Python 3.7
- pip (Python package installer) available for download : [https://pip.pypa.io/en/stable/installing/](https://pip.pypa.io/en/stable/installing/)
- Node.js(for npm package manager) download at: [https://nodejs.org/en/](https://nodejs.org/en/)
- Conda, for managing virtual environments, download at : [https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html#](https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html#)
- MongoDB, download at : [https://docs.mongodb.com/manual/administration/install-community/](https://docs.mongodb.com/manual/administration/install-community/)


**Setting up Project:**

- Clone repository from [https://github.com/mechastriker3/SendIt.git](https://github.com/mechastriker3/SendIt.git)
- Directory Structure (blue = folder, white = files):
  - ![](RackMultipart20200726-4-6pxwre_html_bdd045760573e25d.png)
- Open the project in IDE(VSCode)
- Open Terminal(for MacOS)
- Start mongoDB
  - Run brew services start mongodb-community@4.2
- To start the **frontend** server:
  - cd into /frontend directory
  - Run npm install (This will install the dependencies required for project to run)
  - Run npm start
  - Once you see that it has compiled successfully means the server is active

![](RackMultipart20200726-4-6pxwre_html_f506dcf03cf7ddda.png)

Next, open a New terminal with the + button on the top right hand corner

- To start the **backend** server:
  - cd into /backend directory
  - Set up virtual environment (so that pip packages will be contained in the environment)
    - Run conda create -n myenv python **=** x.x anaconda(replace x.x with python version, in our case python 3.7)
    - This will create a virtual environment named myenv. Run conda env list to check if the environment is created. You should see an environment myenv.
    - Next we will activate the virtual environment by running conda activate myenv

You should see a (env) at the front:

![](RackMultipart20200726-4-6pxwre_html_2792bd5f194ea8a8.png)

- After our virtual environment has been set up, we need to install our requirements for the backend.
  - Run pip install -r requirements.txt
- To start the backend server:
  - Run python main.py
  - You should see something like this:

![](RackMultipart20200726-4-6pxwre_html_212f6024ee712953.png)

Now that the frontend and backend servers are running you may test the application out with your own google accounts.

Note: App runs on local database as this app is in development mode.





## <a name="user-stories"></a>3. User Stories

**High priority \> Must Have: \* \* \***

**Medium priority \> Should Have: \* \***

**Low priority \> Good to Have: \***

**A User is a general term for any one who uses our application, this includes a user that needs parcel delivered as well as deliverers.**

| **Priority** | **As a...** | **I want to be able to ...** | **So that I can ...** |
| --- | --- | --- | --- |
| \* \* \* | Sender | Add a delivery job | Have my parcel delivered by a deliverer |
| \* \* \* | User | Login securely | Keep my account safe |
| \* \* \* | User | View my job history | Keep a track record of all my previous transactions and jobs |
| \* \* \* | User | View my ongoing jobs | Keep a track record of the status of my ongoing jobs |
| \* \* \* | User | View my personal information | Ensure my information is correct |
| \* \* \* | Deliverer | View a list of all the jobs available | Accept jobs from the list |
| \* \* \* | Deliverer | Search and filter through the list of jobs | Find the jobs that is convenient and suitable for me |
| \* \* | Sender | Cancel a job i posted if it has not been accepted | Remove a job if i no longer need it |
| \* \* | Sender | View details of deliverer who accepted the job I posted | Keep in contact the deliverer |
| \* \* | Sender | Have a confirmation that my delivery was complete | Know when the delivery was completed |
| \* \* | User | Exchange reviews after a job | Provide my feedback based on the service provided|
| \* | Administrator | Warn or ban users who are irresponsible on the platform | Prevent abuse of the application |
| \* | User | Communicate with the other party | Keep in contact with the other party should there be any issues |
| \* | Sender | Edit a delivery job&#39;s details if it has not been accepted | Change the details should there be any mistakes |

_Note: all the low priority features (features that we deem non vital for normal use of the application), will be mentioned in the section [Future Extension]_ _(put a section link here in .md file__)_

## <a name="components"></a>4. Components
### <a name="main-components"></a>4.1 Main Components
Our web-application&#39;s frontend is made up of these main components:

- Landing Page
- About Page
- Dashboard
- Job Listings Page
- Jobs Accepted Page
- Jobs Posted Page
- Schedule Job Page
- User Information Page
- View Feedback Page

Below are some screenshots of the application:

Dashboard:

![](RackMultipart20200726-4-6pxwre_html_a7c2c8c2a79b2b0d.png)

Job Listing Page:

(Note: All pages with tables have expandable rows. Click on the job for the row to expand)

![](RackMultipart20200726-4-6pxwre_html_8696a003feb977a2.png)

Schedule Job Page:

![](RackMultipart20200726-4-6pxwre_html_3a3dad7018cd401b.png)

User Information:

![](RackMultipart20200726-4-6pxwre_html_41a0ebf8d7ddfcfe.png)

### <a name="features"></a>4.2 Features

A **Web-application** that supports three main features. The user will be able to view their information on the profile tab, including their jobs accepted, jobs posted. Secondly, the user will be able to view all the job listings and accept jobs that they want to take up. Lastly the user will be able to post jobs up for delivery.

#### <a name="milestone2-features"></a>**Features implemented in Milestone 2**

a. Login to account

- New User Sign Up
- Log out

b. User Profile

- User information
  - Displays user&#39;s name and email address
- Jobs Accepted:
  - Job History
    - List of all past jobs and its information
    - Filter search:
      - Parcel size (small/medium/large/extra large)
      - Pick up Location
      - Destination Location
      - Fragile?
    - Status: Completed
  - Ongoing Jobs
    - List of all jobs where parcel picked up and on the way
      - Button to mark the job as complete.
      - Status: On the Way
    - List of all jobs where parcel has not been picked up
      - Button to click when the parcel has been picked up.
      - Status: Accepted(not picked up)
    - Filter search:
      - Parcel size (small/medium/large/extra large)
      - Pick up Location
      - Destination Location
      - Fragile?
      - Status
      
- Jobs Posted:
  - Job History
    - List of all past jobs and its information
    - Filter search:
      - Parcel size (small/medium/large/extra large)
      - Pick up Location
      - Destination Location
      - Fragile?
    - Status: Completed
  - Ongoing Jobs
    - List of all jobs where parcel picked up and on the way
      - Status: On the Way
    - List of all jobs where parcel has not been picked up
      - Status: Accepted(not picked up)
    - Filter search:
      - Parcel size (small/medium/large/extra large)
      - Pick up Location
      - Destination Location
      - Fragile?
      - Status
  - Pending
    - List of all jobs that have not been accepted by a deliverer
    - Filter search:
      - Parcel size (small/medium/large/extra large)
      - Pick up Location
      - Destination Location
      - Fragile?

c. Job Listings

- A list of jobs available to be accepted
- Filter search:
  - Parcel size (small / medium / large / extra large)
  - Pick up Location
  - Destination Location
  - Fragile?

d. Schedule a new job

- A form to fill in the details of the job:
  - Parcel size (small/medium/large/extra large)
  - Pick up Location
  - Destination Location
  - Fragile?
  - Sender&#39;s information
  - Recipient&#39;s information
  - Comments
- Form validation (Required fields)

#### <a name="milestone3-features"></a>**Features completed in Milestone 3**

a. Integrating A Feedback And Rating System For Users:

- Users exchange feedback and provide ratings(From 1-5) for each other based on the job completed.
- Deliverers are able to view sender&#39;s past feedback and ratings before accepting the job and after they accept the job.
- Senders are able to view deliverer&#39;s past feedback and ratings once a deliverer has accepted their job.

b. Email confirmation:

- A confirmation email will be sent to the user when the delivery has been completed with the job details.
- See appendix A for more details about this feature

![](RackMultipart20200726-4-6pxwre_html_eefd4477c9e88462.png)

c. Dashboard:

- Welcomes the user by name.

- Displaying the current activity: number of jobs ongoing/pending etc.

d. Cancel Job:

- Senders are able to cancel their job if a deliverer has not accepted the job.

e. Additional Job details:

- Each Job&#39;s expanded row will contain more information.
- When deliverers accept a job they will be able to view sender&#39;s and recipient&#39;s name and contact numbers in Jobs Accepted.

![](RackMultipart20200726-4-6pxwre_html_b32165226ca42172.png)

- Senders will be able to view the deliverer&#39;s name and contact number once a deliverer has accepted the job under Jobs Posted.

![](RackMultipart20200726-4-6pxwre_html_1eb344f24d5ab8f9.png)

#### <a name="additional-features"></a>**Additional features implemented:**

a. Form Validation

- Implemented form validation in our schedule job form as well as in our Accept Job modal. Our form validation ensures that users have filled in all the required fields before they are able to submit the form. Additionally we made use of regex for certain fields like postal code and contact number to ensure that users key in the correct number of digits. Contact numbers must start with 6, 8 or 9.

Below are some screenshots:

Accept Job Modal contact number validation:

![](RackMultipart20200726-4-6pxwre_html_ea9faceaad527a7d.png)

Schedule Job Contact number and postal code validation.

![](RackMultipart20200726-4-6pxwre_html_58a8958ec3f5f835.png)

b. Responsive Design

Our application was styled with responsive react bootstrap components, hence our application is responsive and able to view on mobile devices.

![](RackMultipart20200726-4-6pxwre_html_2a21c1dfa155e613.png) ![](RackMultipart20200726-4-6pxwre_html_3d39bac0ec8be13e.png) ![](RackMultipart20200726-4-6pxwre_html_5f226617e8591593.png) ![](RackMultipart20200726-4-6pxwre_html_ab8bed69b9b9e451.png)

#### **Possible Future Implementations:**

1. Integrating Google Maps API for our Schedule Jobs form. This way users can just key in a keyword or the postal code and their address will be filled up
   - Implementation: [https://mamoonblog.wordpress.com/2012/01/17/get-address-by-postcodegoogle-geocoding-api/](https://mamoonblog.wordpress.com/2012/01/17/get-address-by-postcodegoogle-geocoding-api/)

2. Integrating our own user database to store information about a user. Currently our user data is managed by Auth0, by using our own user database we will be able to store more information about a user (ie contact number and address). This will allow us to extend more features like auto-filling their contact number and address when they are scheduling jobs.
   - Implementation: API call to user DB when user logs in. Checks if user is a new user, if new user

3. Notification alert when status of the job changes (eg. when a deliverer accepts a job, when a deliverer marks the job as complete, the deliverer left feedback for the sender etc.) This way users will be notified immediately on any updates to their jobs.
    - Implementation: eg. Look into Telegram API to send Telegram message as a notification

3. Payment System to give deliverers extra incentive when helping to deliver a parcel.

## 5. Architecture

### 5.1 Design Diagrams
**Entity diagram**

![](RackMultipart20200726-4-6pxwre_html_c94165b2d637ab05.jpg)

**UX Flowchart**

![](RackMultipart20200726-4-6pxwre_html_98cd7af00b97d041.jpg)

Link to higher definition flowchart:

[https://drive.google.com/file/d/105FR5FxnScB15wu7PLYDVwAzVQ5WjKyX/view?usp=sharing](https://drive.google.com/file/d/105FR5FxnScB15wu7PLYDVwAzVQ5WjKyX/view?usp=sharing)



### 5.2 Process

**1. Tech Stack**

Frontend User Interface (Client side):

- HTML/CSS/Javascript (Languages)
- React.JS (Library)

Backend (Server side):

- Python (Language)
- Flask (Python framework)
- MongoDB (Database)

Extras:

- Auth0 - for users to log in to the application and authentication
- GmailAPI - sends an email to the user when delivery is complete

**2. Backend API Documentation:**

[https://docs.google.com/document/d/1C6WGdDMYPHBBic84uD\_fXKpEUjGJFxsUaEzFwxNlIE8/edit?usp=sharing](https://docs.google.com/document/d/1C6WGdDMYPHBBic84uD_fXKpEUjGJFxsUaEzFwxNlIE8/edit?usp=sharing)

**3. Frontend Development:**

**Auth0:**

We decided to use Auth0&#39;s services as it can add authentication and authorization services to our application. Auth0 is flexible, secure and scalable. Auth0 is able to provide social connections to other social platforms like facebook, which can be implemented in the future.

**ReactJS**

We decided to use ReactJS because ReactJS is lightweight, and flexible.

We used npm package manager for JavaScript which is the default package manager for the JavaScript runtime environment Node.js. This allows us to specifically install dependencies required for our project.

Dependencies installed:

- &quot;@auth0/auth0-spa-js&quot;: &quot;^1.8.2&quot;
  - For login and authentication.
- &quot;axios&quot;: &quot;^0.19.2&quot;
  - To make API requests (CRUD functions).
- &quot;bootstrap&quot;: &quot;^4.5.0&quot;
  - CSS Framework for styling components.
- &quot;formik&quot;: &quot;^2.1.4&quot;
  - For creating forms.
- &quot;react-bootstrap&quot;: &quot;^1.0.1&quot;
  - ReactJS framework, with components prebuilt.
- &quot;react-bootstrap-table-next&quot;: &quot;^4.0.3&quot;
  - To implement a table component
- &quot;react-bootstrap-table2-filter&quot;: &quot;^1.3.3&quot;
  - To implement filter search function with react-bootstrap-table-next
- &quot;react-bootstrap-table2-paginator&quot;: &quot;^2.1.2&quot;
  - To implement pagination for react-bootstrap-table-next
- &quot;yup&quot;: &quot;^0.29.1&quot;
  - For validation(form input)

**Issues faced:**

Auth0:

We had trouble implementing the authorization with the backend to make API requests. Console was showing an error &quot;Uncaught (in promise)&quot; in react-auth0-spa.js, which was obtained from the Auth0 tutorial. This error was caused by including the API audience identifier in our auth\_config.json file. However it was strange that the error was gone after a day. We concluded that it could have been an issue with the server on Auth0&#39;s side.

**4. Backend Development:**

**Python Flask**

We chose to use Python for the backend for ease of future implementation with AI components for a recommendation engine for jobs. We are using Flask for its extensibility and flexibility and it is relatively lightweight compared to django.

**MongoDB**

We choose to change the database to mongoDB due to ease of use with Python and also flexibility of the documents stored.

Python Dependencies Installed:

- Flask
  - To create a backend server for the frontend to call
- Pymongo
  - Connection layer between flask server and MongoDB
- Python-jose-cryptodome
  - Decoding of JWT returned by Auth0
- See requirements.txt in the folder for packages version information

## 6. Dev Ops
### Deployment to remote machine(example using Heroku)

**Prerequisites:**

- git
- A Heroku Account
- A Mongo Atlas account
- Heroku CLI (install from: [https://devcenter.heroku.com/articles/heroku-cli](https://devcenter.heroku.com/articles/heroku-cli))


**Setting for up deployment:**

- Clone repository from [https://github.com/mechastriker3/SendIt.git](https://github.com/mechastriker3/SendIt.git)
- Directory Structure (blue = folder, white = files):
  - ![](RackMultipart20200726-4-6pxwre_html_bdd045760573e25d.png)
- To set up DB
  - Login to mongo atlas and create a cluster, inside the cluster create a database and inside the database create a collection called jobs
- To deploy the **backend** API service:
  - Open a terminal
  - cd into /backend directory
  - Run ```heroku login -i``` and login to your heroku account
  - Run ```heroku config:set DB_USERNAME=<your_db_username> DB_PASSWORD= <your_db_password> DB_NAME=<send_it CLUSTER\_URL=\&lt;your\_cluster\_url```
  - Cluster url highlighted in the example below ![](RackMultipart20200726-4-6pxwre_html_2a4487eb79f728d6.png)
  - Run heroku create \&lt;name\_of\_your\_backend\_API\&gt;
  -
  - Run git push heroku master
- To deploy the **frontend** UI:
  - cd into the /frontend directory
  - Run heroku create \&lt;name\_of\_your\_app\&gt; --buildpack mars/create-react-app
  - Run git push heroku master
  - Your app is now deployed!!

## 7. System testing:

**Basic Testing in Development:**

We did basic system testing by using 2 different google accounts to test our application. One account was of a sender and the other was of a deliverer.

The sender schedules the job and the job shows up in the job listing page as well as the jobs posted page and splits according to its status(pending/ongoing/history). We also tested to make sure that a sender cannot accept his own job(instead a cancel job button will be shown as seen in the screenshot below)

![](RackMultipart20200726-4-6pxwre_html_2c95aab6ace21b64.png)

As a deliverer, jobs viewed in the job listing page will have an accept job button in the job&#39;s expanded row as seen in the screenshot below:

![](RackMultipart20200726-4-6pxwre_html_7cc95a9bb5fec15a.png)

Once a job has been accepted we tested to make sure the status is changed correctly and shows up on the deliverer&#39;s jobs accepted page as well as the sender&#39;s jobs posted page(ongoing jobs tab). One status change will update the table for both the sender and the deliverer accordingly.

We also tested to ensure that users are able to leave feedback for one another once the job is complete.

**System testing in Mobile**

We tested to ensure that all components work properly in mobile and that all components are responsive.

However we encountered certain bugs in the mobile version.

1. Options are not displaying as select options in the leave feedback rating input as well as the select parcel size select input.

![](RackMultipart20200726-4-6pxwre_html_9d0f94acd1caff95.png)

This was rectified by correcting the option tag in these inputs.

1. Third party cookies bug in Safari. Users do not stay logged in when they are routed back to the dashboard. This causes users to be routed back to the landing page instead of the dashboard. Upon research Auth0 noted that this can happen when browsers like Safari block third party cookies.



## Appendix A
**Appendix A - Gmail API Integration:**

1. Before integration you will need an API credentials file from Google. Follow step one from this link and click on enable Gmail API. This will result in you getting a credentials.json file from Google.
2. Clear the folder backend/src/creds (relative to the root folder SendIt) and put the credentials.json file there.
3. Run the backend of the app, it should pop open a browser that will prompt you to log in to google. The account that you log in with here will be the account that will be used to send out the confirmation email.
4. This flow will only need to happen once. If you need to change the account used to send out the email, delete the token.pickle file in backend/src/creds and run the backend of the app again.
5. NOTE: This generation of creds should only be done in development and the creds folder should be securely stored in deployment with proper access permissions set.
