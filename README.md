# Flask Docker CI Example

A simple Flask application with Docker and GitHub Actions CI.
This App makes use of a github action and has been tested and its working properly

## Project Structure

- `app.py`: Simple Flask application
- `test_app.py`: Tests for the Flask application
- `Dockerfile`: Docker configuration for containerizing the app
- `.github/workflows/docker-ci.yml`: GitHub Actions workflow for CI

## CI Pipeline

The CI pipeline performs the following steps:

1. Builds a Docker image from the Dockerfile
2. Runs pytest tests inside the Docker container
3. Starts the application container
4. Tests the running application with HTTP requests
5. Cleans up the container

## Local Development

### Build and Run with Docker

```bash
# Build the Docker image
docker build -t flask-app:local .

# Run the container
docker run -p 5000:5000 flask-app:local
```
![Screenshot](https://github.com/Omokehinde-hub/flask-docker-ci/blob/main/flask-app-ci.png)
