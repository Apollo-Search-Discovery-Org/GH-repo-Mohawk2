# Order Placed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Order Placed",
    "cart": {
        "cartID": "<cartID>"
    },
    "transaction": {
        "item": [
            {
                "price": {
                    "sellingPrice": "<sellingPrice>"
                },
                "productInfo": {
                    "isGiftWrapped": "<isGiftWrapped>",
                    "productID": "<productID>"
                },
                "quantity": "<quantity>",
                "voucherDiscount": {
                    "orderLevelDiscountCode": "<orderLevelDiscountCode>"
                }
            }
        ],
        "payment": [
            {
                "paymentAmount": "<paymentAmount>",
                "paymentID": "<paymentID>",
                "paymentMethod": "<paymentMethod>",
                "paymentSequence": "<paymentSequence>"
            }
        ],
        "profile": {
            "address": {
                "country": "<country>",
                "postalCode": "<postalCode>",
                "stateProvince": "<stateProvince>"
            }
        },
        "purchaseID": "<purchaseID>",
        "total": {
            "currency": "<currency>",
            "numPayments": "<numPayments>"
        }
    }
});
```

## Variable Definitions

|Field|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|cartID|string|Back-end identifier for a shopping cart|12345, 435678, 34567, XCV456, XCV876|||||||
|country|string|Indicates the country of the billing address. ISO 3166 (alpha-2) Uppercase.|US, CA, FR, UK|^[A-Z]{2}$||||||
|currency|string|Currency of the transaction. ISO 4217 (3 character alpha), uppercase |USD, CAD, GBP, CHF|^[A-Z]{3}$|3|3||||
|isGiftWrapped|boolean|At order confirmaton, set a to true for every product that is gift wrapped.||||||||
|numPayments|integer|Collects the number of payment methods used for an order at order confirmaton||||||||
|orderLevelDiscountCode|string|Order Level Discount code applied at the item level of a transaction. |FRIENDSANDFAMILY20, EASTER10|||||||
|paymentAmount|string|String representation of the payment amount. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|paymentID|string|Unique identifier of a payment.  Typically an integration key from a back-end system.|ZPH-87698-098|||||||
|paymentMethod|string|Describes the method of payment for a transaction. |Credit Card, PayPal, Mastercard, Visa, Amex, Discover|||||||
|paymentSequence|integer|Integer indicator of the sequence in which payments were applied within a transaction.  Starting with 1.|1, 2, 3, 4, 5||||1|||
|postalCode|string|The mailing zip or postal code associated with the billing address. |53533, 30381, M1R 0E9, M3C 0C1|||||||
|productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|purchaseID|string|Unique identifier of the purchase. Max Length 20. Used as Unique ID of the purchase or deduplication.|ABC-132456789, DEF-132456789, 0987654567|^[a-zA-Z0-9]{6,20}$|6|20||||
|quantity|integer|Integer number of products being acted upon (added to a cart, removed from wishlist, purchased, reserved)|1, 2, 3, 4, 5||||1|||
|sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|stateProvince|string|The mailing state or province associated with billing address. |WI, GA, NB, ON|||||||
