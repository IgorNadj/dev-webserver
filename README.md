Dev Server

## Setup:

### Manual:
1. create ec2 instance 
   1. (ubuntu, username: ubuntu)
   2. install docker (official)
   3. git clone this repo into /home/ubuntu/dev-webserver
   4. add user to docker group `sudo usermod -aG docker ubuntu`
   5. re-log in
   6. docker login
   7. docker compose up


### Set up GitHub redeploy

1. In Docker Hub
   1. Generate an Access Token
   2. Add it to ~/.docker-hub-secret
2. ssh in
   1. `ssh-keygen -t ed25519 -C "your_email@example.com"`
   2. Copy pub key
3. In Github `Settings > Secrets and variables > Actions`:
   1. Add `DEV_SERVER_SSH_KEY`
   2. Set up GHA ssh redeploy workflow

## Run

- dev: `docker compose -f docker-compose.yml -f docker-compose.dev.yml up`
- prod: `docker compose -f docker-compose.yml -f docker-compose.prod.yml up -d` 

Then view the traefik dashboard at: `http://<public ip>:8080/`
