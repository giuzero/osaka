# osaka

## Install go
```
wget https://golang.org/dl/go1.15.6.linux-amd64.tar.gz
sudo tar -C /usr/local -xzf go1.15.6.linux-amd64.tar.gz
```
Add `export PATH=$PATH:/usr/local/go/bin` in `/etc/profile`


## Install docker
```
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
sudo apt update
sudo apt install docker-ce
sudo usermod -aG docker ${USER}
sudo systemctl start docker
sudo systemctl enable docker
```

## Install docker-compose (1.27.4)
```
sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

# Install HLF2
```
curl -sSL https://bit.ly/2ysbOFE | bash -s
git clone https://github.com/hyperledger/fabric-samples.git
```
Export fabric-samples/bin