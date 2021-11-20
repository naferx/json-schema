# JSON Schema

Personal notes exploring [JSON Schema](https://json-schema.org/)

## Description

> JSON Schema is a vocabulary that allows you to annotate and validate JSON documents.


## Use cases
- Describes your existing data format(s).
- Provides clear human- and machine- readable documentation.
- Validates data which is useful for:
   - Automated testing.
   - Ensuring quality of client submitted data.



## Notes
JSON Schema is a proposed IETF standard that provides metadata and describes JSON data


### Terminology

Schema Keyword: $schema and $id.

Schema Annotations: title and description.

Validation Keyword: type.


For this JSON

    {
        "productId": 1,
        "productName": "A green door",
        "price": 12.50,
        "tags": [ "home", "green" ]
    }


The corresponding JSON Schema would be:

        {
            "$schema": "https://json-schema.org/draft/2020-12/schema",
            "$id": "https://example.com/product.schema.json",
            "title": "Product",
            "description": "A product from Acme's catalog",
            "type": "object",

            "properties": {
                "productId": {
                    "description": "The unique identifier for a product",
                    "type": "integer"
                }
            },
            "required": [ "productId" ]
        }



## References
 - https://json-schema.org/blog/posts/bundling-json-schema-compound-documents
