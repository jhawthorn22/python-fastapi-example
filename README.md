# Hackathon ArgoCD Python FastApi Example



## Requirements
You will need the following installed to follow this example:
- Docker
- Python 3.9



## Python Fast Api
Links:
- https://fastapi.tiangolo.com/deployment/docker/
- https://levelup.gitconnected.com/getting-started-with-argocd-on-your-kubernetes-cluster-552ca5d8cf41



### Build Docker Image and Run Locally
```bash
docker build -t argocd-python-fastapi:latest .
docker run -d --name argocd-python-fastapi -p 80:80 argocd-python-fastapi:latest

# NOTE: You can access swagger at localhost/docs or localhost/redocs once container is running
```



### Push Docker Image to Docker Hub
```bash
docker login

# List local images
docker images

# Tag with docker hub username and push
docker tag argocd-python-fastapi jhawthorn22/argocd-python-fastapi:1.0.0
docker push jhawthorn22/argocd-python-fastapi:1.0.0
```
