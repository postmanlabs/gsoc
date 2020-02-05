Postman in Google Summer of Code 2020 - Ideas
=============================================

## Project Ideas

We accept original ideas and proposals for every project. Following is a list of ideas which you can use as a reference.

### Newman

### Collection SDK

### Code Generators

* **Collection-level codegen**: Convert a Postman collection to a client SDK. Work on a module that utilizes Postman's existing code-generators to create an SDK for an entire collection, not just a request. This could be extremely beneficial to advanced users.

* **Generate an Axios/Superagent snippet from a Postman request**: This is a very popular feature request from our community - https://github.com/postmanlabs/postman-app-support/issues/3822 and https://github.com/postmanlabs/postman-app-support/issues/6331, and could help solve use-cases for a lot of users.

### Importers

* **Support for Links in OpenAPI3**: Links are an OpenAPI feature that provide the ability to define custom workflows. This fits in well with Postman's collections, where you can use the in-built API to create branching/looping in workflows. If implemented correctly, links could truly bridge the gap between a workflow definition in OAS, and a working collection in Postman.

* **SoapUI conversion to Postman's collection format**: SoapUI is a popular SOAP API platform. It supports WSDL export, and that's something we'd like to include as a format Postman supports. WSDL is really extensive, so this will require research around what's possible with WSDL, and how you'd want to perform the conversion.

* **AsyncAPI conversion to Postman's collection format**: AsyncAPI is an upcoming schema format that supports messaging-based API communication patterns. It's a relatively new format, and a working converter would require a thorough exploration of webhooks and Postman features you'd like to implement from a spec.

## Contact

If you have any questions or queries please create an issue on this project (with a prefix GSoC 2020) or send an email to us at gsoc@postman.com