# Purchase

### 

## Event Firing Instructions

<p>Fires on form confirmation page.</p>
<p>We then use Google Tag Manager to grab the values passed in the data layer below and pass to Google Analytics.</p>

## Javascript Code
```js
window.dataLayer = window.dataLayer || [];
dataLayer.push({ ecommerce: null });  // Clear the previous ecommerce object.
dataLayer.push({
  "event": "purchase",
    "ecommerce": {
        "value": "<value>",
        "currency": "<currency>",
        "transaction_id": "<transaction_id>"
    }
});
```


## Variable Definitions

|Name|Type|Description|Example|
| --- | --- | --- | --- |
|ecommerce.value|number|Total value of gift. Dynamic value. |1750|
|ecommerce.currency|string|The currency, in 3-letter ISO 4217 format. |USD|
|ecommerce.transaction_id|string or number - depending on format|The ID from the transaction, if available. If not, you can remove this line of code. |1234|


