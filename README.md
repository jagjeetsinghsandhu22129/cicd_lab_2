Express.js CI/CD Pipeline Project
Repository Structure
bash
Copy code
/.github/workflows/ci.yml  # GitHub Actions CI pipeline definition
/Dockerfile                # Dockerfile to build the application image
/package.json              # Project metadata and dependencies
/index.js                  # Main Express.js application
Instructions to Build and Run the Application
Clone the repository:

bash
Copy code
git clone https://github.com/your-username/your-repo.git
cd your-repo
Install dependencies: Run the following command to install the required Node.js modules:

bash
Copy code
npm install
Run the application locally: Start the application using:

bash
Copy code
npm start
The server will start on http://localhost:8080 by default.

Steps to Test the CI Pipeline
Trigger the CI Pipeline:

Every push or pull request to the main branch will trigger the CI pipeline defined in .github/workflows/ci.yml.
Check Build & Test Results:

GitHub Actions will automatically run the following steps:
Install dependencies (npm install)
Run unit tests (npm test)
Build a Docker image
Push the Docker image to Docker Hub
To verify the results, check the "Actions" tab in your GitHub repository.
Pulling the Docker Image from the Registry
Log in to Docker Hub: Make sure you are logged in to Docker Hub:

bash
Copy code
docker login
Pull the Docker image: You can pull the latest version of the Docker image from Docker Hub with the following command:

bash
Copy code
docker pull jaggi22129/nodeapp:latest
Run the Docker container: Once the image is pulled, you can run it using:

bash
Copy code
docker run -p 8080:8080 jaggi22129/nodeapp:latest
The application will be accessible at http://localhost:8080.
