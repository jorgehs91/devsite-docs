---
  indexable: false
---

# Devolución de pagos

Se utiliza el `id` del Advanced Payment realizando un `PUT` como muestra el ejemplo.

#### Request
```curl
curl -X PUT \
    -H 'Accept: application/json' \
    -H 'Content-Type: application/json' \
    'https://api.mercadopago.com/v1/advanced_payments/ID/refunds?access_token=SELLER_TOKEN' \
```

#### Response
`HTTP Status 200 OK`
```json
{
   "id":10458724,
   "status":"refunded",
   "wallet_payment":{
      "transaction_amount":700.50,
      "description":"Payment",
      "external_reference":"Pago_123"
   },
   "payments":[
      {
         "id":3870106238,
         "status":"refunded",
         "status_detail":"refunded",
         "payment_type_id":"account_money",
         "payment_method_id":"account_money",
         "transaction_amount":700.50,
         "installments":1,
         "description":"Payment",
         "capture":true,
         "external_reference":"Pago_123"
      }
   ],
   "payer":{
      "id":786547
   },
   "binary_mode":true,
   "date_created":"2018-10-20T09:34:20.518-04:00",
   "date_last_updated":"2018-10-20T09:34:20.518-04:00"
}
```