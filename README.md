
===

Requirements
---
- install serverless framework:
`npm install -g serverless`
- configure secret / access key for AWS account in home directory:
`~/.aws/credentials`

Options
---
- `--timeoutDuration=<n>` : number of seconds to sleep on 'timeout' requests
- `--timeoutPercentage=<n>` : percentage of requests to 'timeout' on

Commands
---
To create instance of mock use: `serverless deploy --timeoutDuration=10 --timeoutPercentage=5` from this directory.
This will take ~60 seconds or so then give you information on hitting the service.

example output:
```
Service Information
service: briteverify
stage: dev
region: us-west-2
api keys:
  None
endpoints:
  GET - https://0hgv6ymrub.execute-api.us-west-2.amazonaws.com/dev/emails.json
functions:
  mockbriteverify: briteverify-dev-mockbriteverify
```

To remove instance run `serverless remove` from this directory.  After ~30 seconds you will
 get a message about successfully removing the instance.
 
example output:
```
Serverless: Getting all objects in S3 bucket...
Serverless: Removing objects in S3 bucket...
Serverless: Removing Stack...
Serverless: Checking Stack removal progress...
.....................
Serverless: Stack removal finished...
```
