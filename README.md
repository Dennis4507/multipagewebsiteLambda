# multipagewebsiteLambda


Multipage Visitor Counter Powered By AWS Lambda.


Part 1: Frontend (JavaScript)

Goal here is to add a visitor counter element to my HTML and write a Javascript code that will fetch and update the visitor counter via an API Gateway.

1. Add a placeholder in your HTML
In your S3-hosted site’s HTML:

![alt text](<Bilder/Screenshot (269).png>)

2. JavaScript event listener fetch code that invokes an API call on AWS

![alt text](<Bilder/Screenshot (270).png>)

Part 2: DynamoDB Setup

3. Created a DynamoDB table to store the count.

Table name: VisitorCounter, Primary key: id (String)
Used On-Demand capacity. 

![alt text](<Bilder/Screenshot (271).png>)

4. Visitor Table 

![alt text](<Bilder/Screenshot (274).png>)


Part 3: Lambda Function (Python + boto3)

5. We write a Lambda function with (Python 3.12 runtime) that reads and updates the count from the DynamoDB Table 

![alt text](<Bilder/Screenshot (289).png>)

![alt text](<Bilder/Screenshot (290).png>)

6. also attach a role with AmazonDynamoDBFullAccess for now

![alt text](<Bilder/Screenshot (291).png>)


Part 4: We Created a REST API Gateway to expose the Lambda function to the Websites frontend.

7. Created a resource: /visitor-count

![alt text](<Bilder/Screenshot (292).png>)

8. Created method: GET → Integrate with your Lambda

![alt text](<Bilder/Screenshot (294).png>)

9. Enable CORS

![alt text](<Bilder/Screenshot (295).png>)

10. Deploy to Stage note the Invoke Lambda REST API URL AND Paste it into my Javascript Fetch request script.

![alt text](<Bilder/Screenshot (296).png>)

11. 






:



