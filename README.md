Implementation of basic GET and POST APIs on the resources of DynamoDB using AWS API Gateway. These APIs invoke Lambda function when called.

## Setup : 
- Create an IAM role <br/>
- For each API / method , make a lambda function <br/>
- Create Dynamo table <br/>
- Create API <br/>
- Deploy API <br/>
- Test it using POSTMAN <br/>

Get "Hello People" - <br/>
![GET Method](/GET.jpeg)

Post - <br/>

```
{
    "operation": "create",
    "tableName": "lambda-apigateway", 
    "payload": {
        "Item": {
            "id": "1234ABCD",
            "number": 5
        }
    }
}
```

![POST Method](/POST.jpeg)

List - To get all the inserted items in the dynamoDB table.<br/>

```
{
    "operation": "list",
    "tableName": "lambda-apigateway",
    "payload": {
    }
}
```

![List Operation using POST method](/LIST.jpeg)
  
