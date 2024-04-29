![web-app](https://github.com/gthell/sfaff-management-web-app/actions/workflows/8873898964.yml/badge.svg)

# Staff Management Application

For simplicity, the application is divided into two parts: the [backend](https://github.com/GTHell/staff-management-backend) and the [frontend](https://github.com/GTHell/staff-management-web-app).

## Table of Contents

- [Staff Management Application](#staff-management-application)
  - [Table of Contents](#table-of-contents)
  - [Features](#features)
  - [Technologies Used](#technologies-used)
  - [Installation](#installation)
    - [Backend](#backend)
    - [Frontend](#frontend)
  - [Usage](#usage)
  - [Testing](#testing)
  - [Continuous Integration](#continuous-integration)

## Features

- Staff management: Add, edit, delete, and search staff records.
- Advanced search: Search for staff members using staff ID, gender, and birthday range.
- Reports: Generate reports in Excel or PDF format based on the search results.

## Technologies Used

- **Backend**: ASP.NET Web API, C#
- **Frontend**: Vue.js
- **Unit Testing**: Xunit
- **Integration Testing**: Xunit with ASP.NET TestHost
- **End-to-End Testing**: Cypress
- **Version Control**: Git, GitHub
- **Continuous Integration**: GitHub Actions
- **Database**: SQLite

## Installation

### Backend

1. Clone the GitHub repository:

   ```shell
   git clone https://github.com/GTHell/staff-management-backend.git
   ```

2. Install the dependencies:

   ```shell
   cd staff-management-backend/StaffManagement.Service
   dotnet restore
   ```

### Frontend

1. Clone the GitHub repository:

   ```shell
   git clone https://github.com/GTHell/staff-management-web-app.git
   ```

2. Install the dependencies:

   ```shell
   cd staff-management-web-app
   npm install
   ```

## Usage

1. Start the backend server. Open a terminal in the backend folder and run the following command:

   ```shell
   dotnet run
   ```

   The backend server will start running on `http://localhost:8000`.

2. Start the frontend development server. Open a terminal in the frontend folder and run the following command:

   ```shell
   npm run serve
   ```

   The frontend development server will start running on `http://localhost:5173`.

## Testing

- **Unit tests**: The unit tests are implemented using Xunit. To run the unit tests:

  ```shell
  dotnet test
  ```

- **Integration tests**: The integration tests are also implemented using Xunit with ASP.NET TestHost. To run the integration tests:

  ```shell
  dotnet test --filter Category=Integration
  ```

- **End-to-End tests**: The end-to-end tests are implemented using Cypress. To run the end-to-end tests, ensure that the backend and frontend servers are running:

  ```shell
  npm run test:e2e
  ```

  To run with the Cypress GUI:

  ```shell
  npm run test:e2e:dev
  ```

## Continuous Integration

Continuous Integration (CI) is set up using GitHub Actions. The CI workflow is triggered on every push to the repository and includes the following steps:

1. Install dependencies for backend and frontend.
2. Run unit tests.
3. Build the backend and frontend code.
