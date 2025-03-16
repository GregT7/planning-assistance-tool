# Project Overview Proposal

## 1. Proposed Project Name
Planning Assistance Tool

## 2. Elevator Pitch
Making plans and goals for the week is a necessity for steering my life in a direction that I want to go. However,
my proclivity for overestimating my capabilities and underestimating task durations causes me devise unfeasible plans.
Jumping from one plan to another without ever completing one is a big morale killer and time waster. For these reasons, I want to devise a planning tool that will help me evaluate the feasibility of my goals while saving me time in the process. Predictions will be limited to school related tasks. 

## 3. Complexity of the Project
### 3.1 Frontend
The user will input data into a table that mimics Notion's "database" component. There will be cards corresponding to the days
of the week that show the task duration sum of the currently existing entries in the database and the predicted allowable time limit
range. These time ranges will be calculated specific to each day of the week. The cards will be colored green if the current time sum is within range, yellow if it's under range, and red if it exceeds the range. At the bottom of the screen, there will be a button that will send
the data entries to the Notion API to sync my plan with my daily management app. Depending on the distribution of card statuses, the button will be some shade of green, yellow, or red to indicate the feasibility of the project. Technologies: React, Tailwind CSS

### 3.2 Backend
The backend will handle database requests and fetches for updating the ml prediction model, load the model, make time prediction calculations, post newly generated tasks to Notion through its API, and handle security for Notion and mongoDB Atlas API access. Lastly, some settings will be stored locally that will determine things like the allowable time ranges for each day of the week. Technologies: Flask, Notion API

### 3.3 Database
The database will store all of my productivity related information where I document my everyday tasks. The data stored here will be used to train the machine learning model. If any updates in the database is detected, the database will be queried to retrain the predictive model. Technologies: MongoDB Atlas

### 3.4 Task Duration Predictor
The machine learning model will be used to predict the time duration for the following school related tasks: labs, projects, homework assignments, quizzes, and exams. Models will be trained once and stored locally with periodic training updates.
Technologies: Scikit-learn

### 3.5 Deployment
The application will be easy to install and setup through docker's environment maintainability functionality.
Technologies: Docker

## 4. Predicted Architecture
![Image](https://github.com/user-attachments/assets/ca6d4d34-1df7-42ac-aec5-58fa37fbf683)
### 4.1 Frontend
Tailwind CSS will be used for a responsive and nicely styled web application. React will be used to handle flask API exchanges and for dynamically updating the web page.

### 4.2 Backend
Flask will be used to load the predictive model, query the database for new data, initiate model retraining, send task data to Notion API, making time prediction calculations, initializing setting values for day specific time ranges, and sending prediction data to the React app.

### 4.3 Database
MongoDB atlas will be used because it's cloud data management eliminates the need to launch or run a database every time I want to boot my application. Additionally, it's free subscription plan provides more than enough memory for my purposes - roughly 2200 rows with 10 columns of data doesn't take up a lot of space. Lastly, this service/technology allows for easier app integration if I decide to expand on this project in the future.

### 4.4 Task Duration Predictor
Scikit-learn will be used for training the model because its ease of use.

### 4.5 Deployment
Docker will be used as a simple form of deploy to help with environment consistency.

## 5. Architecture Justification
- **Tailwind CSS:** provides responsive and nice styling for web applications.
- **React:** popular framework, strong community support, good documentation
- **MongoDB Atlas:** cloud data management eliminates the need to launch or run a database every time the application is booted, free subscription plan with ample memory for application, offers easier app integration for future improvements.
- **Flask:** loads the predictive model, queries the database for new data, initiates model retraining, sends task data to Notion API, makes time prediction calculations, initializes setting values for day specific time ranges, and sends prediction data to the React app.
- **Scikit-learn:** trains the model, good documentation and project examples, high ease of use
- **Docker:** offers consistency and portability, simplifies deployment and ongoing management

## 6. Predicted Life Cycle/Methodology
Feature-driven development is the best fit for the software development methodology of our project. FDD caters towards our experience levels. We don’t have in depth experience in creating full-stack projects and want to apply a method that ensures individual features work before progressing. Moreover, with this methodology the simpler features can be targeted early to cultivate confidence and an efficient group dynamic while satisfying the FDD construct. This project has already started using this framework by briefly conceptualizing an overall model with an accompanying feature list, granting us some momentum. Because we need flexibility in the initial stages of development FDD is the best methodology for us.

## 7. Notes
Over the past year and a half, I've been collecting data for a variety of different tasks. One of the metrics collected is task duration
which is vital in considering when making plans for the week. More importantly, when grouped together, the amount of time spent planning per
week can be summed, providing baseline metrics for future comparisons. This will allow for me to objectively determine the efficacy of the planning tool in regards to time reduction. The following stats were calculated on a dataset spanning from 8/14/2023 to 3/9/2025
* 43 weeks / 82 weeks included a plan
* task duration
  * average = 66 mins
  * median = 50 mins
  * standard deviation = 52.5 mins
  * min = 6 mins
  * max = 216 mins
