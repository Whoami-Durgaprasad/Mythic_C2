# Mythic_C2 Installation Process 

sudo apt update && sudo apt install -y \
    docker.io \
    docker-compose \
    git \
    python3 \
    python3-pip
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker $USER
newgrp docker  # or log out and log back in
git clone https://github.com/its-a-feature/Mythic.git
cd Mythic
make
./mythic-cli install
./mythic-cli start

# To know username and password try below command 
cat .env

# Look for below lines
\
MYTHIC_ADMIN_PASSWORD="v6oqC9PmNBbjwwnh13gr4DeEHa5CFW"

MYTHIC_ADMIN_USER="mythic_admin"

