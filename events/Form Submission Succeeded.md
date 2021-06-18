# Form Submission Succeeded

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Form Submission Succeeded",
    "form": {
        "formID": "<formID>",
        "formName": "<formName>",
        "formType": "<formType>"
    },
    "locationList": [
        {
            "locationId": "<locationId>",
            "locationName": "<locationName>"
        }
    ],
    "transaction": {
        "transactionID": "<transactionID>"
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|formID|string|Unique identifier of a form. |F-0113, 2543, CU001, PI-0988|||||||
|formName|string|Plain text form name. Generally used if formID is not obtainable. |Payment Info, Mailing Address, Payment Address, Contact Us|||||||
|formType|string|Form type used for grouping of similar forms in reports.  |Address, Contact, Comment, Review, Payment|||||||
|locationId|string|Unique Identifier of a Location. |155, 65588, 987764448|||||||
|locationName|string|The friendly name of the location.|Deerefiled Outlet, Old Orchard, Manhatten Midtown|||||||
|transactionID|string|Unique identifier of the transaction. Max Length 100. Used as a key for upload of post transaction data. |123e4567-e89b-12d3-a456-426614174000|^[a-zA-Z0-9]{6,100}$|6|100||||
