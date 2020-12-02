# Outbound Request 

## Booking Inbound Request 

### Header Request 

|Section | Mapping Description | 
|--------|-----------------------------|
| MessageTYpe | Fixed 
| MessageVersion | If multiple version then provide the version no 
| MessageIdentifier | Unique number to identify integration message 
| MessageDateTime | Message date time 

### Bookings Request 
Request body must be a JSON document with the following properties

| Section | Node   | Subnode  | Description | Expected Value | Required 
| ----- | ------| ------| ------------------ | ----| --- | 
| BasicDetails | Booking Type ||Fixed |Normal | Yes
||BookingNo | | Unique Number |Alphanumeric | Yes
||BookingDate ||Message Received date | Date [yyyymmdd]| Yes
||ServiceClass ||Fixed |Normal |Yes
||Client |Code|Fixed |SIRCLO |Yes
||Shipper |Code |Brand/Seller Code | Alphanumeric | Yes 
||Consignee | Code |Brand/Seller Code | Alphanumeric | Yes 
||PONo ||Order PONo from Odoo | Alphanumeric | No 
||PODate ||Order PODate from Odoo |Date [yyyymmdd]|No 
||Due Date |Date |Order Due Date from Odoo | Date [yyyymmdd]
|||Time | Time in 24 hour format | HHMM | No
|||Zone | Fixed Jakarta | Fixed | No 
||Movement |Place of delivery |Based on Consignee | Alphanumeric |No 
||Movement |MovementType | Fixed | Direct | No 
||PackageSummary | TotalPackages | Total Quantity |Numeric |No
||SystemInformation| BookingOffice | Destination Warehouse Code | KLOGWH Name | Yes 
||ServiceTemplateName ||Fixed |Fixed-"WHINB"|Yes 
|[Loop] Products|LineItemId||Line item id fi Odoo Maintain | Numeric | No 
||ProductCode | | Product Code from Odoo |Alphanumeric | Yes 
||Quantity | Value | Product Quantity from Odoo | Numeric | Yes 
|||UOM |Product UOM | Text | Yes 
||Brand/Seller | |Brand/Seller Code|Text | Yes 
||OrderDetails |Manufacturing Date|Manufacturing date|Date [yyyymmdd] |No 
|||ExpiryDate | ExpiryDate |Date [yyyymmdd]|No 
|||PONo | PONo | Text | No 
|||BatchNo | Batch No | Text | No 
|||LotNo | LotNo | Text | No 




## Booking Outbound Request 

### Header Request  

|Section | Mapping Description | 
|--------|-----------------------------|
|MessageType | Fixed 
|MessageVersion | If multiple version the provide the version no 
|MessageIdentifier |Unique number to identify integration message 
|MessageDateTime | Message date time  

### Bookings Request 

Request body must be a JSON document with the following properties

| Section | Node   | Subnode  | Description | Expected Value | Required 
| ----- | ------| ------| ------------------ | ----| --- | 
|BesicDetails|BookingType || Fixed | Normal | Yes 
||BookingNo  ||Order No from Odoo | Alphanumeric | Yes 
||BookingDate ||Order Date from Odoo | Datetime [yyyymmdd]|Yes 
||ServiceClass || Order Type from Odoo |Urgent, Normal or Same Day|Yes
||Client | Code |Fixed |Alphanumeric | Yes 
||Shipper |Code |Brand/Seller Code | Alphanumeric | Yes
||ShipperPhone ||Brand/Seller Phone |Alphanumeric | Yes 
||Marketplace ||Marketplace|Text |Yes 
||CustomerReferenceNo||Customer Reference Number | Text | Yes
||Consignee | Code | Fixed for Customer Details will updated in party section | Customer | Yes 
||PONo ||PO Number ||No 
||PO Date ||PO Date ||No 
||Due Date|Date | This is Due date for KLOG WH for delivery | Date [yyyymmdd] | Yes 
||Time | Due Time | HHMM | Yes 
||Zone | Due zone always Indonesia time | Fixed | Yes 
||Movement | Place of Delivery | Based on Consignee | Alphanumeric | No 
||Movement | MovementType |Fixed | Direct | No 
||PackageSummary | TotalPackages | Total quantity | Numeric | No 
||SystemInformation | BookingOffice | If multiple warehouse then provide warehouse code else fixed | Yes 
||Courier | Code | 3PL Transport Partner | Text | Yes 
||Courier Service Type | | Courier service type | Text | Yes 
||WaybillNo | AWB Number | Text | No 
||ServiceTemplateName | Fixed | Fixed - WHOB | Yes 
||Barcode1Label||The barcode label, eg: Order number, or Airway Bill Number|Text|No 
||Barcode1Type||The barcode type, eg: Code 19 or Code 128, or QR Code|Text | No 
||Barcode1Value||The barcode content, eg: The AWB value|Text|No 
