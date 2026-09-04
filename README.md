# RaceDay

## Project Overview

RaceDay is a full-stack web-based event management system designed specifically for the South African road running, walking, and cycling community.

The system is designed to make it easier for Event Organisers to manage events, categories, participant enrolments and results. Participants can use the platform to register, browse upcoming events, enrol in events and view their personal performance history.

The project is being developed progressively across multiple parts, following real-world software development practices.


## User Roles

### Participant

Participants can:

- Register and log in to the system.
- View and update their own profile.
- Browse available events.
- View event categories.
- Enrol in an event by selecting a category.
- View their own results and performance history.

### Organiser

Organisers can:

- Register and log in to the system.
- View and update their own profile.
- Create, update and delete events.
- Create and manage event categories.
- View enrolments for their events.
- Capture participant finishing times and finishing positions.



## Database

The RaceDay database is designed using Microsoft SQL Server and can be created and tested using SQL Server Management Studio (SSMS).

The current database model contains the following entities:

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

---

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
| POST | `/api/events/{eventId}/registrations` | Allows a participant to enrol in an event by selecting a category. |
| GET | `/api/events/{eventId}/registrations` | Allows an organiser to view enrolments for their event. |

### Results

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/registrations/{registrationId}/result` | Records a participant's finishing time and position. |
| GET | `/api/results/me` | Allows a participant to view their own results. |

---

## Project Documentation

The `/docs` folder contains the documentation required for the project.

The folder should contain:

- `RaceDay_ERD.png` or `RaceDay_ERD.pdf`
- `API_Endpoint_Plan.md` or PDF version
- `RaceDay_Section_C.sql`

---

## Database Setup

To create the RaceDay database:

1. Install Microsoft SQL Server and SQL Server Management Studio (SSMS).
2. Open SSMS and connect to your SQL Server instance.
3. Open the `RaceDay_Section_C.sql` script.
4. Execute the complete script.
5. The script creates the RaceDay database and its tables.
6. Sample data is inserted automatically.
7. The SELECT statements at the end of the script can be used to verify the data.

---

## Sample Data

The database contains sample data that satisfies the minimum requirements of the assignment:

- 2 Organisers
- 2 Participants
- 3 Events
- Categories for each Event
- Sample Enrolments
- Sample Results

---

## Repository Structure

```text
RaceDay/
│
├── docs/
│   ├── RaceDay_ERD.png
│   ├── API_Endpoint_Plan.md
│   └── RaceDay_Section_C.sql
│
├── README.md
│
└── [application source code]

