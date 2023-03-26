# Ubuntu new instance
It is a guide for anyone that just installed fresh Ubuntu OS and now wanted to start web development with php.

## Installing required dependencies

`sudo apt update`

`sudo apt upgrade`

`sudo apt install  ca-certificates apt-transport-https software-properties-common`

## Install git

Most likely git il already installed on your Ubuntu OS.
To check this out type:

`git --version`

If it is not, just install it through snap package

`sudo apt install git`

## Installing PhpStorm
The most easy way to install PhpStorm IDE is ti use snap package.

`sudo snap install phpstorm --classic`

To run PhpStorm type 
`phpstorm` in the terminal

## Install PHP

`sudo apt install --no-install-recommends php(ver)`

Check if the php installed

`php -v`

### Install PHP extension

`sudo apt install php8.1-common php8.1-mysql php8.1-xml php8.1-xmlrpc php8.1-curl php8.1-gd php8.1-imagick php8.1-cli php8.1-dev php8.1-imap php8.1-mbstring php8.1-opcache php8.1-soap php8.1-zip php8.1-redis php8.1-intl -y`

## Install docker
1. Update the apt package index and install packages to allow apt to use a repository over HTTPS:

`sudo apt-get update`

`sudo apt-get install \
ca-certificates \
curl \
gnupg`

2. Add Docker’s official GPG key:

`sudo mkdir -m 0755 -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg`

3. Use the following command to set up the repository:


`echo \
"deb [arch="$(dpkg --print-architecture)" signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu \
"$(. /etc/os-release && echo "$VERSION_CODENAME")" stable" | \
sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`

4. Install Docker Engine

`sudo apt-get update`

`sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin`

5. Verify that the Docker Engine installation is successful by running the hello-world image:

`sudo docker run hello-world`
