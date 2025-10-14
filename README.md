Dev Server

## Setup:

### Manual:
1. create ec2 instance
2. install docker (official)
3. ssh in
4. git clone this repo
5. docker login
6. sudo docker compose up

### Set up GitHub redeploy

1. ssh in
2. `ssh-keygen -t ed25519 -C "your_email@example.com"`
3. Copy pub key
4. In Github `Settings > Secrets and variables > Actions`:
5. Add `DEV_SERVER_SSH_KEY`, `DEV_SERVER_USERNAME`, `DEV_SERVER_HOST`


