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
 'warranty_at': '2030-06-28',
 'payment_method': 'card',
 'payment_plan': 'yearly',
 'date_renew': '2031-06-21',
 'sck': 'palpatine',
 'offer_id': null, # Quando é uma oferta vem preenchido
 'offer_code': null,
 'offer_price': null,
 'plan_code': '2sbwfgct',
 'plan_id': 56,
 'plan_price': 500.0,
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
 'warranty_at': '2030-06-28',
 'payment_method': 'card',
 'payment_plan': 'yearly',
 'date_renew': '2031-06-21',
 'sck': 'palpatine',
 'offer_id': null, # Quando é uma oferta vem preenchido
 'offer_code': null,
 'offer_price': null,
 'plan_code': '2sbwfgct',
 'plan_id': 56,
 'plan_price': 500.0,
 'periodicity': 'yearly',
 'type': 'payment', 
 'status': 'reversal',
 'created_at': '2030-06-21 13:42:22.400441+00:00',
 'reversal_at': '2030-06-21 18:42:22.400441+00:00',
 'timestamp': '1655830333.414318',
 'external_id': '1977',
}
```
------

### Chargeback
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
 'warranty_at': '2030-06-28',
 'payment_method': 'card',
 'payment_plan': 'yearly',
 'date_renew': '2031-06-21',
 'sck': 'palpatine',
 'offer_id': null, # Quando é uma oferta vem preenchido
 'offer_code': null,
 'offer_price': null,
 'plan_code': '2sbwfgct',
 'plan_id': 56,
 'plan_price': 500.0,
 'periodicity': 'yearly',
 'type': 'payment', 
 'status': 'chargeback',
 'created_at': '2030-06-21 13:42:22.400441+00:00',
 'chargeback_at': '2030-06-21 18:42:22.400441+00:00',
 'timestamp': '1655830333.414318',
 'external_id': '1977',
}
```
------
### Unsubscribe
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
 'warranty_at': '2030-06-28',
 'payment_method': 'card',
 'payment_plan': 'yearly',
 'date_renew': '2031-06-21',
 'sck': 'palpatine',
 'offer_id': null, # Quando é uma oferta vem preenchido
 'offer_code': null,
 'offer_price': null,
 'plan_code': '2sbwfgct',
 'plan_id': 56,
 'plan_price': 500.0,
 'periodicity': 'yearly',
 'type': 'subscription', 
 'status': 'unsubscribe',
 'created_at': '2030-06-21 13:42:22.400441+00:00',
 'cancel_signature_at': '2030-06-21 18:42:22.400441+00:00',
 'timestamp': '1655830333.414318',
 'external_id': '1977',
}
```
------

### Boleto Gerado

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
 'warranty_at': '2030-06-28',
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
 'created_at': '2030-06-21 13:42:22.400441+00:00',
 'timestamp': '1655830333.414318',
 'external_id': '1977',
 'type': 'billet',
 'status': 'generate',
 'billet': {
      'url': 'https://simulatorpages.pagar.me/boleto/5337e93d-55eb-4cb9-9c11-2bce4491d697',
      'pdf': 'https://api.pagar.me/core/v5/transactions/tran_XyMLy8cMOc3GgP9v/pdf',
      'barcode': 'https://api.pagar.me/core/v5/transactions/tran_XyMLy8cMOc3GgP9v/barcode',
      'qr_code': 'https://api.pagar.me/core/v5/transactions/tran_XyMLy8cMOc3GgP9v/qrcode',
      'line': '13792656029000525335745005393702878430000005379',
      'due_date': '28/06/2030'
    }
}
```

### Falha na cobrança 

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
 'warranty_at': '2030-06-28',
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
 'created_at': '2030-06-21 13:42:22.400441+00:00',
 'timestamp': '1655830333.414318',
 'external_id': '1977',
 'type': 'payment',
 'status': 'failed'
}
```
 ---
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
---
### Pix Generate
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
 'warranty_at': '2030-06-28',
 'payment_method': 'card',
 'payment_plan': 'yearly',
 'date_renew': '2031-06-21',
 'sck': 'palpatine',
 'offer_id': 10,
 'offer_code': 8uc3iu,
 'offer_price': '300.0',
 'plan_code': null,
 'plan_id': null,
 'plan_price': null,
 'periodicity': null,
 'type': 'pix', 
 'status': 'generate',
 'qr_code_url': 'https://api.pagar.me/core/v5/transactions/tran_zlMOKovHgXIRMOB9/qrcode?payment_method=pix',
 'pix_amount': '300.0',
 'pix_expires_at': '2030-06-21 20:42:22.400441+00:00',
 'created_at': '2030-06-21 13:42:22.400441+00:00',
 'timestamp': '1655830333.414318',
 'external_id': '1977',
}
```
---
### Payment Completed
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
 'warranty_at': '2030-06-28',
 'payment_method': 'card',
 'payment_plan': 'yearly',
 'date_renew': '2031-06-21',
 'sck': 'palpatine',
 'offer_id': 10,
 'offer_code': 8uc3iu,
 'offer_price': '300.0',
 'plan_code': null,
 'plan_id': null,
 'plan_price': null,
 'periodicity': null,
 'type': 'payment',
 'status': 'completed',
 'paid_at': '2030-06-21 13:42:22.400441+00:00',
 'completed_at': '2030-07-21 13:42:22.400441+00:00',
 'created_at': '2030-06-21 13:42:22.400441+00:00',
 'timestamp': '1655830333.414318',
 'external_id': '1977',
}
```
