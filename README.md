# Postman-Comment-Collection
This repository includes a Postman collection that based on comment functionality tests for new social application, where users can make posts. 

## Instructions on How to Run the Tests
To run the tests in this repository, please follow the steps below:

### Pre-requisites
Make sure you have Postman and Node.js installed on your machine. If you don't have them, you can download and install them from the following official websites:

Postman: [Postman Website](https://www.postman.com/downloads/)
Node.js: [Node.js Website](https://nodejs.org/en)


### Clone the repository 
Clone this repository to your local machine using the following command: 

`git clone https://github.com/OsmanEgretli/Postman-Comment-Collection.git`

You can find Postman collection and environment files in repo.


### Setup Test Environment 
**1. Install JSON Server:** Start by installing JSON Server globally on your machine. You can use npm (Node Package Manager) to do this. Open your terminal and run the following command:

`npm install -g json-server`

**2.Create a new directory:** Create a new directory where you want to set up your test environment. You can choose any suitable name for the directory. You can use mkdir and touch commands on terminal if you're using Mac OS machine.

**3.Navigate to the directory:**  Use the cd command in your terminal to navigate to the directory you just created. For example:

`cd /path/to/your/directory`

**4.Create a db.json file:** Inside the directory, create a file named db.json. This file will serve as your database file and will contain the data from JSONPlaceholder. You can use any text editor or IDE to create the file.

**5.Seed the db.json file:** To seed the db.json file with data from JSONPlaceholder, you can make use of the curl command in your terminal. Run the following command to fetch the posts data:

`curl https://jsonplaceholder.typicode.com/posts > db.json`

**6.Seed comments data:**  Similarly, run the following command to fetch the comments data and append it to the db.json file:

`curl https://jsonplaceholder.typicode.com/comments >> db.json`

**7.Start the JSON Server:**  Once you have seeded the db.json file with data, you can start the JSON Server. Run the following command in your terminal:

`json-server --watch db.json`

This command starts the JSON Server and watches the db.json file for any changes. It creates a RESTful API that mimics a real server, serving the data from db.json.

**Test the API:** You can now access the REST API endpoints provided by JSON Server. The server runs at http://localhost:3000 by default. For example, you can access the posts data by making a GET request to http://localhost:3000/posts.


### Import The Collection and Environment

Open Postman and import the collection file (collection.json) and the environment file (environment.json) located in the repository. You can import the collection by clicking on "Import" in the Postman toolbar and selecting the JSON file.

<img width="1264" alt="image" src="https://github.com/OsmanEgretli/Postman-Comment-Collection/assets/99646672/dcc6f9be-7bde-495f-9522-61b5822eb90a">


<img width="1244" alt="image" src="https://github.com/OsmanEgretli/Postman-Comment-Collection/assets/99646672/8fe630c4-b942-4b48-b525-e1c2d7fe05cf">


### Set up environment variables

Before running the tests, make sure to set up the necessary environment variables. Open Postman click dropdown menu for test environment which is located on the right top and select Comment Test Environment.

<img width="1069" alt="image" src="https://github.com/OsmanEgretli/Postman-Comment-Collection/assets/99646672/375d8279-12d7-41d4-8580-03f81abd28e3">


### Run the tests

Once the collection is imported and the environment variables are set, you can run the tests by selecting the collection folder in the left sidebar and clicking on the "Run" button. This will execute all the requests and tests within the collection.

### Review the test results 

After running the tests, you can review the test results in the Postman runner. The tests will provide feedback on whether they passed or failed, allowing you to verify the functionality of the API endpoints and assertions.

## Approach to the Assignment

  In this assignment, I chose to test the functionality of certain API endpoints using Postman. The specific endpoints and test scenarios were based on the requirements provided.

### Testing Approach
 - I identified the critical API endpoints and scenarios that needed to be tested based on the assignment requirements.
 - For each test scenario, I created corresponding requests and assertions within the Postman collection.
 - I utilized environment variables to store and reuse values across different requests and tests, improving the maintainability of the collection.
 - To ensure comprehensive coverage, I included positive and negative test cases, validating both expected and unexpected behavior.

### Future Expansion
In the future, these tests can be expanded by incorporating additional test scenarios, edge cases, and performance testing. Additionally, integration with a continuous integration/continuous deployment (CI/CD) pipeline can be set up to automatically run the tests on each code change or deployment. We can expand the test coverage by defining user behaviour and business rules.
  
### Technical Challenges
During the assignment, I encountered some technical challenges such as handling dynamic data, managing environment variables. To overcome these challenges, I leveraged Postman's features, such as environment variables, dynamic request/response handling, and pre-request scripts.
