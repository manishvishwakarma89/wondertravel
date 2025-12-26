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
```bash
make sure install mongoDB and run it port 27017
Option 1: mongoimport
mongoimport --db wanderlust --collection posts --file ./data/sample_posts.json --jsonArray
4. Setup Redis
cp backend/.env.sample backend/.env && cp frontend/.env.sample frontend/.env.local
Make sure to set the correct Redis URL in backend/.env
5. Launch the development server with npm start in the root directory of the repository.
```bash
