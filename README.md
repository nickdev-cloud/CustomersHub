# CustomersHub


## Install OpenSSH Server on your machine for connecting

sudo apt update
sudo apt install -y openssh-server

sudo service ssh start

## Setup FrontEndServer - Ubuntu 22.04


1. Install NodeJS and NPM

sudo apt update

curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt install -y nodejs

verify node installation

node -v
npm -v


2. Install Git (if not already installed)

sudo apt install git

verify git installation

git --version

3. Clone the repository

git clone https://github.com/nickdev-cloud/CustomerHub

4. Install NPM Packages - FrontEnd

cd frontend

npm install @mui/material @emotion/react @emotion/styled react-router-dom @types/react-router-dom sass @mui/icons-material

5. Start the FrontEndServer

npm start

## Setup BackEndServer - Ubuntu 22.04

mkdir backend
cd backend
1. Initialize NodeJS Project
npm init -y

2. Install Express
npm install express
npm install --save-dev typescript ts-node @types/node @types/express

3. initialize typescript config
npx tsc --init

4. Install Prisma ORM
npm install prisma --save-dev
npm install @prisma/client
npx prisma init

5. Install Additional NPM Dependencies
npm install bcryptjs jsonwebtoken
npm install --save-dev @types/bcryptjs @types/jsonwebtoken dotenv cors

6. Set Prisma to use MariaDB (RDS, On-Premise,etc.)
Edit the prisma/schema.prisma file to use your MariaDB connection string

7. Set the .env file in prisma directory to use your MariaDB credentials
mysql://USER:PASSWORD@HOST:PORT/DATABASE

8. Run Prisma Migrations
npx prisma migrate dev --name init

9. Test the BackEndServer DB Connection
npx prisma db pull

10. Start the BackEndServer
npm start


