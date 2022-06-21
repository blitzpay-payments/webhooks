# Eventos

Todos os eventos são enviado no formato POST FORM, é possível solicitar o envio no formato JSON

- Content-Type: application/json (JSON)
- Content-Type: application/x-www-form-urlencoded (Form Data)

#### Payment Method (payment_method)
- card
- billet
- pix
- two_card
- smart_card (Recuperacão de Vendas)

### Pagamento Aprovado

```
{'tid': '2aabb487-f2af-4ac5-9ac1-006d09aae721',
 'order': 'BP126870',
 'name': 'Anakin Skywalker Vader',
 'email': 'anakin.skywalker@starwars.com',
 'document': '90048701977',
 'doc_type': 'cpf',
 'country': 'BR',
 'phone': '551199998888',
 'product_id': 278,
 'product_code': 'EVJ8ZG',
 'product_name': 'Como se tornar um Sith',
 'product_price': 500.0,
 'full_price': 500.0,
 'payment_type': 'signature',
 'charge_type': 'signature',
 'warranty_at': '2030-06-21',
 'payment_method': 'card',
 'payment_plan': 'yearly',
 'date_renew': '2031-06-21',
 'sck': 'palpatine',
 'offer_id': null, # Quando é uma oferta vem preenchido
 'offer_code': null,
 'offer_price': null,
 'plan_code': '2sbwfgct',
 'plan_id': 56,
 'plan_price': 450.0,
 'periodicity': 'yearly',
 'type': 'payment', 
 'status': 'approved',
 'created_at': '2030-06-21 13:42:22.400441+00:00',
 'paid_at': '2030-06-21 13:42:22.400441+00:00',
 'timestamp': '1655830333.414318',
 'external_id': '1977',
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
 'payment_method': 'billet',
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



