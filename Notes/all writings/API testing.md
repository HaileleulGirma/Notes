## payloads
#GRAPHQL #graphql  
- mainly for GraphQL, [payload all the things](https://github.com/swisskyrepo/PayloadsAllTheThings)found in the GraphQL injection folder.
- API enumeration using wordlists. provided by [fuzzdb](https://github.com/fuzzdb-project/fuzzdb/blob/master/discovery/common-methods/common-methods.txt)
- IF you see `/api/v3/users` you also need to check if other versions of API(higher or lower) are up and vulnerable too for eg. `/api/v1/users`
## How to bypass object level authorization:

- Wrap the ID with an array.  
    Instead of {“id”:111} send {“id”:[111]}
- Wrap the ID with a JSON object  
    Instead of {“id”:111} send {“id”:{“id”:111}}
- Try to perform [HTTP parameter pollution](https://medium.com/@0xgaurang/case-study-bypassing-idor-via-parameter-pollution-78f7b3f9f59d):  
    _/api/get_profile?user_id=<legit_id>&user_id=<victim’s_id>_  
    OR  
    _/api/get_profile?user_id=<victim’s_id>&user_id=<user_id>_  
    This can work in situations where the component that performs the authorization check and the endpoint itself use different libraries to parse query parameters. In some cases, library #1 would take the first occurence of “user_id” while library #2 would take the second.
- Try to send a wildcard instead of an ID. It’s rare, but sometimes it works.
## methodologies
-  [API Pentesting mindmap](https://github.com/cyprosecurity/API-SecurityEmpire/blob/main/README.md)
-  [beginners guide to API hacking](https://danaepp.com/beginners-guide-to-api-hacking)
- [31-days-of-API-security-tips](https://github.com/inonshk/31-days-of-API-Security-Tips)
- [pentips about API](https://csbygb.gitbook.io/pentips/web-pentesting/api)
## RESOURCES
- Twitter [Nithin](https://twitter.com/thebinarybot)

