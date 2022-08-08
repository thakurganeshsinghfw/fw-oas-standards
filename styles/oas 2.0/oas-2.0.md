# Freshworks OpenAPI 2.0 Style Guide

## What is Open API 2.0 standard?

Open API standard (OAS) is a RESTful API Documentation Specification defined under Swagger™ project. The Swagger specification is licensed under [The Apache License, Version 2.0](http://www.apache.org/licenses/LICENSE-2.0.html). The detailed specification can be found [here](https://github.com/OAI/OpenAPI-Specification/blob/main/versions/2.0.md#specification)

## What is linting?

API linting is the process of making sure that APIs are not just technically correct, but that they also comply with a set of additional constraints that often are documented in the form of API guidelines.

## What is Spectral?

Spectral is an open-source API linting tool by [Stoplight](https://stoplight.io/) that allows users to create custom style guides to enforce validations on API design automatically. Typically, these would be in description languages such as OpenAPI, AsyncAPI, or JSON Schema.

## Where can I find these linting rules for Freshworks OAS 2.0 API's?

The standard industry rules for OAS specification can be found [here](https://meta.stoplight.io/docs/spectral/4dec24461f3af-open-api-rules#openapi-rules).

The Linting rules for Freshworks products can be found [here](https://github.com/freshworks/oas-style-guide). Freshworks internal lint rules to validate Open API 2.0 Specification using [Spectral](https://stoplight.io/open-source/spectral/). This extends ***spectral:oas*** package and adds custom rules on top of it.

## Usage

### Extending this style guide

#### YAML

```yaml
extends:
    - https://unpkg.com/@freshworks/oas
rules:
    ...
```

#### JSON

```json
     {
        "extends": [
            "https://unpkg.com/@freshworks/oas"
        ],
        "rules": {
            ...
        }
    }
```

## Rules

Some rules are used from ***spectral:oas*** as it is and overridden the severity to **ERROR**. Rules that are not extended from ***spectral:oas*** will have prefix `fw-`.

> Severity is set to **ERROR** for all rules defined below. Individual  
> projects can override severity level to suit their needs.

### info-description

OpenAPI object info `description` must be present and non-empty string.

### info-contact

Info object should contain `contact` object.

### operation-tags

Operation should have non-empty `tags` array.

### operation-tag-defined

Operation tags should be defined in global tags.

### operation-operationId

Operation should have an `operationId`.

### fw-info-license

Info object should contain `license` object

### fw-operation-summary

Each operation should have `summary`

## fw-schema-properties-example

Schema properties should have an example value defined

### fw-properties-underscore-case

Schema properties should be in underscore case

### fw-ensure-no-legacy-tags

Tags should not have legacy in its name

### fw-path-kebab-case

Path should be in kebab case.

> Private APIs follows the convention of `/api/_/...` . One underscore (`_`) followed by `/api/` is allowed for private APIs as an exception.

### fw-path-param-underscore-case

Path parameter should be in underscore case

### fw-query-param-underscore-case

Query parameter should be in underscore case

### fw-form-param-underscore-case

Form data parameter should be in underscore case
