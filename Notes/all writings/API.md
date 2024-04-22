# API
## What is an API?
- API stands for application programming interface.
- it provides a computer friendly method of interacting with a data source or backend logic
- they are used for both mobile and web. this takes loads of developers.
- it sits between the user(GUI) and the back-end(database or other)
## what do they look like?
- API's often use plain text
	- commonly this is JSON or XML
	- JSON is far more common
- often they return data directly from the database or some backend logic
- for example
	- `GET /employee/1/` for a RESTFUL API 
	- `GET /gql?1=` for GRAPHQL API
	- `/employee/1/` is called the resource or endpoint
## Introduction to JSON
#json #JSON 
- JSON is a way to represent data in a text format
- it starts with a curly brace `{` and ends with one `}`
- JSON contains objects which are denoted with `{}` and arrays/lists `[]`
- within these we have key-value pairs which store the data
- it is important to learn or become familiar with reading JSON to understand API's.
## Types of API
- SOAP 
	- less common nowadays
	- usually uses XML 
	- has a header and a body
- RESTful
	- most common API
	- uses JSON 
	- has a defined structure in requests
- GraphQL 
	- a newcomer on the scene
	- uses a custom query language
	- A single endpoint power all of the api
- Others
	- sometimes you'll see standalone JSON calls
	- websockets are also used as APIs
### RESTful
#RESTFUL-API 
- restful api's are really easy to spot
	- they have a defined structure which relates to CRUD functionality
	- mostly GET and POST methods are used for all.
- if you know an application, it would be easy to predict new endpoints.
	- if youtube's api has something like `GET /video/1`  , you can assume `DELETE /video/1 ` also exists or `GET /comments/1` for comments.
- they are widely used however some of the endpoints maybe more custom
	- eg. `DELETE /posts/1` vs `/posts/1/delete`
- they usually return JSON 
	- you can get a burp plugin to automatically visualize JSON (JSONBeautifier)
### GraphQL
#GRAPHQL #graphql [[GRAPHQL]]
- graphql can be more difficult to spot
	- usually it maybe some endpoint like `gql?q=...` or `graphql?q=...` or `g?q=`
	- an easier way to spot these is to try to find a reference to query or mutation
- its major advantage for hackers is its super easy to enumerate
- returns JSON but it looks weird compared to REST 
- however you probably need some practice forming queries
	- hacker101 graphql ctf level are good.
## API documentation
- sometimes they have their own documentation for developers to use and can be a fantastic recon tool
	- often they list endpoints and describe how to interact with the API in detail
- its worth looking for `[target] developer docs` or `[target] API`
- sometimes it maybe found on tutorials designed for developers or on stack overflow
## Enumerating APIs
- very important for API test
- enumerating allows us to be sure we know everything within an API
- the goal is to use our knowledge on how endpoints are constructed to find more resources
- this works a little differently for RESTful and GraphQL 
### Enumerating RESTful APIs
#RESTFUL-API #restful-api
- RESTful APIs can be challenging to enumerate since we need to guess the resource names
	- common resource names
		- using a list of common restful endpoints or a wordlist. [[API testing]] 
	- custom resource names
		- curate some likely endpoints from seeing the functionality
### Enumerating GraphQL
- enumerating GraphQL is much easier. sending an introspection query to the endpoint will return every query that can be run on the database and what parameters these queries need to work.
- Tools like GraphQL voyager(allows us to visualize the result of the introspection query), InQL(burp extension), 

## How to find API'S
We can spot API'S if we lookout for:
- a webapp which has a mobile app(it makes it easier for them to build one API
- that handles requests for both the webapp and the mobile app)
- a webapp that has complex front end activity(if they use a lot of javascript to handle the front-end, then usually, they use API's to handle the back-end to make it feel more responsive)
- almost all mobile apps use API
- a website that takes long to load(it may be calling for multiple different resources from multiple different servers)
- a webapp with developer documentation
## Bugs found in API's
- information disclosure
- authorization issues
- business logic
- IDORs
- XSS and CSRF
- FOR more info check OWASP TOP 10 API on OWASP website or insiderphd YT video

[[GRAPHQL]] 
[[API testing]]
## TOOLS
-  [7 burp extensions for hacking API's](https://danaepp.com/7-essential-burp-extensions-for-hacking-apis)

## RESOURCES
- [insiderphd's everything api hacking playlist](https://www.youtube.com/playlist?list=PLbyncTkpno5HqX1h2MnV6Qt4wvTb8Mpol)
- 
