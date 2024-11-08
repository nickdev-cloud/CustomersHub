# CustomersHub

Install OpenSSH Server on your machine for connecting
sudo apt update sudo apt install -y openssh-server

sudo service ssh start

Setup FrontEndServer - Ubuntu 22.04
Install NodeJS and NPM
sudo apt update

curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash - sudo apt install -y nodejs

verify node installation

node -v npm -v

Install Git (if not already installed)
sudo apt install git

verify git installation

git --version

Clone the repository
git clone https://github.com/nickdev-cloud/CustomerHub

Install NPM Packages - FrontEnd
cd frontend

npm install @mui/material @emotion/react @emotion/styled react-router-dom @types/react-router-dom sass @mui/icons-material

Start the FrontEndServer
npm start

Setup BackEndServer - Ubuntu 22.04
mkdir backend cd backend

Initialize NodeJS Project npm init -y

Install Express npm install express npm install --save-dev typescript ts-node @types/node @types/express

initialize typescript config npx tsc --init

Install Prisma ORM npm install prisma --save-dev npm install @prisma/client npx prisma init

Install Additional NPM Dependencies npm install bcryptjs jsonwebtoken npm install --save-dev @types/bcryptjs @types/jsonwebtoken dotenv cors

Set Prisma to use MariaDB (RDS, On-Premise,etc.) Edit the prisma/schema.prisma file to use your MariaDB connection string

Set the .env file in prisma directory to use your MariaDB credentials mysql://USER:PASSWORD@HOST:PORT/DATABASE

Run Prisma Migrations npx prisma migrate dev --name init

Test the BackEndServer DB Connection npx prisma db pull

Start the BackEndServer npm start
