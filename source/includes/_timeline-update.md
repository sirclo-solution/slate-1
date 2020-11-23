# Timeline Update 

##Order Timeline Update

### HTTP Request

`POST //klog/v1/operation/timeline`

### Request Body Parameters

Request body must be a JSON document with the following properties

| Section | Node   | Subnode  | Description | Map to Odoo | Expected Value | Required | 
| ----- | ------| ------| ---------------------------------| ------------------ | ----| --- | 
| basic details|bookingNo||Booking No (BookingNo as specified by Inbound/Outbound Booking) |*sale_id.partner_id.name + sale_id.client_order_ref*, **Suggested pattern:** *{partner_name}-{client_order_ref}* (Masing2 bagian hanya mengandung karakter alfanumerik (alfabet atau angka) tanpa karakter lainnya.)|Alphanumeric| Yes | 
||messageId||unique number to identify integration message| Generate UUID (Universally Unique Indentifier) |UUID (Universally Unique Identifier) | Yes|
|[Loop] checkpoints|type|Checkpoint type|Activity type based on Below table (eg. : Order Processing, Warehouse, Outbound, Courier Handover, etc)|Text | Yes
||start |Checkpoint timestamp, ISO8601, in UTC|Start time of activity (eg: 2020-05-26T10:24:46Z for May 26 at 10:24:46 AM)|Alphanumeric|Yes
||end |Checkpoint timestamp, ISO8601, in UTC|End time of activity (eg: 2020-05-26T10:24:46Z for May 26 at 10:24:46 AM)|Alphanumeric|Yes

> Request body example:

```json
{
  "basicDetails": {
    "bookingNo": "20200811_081455_budi",
    "messageId": "52a9df58-h62c-8b10-8b3v-ag5c007f9115"
  },
  "checkpoints": [
    {
      "type": "string",
      "start": "2020-11-19T08:43:14.442Z",
      "end": "2020-11-19T08:43:14.442Z"
    }
  ]
}
```

### Responses 

|Code| Description 
|----|---------------------
| 200| Request acknowledged 


> The above request returns JSON structured like this:

```json
{"200" : "Request acknowledged"}
```
