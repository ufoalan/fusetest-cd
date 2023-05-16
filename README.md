# fusetest-cd
This example is to deploy springboot camel applications using Helm Chart. The first application is to search tweets by providing keywords and pass the searched tweets to a public mqtt queue.
And another application is to consume the messages from mqtt and create new user accounts on Salesforce.

## 
FuseTest is an fuse camel application running in springboot.
It provides a REST API for searching tweets based on a keyword. The returned tweets will be enriched using sentiment analysis in order to understand the sentiment of particular topic.
The result will then be transformed into JSON format and will be published on a mqtt topic for further processing.

##
SalesForceTest is an fuse camel application running in springboot.
It consumes messages from a mqtt topic and transform the message into Salesforce object and create a usre account on Salesforce.
