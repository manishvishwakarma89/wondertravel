Setting up the Project
======================
1. Clone your forked repository.
```bash
git clone https://github.com/manishvishwa1989/wanderlust.git
2. Download the required dependecies
```bash
pip install -r requirements.txt
cd wanderlust
run npm i
3. Set up the database

curl -fsSL https://www.mongodb.org/static/pgp/server-8.0.asc | \
   sudo gpg -o /usr/share/keyrings/mongodb-server-8.0.gpg \
   --dearmor
echo "deb [ arch=amd64,arm64 signed-by=/usr/share/keyrings/mongodb-server-8.0.gpg ] https://repo.mongodb.org/apt/ubuntu noble/mongodb-org/8.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-8.2.list
https://www.mongodb.com/docs/manual/administration/install-community/?linux-distribution=ubuntu&linux-package=default&operating-system=linux&search-linux=with-search-linux#reload-the-package-database.-2
sudo apt-get update
sudo apt-get install -y mongodb-org
sudo systemctl start mongod
sudo systemctl enable mongod

4. Import Sample data

mongoimport --db wanderlust --collection posts --file ./data/sample_posts.json --jsonArray

5. Configure Environment variables
  cp .env.sample .env

6. Start Backend Server
  npm run
  npm start port: 5000

7. Setting up Frontend 

cd wondertravel/frontend
-npm i
- Configure environment variables
cp .env.sample .env.local

8. Start Frontend Server
npm start port: 5173
9. Open your browser and navigate to http://localhost:5173 to view the application.
