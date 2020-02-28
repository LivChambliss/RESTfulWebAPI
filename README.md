# RESTfulWebAPI
Mizzou INFOTC 4320 Design a RESTful Web API

You would request the GET for Documents with the author visible with:
GET/documents?include=author HTTP/1.1

Then what would be returned is:
HTTP/1.1 200 OK
Content-Type: application/vnd.api+json

{
  "data": {{
  "type": documents",
  "id":"1",
  "attributes":{
  "title":"JSON:API Mizzou Information Technology",
  "body":"Here is a list of all of the course requirements in Mizzou's Information Technology Program.",
  "created":"2020-02-27",
  "updated":"2020-02-27",
  },
  "relationships":{
  "author": {
  "data": {"id":"26", "type": "people"}
  }
  }
  }},
  
  
"included": {
{
"type": "author"
"id":"26",
"attributes":"{
"name":"Liv",
"age":21,
"gender":"female",
}
}
}
}


With this text, the API retrieves the "documents", displays it's id, title, body, when it was created and when it was last updated. The 200 OK at the top means that everything ran smoothly and the request was completed successfully. The API can also fetch information about the author which will display their name, age, gender, id, and any applicable attributes. 
