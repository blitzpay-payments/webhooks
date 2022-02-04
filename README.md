# Eventos

Todos os eventos são enviado no formato POST FORM, é possível solicitar o envio no formato JSON

- Content-Type: application/json (JSON)
- Content-Type: application/x-www-form-urlencoded (Form Data)

### Pagamento Aprovado

```
{'tid': '709c92ad-8472-4ca2-a9d9-dcc77319dfde',
 'order': 'BP79206',
 'name': 'Arishem Celestial',
 'email': 'arishem@gmail.com',
 'document': '197619761976197',
 'doc_type': 'cpf',
 'country': 'BR',
 'phone': '5511988888888',
 'product_id': 474,
 'product_code': 'Q8GDWP',
 'product_name': 'Arishem the Judge',
 'product_price': 297.0,
 'payment_type': 'online_course',
 'charge_type': 'unique',
 'warranty_at': '2022-02-11',
 'payment_method': 'card',
 'payment_plan': 'unique',
 'date_renew': '2023-02-04',
 'status': 'pending',
 'sck': 'marvel',
 'offer_id': 371,
 'offer_code': 'houuwcu9',
 'offer_price': 297.0,
 'type': 'payment',
 'status': 'approved'
}
```
------

### Estorno de Pagamento
```
{'tid': '709c92ad-8472-4ca2-a9d9-dcc77319dfde',
 'order': 'BP79206',
 'name': 'Arishem Celestial',
 'email': 'arishem@gmail.com',
 'document': '197619761976197',
 'doc_type': 'cpf',
 'country': 'BR',
 'phone': '5511988888888',
 'product_id': 474,
 'product_code': 'Q8GDWP',
 'product_name': 'Arishem the Judge',
 'product_price': 297.0,
 'payment_type': 'online_course',
 'charge_type': 'unique',
 'warranty_at': '2022-02-11',
 'payment_method': 'card',
 'payment_plan': 'unique',
 'date_renew': '2023-02-04',
 'status': 'pending',
 'sck': 'marvel',
 'offer_id': 371,
 'offer_code': 'houuwcu9',
 'offer_price': 297.0,
 'type': 'payment',
 'status': 'reversal'
}
```
------

### Boleto Gerado

```
{'tid': '709c92ad-8472-4ca2-a9d9-dcc77319dfde',
 'order': 'BP79206',
 'name': 'Arishem Celestial',
 'email': 'arishem@gmail.com',
 'document': '197619761976197',
 'doc_type': 'cpf',
 'country': 'BR',
 'phone': '5511988888888',
 'product_id': 474,
 'product_code': 'Q8GDWP',
 'product_name': 'Arishem the Judge',
 'product_price': 297.0,
 'payment_type': 'online_course',
 'charge_type': 'unique',
 'warranty_at': '2022-02-11',
 'payment_method': 'card',
 'payment_plan': 'unique',
 'date_renew': '2023-02-04',
 'status': 'pending',
 'sck': 'marvel',
 'offer_id': 371,
 'offer_code': 'houuwcu9',
 'offer_price': 297.0,
 'type': 'billet',
 'status': 'generate',
  'billet': {
      'url': 'https://simulatorpages.pagar.me/boleto/5337e93d-55eb-4cb9-9c11-2bce4491d697',
      'pdf': 'https://api.pagar.me/core/v5/transactions/tran_XyMLy8cMOc3GgP9v/pdf',
      'barcode': 'https://api.pagar.me/core/v5/transactions/tran_XyMLy8cMOc3GgP9v/barcode',
      'qr_code': 'https://api.pagar.me/core/v5/transactions/tran_XyMLy8cMOc3GgP9v/qrcode',
      'line': '13792656029000525335745005393702878430000005379',
      'due_date': '07/02/2022'
    }
}
```

### Falha na cobrança 

```
{'tid': '709c92ad-8472-4ca2-a9d9-dcc77319dfde',
 'order': 'BP79206',
 'name': 'Arishem Celestial',
 'email': 'arishem@gmail.com',
 'document': '197619761976197',
 'doc_type': 'cpf',
 'country': 'BR',
 'phone': '5511988888888',
 'product_id': 474,
 'product_code': 'Q8GDWP',
 'product_name': 'Arishem the Judge',
 'product_price': 297.0,
 'payment_type': 'online_course',
 'charge_type': 'unique',
 'warranty_at': '2022-02-11',
 'payment_method': 'card',
 'payment_plan': 'unique',
 'date_renew': '2023-02-04',
 'status': 'pending',
 'sck': 'marvel',
 'offer_id': 371,
 'offer_code': 'houuwcu9',
 'offer_price': 297.0,
 'type': 'payment',
 'status': 'failed'
}
```
 
### Carrinho Abandonado
```
{
    'tid': '709c92ad-8472-4ca2-a9d9-dcc77319dfd9',
    'name': 'Tiamut 616',
    'email': 'tiamut@gmail.com',
    'phone': '119777755555',
    'product_id': 190,
    'country': 'US',
    'query_params': 'utm=10&ref=20',
    'recovery_checkout': "https://pay.blitzpay.com.br/pagar/709c92ad-8472-4ca2-a9d9-dcc77319dfd9",
    'type': 'lead',
    'status': 'abandoned_cart'
}
```



