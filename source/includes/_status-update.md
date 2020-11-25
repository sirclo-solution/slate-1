# Status Update

##Order Status UPdate

### HTTP Request

`POST /klog/v1/operation/status-update`

### Request Body Parameters

Request body must be a JSON document with the following properties

| Section | Node   | Subnode  | Description | Map to Odoo | Expected Value | Required | 
| ----- | ------| ------| ---------------------------------| ------------------ | ----| --- | 
| basic details|bookingNo||Booking No (BookingNo as specified by Inbound/Outbound Booking) |*sale_id.partner_id.name + sale_id.client_order_ref*, **Suggested pattern:** *{partner_name}-{client_order_ref}* (Masing2 bagian hanya mengandung karakter alfanumerik (alfabet atau angka) tanpa karakter lainnya.)|Alphanumeric| Yes | 
| | timestamp |  | Format = ISO8601, in UTC (eg: 2020-05-26T10:24:46Z for May 26 at 10:24:46 AM) | x_module_status_updated_timestamp ( Not Exist )| Alphanumeric| Yes|
||status||Waiting or Allocated|Booking Status ( state )|Waiting or Allocated| Yes
||messageId||unique number to identify integration message| Generate UUID (Universally Unique Indentifier) |UUID (Universally Unique Identifier) | Yes|

> Request body example:

```json
{
  "basicDetails": {
    "bookingNo": "20200811_081455_budi",
    "timestamp": "2020-11-18T09:45:08.266Z",
    "status": "Waiting",
    "messageId": "65a9df59-c64d-4h20-6b8c-ac5c007f9223"
  }
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
