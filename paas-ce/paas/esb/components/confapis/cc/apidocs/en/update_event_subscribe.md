### Functional description

update event subscribe

### Request Parameters

{{ common_args_desc }}

#### General Parameters

| Field                   |  Type    | Required	   |  Description                                            |
|------------------------|----------|--------|--------------------------------------------------|
| bk_biz_id              | int      | Yes     | Business ID                                           |
| bk_supplier_account    | string   | Yes     | Supplier account                                       |
| subscription_id        | int      | Yes     | Subscription ID                                           |
| subscription_name      | string   | Yes     | Subscription name                                        |
| system_name            | string   | Yes     | Subscription system name                              |
| callback_url           | string   | Yes     | Url of callback                                         |
| confirm_mode           | string   | Yes     | Verification mode of event sending success, optional: 1-httpstatus,2-regular |
| confirm_pattern        | string   | Yes     | Httpstatus or regex of callback                       |
| subscription_form      | string   | Yes     | Subscription form, separated by ','                            |
| timeout                | int      | Yes     | Timeout of sending event                                 |


### Request Parameters Example

```python
{
  "bk_biz_id": 0,
  "bk_supplier_account": "0",
  "subscription_name":"mysubscribe",
  "subscription_id": 2,
  "system_name":"SystemName",
  "callback_url":"http://127.0.0.1:8080/callback",
  "confirm_mode":"httpstatus",
  "confirm_pattern":"200",
  "subscription_form":"hostcreate",
  "timeout":10
}
```

### Return Result Example

```python

{
    "result": true,
    "code": 0,
    "message": "",
    "data": "success"
}
```
