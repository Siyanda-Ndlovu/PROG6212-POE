# RaceDay

## Project Overview

RaceDay is a full-stack web-based event management system designed for the South African road running, walking and cycling community.

The system allows event organisers to manage events, categories, participant enrolments and race results. Participants can register, log in, browse upcoming events, enrol in events and view their personal performance history.

RaceDay aims to make event management more organised, efficient and accessible by bringing important event information and activities into one system.

## User Roles

### Participant

Participants can:

- Register and log in to the system.
- View and update their profile.
- Browse upcoming events.
- View event categories.
- Enrol in an event by selecting a category.
- View their personal results and performance history.

### Organiser

Organisers can:

- Register and log in to the system.
- View and update their profile.
- Create, update and delete events.
- Create and manage event categories.
- View participant enrolments for their events.
- Capture participant finishing times and finishing positions.

## CI/CD Pipeline

The RaceDay project uses a CI/CD pipeline to automate the process of building, testing and deploying the application. This helps ensure that changes made to the project are checked and integrated consistently.

The screenshot below shows the CI/CD pipeline used for the RaceDay project.

![RaceDay CI/CD Pipeline](docs/ci-cd-pipeline.png)

## YouTube Demonstration

The YouTube video demonstrates the main features and functionality of the RaceDay system.

[Watch the RaceDay System Demonstration on YouTube](https://youtu.be/PpDs1l_wEtg?si=pg5pXyjUv_zTDCap)

## Database

The RaceDay database is designed using Microsoft SQL Server and can be created and tested using SQL Server Management Studio (SSMS).

The database contains the following entities:

- Account
- Participant
- Organiser
- Event
- Category
- Enrolment
- Result

The database script is located in:

`/docs/RaceDay_Section_C.sql`

The SQL script includes:

- Database and table creation.
- Primary keys.
- Foreign keys.
- NOT NULL constraints.
- UNIQUE constraints.
- DEFAULT constraints.
- Sample organisers.
- Sample participants.
- Three sample events.
- Categories for the events.
- Sample enrolments.
- Sample results.
- Verification queries.

## API Endpoint Plan

The API is planned around the main functional requirements of the RaceDay system.

### Authentication

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Register a new user. |
| POST | `/api/auth/login` | Authenticate a registered user. |

### User Profile

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/profile` | View the logged-in user's profile. |
| PUT | `/api/profile` | Update the logged-in user's profile. |

### Events

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/events` | View available events. |
| GET | `/api/events/{id}` | View a specific event. |
| POST | `/api/events` | Create an event. |
| PUT | `/api/events/{id}` | Update an event. |
| DELETE | `/api/events/{id}` | Delete an event. |

### Categories

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/events/{eventId}/categories` | View categories for an event. |
| POST | `/api/events/{eventId}/categories` | Create a category for an event. |
| PUT | `/api/categories/{id}` | Update a category. |
| DELETE | `/api/categories/{id}` | Delete a category. |

### Event Enrolments

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/events/{eventId}/registrations` | Enrol in an event by selecting a category. |
| GET | `/api/events/{eventId}/registrations` | View enrolments for an event. |

### Results

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/registrations/{registrationId}/result` | Record a participant's finishing time and position. |
| GET | `/api/results/me` | View the logged-in participant's results. |

## Project Documentation

The `/docs` folder contains the documentation required for the project.

The folder should contain:

- `RaceDay_ERD.png` or `RaceDay_ERD.pdf`
- `API_Endpoint_Plan.md` or a PDF version
- `RaceDay_Section_C.sql`
- `ci-cd-pipeline.png`

## Database Setup

To create the RaceDay database:

1. Open SQL Server Management Studio (SSMS).
2. Open `RaceDay_Section_C.sql`.
3. Connect to a SQL Server instance.
4. Run the complete script.
5. The script creates the RaceDay database and its tables.
6. Sample data is inserted automatically.
7. The SELECT statements at the end of the script can be used to verify the data.

## Sample Data

The database contains sample data that satisfies the minimum requirements of the assignment:

- 2 Organisers
- 2 Participants
- 3 Events
- Categories for each event
- Sample enrolments
- Sample results

## Development Approach

RaceDay is being developed progressively. The database design and API endpoint plan are prepared before implementation to ensure that the database, API and application functionality remain consistent.

The ERD, SQL database script and API implementation should be kept aligned throughout development.

Any deliberate difference between the approved plan and the final implementation should be explained in this README.

## Technologies

The database component uses:

- Microsoft SQL Server
- SQL Server Management Studio (SSMS)

The technologies used for the API and front end will follow the requirements specified for the relevant project part.

## Project Status

**Current stage:** Database design, API planning and application development.
