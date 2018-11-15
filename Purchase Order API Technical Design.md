# Purchase Order API

## Packages
### TollGtpB2BPurchaseOrder
---
1. Receive inbound request, either via CSV or EDI
2. Map the request to a publishable document (PurchaseOrderAPI DocType) 
3. Publish the request to messaging layer with parameter consumer = facade


### TollGtpAPIPurchaseOrder
---

 1. Subscribe to Purchase Order API DocType
 2. Get subscriber list from config
 3. For each backend subscriber, invoke mapping service and publish request parameter consumer = [list of consumers]
 4. 
---
### TollGtpAdpPurchaseOrder


 1. Single document type with one or more triggers
 2. One trigger for each subscriber (backend system)
 3. One subscribing backend mapping service for each subscriber
---
# Questions:

Do we really need the API and ADP layers; Could they be combined?
 - [ ] Yes
 - [ ] No
 
Do we need to define an intermediary document type?
 - [ ] Yes
 - [ ] No


<!--stackedit_data:
eyJoaXN0b3J5IjpbLTk4MjM3MjY3M119
-->