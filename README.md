# Social Customer

This app aims to show you your customer's latest tweets and their Facebook profile picture.


## Setup
#### Requirements
This app requires the following:
- Mule Standalone 3.7.3
- MySQL (any earlier version)
- Access to Facebook and Twitter
- App credentials to Facebook and Twitter
- Write permition on /tmp/customers

#### Facebook and Twitter credentials
Put app credentials on ```src/main/app/mule-app.properties``` 

#### Customer test data
Social Customer app watchs ```/tmp/customers``` folder for new CSV files in order to import to customers database

So, let's import test data by running the follow line from project's root folder:

```
cp src/test/resources/customer-input.csv /tmp/customers
```
> Obs.: This is a random data got on a quick internet surf 

## Using
#### Facebook authorization
First you will need to authorize this app to use your Facebook account to get customer's profile picture. So, open http://localhost:8082/fbauthorize

#### API
- /fbauthorize - Facebook API authorization
- /customers - Returns all customers with their latest tweets
- /fbphoto?fbuser=[facebookId] - Returns someones profile picture.

## Enjoy it :)
