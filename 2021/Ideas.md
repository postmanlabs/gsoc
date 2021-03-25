Postman in Google Summer of Code 2021 - Ideas
=============================================

## Project Ideas

We accept original ideas and proposals for every project. Following is a list of ideas which you can use as a reference.


### Idea 1: Newman Request
Newman already makes it effortless for you to run Postman collections. It enables you to see the results with your favourite reporters on CLI, as JSON, HTML etc. making it easy to summarise data and at the same time, use it in automations and build systems. But currently, it is limited to only running a collection of requests. This project aims to enable users to use these same capabilities for a single request.

**Expected outcome** </br>
Users can send a single request with Newman and show the request/response using a reporter of their choice.</br>
Replacing curl with newman request in a curl command should run the send the request using Newman.</br>
If user is logged in, the request should show up in Postman app’s History in sidebar.</br>

**Relevant skills**</br>
JavaScript language</br>
Understanding of HTTP protocol.</br>
curl</br>

**Complexity**: low </br></br>

### Idea 2: Parallel Iterations in Newman</br>
Newman supports running multiple iterations of a collection with different data provided in a CSV or JSON file, enabling users to test an API against multiple scenarios. But Newman executes each iteration serially and this can take a lot of time as the number of requests in a collection and iterations grow. This project aims to bring parallelism into Newman by splitting the iterations data into multiple chunks and running them as threads to bring down the total time roughly by a factor of n, where n is the number of threads.

**Expected outcome**</br>
Newman can split iteration data and run multiple runs using this data.</br>
Users can specific the number of parallel iterations that Newman can run.</br>

**Relevant skills**</br>
JavaScript language</br>
Understanding of threads and processes communication</br>

**Complexity**: low </br></br>

### Idea 3: Newman Dashboard</br>
Newman has an array of reporters that consume the run data that Newman provides. These include viewing a run in the terminal using CLI, as JSON which can be easily transported by a build system, as an HTML summary webpage, and many more. However, Newman lacks a way to control the runs in a central dashboard. This project aims to create a dashboard on a browser which can be used to start, resume, pause and stop Newman runs.

**Expected outcome**</br>
A dashboard can be opened on a browser which shows currently running Newman runs.</br>
The dashboard can be used to start, stop, pause and stop any Newman run.</br>
There is an option in Newman to connect to the dashboard and wait for run to be started by the dashboard.</br>

**Relevant skills**</br>
JavaScript language</br>
Understanding of daemons and IPC (websockets is a plus).</br>
Basic understanding of HTML, CSS</br>

**Complexity**: medium</br></br>

