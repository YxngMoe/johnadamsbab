Open the terminal window in Apporto to access the Linux shell.
Navigate to the directory containing the AAC Outcomes CSV file:
bash
Copy code
**cd /usr/local/datasets/**


Use mongoimport to import the CSV file into MongoDB with the specified database and collection names:
bash
Copy code
**mongoimport --db AAC --collection animals --type csv --headerline --file aac_shelter_outcomes.csv**


Take screenshots of the import command and its execution.
Step 2: Creating a Simple Index on "breed"
Open the mongo shell:
bash
Copy code
**mongo**


In the mongo shell, create a simple index on the "breed" key:
javascript
Copy code
**db.animals.createIndex({ breed: 1 })**


Show an example query using this index.
Use the explain function to verify that the index will be used.
Take screenshots of the example query and the explain result.
Step 3: Creating a Compound Index on "breed" and "outcome_type"
Create a compound index on "breed" and "outcome_type":
javascript
Copy code
**db.animals.createIndex({ breed: 1, outcome_type: 1 })**


Show an example query using this compound index.
Use the explain function to confirm that the index will be used.
Take screenshots of the example query and the explain result.
Part II: User Authentication
Step 4: Creating a User Account
In the mongo shell, create a new user account named "aacuser" for the AAC database:
javascript
Copy code
use admin
**db.createUser({
    user: "aacuser",
    pwd: "YourChosenPassword",
    roles: ["readWrite", "dbAdmin"]
})**




Replace "YourChosenPassword" with the actual password you choose.
Take a screenshot of the commands.
Open a second terminal session and set environment variables for the new user:

bash
Copy code
**export MONGO_USER=aacuser
export MONGO_PASS=YourChosenPassword**



Run mongosh in the second terminal session as the new user:

bash
Copy code
**mongosh**


Take a screenshot of the login process.
Use the db.runCommand({ connectionStatus: 1 }) command to verify the connection as a specific user.
Include the results in your screenshot.
Confirm that you can access MongoDB and list the databases using both the admin and aacuser accounts.

Take screenshots of the commands and results for both accounts.
Submit a Word document containing all the screenshots. Make sure to include your username in every screenshot. Enlarge the images before submission for better readability.
