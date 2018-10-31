# Main Image Relationship

{% api-method method="post" host="https://api.moltin.com" path="/v2/products/:productId/relationships/main-image" %}
{% api-method-summary %}
Create a Main Image Relationship
{% endapi-method-summary %}

{% api-method-description %}
Create a Product relationship to a single File, which can be used as a main\_image.  You can only have one main image relationship.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="productId" type="string" required=true %}
The **ID** of the product you wish to relate to the image.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
The Bearer token used to access the API.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="data\[\].type" type="string" required=true %}
Represents the type of the object \(should be **main\_image**\).
{% endapi-method-parameter %}

{% api-method-parameter name="data\[\].id" type="string" required=true %}
The **ID** of the image.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```bash
{
    "data": [
        {
            "type": "main_image",
            "id": "8df7738-febe-4987-bc0e-b857297b30e9"
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% tabs %}
{% tab title="cURL" %}
```javascript
curl -X "POST" https://api.moltin.com/v2/products/:productId/relationships/main-image \
     -H "Authorization: Bearer XXXX" \
     -H "Content-Type: application/json" \
     -d $'{
      "data": {
        "type": "main_image",
        "id": "98df7738-febe-4987-bc0e-b857297b30e9"
      }
    }'
```
{% endtab %}

{% tab title="JavaScript SDK" %}
```javascript
const MoltinGateway = require('@moltin/sdk').gateway

const Moltin = MoltinGateway({
  client_id: 'X',
  client_secret: 'X'
})

const productId = 'XXXX'

Moltin.Products.CreateRelationships(productId, 'main-image', '98df7738-febe-4987-bc0e-b857297b30e9').then((relationships) => {
  // Do something
})
```
{% endtab %}
{% endtabs %}

{% api-method method="put" host="https://api.moltin.com" path="/v2/products/:productId/relationships/main-image" %}
{% api-method-summary %}
Update a Main Image Relationship
{% endapi-method-summary %}

{% api-method-description %}
Update the main image relationship.  This will replace any currently related image.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="productId" type="string" required=true %}
The **ID** of the product you wish to relate to the image.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
The Bearer token used to access the API.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="data\[\].type" type="string" required=true %}
Represents the type of object \(should be **main\_image**\)
{% endapi-method-parameter %}

{% api-method-parameter name="data\[\].id" type="string" required=true %}
The **ID** of the image.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```bash
{
    "data": [
        {
            "type": "main_image",
            "id": "e9737dc6-876a-4eab-b3b7-af62a1999123"
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% tabs %}
{% tab title="cURL" %}
```javascript
curl -X "PUT" https://api.moltin.com/v2/products/:productId/relationships/main-image \
     -H "Authorization: Bearer XXXX" \
     -H "Content-Type: application/json" \
     -d $'{
      "data": {
        "type": "main_image",
        "id": "e9737dc6-876a-4eab-b3b7-af62a1999123"
      }
    }'
```
{% endtab %}

{% tab title="JavaScript SDK" %}
```javascript
const MoltinGateway = require('@moltin/sdk').gateway

const Moltin = MoltinGateway({
  client_id: 'X',
  client_secret: 'X'
})

const productId = 'XXXX'

Moltin.Products.UpdateRelationships(productId, 'main-image', 'e9737dc6-876a-4eab-b3b7-af62a1999123').then((relationships) => {
  // Do something
})
```
{% endtab %}
{% endtabs %}

{% api-method method="delete" host="https://api.moltin.com" path="/v2/products/:productId/relationships/main-image " %}
{% api-method-summary %}
Delete a Main Image Relationship
{% endapi-method-summary %}

{% api-method-description %}
Delete the main image relationship. This will remove the related main image.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="productId" type="string" required=true %}
The **ID** of the product you wish to remove the relationship for.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
The Bearer token used to access the API.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="data\[\].type" type="string" required=true %}
Represents the type of object \(should be **main\_image\).**
{% endapi-method-parameter %}

{% api-method-parameter name="data\[\].id" type="string" required=true %}
The **ID** of the image.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% tabs %}
{% tab title="cURL" %}
```javascript
curl -X "DELETE" https://api.moltin.com/v2/products/:productId/relationships/main-image \
     -H "Authorization: Bearer XXXX" \
     -H "Content-Type: application/json" \
     -d $'{
      "data": {
        "type": "main_image",
        "id": "e9737dc6-876a-4eab-b3b7-af62a1999123"
      }
    }'
```
{% endtab %}

{% tab title="JavaScript SDK" %}
```javascript
const MoltinGateway = require('@moltin/sdk').gateway

const Moltin = MoltinGateway({
  client_id: 'X',
  client_secret: 'X'
})

const productId = 'XXXX'

Moltin.Products.DeleteRelationships(productId, 'main-image', 'e9737dc6-876a-4eab-b3b7-af62a1999123').then((relationships) => {
  // Do something
})
```
{% endtab %}
{% endtabs %}



