# Freshworks OpenAPI Style Guide

> This document details the API standard and guidelines defined as part of Freshworks products.

Freshworks products use REST architectural standard for building API capabilities in to our products. There are 2 REST API standards supported in Freshworks products for defining the API specifications namely [OpenAPI 2.0](https://github.com/OAI/OpenAPI-Specification/blob/main/versions/2.0.md) (formerly Swagger) and [Open API 3.0](https://swagger.io/specification/#:~:text=The%20OpenAPI%20Specification%20(OAS)%20defines,or%20through%20network%20traffic%20inspection)

For onboarding and adding support for Documentation and SDK, the product teams need to ensure the below list of items are met.

## Overview of Freshworks API Onboarding process

![Freshworks API Onboarding process](/assets/API-onboarding-process.svg)
## Tech Writing onboarding checklist

### Prerequisites

- [ ] Product is currently supported by Tech writing team and has it's own API Doc Portal. Eg. [Freshteam](https://www.freshworks.com/hrms/hr-software/) has [Freshteam API Docs](https://developers.freshteam.com/api/).
- [ ] Product supports RESTful API's. Alternative architectural standards such as FALCOR, gRPC, Apache Thrift, GraphQL, OData etc are currently not supported.
- [ ] Product API Specification are written in one of the 2 supported standards. [Open API 2.0 standard](/styles/oas%202.0/oas-2.0.md) or [Open API 3.0 standard](/styles/oas%203.x.x/oas-3.x.x.md). The other common API documentation standards such as [RAML](https://raml.org/), [JsonAPI](https://jsonapi.org/), [OData](https://www.odata.org/) etc are currently not supported
- [ ] Written Specification adheres to [Freshworks API Guidelines](https://confluence.freshworks.com/display/PLAT/API+Design+Guidelines)
- [ ] The product API specs are available on [Freshworks Stoplight workspace](https://freshworks.stoplight.io/).
- [ ] API methods must have `tags` and `summary` against all the mentioned endpoints. Optionally they can have a quick summary of API behaviour.

### Access and resources

- [ ] The `Tech Writing` team is provided with necessary read and write privieges to the stoplight project. For details on members kindly reach out to [Menaka Lekshmiganthan](mailto:menaka.lekshmiganthan@freshworks.com)
- [ ] The necessary authentication credentials for respective product API servers are shared with `Tech Writing` team to test the API's. Eg. Freshteam uses a live server say [https://some-subdomain.freshteam.com/api](https://some-subdomain.freshteam.com/api) that uses ApiKey for authentication and authorization say `Authorization:123`.
- [ ] A Technical POC for respective product team is assigned to provide support around technical doubts and API functionality.

## DevRel API SDK onboarding checklist

### DevRel Prerequisites

- [ ] API methods must have `tags` and `summary` against all the mentioned endpoints. Optionally they can have a quick summary of API behaviour.
- [ ] A Technical POC for respective product team is assigned to provide support around technical doubts and API functionality.
- [ ] The API specs must cover all the possible output scenarios. These may include standard HTTP Status codes or custom HTTP codes returned by product API's. Eg. `20001`-`New entry has been made`, `20002`-`Entry has been updated`, etc.
- [ ] Tech Writing onboarding checklist is met successfully.
- [ ] Optionally, API Docs draft or finalized version is available on respective API Docs portal.

### DevRel Access and resources

- [ ] The `DevRel` team is provided with necessary read and write privieges to the stoplight project. For details on members kindly reach out to [DevRel Team](mailto:devrel@freshworks.com)
- [ ] The `DevRel` team is provided with necessary read and write privieges to respective Git repositories
- [ ] A Technical POC for respective product team is assigned to provide support around technical doubts and API functionality.
- [ ] Optionally, If API methods supported are too large, and product has critical timeline for SDK delivery, then respective product team must assign additional engineering capacity as Contributers to the [API SDK project](https://github.com/freshworks/freshworks-api-sdk).
- [ ] Contributers must be familiar with these [contribution guidelines](https://github.com/freshworks/freshworks-api-sdk/blob/main/CONTRIBUTING.md)
