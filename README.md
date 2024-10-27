Instruction: -
Requirement: - 
1.	Python (version 3.6 or higher)
2.	Flask (install using pip install Flask)
3.	Visual Studio Code
4.	Insomnia or Postman API

Steps to Run the Flask API
1.	Setup the Project
Ensure that you have your Flask project directory set up properly. Your app.py file should be located at "C:\Users\user\Project\App.py".
2.	Running the Flask API
2. 1	Open a terminal in your project directory.
2. 2	Run the Flask app using the following command:
python "C:/Users/Acer/Desktop/Django Projects/Flask/App.py" OR python App.py
3.	Once the Flask app is running, you should see the following output in the terminal:
Serving Flask app 'App'
Debug mode: off
Running on http://127.0.0.1:5000/
Your API is now running locally on port 5000.

API Endpoints
The Rule Engine API consists of the following endpoints:
1.	Create Rule: POST /api/create_rule
2.	Combine Rules: POST /api/combine_rules
3.	Evaluate Rule: POST /api/evaluate_rule

Testing with Insomnia
Install Insomnia to test the API using Insomnia.
Click on the “Create” button and then click on the “Request Collection” and then give the name to the collection and then press on the “Click” button.


Create and Send Requests
A.	Add a New Rule
1.	Create a New Request:
Click on the       button and click on the “HTTP Request”

2.	Set the Request Type:
Choose POST from the dropdown next to the URL input field.

3.	Enter the Request URL:
Type in the following URL:
http://127.0.0.1:5000/api/create_rule

4.	Add Headers:
Click on the Headers tab.
Add the following header
Content-Type: application/json

5.	Add the Request Body:
Go to the Body tab and select JSON.
Enter the following JSON data (modify the rule as needed)
{
"name": "Rule1", 
"rule": "age > 30 AND department = Sales"
}

6.	Send the Request:
Click the Send button.

7.	Check the Response:
You should see a success message confirming that the rule was created. For example
{
"message": "Rule 'Rule1' created!"
}

B.	Combine Multiple Rules
1.	Create a New Request:
Click on the       button and click on the “HTTP Request”

2.	Set the Request Type:
Choose POST from the dropdown next to the URL input field.

3.	Enter the Request URL:
Use the following URL:
http://127.0.0.1:5000/api/combine_rules

4.	Add Headers:
1.	Click on the Headers tab.
2.	Add the following header
Content-Type: application/json

5.	Add the Request Body:
1.	Go to the Body tab and select JSON.
2.	Enter the following JSON data
{
"name": "Rule3", 
"rules": ["Rule1", "Rule2"], 
"operator": "AND"
}

6.	Send the Request:
Click Send button

7.	Check the Response:
You should receive a confirmation that the combined rule was created
{
"message": "Combined rule 'Rule3' created!"
}

C.	Evaluate a Rule
1.	Create a New Request:
Click on the       button and click on the “HTTP Request”

2.	Set the Request Type:
Choose POST from the dropdown next to the URL input field.

3.	Enter the Request URL:
Use the following URL
http://127.0.0.1:5000/api/evaluate_rule

4.	Add Headers:
1.	Click on the Headers tab.
2.	Add the following header:
Content-Type: application/json

5.	Add the Request Body:
Go to the Body tab and select JSON.
Enter the following JSON data
{
"name": " Rule3"  // Replace with the rule you want to evaluate
}

6.	Send the Request:
Click Send.

7.	Check the Response:
You should see the result of the evaluation (either true or false), for example:
{
"result": true
}

Screenshot: -
 

 

 

 

