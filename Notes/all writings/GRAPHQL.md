#GRAPHQL #RESTFUL-API
# GRAPHQL
## Definiton
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

## REST API has drawbacks like
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

## RESOURCES
[GRAPHQL crash course by net ninja](https://www.youtube.com/playlist?list=PL4cUxeGkcC9gUxtblNUahcsg0WLxmrK_y)

##