# linux docker

# ubuntu
## add apt repository
```
# Add Docker's official GPG key:
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "${UBUNTU_CODENAME:-$VERSION_CODENAME}") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
## install docker
`sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin`
## verify
`sudo docker run hello-world`
## manage docker as a non-root user [optional]
```
sudo groupadd docker
sudo usermod -aG docker $USER
# log-out and log back in
docker run hello-world
```
## config docker to start on boot
```
sudo systemctl enable docker.service
sudo systemctl enable containerd.service
```
## to disable auto start on boot
```
sudo systemctl disable docker.service
sudo systemctl disable containerd.service
```
