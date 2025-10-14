Dev Server

## Setup:

### Manual:
1. create ec2 instance (ubuntu, username: ubuntu)
2. install docker (official)
3. ssh in
4. git clone this repo into /home/ubuntu/dev-webserver
5. add user to docker group `sudo usermod -aG docker ubuntu`
6. re-log in
7. docker login
8. docker compose up

### Set up GitHub redeploy

1. ssh in
2. `ssh-keygen -t ed25519 -C "your_email@example.com"`
3. Copy pub key
4. In Github `Settings > Secrets and variables > Actions`:
5. Add `DEV_SERVER_SSH_KEY`, `DEV_SERVER_USERNAME`, `DEV_SERVER_HOST`
6. Add `DOCKER_ACCESS_TOKEN` (username: igornadj)


