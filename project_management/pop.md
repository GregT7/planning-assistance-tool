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
the data entries to the Notion API to sync my plan with my daily management app. Depending on the distribution of card statuses, the button will be some shade of green, yellow, or red to indicate the feasibility of the project.


### 3.2 Backend


### 3.3 Database

### 3.4 Task Duration Predictor

### 3.5 Docker Containerization


## 4. Predicted Architecture

## 5. Architecture Justification

## 6. Predicted Life Cycle/Methodology

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
