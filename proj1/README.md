# Project 1

## Group Details: Group No - 31
1) [Jay Patel](https://github.com/jaypatel31): jhpatel9
2) [Devansh Shah](https://github.com/drs1951): dshah8
3) [Shyamal Gandhi](https://github.com/shyamal31): sgandhi6
4) [Shail Shah](https://github.com/shail611): sshah38

## Part 1: Project Rubrics
1. Project O [GITS](https://github.com/harshitpatel96/GITS): [Project O GITS Rubric.csv](https://github.com/jaypatel31/CSC510_Group31/blob/main/proj1/Project%20O%20GITS%20Rubric.csv)
2. Project A [86 No More](https://github.com/shantanu109/CSC510_Group25_Project1): [Project A 86 No More Rubric.csv](https://github.com/jaypatel31/CSC510_Group31/blob/main/proj1/Project%20A%2086%20No%20More%20Rubric.csv)
3. Project T [GITS](https://github.com/bhavesh242/GITS): [Project T GITS Rubric.csv](https://github.com/jaypatel31/CSC510_Group31/blob/main/proj1/Project%20T%20GITS%20Rubric.csv)
4. Project f [Slash](https://github.com/NCSU-Group7-SE2021/slash/): [Project f Slash Rubric.csv](https://github.com/jaypatel31/CSC510_Group31/blob/main/proj1/Project%20f%20Slash%20Rubric.csv)
5. Project m [Classmate Bot](https://github.com/lyonva/ClassMateBot): [Project m Classmate Bot Rubric.csv](https://github.com/jaypatel31/CSC510_Group31/blob/main/proj1/Project%20m%20Classmate%20Bot%20Rubric.csv)

## Part 2: Project Walkthrough Video
Youtube Link: https://youtu.be/dsR_W8TjSJ8

## Part 3: Essay

### Introduction:

This web application project primarily focuses on providing a smart inventory management solution to restaurants. The software has the feature of sending notifications to managers whenever the restaurant is running low on specific ingredients. Additionally, the software tracks the analytics of the usage of different food items and the ingredients used for that. We have selected this software as part of our "Software Engineering" project, and we will try to enhance the software experience by removing its discrepancies and issues.

### Difficulties Faced While Running the Software:

First, we forked the GitHub repository of "86 No more" and cloned it to our local machines. We faced many difficulties while running the software on our local machines. As the project was made 2-3 years ago, we expected to encounter many outdated dependencies, but there were many other issues associated with the project as well. 

- First of all, they have used separate repositories for frontend and backend, which generally should not be the case. 
- Also, no documentation was provided to overcome the installation challenges faced due to outdated dependencies. 
- Initially, the project was not able to run with the latest version of Node.js. 
- We also ran into the peer dependencies error as we have npm version > 7. npm by default installs peer dependencies which can result in the version conflicts of those dependencies that break the installation of the rest of the packages. To overcome this, while installing the packages we have to pass the "--legacy-peer-deps" flag to ignore the auto installation of peer dependencies.
- After solving those installation-related issues, we were able to build the project and see the running version of web applications. However while navigating through different functionalities of the project, we ran into several other problems that led to breaking the web applications. One such major issue was that whenever the client sends the request to the server, it expects the server to send a web authentication token along with the response data. But in the backend code, it was only sending the response data, not the authentication token. Since the server was not sending the token with each request, the application kept breaking with each API call.

There were some other logical issues associated with the various functionalities:

1. The restaurant name was shown as undefined in the list of menu items.
2. There is no logical relationship between the inventory and menu items in the web application.
3. The constraints for all the fields in the form were not set at all; for example, a user can pass a string into the date field, which can create a lot of trouble in the database.
4. A lot of redundant data is being stored in the database.

**Security Issue:** For proper authorization of data, the API should restrict the access of data from other restaurants from being publicly accessible.

### How These Challenges Could Have Been Avoided:

- They should have removed all the unused variables so that the debugging process would have become easier for us.
-  Instead of using a local database, they could have used a cloud-based version of a database to collaborate easily with peers.
-  Even after knowing that the test cases are failing, they should have properly documented the steps needed to overcome the issues.
-  The last commit of the project was made in 2021, and during that time, they should have made sure that the project was compatible with the latest version of Node.js present at that time.

### Pathway to Project 2

- First, we will merge the separate repositories of frontend and backend.
- There are various security-related issues in the project. Firstly, the password is directly stored in the database without any kind of encryption. Secondly, the API is created in such a way that the data of all the restaurants is sent to the client, and the filtration of data is done on the client side. This is a major security issue because the user of one restaurant should not be able to access the data of other restaurants. Lastly, there should have been a .env file for storing confidential tokens such as API token and database password.
- We will establish a proper relationship between menu items and inventory.
- When there are any updates made by the client, a notification will be shown.
- To avoid the risk of signups through spam emails, we’ll add an additional verification method for signups.
- We’ll make sure all the functionalities mentioned in the documentation will work properly.
- We will provide proper documentation to run this project on the latest version of Node so that our successors won’t have to deal with such issues.

## Repo Forked Links:
- Frontend: https://github.com/drs1951/CSC510_Group31
- Backend: https://github.com/drs1951/86_Backend 

