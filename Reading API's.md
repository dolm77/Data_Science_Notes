##Course 3 Getting and Cleaning Data - Reading API's

#Reading API’s - Application Programming Interfaces

Package that utilizes the API’s is the httr package

Accessing Twitter from R --Allows you to access data from twitter based on the below authorization when creating an API account.
-install.packages(“httr”)
-library(httr)
-my app = oauth_app(“twitter”, key = “yourConsumerKeyHere”, secret = “yourConsumerSecretHere”)
-sig = sign_oauth1.0(myapp, token = “yourTokenHere”, token_secret = “yourTokenSecretHere”)
-homeTL = GET(“https://api.twitter.com/1.1/statues/home_timeline.json”, sig)

Converting the json object
-json1 = content(homeTL)
-json2 = jsonlite::fromJSON(toJSON(json1))
-json[1,1:4]

httr Package Contents
-Allows GET, POST, PUT, DELETE, requests if you are authorized
-You can authenticate with a user name or a password
-Most modern API’s use something like oauth
-httr works well with Facebook, Google, Twitter, Github, Yahoo, etc.
