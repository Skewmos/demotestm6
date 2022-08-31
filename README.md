## Installation

demotestm6 fonctionne avec docker il vous faudra donc vous munir de [docker](https://www.docker.com/)

**Pour Windows :**

Suivre les indications [suivantes](https://docs.docker.com/docker-for-windows/install/)

**Pour linux :**

```bash
sudo apt update -y & sudo apt upgrade -y
sudo apt-get install  curl apt-transport-https ca-certificates software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt update
sudo apt install docker-ce
```

**Pour Mac :**

Suivre les indications [suivantes](https://docs.docker.com/docker-for-mac/install/)

# Mettre en place

**1. Cloner le repository**

`https://github.com/Skewmos/demotestm6.git  && cd demotestm6`

**2. Construisez le conteneur**

`cd .docker && docker-compose up -d`

**3. Installer les packages**

`docker exec -ti (nom ou id du container) bash`

`composer install`
