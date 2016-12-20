# roll_the_dice

*Return the results of a dice roll using the number of dice and number of sides you define, as a JSON object.*

----

## Overview

This API allows a client to make a request with `ANY` method to the `/roll-the-dice` resource.  The `Lambda Function` configured as a `Proxy Integration Request Endpoint` is coded to only accept `GET` and `POST` methods for returning the results of a dice roll.

* Try to submit a request using a method type other than `GET` and `POST`, and see what response you receive.

All responses are configured as JSON objects.

## Requirements

This API requires:
* The Lambda Function [roll_the_dice] must be created before the API is created.
* Three modifications need to be made to the Swagger Template before importing it into API Gateway.
  * Replace the AWS Account ID `123412341234` in the Lambda Function `uri` with your AWS Account ID.
    * *"arn:aws:apigateway:us-west-2:lambda:path/2015-03-31/functions/arn:aws:lambda:us-west-2:*`123412341234`*:function:roll_the_dice/invocations"*
  * Replace the Lambda Function region `us-west-2` in the `uri` with the region you created the Lambda Function `roll_the_dice`.
    * *"arn:aws:apigateway:us-west-2:lambda:path/2015-03-31/functions/arn:aws:lambda:*`us-west-2`*:123412341234:function:roll_the_dice/invocations"*
  * Replace the API Gateway region `us-west-2` in the `uri` with the region you will create the API in.
    * *"arn:aws:apigateway:us-west-2:lambda:path/2015-03-31/functions/arn:aws:lambda:*`us-west-2`*:123412341234:function:roll_the_dice/invocations"*

## API Gateway Features Utilized

* `Lambda Proxy Integration` Request Type
  * The client's `request payload and parameters are passed-through` directly to the Lambda Function
  * The Lambda Function responds with a `HTTP status code (type: int)`, and can optionally include `headers (type: dict)`, and `body (type: str)`


[roll_the_dice]: https://github.com/andrewdefilippis/aws-lambda/tree/master/Functions/Python/roll_the_dice
