# Flask Application with Docker and Kubernetes Deployment

This repository contains a simple Flask web application with Docker containerization and Kubernetes deployment configurations.

## Project Structure
```
app/
├── app.py              # Flask application
├── requirements.txt    # Python dependencies
├── Dockerfile         # Docker configuration
├── k8s-deployment.yaml # Kubernetes deployment manifest
├── static/
│   └── style.css     # Application styling
└── templates/
    ├── index.html    # Home page template
    └── about.html    # About page template
```

## Setup and Deployment

### Local Development
1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Run the application:
```bash
python app.py
```

### Docker Deployment
1. Build the Docker image:
```bash
docker build -t purvashinde21/flask-app:latest .
```

2. Run the container:
```bash
docker run -p 5000:5000 purvashinde21/flask-app:latest
```

### Kubernetes Deployment (Minikube)
1. Start Minikube:
```bash
minikube start --driver=docker
```

2. Apply the Kubernetes manifests:
```bash
kubectl apply -f k8s-deployment.yaml
```

3. Access the application:
```bash
minikube service flask-service
```

## Docker Hub Repository
The Docker image is available at: `purvashinde21/flask-app:latest`