### Idea 4: API-First Blueprint for a Commerce API</br>
Building out an OpenAPI, mock, documentation, testing, and deployment of a commerce (or other) API that uses the Schema.org (http://Schema.org) as the underlying schema, providing a functioning and well documented example of what an API can be.

**Use case:**</br>
Increasing the number of API blueprints that could serve as learning material for individuals/teams working on an API first approach.</br>
An API blueprint could be useful for anyone to hit the ground running when building a Commerce API.</br>

**Required knowledge:**</br>
Understanding of the API first philosophy - https://www.postman.com/use-cases/api-first-development/.</br>
Comfort with YAML/JSON formats.</br>
Understanding of API lifecycle phases - Design, Document, Test</br></br>


### Idea 5: API Conversion API</br>
Aggregating all of the OpenAPI conversion tooling that exists out there into a single API conversion solution that will convert all API formats similar to API Transformer - https://www.apimatic.io/transformer/, publishing as a single API that can be hosted and operated by anyone as an open source conversion solution.

**Use case:**</br>
There is no open source solution that provides conversion among all formats in one place. There are a lot of open source CLI tools - https://github.com/postmanlabs/openapi-to-postman, https://github.com/postmanlabs/swagger2-postman2, APIs, apps that have converters but the idea is to have a common interface for all of them.

**Required knowledge:**</br>
Depends on the tech stack used by existing converters</br>
Comfortable with building APIs and learning how to build an API on top of existing converters</br>
Exposure to frontend technologies to build the UI for the conversions.</br>
Willingness to learn about different API formats - swagger, raml, openapi</br></br>


### Idea 6: Contributing to Postman Public Workspace</br>
https://www.postman.com/api-evangelist/workspace/openapi/overview </br>

The workspace above has a list of tasks/ideas that could serve as utilities for managing OpenAPI specifications eg. cleanup tasks, adding default responses.
Similarly, there are other public workspaces:</br>
Managing Postman collections - https://www.postman.com/api-evangelist/workspace/collections/overview</br>
Managing Postman environments - https://www.postman.com/api-evangelist/workspace/environments/overview</br>

**Expectation:**</br>
Build utilities for managing Postman entities (OpenAPI definitions/collections/environments). These utilities could be scripts embedded in Postman requests/collections or an open source project eg. openapi-utils.

**Required knowledge:**</br>
Should be familiar with or willing to learn how to use the Postman API, OpenAPI concepts. Hands-on experience with Javascript is necessary. Some familiarity with version control (https://learning.postman.com/docs/collaborating-in-postman/version-control-for-collections/) in Postman would help in managing contributions.</br></br>
 
### Idea 7: Simple schema registry</br>
Provide a simple implementation of the schema registry API (https://github.com/cloudevents/spec/blob/master/schemaregistry/schemaregistry.md) and showcase how this can be used with AsyncAPI document and schema references. It can do an in-memory persistence for schemas as it would be used purely for showcases, and learning materials.

**Use case:**</br>
In AsyncAPI file you can provide schemas for the payload of the message. Those schemas can be shared between different applications, meaning, different AsyncAPI files. Schema registries that store such shareable schemas are becoming a de-facto standard. Would be great to have a simple mock implementation of such a schema to show how it would work with AsyncAPI documents.

**Required knowledge:**</br>
You do not need any specific deep knowledge of any subject here. You will only have to provide an implementation of this API (https://github.com/cloudevents/spec/blob/master/schemaregistry/schemaregistry.yaml). It is not supposed to be a production-ready implementation, but only for testing and showcasing. Knowledge about how to use this registry with AsyncAPI is something that you can learn while working on the task with mentor support. There is not specific repository where you can place the code. It is something that can be decided anytime during development.</br></br>

### Idea 8: Duplications discovery - optimizer</br>
Build a library that code-first users would benefit from the most but not only. A library that as the input gets AsyncAPI document and as output provides optimized AsyncAPI document. </br></br>
For example:</br>
Reuse of components</br>
Duplicated schemas moved to components and ref-ed from a message</br>
Remove not used components</br>
The goal is to shrink the document to a minimum. There should be flags to disable specific parts of optimization, like removal of not used components for example.

**Use case:**</br>
AsyncAPI offers many different ways to reuse certain parts of the document like messages or schemas definitions or references to external files, not to even mention the traits. There is a need for a tool that can be plugged into any workflows and optimize automatically documents that are generated from code. 

**Required knowledge:** </br>
This task will require you to learn some details about the AsyncAPI spec to understand what parts can be componentized and how reuse works in the spec. This knowledge will be essential to be able to apply optimizations. You will for sure have to go through our getting stated (https://www.asyncapi.com/docs/getting-started) guides and later the spec (https://www.asyncapi.com/docs/specifications/2.0.0). Mentors will be available for any questions and setting directions.
We already started work on the CLI so before summer there will be enough to plug in this functionality https://github.com/asyncapi/cli  </br></br>

### Idea 9: AsyncAPI Diff</br>
A library that as the input gets two AsyncAPI documents and shows changes between them. As an output, you get json pointers to sections that are different. The main purpose of such a tool is a changelog where you can present to the user what has changed between v1 and v2 of the document. Some ideas can be picked up from https://github.com/OpenAPITools/openapi-diff  </br>
We basically need a library that can be later used to build such a UI (http://www.jsondiff.com/)

**Use case:**</br>
The result of diff is a part of changelog/release notes, so users can easily spot what parts of the document changed so they can understand how affected they are by the change</br>
Diff is needed in a review process, so the reviewer gets an overview of specification changes

**Required knowledge:**</br>
There is not much knowledge about the spec itself needed. It is about pointing out differences in 2 different files, but not as pointing what lines changed but in general what objects changed. So if there was an update in payload, the library must specify what channel in what message got updated (with json pointers most probably). You can familiarize with other tools that do it already for other specifications.
We already started work on the CLI so before summer there will be enough to plug in this functionality https://github.com/asyncapi/cli </br></br>

### Idea 10: AsyncAPI Applications Relations Finder</br>
A library that as the input gets a list of AsyncAPI documents and analyzes them to get information about Applications described by those files:</br>
If they subscribe or publish to the same channels</br>
If one subscribes to a channel that the other one publishes to</br>
If there are apps that are subscribed to channels that no one publishes too</br>
As an output, we should get a format that can be used to generate a diagram of relations between applications with additional metadata information about them (message, schemas).</br>
 
**Use case:**</br>
Visualization of the architecture and understanding what happens with the system if one of the puzzles is removed.</br>
Later on, we could use this library in AsyncAPI CLI and also the AsyncAPI Studio.</br>

**Required knowledge:**</br>
There is no need to have any experience in event-driven architecture. You do not even need to know AsyncAPI spec too much. It is a pure coding task where you will need to find matching patterns between different documents and return this information. You will have the full support of the mentor on the subject. Mentors will define requirements, etc.</br>
There is no decision yet if this is a library that will have to live in a separate repository or be a part of an existing CLI or UI project.</br>
We already started work on the CLI so before summer there will be enough to plug in this functionality asyncapi/cli (https://github.com/asyncapi/cli)</br></br>
 
### Idea 11: AsyncAPI Extensions registry</br>
Provide an implementation of the extensions registry for AsyncAPI. This task includes action points:</br>
- improve the shape/definition of the single extension (describe it by JSON Schema) - reference asyncapi/extensions-catalog (https://github.com/asyncapi/extensions-catalog)</br>
- like for schema registry: implement an extensions registry API</br>
- add support in parser-js </br>
-  -asyncapi/parser-js (https://github.com/asyncapi/parser-js)- for validation of extension against provided extension schema </br></br>
 
**Required knowledge:**</br>
The main contribution will go into the parser. So you will have to first onboard on the project with few basic tasks handed over by the mentor. The rest will be explained by the mentor. </br></br>

### Idea 12:  Chatbot for AsyncAPI creators</br>
Explore how we could help people to write the spec document without knowing the specification. Prepare a kind of prototype. Instead of learning the spec, users talk to a chatbot, and as a result of the conversation, they get an AsyncAPI document generated. The chatbot should learn from the specification what are the possible solutions and options.

**Use case:**</br>
Learning the AsyncAPI spec (https://github.com/asyncapi/asyncapi/blob/master/versions/2.0.0/asyncapi.md) can be a time-consuming process. This is what causes learning of every new specification hard. Let’s explore if we can have a machine that can consume the spec, its JSON schema and serve the users as an expert. Based on a set of questions and answers it should generate an AsyncAPI document for the user.</br>

Example conversation: (real-time we show a preview of the AsyncAPI document that will be generated)</br>
Bot: what do you want to describe?</br>
User: app that connects with kafka?</br>
Bot: can you provide some more details about the kafka server? Like the url?</br>
User: no</br>
Bot: no problem, let us skip the server details for now. What topics does your app subscribe to?</br>
 
**Visible challenges:**</br>
Vocabulary: bot needs to know that AsyncAPI channels mean topic in Kafka</br>
Real-time object generation</br>
Vocabulary: understand that bot needs to ask questions “subscribe to” but in document write it as “publish” operation</br>
 
**Required knowledge:**</br>
This project requires you to have a basic knowledge about the location of spec related materials that could be used to feed the bot. This is a research task that only requires a prototype to see if this is even possible or what is missing to make it possible. As prerequisite you of course need to read about current technologies that are available for building a chatbot. </br></br>

### Idea 13: AsyncAPI application simulation</br>
A simulation library that can trigger events in your applications based on AsyncAPI definition(s). The main purpose is to stimulate your application(s) in a development environment (staging?). Use it for stress testing, hunting down concurrency problems, stimulating visual applications, finding scalability issues in your application and more.</br></br>
You provide one or more AsyncAPI files</br>
You decide which channel(s) and applications should be stimulated and with which parameters.</br>
The library simulates messages to the application(s) based on the parameters, in the given protocol described in the AsyncAPI file. </br>
Inspect the application(s) and their state to figure out if errors occurred etc
 
**Extra thoughts: **</br>
Can it be used directly in a system test so you can decide on the expected outcome? </br></br>

**Required knowledge:**</br>
You need to learn the spec basics (what channels are). It will be useful to learn first how to set up environments with Docker compose and mocks and a proper testing environment will have to be created first to work on the implementation and load generation.


