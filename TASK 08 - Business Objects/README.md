# ADR 8:  Business Objetcs (requests and responses) 

## Status
Proposto

## Decisores
- Paulo Carvalho, Estudante Nº: 62688
- Tiago Ferreira, Estudante Nº: 56963

## Data
10-05-2024

## Contexto
Nesta etapa do desenvolvimento do projeto final da aplicação QR Meat, procurou-se defenir os Business objectes da app, os request e responses necessários e um Schema. Voltou-se a tomar liberdade de propor a funcionalidade de compra de carne, não existente no protótipo inicial.
# PROJECT TASK 8

## Business Objects

| Business Objects       | Request                                 | Responses                                  | Schema (Expanded)                                                                                           |
|------------------------|-----------------------------------------|--------------------------------------------|------------------------------------------------------------------------------------------------------------|
| Autenticação¹          | "/components/schemas/User"              | "/components/schemas/AuthenticationResponse" | `components: { schemas: { Authentication: { type: "object", required: ["username", "password"], properties: { username: { type: "string" }, password: { type: "string" } } }, AuthenticationResponse: { 200: { description: "Successful login" }, 401: { description: "Invalid credentials" }, 404: { description: "User not found" }, default: { description: "Unexpected error" } } }` |
| Produtos               | "/components/schemas/ProductRequest"    | "/components/schemas/ProductResponse"       | `components: { schemas: { ProductRequest: { type: "object", properties: { ... } }, ProductResponse: { type: "object", properties: { ... } } }` |
| Cestos e Guardados     | "/components/schemas/BasketRequest"     | "/components/schemas/BasketResponse"        | `components: { schemas: { BasketRequest: { type: "object", properties: { ... } }, BasketResponse: { type: "object", properties: { ... } } }` |
| Check out e pagamento² | "/components/schemas/CheckoutRequest"   | "/components/schemas/PaymentResponse"       | `components: { schemas: { CheckoutRequest: { ... }, PaymentResponse: { 200: { description: "Successful transaction" }, 400: { description: "Invalid request" }, 401: { description: "Unauthorized or invalid payment details" }, 500: { description: "Internal Server Error" }, default: { description: "Unexpected error" } } }` |

¹ Autenticação é considerada um Objeto de Negócio (BO) apenas no contexto promocional, como por exemplo numa campanha que oferece condições especiais a usuários selecionados com base no histórico de compras.

² A funcionalidade de 'Check out e pagamentos' não está incluída no aplicativo original. A inclusão nesta tabela serve como uma sugestão de melhoria para abordar processos de checkout e pagamento.
