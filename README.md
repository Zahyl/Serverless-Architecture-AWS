# Implementing Music Application on Serverless Architecture on AWS
<img width="466" alt="serverless-music" src="https://github.com/Zahyl/Serverless-Architecture-AWS/assets/71133664/c634b129-4dee-4bc4-af1f-759744e9545e">

This project showcases the development of a serverless music web application using AWS services to manage music albums. The application's front-end is built with HTML, CSS, and JavaScript and hosted on Amazon S3. The back-end is powered by AWS Lambda, Amazon API Gateway, and Amazon DynamoDB.

**Configuration:**

- **User Registration and Authentication:** Utilizes a Cognito User Pool named "projectpool" for user registration and authentication. Users can sign up with their username, email, and password. After successful verification, they gain access to the Music Dashboard page.

- **DynamoDB Database:** A DynamoDB table named "Albums" is used to store music album details in JSON format. The table serves as the persistence layer for the application.

- **Music Dashboard Page:** Displays music albums fetched from the "Albums" DynamoDB table using the GET method. It includes options for editing and deleting albums, a Sign Out button, and an Add Album button.

- **Add Album Page:** A page where users can input details for a new album. Upon hitting the "Add" button, a POST function is executed, updating the "Albums" table with the new item.

- **Lambda Functions:** Four Python Lambda functions are created for GET, POST, PUT, and DELETE methods. Each function performs the desired operation on the "Albums" DynamoDB table.

- **API Gateway:** An API named "testproject" is created in API Gateway with CORS enabled. A resource named "/album" is added with four methods (GET, PUT, POST, and DELETE), each configured with its respective Lambda function.

- **Testing:** The API can be tested using Postman by selecting the method and pasting the API Gateway URL. A 200 (Success) code should be returned.

- **Frontend Development:** The front-end is developed using HTML, CSS, and JavaScript, including relevant details like the DynamoDB table name, API Gateway URL, and Cognito User Pool details.

- **Static Web Hosting:** The front-end files are hosted on a public S3 bucket named "testprotest." Static Web Hosting is enabled to generate a URL for external users to access the application.

In summary, the implementation of the music application showcases the benefits of serverless architectures on AWS. Utilizing AWS services such as Lambda, API Gateway, DynamoDB, and Cognito, I built a scalable, cost-effective, and secure application with ease. The use of conditional expressions in DynamoDB ensured data consistency and prevented data duplication, while API Gateway endpoints provided a user-friendly interface for users to interact with the application. Furthermore, Cognito allowed for secure authentication and authorization of users. By leveraging the advantages of serverless architectures, businesses can build complex and secure applications without the need for managing servers or infrastructure, resulting in significant cost savings and increased agility.

