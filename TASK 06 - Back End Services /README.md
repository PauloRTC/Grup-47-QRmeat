# ADR 6:  Back End Services 

## Status
Proposto

## Decisores
- Paulo Carvalho, Estudante Nº: 62688
- Tiago Ferreira, Estudante Nº: 56963

## Data
26-4-2024

## Contexto
Nesta etapa do desenvolvimento do projeto final da aplicação QR Meat, procurou-se defenir os Back End Services necessários a definir a app QR Meat, definindo para estes a sua descrição e uma curta descrição dos recursos utilizados.

# PROJECT TASK 6

## Business Objects

| BE Services      | Service description                             | Resource description                                                                                                                            
|------------------------|-----------------------------------------|--------------------------------------------|
| GetUsers          | Permite gerir a informação do utilizador, incluindo credenciais e detalhes pessoais | Lista de pares contas, passwords e detalhes (idade, sexo, morada…)| 
| Autenticação               | Gere o ciclo de vida da sessão do usuário, incluindo login, logout e renovação de sessão| Armazena e gere os tokens de sessão, estado de autenticação e registo de atividade de login do utilizador|
| Produtos     | Fornece acesso a uma lista de produtos, detalhes individuais e gere feedback de produtos |Obtém lista de informação detalhada do produto      |
| Avaliação de sustentabilidade | Representa o nível de sustentabilidade do produto através de widgets e gráficos informativos|Sistema de avalização baseado em critérios de sustentabilidade, estatísticas qualitativa e de índices de produção|
|Noticias relacionadas|Exibe notícias destacadas e lista de noticias relacionando a carne e a sustentabilidade|Agrega conteúdos filtrados que reúne noticias de diferentes fontes|
|Leitor de QR Codes | Acesso rápido à informação do produto após a digitalização de um código QR |Faz a leitura do QR code utilizando a câmara do dispositivo móvel e faz a ligação com a pagina do produto|
Localização de lojas | Integra-se com serviço de mapas e permite a seleção de lojas para exibir os produtos disponíveis | Compila uma lista de lojas, incluindo detalhes como endereço e disponibilidade de produtos|
|Serviço de mapas | Oferece visualização de lojas no mapa e suas informações por meio de uma integração de API de mapa.| Armazena dados geográficos e coordenadas das lojas, permite visualizar e interagir com a localização das lojas no mapa|
|Custo e Guardados | Gere as ações do utilizador no cesto de compras e na lista de produtos guardados, como adicionar ou remover produtos, e no caso do cesto, calcular totais|Armazena numa lista os elementos escolhidos pelo utilizador|
|Serviço de Checkout e Pagamento * |Processa a confirmação dos pedidos e integra com serviços de pagamento para transações monetárias.|Confirma o pedido de acordo com a aprovação recebida com o método de pagamento|
|Feedback *| Recebe e cataloga o feedback dos utilizadores sobre os produtos, disponibilizando para consulta e gestão|Armazena a submissão de feadback do utilizador e exibe lista de feedbacks|

-* Novas funcionalidades, não presentes no prótotipo original.
