# poc-1

Here's the `README.md` file with proper formatting:  

```md
# Docker Installation Guide

Follow the steps below to install Docker on an Ubuntu system.

## Step 1: Update Package List and Install Dependencies

```sh
sudo apt update
sudo apt install -y ca-certificates curl gnupg
```

## Step 2: Add Docker’s Official GPG Key

```sh
sudo install -m 0755 -d /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo tee /etc/apt/keyrings/docker.asc > /dev/null
sudo chmod a+r /etc/apt/keyrings/docker.asc
```

## Step 3: Add Docker Repository

```sh
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
```

## Step 4: Install Docker Engine

```sh
sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

## Step 5: Add User to Docker Group (Optional)

To use Docker without `sudo`, add your user to the `docker` group:

```sh
sudo usermod -aG docker $USER
newgrp docker
```

Now, Docker is installed and ready to use on your system! 🚀
```

This README file is structured, easy to read, and follows markdown conventions. Let me know if you need modifications! 😊
