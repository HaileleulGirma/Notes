#GRAPHQL #graphql 
# GRAPHQL
## Definition
GRAPHQL is a query language, an alternate to using a REST API.
When we use REST API we send specific http request to access a resource / interact with the data.
EXAMPLE:
- `example.com/api/course
- `example.com/api/course/1`
GRAPHQL  has a single endpoint unlike RESTFUL API  which has endpoints every where we go.
- `mygraphqlsite.com/graphql`
GRAPHQL lets us customize our query so we can get the output we need in return without [[#^2e25f8| over fetching]] or  [[#^6dd0ee| under fetching]].
EXAMPLE:
<pre>Query {
	courses{
		id,
		title,
		thumbnail_url	
	}
} 
</pre>
## How to write a GRAPHQL query
You start using the keyword `query` followed by the name of the query, then open curly brackets and inside, you are going to write the resources you want to get back.
<pre>
query ReviewsQuery{
	reviews{
		ratings,
		content,
		}
}
</pre>
If we leave the inside of the second curly brace empty(removing ratings and content) it won't return a resource since we need to specify exactly what we need. This is the main reason what makes GRAPHQL favorable compared to RESTFUL API.
The above query may return the following
```
{
	"data":{
		"reviews":[{
			"rating": 9,
			content: "excellent service!!!"
		},
		{
		"rating": 2,
		"content": "horrible experience!!!"}
		]
	}
}

