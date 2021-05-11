# Install percona - toolkit 

## Walkthrough (Ubuntu 20.04) 

```
# Howto 
# https://www.percona.com/doc/percona-toolkit/LATEST/installation.html

# Step 1: repo installieren mit deb -paket 
wget https://repo.percona.com/apt/percona-release_latest.focal_all.deb
apt update 
apt install -y curl 
dpkg -i percona-release_latest.focal_all.deb
apt update
apt install -y percona-toolkit 
```

## Walkthrough (Debian 10) 

```
sudo apt update
sudo apt install -y wget gnupg2 lsb-release curl
cd /usr/src 
wget https://repo.percona.com/apt/percona-release_latest.generic_all.deb
dpkg -i percona-release_latest.generic_all.deb
apt update
apt install -y percona-toolkit 
```

```
sudo apt update; sudo apt install -y wget gnupg2 lsb-release curl; cd /usr/src; wget https://repo.percona.com/apt/percona-release_latest.generic_all.deb; dpkg -i percona-release_latest.generic_all.deb; apt update; apt install -y percona-toolkit 
```
