# aws-python-deployment-demo
50
# Python Deployment Demo

This project demonstrates automated deployment of a Python application to an AWS EC2 instance using GitHub Actions.

## Workflow

On every push to the `main` branch, GitHub Actions:

* Checks out the repository
* Sets up Python 3.13
* Installs dependencies from `requirements.txt`
* Runs `deploy.py`
* Connects to the EC2 instance via SSH
* Pulls the latest code
* Starts the application using `python3 app.py`

## Required GitHub Secrets

* `EC2_HOST` – EC2 public IP or hostname
* `EC2_USERNAME` – SSH username
* `PRIVATE_KEY` – SSH private key for the EC2 instance
