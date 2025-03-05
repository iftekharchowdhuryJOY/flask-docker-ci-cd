# 🚀 Flask Docker CI/CD Pipeline with GitHub Actions

This project is a **Flask application** containerized using **Docker** and automated with **GitHub Actions** for Continuous Integration and Deployment (CI/CD). The pipeline builds a Docker image and pushes it to **Docker Hub** every time code is pushed to the `main` branch.

---

## 📌 Features
✅ **Flask Web Application** – A simple Python-based web app.  
✅ **Dockerized** – Packaged inside a Docker container.  
✅ **CI/CD with GitHub Actions** – Automates build and push to **Docker Hub**.  
✅ **Cloud Deployable** – Can be deployed on **AWS, Azure, DigitalOcean, or Kubernetes**.  

---

## 🚀 **Getting Started**

### **1️⃣ Clone the Repository**
```bash
git clone https://github.com/your-username/flask-docker-ci-cd.git
cd flask-docker-ci-cd
flask-docker-ci-cd/
│── .github/workflows/docker-ci.yml   # GitHub Actions workflow
│── app.py                            # Flask application
│── requirements.txt                   # Python dependencies
│── Dockerfile                         # Docker build instructions
│── README.md                          # Project documentation

Running Locally with Docker
docker build -t flask-app .
docker run -p 5000:5000 flask-app
http://localhost:5000/
```
## 🔄 GitHub Actions CI/CD Pipeline
This project uses GitHub Actions for automated Docker builds and deployments.

## How It Works
1. Triggers when code is pushed to the main branch.
2. Builds the Docker image inside a GitHub-hosted runner.
3. Logs into Docker Hub using stored secrets.
4. Pushes the image to Docker Hub with the latest tag.

🔑 Setting Up GitHub Secrets
To allow GitHub Actions to push images to Docker Hub, follow these steps:

```bash
Go to GitHub → Repository → Settings → Secrets and Variables → Actions.
Click New repository secret.
Add the following secrets:
DOCKER_USERNAME → Your Docker Hub username.
DOCKER_PASSWORD → Your Docker Hub password.
```
Now, GitHub Actions will authenticate with Docker Hub automatically.

## 🛠 Troubleshooting
If GitHub Actions workflow is stuck in "Queued" or "Waiting for a runner":

* Wait a few minutes (GitHub runners can be busy).
* Check GitHub Status.
Try canceling the job and pushing a new commit:
```
git commit --allow-empty -m "Retry CI/CD"
git push origin main
```
## 📝 License
This project is MIT licensed – feel free to modify and use it.
