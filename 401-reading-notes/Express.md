# Review, Research, and Discussion

- What's the difference between PUT and PATCH?
PUT overwrites the entire entity if it already exists, and creates a new resource if it doesn’t exist.
Unlike PUT, PATCH applies a partial update to the resource. This means that you are only required to send the data that you want to update, and it won’t affect or change anything else

- Provide links to 3 services or tools that allow you to "mock" an API for development like json-server

1- [Postman Mock Server](https://learning.getpostman.com/docs/postman/mock-servers/setting-up-mock/)  
2- [reqres](https://reqres.in/)  
3- [mocki.io](https://mocki.io/fake-json-api)

- Compare and contrast Swagger and APIDoc.js 1 Which HTTP status codes should be sent with each type of (un)successful API call?  

```text
apiDocjs: Inline Documentation for RESTful web APIs. It creates a documentation from API annotations in your source code. It includes a default template which uses handlebars, Bootstrap, RequireJS and jQuery for the output of the generated apidata.js and apiproject.js as a html-page;  
Swagger Inspector: Test and Document Your APIs With Ease. It is a free cloud-based API testing and documentation tool to simplify the validation of any API and generate its corresponding OpenAPI documentation. 
```

```text
From 400s and 500s
```

- Compare and contrast SOAP and ReST

```text
1) SOAP
- Communication happens using XML only
- Request is sent to SOAP methods
- Documentation is in WSDL (Wizdal)
- Heavy, more secure, more stable
- getting less popular
2) REST API
- Communication happens using Json, XML
- Requests are sent to API methods/urls using
- Communication happens in HTTP(Internet)
- Lightweight, stable
- Easy to develop and automate
- very popular
```

***for more info search for the following terms***

- web server
- Express
- Routing
- WRRC

## Discussions

- Which 3 things had you heard about previously and now have better clarity on?  
    REST APIs , HTTP Requests, React Life cycle  
- Which 3 things are you hoping to learn more about in the upcoming lecture/demo?  
    PipeLines, Access Tokens, Fetching the data  
- What are you most excited about trying to implement or see how it works?  
    the ta-daaa moment when I have a clear idea about something  

## Preparation Materials

- [An introduction to NodeJS and Express](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction)
- [What is NPM?](https://docs.npmjs.com/getting-started/what-is-npm)
- [What is TDD?](https://www.agilealliance.org/glossary/tdd/)
- [CI/CD](https://www.youtube.com/watch?v=xSv_m3KhUO8)

## Bookmark

- [nodeJS docs](https://nodejs.org/en/docs/)
- [npm docs](https://docs.npmjs.com/)
- [express docs](https://expressjs.com/en/4x/api.html)
- [http status codes](https://www.restapitutorial.com/httpstatuscodes.html)
- [supertest](https://github.com/visionmedia/supertest)
