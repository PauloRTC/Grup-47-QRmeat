# PROJECT TASK 8

## Business Objects Schema

The following table outlines the schema for business objects:

| Business Objects       | Request                                 | Responses                                  | Schema                                                                                     |
|------------------------|-----------------------------------------|--------------------------------------------|--------------------------------------------------------------------------------------------|
| Autenticação¹          | `/components/schemas/Users`              | `/components/schemas/AuthenticationResponse` | ```json\n{ "components": { "schemas": { "Authentication": { "type": "object", "required": ["username", "password"], "properties": { "username": { "type": "string" }, "password": { "type": "string" } } }, "AuthenticationResponse": { "200": { "description": "Successful login" }, "401": { "description": "Invalid credentials" }, "404": { "description": "User not found" }, "default": { "description": "Unexpected error" } } } }\n``` |
| Produtos               | `/components/schemas/ProductRequest`    | `/components/schemas/ProductResponse`       | ```json\n{ "components": { "schemas": { "ProductRequest": { "type": "object", "properties": { ... } }, "ProductResponse": { "type": "object", "properties": { ... } } } }\n``` |
| Cestos e Guardados     | `/components/schemas/BasketRequest`     | `/components/schemas/BasketResponse`        | ```json\n{ "components": { "schemas": { "BasketRequest": { "type": "object", "properties": { ... } }, "BasketResponse": { "type": "object", "properties": { ... } } } }\n``` |
| Check out e pagamento² | `/components/schemas/CheckoutRequest`   | `/components/schemas/PaymentResponse`       | ```json\n{ "components": { "schemas": { "CheckoutRequest": { ... }, "PaymentResponse": { "200": { "description": "Successful transaction" }, "400": { "description": "Invalid request" }, "401": { "description": "Unauthorized or invalid payment details" }, "500": { "description": "Internal Server Error" }, "default": { "description": "Unexpected error" } } } }\n``` |

¹ Autenticação é considerada um Objeto de Negócio (BO) apenas no contexto promocional, como por exemplo numa campanha que oferece condições especiais a usuários selecionados com base no histórico de compras.

² A funcionalidade de 'Check out e pagamentos' não está incluída no aplicativo original. A inclusão nesta tabela serve como uma sugestão de melhoria para abordar processos de checkout e pagamento.

