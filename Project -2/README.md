# Atlas-Core CI/CD Pipeline

## Project Overview

Atlas-Core is a simple Node.js project with an automated CI/CD pipeline using GitHub Actions.

The pipeline automatically checks the project whenever code is pushed to the `main` branch or when a pull request is created.

## Technologies Used

* Node.js
* npm
* JavaScript
* Git
* GitHub
* GitHub Actions
* YAML

## Project Structure

```text
Project -2/
│
├── .github/
│   └── workflows/
│       └── ci-cd.yml
│
├── src/
│   └── app.js
│
├── package.json
├── package-lock.json
├── test.js
└── README.md
```

## CI/CD Pipeline Steps

The GitHub Actions workflow performs the following steps:

### 1. Checkout Repository Code

The workflow gets the latest project code from the GitHub repository.

### 2. Set Up Node.js

Node.js version 20 is installed and configured for the project.

### 3. Install Dependencies

The workflow uses:

```bash
npm ci
```

to install the project dependencies.

### 4. Run Tests

The workflow runs:

```bash
npm test
```

to check whether the project tests are successful.

### 5. Build Project

The workflow runs:

```bash
npm run build --if-present
```

to build the project when a build script is available.

### 6. Upload Artifact

The workflow creates an artifact named:

```text
atlas-distribution
```

The artifact contains the `src` folder and `package.json`.

## How to Run the Project Locally

Open the terminal inside the project folder.

Install dependencies:

```bash
npm install
```

Run the tests:

```bash
npm test
```

Run the build:

```bash
npm run build
```

Run the application:

```bash
node src/app.js
```

## Expected Output

When the application is run:

```text
Atlas-Core application is running
```

When the tests are run:

```text
Atlas-Core tests passed successfully
```

When the build is run:

```text
Build completed successfully
```

## GitHub Actions

The CI/CD workflow is stored in:

```text
.github/workflows/ci-cd.yml
```

The workflow runs automatically for:

* Pushes to `main`
* Pull requests to `main`

## Benefits

* Automates testing
* Automates the build process
* Detects errors early
* Provides a consistent environment
* Stores project artifacts
* Reduces manual work

## Conclusion

This project demonstrates a basic CI/CD pipeline for a Node.js application using GitHub Actions. It automatically installs dependencies, runs tests, builds the project, and uploads the required files as an artifact.
