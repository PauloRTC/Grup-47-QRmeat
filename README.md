# ADR 1: Uso de Micro-frontends e MVVM no Projeto QRmeat

## Status
Proposto

## Decisores
- Paulo Carvalho, Estudante Nº: 62688
- Tiago Ferreira, Estudante Nº: xxxx

## Data
07-MAR-2024

## Contexto
Este Architectural Decision Records (ADR) é criado no contexto da disciplina de Aplicações WEB. Este projeto tem como objetivo criar uma arquitetura micro-frontends e padrão Model-View-ViewMode (MVVM) com base numa aplicação protótipo desenvolvido em Justinmind (QRmeat) cedido pelo docente.

## Decisão
Decidimos adotar uma arquitetura baseada em micro-frontends e o padrão MVVM para o desenvolvimento do projeto QRmeat. O projeto será organizado em módulos funcionais independentes, com cada micro-frontend representando uma parte distinta da funcionalidade da APP.

As razões para esta decisão incluem:

- **Simplicidade:** Cada micro-frontend lida com sua própria lógica, simplificando a base de código.
- **Responsabilidade Individual: ** Distribuição clara de responsabilidades, melhorando a manutenção.
- **Reutilização:** Possibilidade de reutilizar componentes em diferentes partes da APP.
- **Implementação Independente:** Capacidade de desenvolver, testar e implantar partes da aplicação de forma independente.
- **Equipas Autônomas:** Possibilita que diferentes equipas trabalhem em diferentes partes da aplicação sem interferência.
- **Serviços Verticais:** Integração com o backend estruturado como microserviços, facilitando a escalabilidade e flexibilidade.
- **Flexibilidade:** Facilidade para adaptar e mudar partes da aplicação conforme necessário.

## Consequências
A escolha por micro-frontends e MVVM deve resultar em uma APP mais modular e manejável. No entanto, esta abordagem pode aumentar a complexidade de integração e requerer um plano cuidado para garantir a consistência e compatibilidade entre os diferentes módulos. Será necessária uma boa coordenação para gerir as dependências e interfaces entre os micro-frontends.

A gestão do projeto no GitHub permitirá colaboração e acompanhar o progresso de todos os envolvidos. O repositório está estruturado para refletir as diferentes áreas do sistema, permitindo um desenvolvimento e revisão de código organizados.

O controlo de progresso do trabalho será visualizado através de um mapa, facilitando a identificação rápida de qualquer atraso ou problema no projeto.
![ProgressoTrabalho](https://github.com/PauloRTC/QRmeat/assets/162343860/d3a51146-1ed1-4c59-8fb8-14250328d68b)

## Detalhes Técnicos dos Micro-frontends
Cada micro-frontend tem por base os critérios estabelecidos para maximizar a eficiência e eficácia do desenvolvimento:

- **Login - Conta do Utilizador:** Autenticação segura e gestão de perfil do utilizador. **Responsável: Carvalho**.
- **Destaques:** Apresentação de conteúdo em destaque, como promoções ou eventos.**Responsável: Carvalho**.
- **Geolocalização:** Serviços baseados na localização do utilizador para personalizar conteúdo e ofertas.**Responsável Tiago**.
- **Produtos:** Gestão detalhada de produtos, incluindo informações e disponibilidade.**Responsável: Tiago**.
- **Lista de Produtos:** Visualização e gestão de listas de produtos, como cestas de compra.**Responsável: Tiago**.
- **Serviço Noticias & Atualidades:** Integração com fluxos de notícias para oferecer conteúdo atualizado referentes ao produto.**Responsável: Tiago**.
- **Estatística:** Análise de dados do utilizador e utilização da APP para melhorar o serviço. **Responsável: Carvalho**.
- **Feedback:** Recolha e gestão de feedback dos utilizadores para melhorias contínuas.**Responsável: Carvalho**.
- **QR Code:** Funcionalidades para geração e leitura de QR Codes, integrando serviços como pagamentos ou identificação de produtos.**Responsável: Carvalho**.

## Acompanhamento e Validação
O sucesso das decisões tomadas será monitorizado através de análise de desempenho e feedback dos utilizadores. As métricas de sucesso incluirão velocidade de desenvolvimento, facilidade de manutenção, e satisfação do utilizador.

---

>[!NOTE]
>A decisão deverá ser revista periodicamente para assegurar que continua alinhada com os objetivos do projeto e as necessidades das  partes interessadas. Mudanças introduzidas pelo docente ou novas prioridades do projeto podem levar a revisões desta ADR. É importante manter a documentação atualizada para refletir o estado atual das decisões arquiteturais.
