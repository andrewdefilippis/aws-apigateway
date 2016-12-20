# checkip

*Return the client's public IP address as a plaintext response body.*

----

## Overview

This API allows a client to make a GET request to the `/` resource, and receive a plaintext response back that includes their public IP address.  An OPTIONS method for CORS is configured on the `/` resource to allow requests from any origin.

## API Gateway Features Utilized

* `Mock` Integration Request Type
* Integration Response `Mapping Template` with Content-Type `text/plain`
* `$context.identity.sourceIp` Context Variable
* Method Response `header definition`
* Integration Response `header mapping` with a `static value`