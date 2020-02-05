Postman in Google Summer of Code 2020 - Ideas
=============================================

## Project Ideas

We accept original ideas and proposals for every project. Following is a list of ideas which you can use as a reference.

### Newman

* **Newman login**: Add support for a new `newman login` command to be an alternative to the conventional way of using cloud URLs to run collections. It will allows users to login with their API key from CLI and simply run collections by providing their unique IDs. This will also require dedicated security considerations to ensure safety of user's Postman API key.

* **Create new or update existing reporters**: Newman reporters provide information about the current collection run in a format that is easy to both: disseminate and assimilate. Create new external reporters or update existing reporters like `newman-reporter-html`. Working examples of how Newman reporters work can be found here - https://github.com/postmanlabs/newman/tree/develop/lib/reporters

### Collection SDK + Runtime
* **Support for more request body methods**: Add support for different request body serialization techniques like Protocol Buffers, JSON RPC, etc. in Postman runtime library. Support for protobuf is one of the most request feature from our comunity - https://github.com/postmanlabs/postman-app-support/issues/2801

* **Support for different authentication schemes**: Add support for different authentication schemes like JWT, NTLM Kerberos, etc.
Steps to be done to add a new auth mechanism https://github.com/postmanlabs/postman-runtime/blob/develop/docs/new-auth-mechanisms.md

### Code Generators

* **Collection-level codegen**: Convert a Postman collection to a client SDK. Work on a module that utilizes Postman's existing code-generators to create an SDK for an entire collection, not just a request. This could be extremely beneficial to advanced users.

* **Generate an Axios/Superagent snippet from a Postman request**: This is a very popular feature request from our community - https://github.com/postmanlabs/postman-app-support/issues/3822 and https://github.com/postmanlabs/postman-app-support/issues/6331, and could help solve use-cases for a lot of users.

### Importers

* **Support for Links in OpenAPI3**: Links are an OpenAPI feature that provide the ability to define custom workflows. This fits in well with Postman's collections, where you can use the in-built API to create branching/looping in workflows. If implemented correctly, links could truly bridge the gap between a workflow definition in OAS, and a working collection in Postman.

* **SoapUI conversion to Postman's collection format**: SoapUI is a popular SOAP API platform. It supports WSDL export, and that's something we'd like to include as a format Postman supports. WSDL is really extensive, so this will require research around what's possible with WSDL, and how you'd want to perform the conversion.

* **AsyncAPI conversion to Postman's collection format**: AsyncAPI is an upcoming schema format that supports messaging-based API communication patterns. It's a relatively new format, and a working converter would require a thorough exploration of webhooks and Postman features you'd like to implement from a spec.

## Contact

If you have any questions or queries please create an issue on this project (with a prefix GSoC 2020) or send an email to us at gsoc@postman.com
