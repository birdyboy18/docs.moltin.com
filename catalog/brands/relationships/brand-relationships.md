# Brand Relationships

{% api-method method="post" host="https://api.moltin.com" path="/v2/brands/:id/relationships/brands" %}
{% api-method-summary %}
Create Brand Relationships
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="id" type="string" required=true %}
The **ID** of the brand you want to modify relationships for
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
The Bearer token to grant access to the API
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="parent.type" type="string" required=true %}
The type of the related object \(should be `brand`\)
{% endapi-method-parameter %}

{% api-method-parameter name="parent.id" type="string" required=true %}
The **ID** of the parent brand
{% endapi-method-parameter %}

{% api-method-parameter name="children\[\].type" type="string" required=true %}
The type of related object \(should be `brand`\)
{% endapi-method-parameter %}

{% api-method-parameter name="children\[\].id" type="string" required=true %}
The **ID** of the brand
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% tabs %}
{% tab title="cURL" %}
```bash
curl -X POST https://api.moltin.com/v2/brands/:id/relationships/brands \
     -H "Authorization: Bearer XXXX" \
     -H "Content-Type: application/json" \
     -d $'{
        "data": {
            "parent": {
                "type": "brand",
                "id": "8a43aea7-79f0-4bcf-9bc8-a0f5d3d3642c"
            },
            "children": [
                {
                "type": "brand",
                "id": "1334e667-7b2b-4159-9e36-8a3b404901c8"
                }
            ]
            }
        }'
```
{% endtab %}
{% endtabs %}

