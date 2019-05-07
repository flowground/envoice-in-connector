# ![LOGO](logo.png) API v1.0.0 **flow**ground Connector

## Description

A generated **flow**ground connector for the API v1.0.0 API (version v1).

Generated from: https://api.apis.guru/v2/specs/envoice.in/v1/swagger.json<br/>
Generated at: 2019-05-07T17:40:21+03:00

## API Description

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/1d39bbcddaf694d81100)
<span style='margin-left: 0.5em;'>or</span>
<a href='https://documenter.getpostman.com/view/3559821/envoice-api/RW1XL1mf' class='openapi-button' _ngcontent-c6>View Postman docs</a>

# Quickstart

Visit [github](https://github.com/EmitKnowledge/Envoice) to view the quickstart tutorial.

<div class='postman-tutorial'>

# Tutorial for running the API in postman

Click on ""Run in Postman"" button
<br /><br />
![postman - tutorial - 1](/Assets/images/api/postman-tutorial/postman-tutorial-1.png)

 --- 

A new page will open.
Click the ""Postman for windows"" to run postman as a desktop app.
Make sure you have already [installed](https://www.getpostman.com/docs/postman/launching_postman/installation_and_updates) Postman.
<br /><br />
![postman - tutorial - 2](/Assets/images/api/postman-tutorial/postman-tutorial-2.png)

 --- 

In chrome an alert might show up to set a default app for opening postman links. Click on ""Open Postman"".
<br /><br />
![postman - tutorial - 3](/Assets/images/api/postman-tutorial/postman-tutorial-3.png)

 --- 

The OpenAPI specification will be imported in Postman as a new collection named ""Envoice api""
<br /><br />
![postman - tutorial - 4](/Assets/images/api/postman-tutorial/postman-tutorial-4.png)

 --- 

When testing be sure to check and modify the environment variables to suit your api key and secret. The domain is set to envoice's endpoint so you don't really need to change that.  
<sub>\*Eye button in top right corner </sub>
<br /><br /> 
![postman - tutorial - 5](/Assets/images/api/postman-tutorial/postman-tutorial-5.png)
<br /><br /> 
![postman - tutorial - 6](/Assets/images/api/postman-tutorial/postman-tutorial-6.png)

 --- 

You don't need to change the values of the header parameters, because they will be replaced automatically when you send a request with real values from the environment configured in the previous step.
<br /><br />
![postman - tutorial - 7](/Assets/images/api/postman-tutorial/postman-tutorial-7.png)

 --- 

Modify the example data to suit your needs and send a request.
<br /><br />
![postman - tutorial - 8](/Assets/images/api/postman-tutorial/postman-tutorial-8.png)
</div>

# Webhooks

Webhooks allow you to build or set up Envoice Apps which subscribe to invoice activities. 
When one of those events is triggered, we'll send a HTTP POST payload to the webhook's configured URL. 
Webhooks can be used to update an external invoice data storage.

In order to use webhooks visit [this link](/account/settings#api-tab) and add upto 10 webhook urls that will return status `200` in order to signal that the webhook is working.
All nonworking webhooks will be ignored after a certain period of time and several retry attempts.
If after several attempts the webhook starts to work, we will send you all activities, both past and present, in chronological order.

The payload of the webhook is in format:
```
{
    Signature: ""sha256 string"",
    Timestamp: ""YYYY-MM-DDTHH:mm:ss.FFFFFFFZ"",
    Activity: {
        Message: "string",
        Link: "share url",
        Type: int,        
        InvoiceNumber: "string",
        InvoiceId: int,        
        OrderNumber: "string",
        OrderId: int,
        Id: int,
        CreatedOn: "YYYY-MM-DDTHH:mm:ss.FFFFFFFZ"
    }
}
```            

## Authorization

Supported authorization schemes:
- API Key- API Key
## Actions

### Return all clients for the account

*Tags:* `Client`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Check if the provided client can be deleted

*Tags:* `Client`

#### Input Parameters
* `id` - _required_
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Delete an existing client

*Tags:* `Client`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return client details. Activities and invoices included.

*Tags:* `Client`

#### Input Parameters
* `id` - _required_
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Create a client

*Tags:* `Client`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Update an existing client

*Tags:* `Client`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return all of the platform supported countries

*Tags:* `General`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return all of the platform supported currencies

*Tags:* `General`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return all of the platform supported Date Formats

*Tags:* `General`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return all of the platform supported UI languages

*Tags:* `General`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return all invoices for the account

*Tags:* `Invoice`

#### Input Parameters
* `queryOptions.page` - _optional_
* `queryOptions.pageSize` - _optional_
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Change invoice status

*Tags:* `Invoice`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Delete an existing invoice

*Tags:* `Invoice`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return invoice data

*Tags:* `Invoice`

#### Input Parameters
* `id` - _required_
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Create an invoice

*Tags:* `Invoice`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Send the provided invoice to the accountant

*Tags:* `Invoice`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Send the provided invoice to the client

*Tags:* `Invoice`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Retrieve the status of the invoice

*Tags:* `Invoice`

#### Input Parameters
* `id` - _required_
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Update an existing invoice

*Tags:* `Invoice`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return the unique url to the client's invoice

*Tags:* `Invoice`

#### Input Parameters
* `id` - _required_
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return all orders for the account

*Tags:* `Order`

#### Input Parameters
* `queryOptions.page` - _optional_
* `queryOptions.pageSize` - _optional_
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Change order shipping details

*Tags:* `Order`

#### Input Parameters
* `orderId` - _required_
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Change order status

*Tags:* `Order`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Delete an existing order

*Tags:* `Order`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return order details

*Tags:* `Order`

#### Input Parameters
* `id` - _required_
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Create an order

*Tags:* `Order`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return all supported payment gateways (no currencies means all are supported)

*Tags:* `Payment`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return all products for the account

*Tags:* `Product`

#### Input Parameters
* `queryOptions.page` - _optional_
* `queryOptions.pageSize` - _optional_
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Delete an existing product

*Tags:* `Product`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return product details

*Tags:* `Product`

#### Input Parameters
* `id` - _required_
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Create a product

*Tags:* `Product`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Update an existing product

*Tags:* `Product`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return all taxes for the account

*Tags:* `Tax`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Delete an existing tax

*Tags:* `Tax`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Create a tax

*Tags:* `Tax`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Update an existing tax

*Tags:* `Tax`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return all work types for the account

*Tags:* `WorkType`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Delete an existing work type

*Tags:* `WorkType`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return work type details

*Tags:* `WorkType`

#### Input Parameters
* `workTypeId` - _required_
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Create a work type

*Tags:* `WorkType`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Return all work types for the account that match the query param

*Tags:* `WorkType`

#### Input Parameters
* `queryOptions.query` - _optional_
* `queryOptions.orderBy` - _optional_
* `queryOptions.order` - _optional_
    Possible values: None, Asc, Desc.
* `queryOptions.page` - _optional_
* `queryOptions.pageSize` - _optional_
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

### Update an existing work type

*Tags:* `WorkType`

#### Input Parameters
* `x-auth-key` - _required_
* `x-auth-secret` - _required_

## License

**flow**ground :- Telekom iPaaS / envoice-in-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