```
GRAPHQL also lets us traverse through the graphs(data in the server) by modifying our queries 
watch this video. It explains it well [GraphQL Crash Course #2 - Query Basics](https://youtu.be/39CPVkZE4nM?list=PL4cUxeGkcC9gUxtblNUahcsg0WLxmrK_y) @3:50

## Schema and types
### Datatypes
GRAPHQL has In GraphQL, data types represent the shape of data that can be queried or mutated. GraphQL defines several built-in scalar types and allows developers to define custom object types, enumerations, interfaces, unions, and input types. Here's an overview of the data types available in GraphQL:

1. **Scalar Types:**
   - Scalars represent atomic values, such as strings, integers, floats, booleans, and IDs. GraphQL defines the following built-in scalar types:
     - `String`: A UTF-8 encoded string.
     - `Int`: A signed 32-bit integer.
     - `Float`: A signed double-precision floating-point value.
     - `Boolean`: Represents true or false.
     - `ID`: A unique identifier, often used to represent an identifier or key.
  
2. **Object Types:**
   - Object types represent complex data structures with multiple fields. They can contain scalar fields or fields that reference other object types. Object types define the structure of data available in the GraphQL schema.

3. **Enumerations:**
   - Enumerations represent a predefined set of possible values. Enum types define a finite set of options, and each field of an enum type must be one of those options.

4. **Interfaces:**
   - Interfaces define a set of fields that must be implemented by object types that implement the interface. Interfaces allow for polymorphism and shared behavior among different types.

5. **Unions:**
   - Unions represent a type that can be one of several possible object types. Unions allow for more flexible querying and can be used to represent heterogeneous collections of objects.

6. **Input Types:**
   - Input types are similar to object types but are used specifically for input arguments in GraphQL mutations and queries. Input types define the structure of data that can be passed as arguments to fields or directives.

These are the primary data types available in GraphQL. Developers can define custom object types, enumerations, interfaces, unions, and input types to represent the specific data requirements of their GraphQL APIs. Additionally, GraphQL allows for complex relationships between types, enabling developers to model rich and expressive data schemas.

### Schema
**schema** is something that describes the shape of the graph and the data available on it. Normally the graphql schema(the data available on the graph) and will be fairly similar to the data you are storing in your application database, but not always.
**Typedef**s are definitions of different types of data we want to expose on our graph. IT maps out what the graph looks like. It defines the datatypes and endpoints.
**Query variables** are variables that we pass to the query for filtering the results to match our need.
**Resolver** is an object that contains resolver functions which handle any incoming requests for us. 
- For more info on schema and types check [GraphQL Crash Course #4 - Schema & Types](https://youtu.be/ginCmJEdZ0g?list=PL4cUxeGkcC9gUxtblNUahcsg0WLxmrK_y)
- For more info on resolvers, check [GraphQL Crash Course #5 - Resolver Functions](https://www.youtube.com/watch?v=mjqfYgFyziU&list=PL4cUxeGkcC9gUxtblNUahcsg0WLxmrK_y&index=5&pp=iAQB)
- For more info on query variables, check [GRAPHQL Crash Course #6 - Query Variables](https://youtu.be/joMO4LwRa5Q?list=PL4cUxeGkcC9gUxtblNUahcsg0WLxmrK_y)


## REST API has drawbacks like
#RESTFUL-API
- **over fetching** means (getting back more data than we need) ^5fd7cb
 `example.com/api/course` may fetch all the resources related to course in JSON while we only wanted a single info like title below.
 EXAMPLE
 <pre>
{
"id": "1",
"title": "thud",
"author": {...},
"thumnail_url": "..."
"video_url": "..." 
}
</pre>
 ^2e25f8

 - **under fetching** means (getting back less data than we need)
`example.com/api/course/1` may return all the resources related to course 1's authors, title, price... but for more info we may need to send an additional request to know about the courses written by the author lets sat the author is author 1.
<pre>
{
"id": "1",
"title": "thud",
"author": {...},
"thumnail_url": "..."
"video_url": "..." 
}
</pre>
`example.com/api/author/1` is another request we are going to send because of under fetching caused by REST API. ^44102d
EXAMPLE ^6dd0ee

## Where to find GRAPHQL?
It is at the same place you find other API's.
GraphQL is usually located at specific endpoints.
- q, ql, gql, graphql, graphiql, graphql/console
- also lookout for requests/responses referencing: queries, mutations, subscriptions...
- q=


## How does GraphQL work?
SOURCE on fragments, metaqueries, queries and mutations: [Finding your next bug: GraphQL](https://youtu.be/jyjGneKJynk)
- GraphQL implements graph structure as the database
- There are queries and mutations
- Queries fetch data
- Mutations allow the data to be edited
- Fragments allow for easily saved lists of fields
- Metafields allow for the inspection of query or mutation information
### QUERIES
**!!!YOU SHOULD NOT FORGET THAT THE QUERIES MUST BE *URL ENCODED!!!***
- written as functions
	- It returns JSON data
	- can return a single result or several
	- can also include arguements
	- or data manipulation
- very structured
- uses the key word `query`
### Mutations
- while queries fetch data, a mutation edits it
- can be an edit with assigned variables or deleting
- can also fetch data after modifying it
- uses the keyword `mutate`
- 
### Fragments and Metaqueries
- fragments allow us to decide a list of fields and requests multiple queries use the same list
- allow for easily saved lists of fields
- used for comparisons
- Metafields allow us to inspect the API(either query or mutation information), `__typename` returns the typename
- Extremely important for introspection queries!


## How to hack GraphQL APIs
- try to introspect to find the GraphQL queries and mutations 
	- `__schema`, `__type` are commonly used introspection queries
	- if introspection is turned off, go for a traditional recon approach, push buttons, use wordlists
- identify the business logic of each endpoint (where does it go? what does it do? what does it power?)
- craft queries to check for:
	- information disclosure, IDORS...
- Remember the hard part of GraphQL bug hunting is the syntax!
	- A great place to practice is the h101 CTF
### TOOLS
are found in the video starting @32:27
- GRAPHQL voyager
![[graphql voyager.png]]
- GRAPHQL IDE
- INQL (burp addon)
- graphql-path-enum (understand large graphs)
![[graphql-path-enum.png]]
## RESOURCES
[GRAPHQL crash course by net ninja](https://www.youtube.com/playlist?list=PL4cUxeGkcC9gUxtblNUahcsg0WLxmrK_y)

