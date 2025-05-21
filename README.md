# Ansible_task
# Ansible Docker Deploy Project

This project automates the deployment of a Dockerized Python Flask web application on a remote Ubuntu server using Ansible.

---

## 🔧 What It Does

- Installs Docker using the official Docker script
- Adds the user to the Docker group
- Copies a simple Flask app and Dockerfile to the server
- Builds the Docker image
- Runs the app inside a container on port `5000`

---

## 📁 Project Structure
ansible_docker_deploy/
├── inventory # Ansible inventory file with server IP and SSH key
├── playbook.yml # Main Ansible playbook
├── app/
│ ├── app.py # Simple Flask app
│ └── Dockerfile # Dockerfile to containerize the app


---

## 🚀 How to Use

### 1. Clone the repo

```bash
git clone https://github.com/your-username/ansible-docker-deploy.git
cd ansible-docker-deploy

2.Update the inventory file
Add your server's public IP and SSH key path
[web]
your.server.ip ansible_user=ubuntu ansible_ssh_private_key_file=~/.ssh/your_key.pem


3. Install required Ansible collection
bash
Copy
Edit
ansible-galaxy collection install community.docker


4. Run the playbook
bash
Copy
Edit
ansible-playbook -i inventory playbook.yml


Access the App
After the playbook runs, open your browser:
http://your.server.ip:5000
