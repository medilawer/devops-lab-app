# DevOps Activity 03

Minimal Flask service containerized with python:3.10-slim and tested through GitHub Actions.

```bash
docker build -t devops-flask-app:v1.0 .
docker run -d -p 5000:5000 --name flask-container devops-flask-app:v1.0
```

Open http://localhost:5000. The CI workflow runs on pushes to main and pull requests targeting main. It builds the image, starts a container, checks HTTP readiness and the welcome message, and cleans up afterward.
