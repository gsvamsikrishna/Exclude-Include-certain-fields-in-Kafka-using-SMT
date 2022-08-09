# Exclude/ Include a subset of fields in Kafka records using SMT
Note: I am using Confluent Cloud which provides a Fully Managed Kafka Service, Connectors, Schema-Registry and ksqlDB for Real-time Event Streaming and Processing.

### Example data generated from source
```
{
  "ordertime": 1498772477201,
  "orderid": 43,
  "itemid": "Item_407",
  "orderunits": 5.0116235412281895,
  "address": {
    "city": "City_96",
    "state": "State_31",
    "zipcode": 25075
  }
}
```

### Use case: Include only orderid, itemid and address

Using ReplaceField Transform without specifying renames. (Renames can be used if required)

![transform_config](https://user-images.githubusercontent.com/73946498/183637330-444b6ea2-9618-4b52-9fb7-8464271b5ac7.png)

Output after Transforms

![filtered records](https://user-images.githubusercontent.com/73946498/183639532-e04e1764-688a-4afb-a7f8-9fe620d61e9b.png)
