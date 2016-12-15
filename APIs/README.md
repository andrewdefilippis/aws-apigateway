# APIs

APIs that I have created in AWS API Gateway.

## Import and Usage
1. Within the AWS API Gateway Console, create a new API and select to import from a Swagger template.
2. Copy the contents of the Swagger template and paste it into the console form, or choose to pick the location of the template on your computer.
3. Deploy the resources to a Stage (such as "dev") by selecting "Actions" in the top of the resources console page, and selecting 'Deploy API'.
4. Copy the "execute-api" invoke URL that includes the stage name in the path, and make a request with the correct method to it using `curl`, `postman`, or a `web browser`.

## Includes

### Level 1
If you are new to using AWS API Gateway, these APIs are for you.

**checkip**
> Return the client's public IP address as a plaintext response body.
