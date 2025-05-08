# Projeto Integrador - Sistema de Gestão para Pizzaria

_(Pizzaria Santory)_

O projeto consiste no desenvolvimento de um sistema de gestão para a Pizzaria Santory, uma empresa familiar que busca modernizar seus processos operacionais. O objetivo principal é automatizar o registro de pedidos, o controle de estoque, a gestão de entregas e a comunicação com os clientes, proporcionando maior eficiência e melhor experiência para os consumidores. A solução também incluirá funcionalidades como pagamento online, rastreamento de pedidos e ferramentas de fidelização, atendendo às necessidades específicas da pizzaria e resolvendo os problemas identificados em sua operação atual.

**IMPORTANTE**: [**Cadastre seu projeto nesse link**](https://docs.google.com/spreadsheets/d/165xR63Yy9C75saQX-I_RsZV-hTrdiToei5Ave0JU1uQ/edit?usp=sharing).

Professor: [Marco André Mendes](github.com/marcoandre)

Equipe:

- [Higor do Amaral Fritz](https://github.com/HigorAmaral)
- [Matheus Gaspar](https://github.com/Gaspatt)
- [Nicolas Sestrem](https://github.com/i-sestrem).
- [Kaue Ian Dombrovski da Cunha](https://github.com/kaue-ian)

Links do projeto:
(_Coloque aqui os links para a documentação do projeto e os repositórios e plubicação do backend e frontend._)

- [Documentação (esse documento)]()
- Backend: [Repositório](https://github.com/Santory-Pizzaria/SantoryBackEnd.git) e [Publicação]()
- Frontend: [Repositório](https://github.com/Santory-Pizzaria/SantoryFrontEnd.git) e [Publicação]()

# 1. Desenvolvimento

**1.1 Modelos de Sistemas**

**Nessa parte a equipe deve escolher um dos modelos de sistemas para desenvolver o projeto. Ao escolher, escreva uma breve descrição do sistema e o motivo da escolha e pode apagar os outros modelos.**

**1.1.1 Ponto de Vendas (PDV)**

**Gerenciamento de pedidos e entregas para uma pizzaria**

O sistema escolhido será um software de gestão para a Pizzaria Santory. O objetivo é automatizar os processos de pedidos, entregas e controle de estoque, além de oferecer opções de pagamento online e ferramentas para fidelização de clientes. A escolha foi motivada pela necessidade de resolver os problemas operacionais identificados, como atrasos, erros no registro de pedidos e falta de controle eficiente de insumos, garantindo uma melhor experiência para os clientes e maior eficiência para a empresa.

#2. Situacao Problema

**Introdução:**
A Pizzaria Santory é uma empresa familiar localizada no centro da cidade, fundada há 10 anos por João e Maria Silva. A pizzaria é conhecida pela qualidade de suas pizzas artesanais e pelo atendimento acolhedor. Atualmente, a empresa conta com 10 funcionários, incluindo pizzaiolos, atendentes e entregadores. Apesar do sucesso local, a pizzaria enfrenta desafios para atender à crescente demanda de pedidos, especialmente nos horários de pico.

**Situação-problema:**
Atualmente, a Pizzaria Santory opera de forma semi-manual. Os pedidos são recebidos por telefone ou presencialmente, o que frequentemente resulta em filas e atrasos no atendimento. Os atendentes anotam os pedidos em papel, o que pode levar a erros de comunicação entre a equipe de atendimento e a cozinha. Além disso, o controle de estoque é feito manualmente, dificultando a previsão de insumos necessários e ocasionando, por vezes, a falta de ingredientes.

O sistema de delivery também apresenta problemas. Os entregadores recebem as informações dos pedidos verbalmente ou por mensagens de texto, o que pode gerar confusões e atrasos nas entregas. Não há um sistema de rastreamento para os clientes acompanharem o status de seus pedidos, o que frequentemente resulta em reclamações.

Outro ponto crítico é a ausência de um sistema de pagamento online. Os clientes só podem pagar em dinheiro ou com cartão no momento da entrega, o que limita as opções e pode causar desconforto para alguns consumidores. Além disso, a pizzaria não possui um canal digital eficiente para divulgar promoções ou fidelizar clientes.

**Conclusão:**
Os problemas identificados, como erros no registro de pedidos, atrasos nas entregas, falta de controle de estoque e ausência de opções de pagamento online, impactam diretamente a experiência do cliente e a eficiência operacional da pizzaria. Um software integrado poderia resolver esses problemas ao automatizar o registro de pedidos, implementar um sistema de rastreamento de entregas, gerenciar o estoque em tempo real e oferecer opções de pagamento online, além de criar um canal digital para promoções e fidelização de clientes.

# 3. Descrição da proposta

O software proposto para a Pizzaria Santory será uma plataforma integrada que automatizará os processos de pedidos, entregas e gestão interna. O objetivo principal é melhorar a eficiência operacional e a experiência do cliente. A seguir, destacam-se os principais pontos da solução:

- **Foco de ação do software:** O sistema permitirá o registro de pedidos online e presencial, o acompanhamento em tempo real do status dos pedidos, o gerenciamento de entregas e o controle automatizado de estoque. Além disso, oferecerá opções de pagamento online e ferramentas para divulgação de promoções e fidelização de clientes.

- **Níveis de usuário do sistema:**

  - **Administrador:** Terá acesso completo ao sistema, podendo gerenciar pedidos, estoque, entregas, promoções e relatórios.
  - **Funcionários:** Divididos em atendentes, pizzaiolos e entregadores, cada grupo terá acesso restrito às funcionalidades relacionadas às suas funções específicas.
  - **Clientes:** Poderão realizar pedidos, acompanhar o status das entregas e acessar promoções.

- **Funcionalidades principais:**
  - Registro de pedidos online e presencial.
  - Rastreamento de entregas em tempo real.
  - Controle automatizado de estoque com alertas de reposição.
  - Integração com sistemas de pagamento online.
  - Ferramentas para criação e divulgação de promoções.
  - Relatórios gerenciais para análise de desempenho.

Com essa solução, a Pizzaria Santory poderá reduzir erros operacionais, melhorar a comunicação interna, aumentar a satisfação dos clientes e otimizar a gestão do negócio.

# 4. Modelagem de Dados

A modelagem de dados do sistema da Pizzaria Santory foi elaborada para garantir o controle eficiente dos pedidos, estoque, entregas, promoções e usuários. Abaixo estão descritas as principais entidades, seus atributos e os relacionamentos entre elas.

## 4.1 Entidades Principais

- **Usuário**
  - id_usuario (PK)
  - nome
  - email
  - senha
  - telefone
  - tipo (administrador, atendente, pizzaiolo, entregador, cliente)

- **Pedido**
  - id_pedido (PK)
  - data_hora
  - status (em preparo, em entrega, entregue, cancelado)
  - valor_total
  - id_cliente (FK)
  - id_endereco_entrega (FK)

- **ItemPedido**
  - id_item_pedido (PK)
  - id_pedido (FK)
  - id_produto (FK)
  - quantidade
  - preco_unitario

- **Produto**
  - id_produto (PK)
  - nome
  - descricao
  - preco
  - categoria (pizza, bebida, sobremesa, etc.)
  - estoque_atual

- **Estoque**
  - id_estoque (PK)
  - id_produto (FK)
  - quantidade
  - data_ultima_atualizacao

- **Entrega**
  - id_entrega (PK)
  - id_pedido (FK)
  - id_entregador (FK)
  - status_entrega (pendente, em rota, entregue)
  - data_hora_saida
  - data_hora_entrega

- **Promoção**
  - id_promocao (PK)
  - titulo
  - descricao
  - data_inicio
  - data_fim
  - desconto_percentual

- **Pagamento**
  - id_pagamento (PK)
  - id_pedido (FK)
  - valor
  - metodo (dinheiro, cartão, online)
  - status_pagamento (pendente, aprovado, recusado)

- **Endereço**
  - id_endereco (PK)
  - id_usuario (FK)
  - rua
  - numero
  - bairro
  - cidade
  - cep

## 4.2 Relacionamentos

- Um **Usuário** pode ser cliente, funcionário ou administrador.
- Um **Cliente** pode ter vários **Pedidos**.
- Cada **Pedido** pode conter vários **ItensPedido**.
- Cada **ItemPedido** está relacionado a um **Produto**.
- O **Estoque** controla a quantidade de cada **Produto**.
- Cada **Pedido** pode gerar uma **Entrega**, realizada por um **Entregador** (Usuário).
- **Promoções** podem ser aplicadas a **Pedidos** ou **Produtos**.
- Cada **Pedido** possui um **Pagamento** associado.
- **Endereços** são cadastrados pelos usuários para entrega.

## 4.3 Diagrama Entidade-Relacionamento (DER)

![Diagrama Entidade-Relacionamento](img/der.png "Diagrama Entidade-Relacionamento")

Essa modelagem garante a rastreabilidade dos pedidos, controle de estoque, gestão de entregas e promoções, além de permitir a expansão para novas funcionalidades no futuro.

# 4. Regras de negócio

RN01: Um pedido pode ser registrado através da plataforma online ou diretamente no ponto de venda (presencial/telefone(site).

RN02: O status de um pedido deve ser atualizado em tempo real e visível para o cliente e funcionários relevantes.

RN03: O controle de ingredientes em estoque deve ser automatizado, com baixas conforme os pedidos são preparados.

RN04: O sistema deve gerar alertas para o administrador quando o estoque atingir um limite mínimo.

RN05: O sistema deve suportar pagamentos online através de métodos seguros.

RN06: Pagamentos na entrega devem ser registrados no sistema pelo entregador ou atendente.

RN07: Clientes cadastrados devem poder rastrear o status de seus pedidos.

RN08: O administrador deve poder criar, gerenciar e divulgar promoções e ofertas.

RN09: O sistema deve gerar relatórios gerenciais para análise de vendas, estoque e desempenho.

RN10: O sistema deve ter três níveis de acesso: Administrador, Funcionário e Cliente.

RN11: O Administrador tem acesso irrestrito ao sistema.

RN12: Funcionários têm acesso limitado às suas responsabilidades.

RN13: Clientes podem realizar e acompanhar pedidos, visualizar histórico e acessar promoções.

RN14: O registro manual de pedidos em papel deve ser substituído pelo sistema digital.

RN15: A comunicação entre atendimento e cozinha deve ocorrer via sistema.

RN16: Informações de entrega devem ser fornecidas aos entregadores via sistema.

RN17: O sistema deve prover um canal digital para comunicação e fidelização de clientes.

RN18: Um pedido só pode ser cancelado antes de iniciar o preparo.

RN19: Cada item do cardápio deve ter preço definido e associação com ingredientes.

RN20: Promoções podem ter validade e condições específicas.

# 5. Requisitos funcionais

(_Nessa parte a equipe deve descrever os requisitos funcionais que serão implementados no sistema. O texto abaixo descreve o que essa etapa deve conter e pode ser apagado depois._)

**5.1 O que são requisitos funcionais?**

Um requisito funcional é uma declaração de como um sistema deve se comportar. Define o que o sistema deve fazer para atender às necessidades ou expectativas do usuário. Os requisitos funcionais podem ser pensados ​como recursos que o usuário detecta.

Os requisitos funcionais são compostos de duas partes:
**função** e **comportamento**.

- A **função** é o que o sistema **faz**. Por exemplo: _“calcular imposto sobre vendas”_.
- O **comportamento** é **como** o sistema faz. Por exemplo: _“O sistema deve calcular o imposto sobre vendas multiplicando o preço de compra pela alíquota do imposto.”_.

**5.2 Tipos de requisitos funcionais**

Os requisitos funcionais podem ser classificados em:

- Regulamentos de Negócios
- Requisitos de Certificação
- Requisitos de relatório
- Funções Administrativas
- Níveis de autorização
- Rastreamento de auditoria
- Interfaces Externas
- Gestão de dados
- Requisitos Legais e Regulamentares

**5.3 Diretrizes para a elaboração de requisitos funcionais**

Cada requisito funcional precisa ser:

- **Específico** sobre o que o sistema deve fazer.
- **Mensurável** para que você possa dizer se o sistema está fazendo isso
- **Alcançável** dentro do prazo que você definiu
- **Relevante** para seus objetivos de negócios
- **Limitado** no tempo para que você possa
  acompanhar o progresso

**5.4 Estrutura do requisito funcional**

Um requisito funcional deve ser estruturado da seguinte forma:

- **Nome do requisito funcional:** descrição do
  requisito.
  - **Dados necessários:** dado 1, dado 2, dado 3.
  - **Usuários:** todos os níveis de usuário.

**5.4.1 Nome do requisito funcional**

**R.F. 99 - Nome do requisito funcional:** é o nome da função que o software terá. Sugerimos, por padronização, que tenha o prefixo R.F. (requisito funcional)
seguida da numeração, para melhor identificação do requisito, acrescido do formato _“Substantivo + onde será feita a ação”_.
Por exemplo:

- R.F. 01 - Registro de Funcionários
- R.F. 15 - Gerenciamento de consultas
- R.F. 04 - Débito em conta corrente

Deixe para definir as numerações ao final, tendo em vista que mudanças podem acontecer e não é prático sempre ficar reajustando os números.

**5.4.2 Descrição do requisito funcional**

**Descrição do requisito:** local para descrever a função deste requisito.

Sempre se preocupe em esclarecer dois pontos: o que o requisito faz e o motivo de sua existência. Isso é especialmente importante se a ação executada nesse requisito não for algo que já acontece naturalmente na empresa.
Um exemplo é um Registro de funcionários, que talvez não exista hoje mas para o software é necessário para viabilizar uma autenticação de
usuários. Outro exemplo é algo que faz sentido apenas para um software, como a própria autenticação.

**5.4.3 Dados necessários**

**Dados necessários:** aqui devem ser colocados os nomes dos dados que serão usados para que esse requisito atenda o que precisa fazer.

Nas **entradas** e **processos**, em geral, são os dados que serão salvos (seja algo digitado pelo usuário ou captado do sistema, como a hora atual).

Já nas **saídas**, são os dados que serão exibidos em tela (sejam eles vindos diretamente do banco, ou criados por um cálculo ou busca na sessão do usuário).

**5.4.4 Usuários**

**Usuários:** aqui devem ser colocados os nomes dos usuários que terão acesso a esse requisito, conforme enumerados na descrição do sistema.

**5.4.5 Exemplo de requisito funcional**

- **R.F. 01 - Autenticação de usuário:** tem como propósito autenticar o acesso ao sistema, verificando se o usuário pode acessá-lo e, caso possa, o direcionando
  para a página principal de seu perfil de acesso.
  - **Dados necessários:** login, senha, nível de permissão.
  - **Usuários:** todos os níveis de usuário.

**5.4.6 Organização dos requisitos funcionais**

As funcionalidades devem ser organizadas em: entradas, processos e saídas.

**Entradas:** São as funcionalidades que alimentarão o software com as informações essenciais para seu uso.

**Exemplos de entradas:**

- “**Registro de usuário**” (para permitir depois seu acesso ao software).
- “**Registro de paciente**” (que seria útil caso nosso software fosse ppara uma clínica, evitando registrar várias vezes os mesmos dados da pessoa a cada consulta e viabilizando um histórico de seus
  atendimentos).

**Processos:** Em geral, englobam toda ação que executa cálculos, processamentos de tomada de decisão ou transforma dados em novos dados.

**Exemplos de processos:**

- “**Autenticação de usuário**”, que usará os dados de “**Registro de usuário**” em sua execução.
- “**Agendamento de consulta**”, que usará dados do “**Registro de paciente**” e talvez do “**Registro de funcionário**” em sua execução.

**Saídas:** São os relatórios, gráficos, impressões, etc., que utilizarem os dados do software para gerar informações pertinentes ao
negócio, mas sem intenção de alterá-los, apenas permitindo sua visualização e filtragem.

**Exemplos de saídas:**

- “Relatório de consultas por paciente”.
- Relatório de vendas”.
- “Log de usuários autenticados”.

Todos esses podem ser consideradas saídas, pois usam informações de entradas e processos de modo a mostrar informações relevantes ao
negócio. Lembre-se que, diferentemente das entradas e processos, aqui os dados necessários devem ser os que a tela exibirá.

**5.4.7 Exemplo de organização dos requisitos funcionais**

(_A seguir, um exemplo de organização de requisitos funcionais, com entradas, processos e saídas._)

**Entradas:**

- **R.F. 01 - Nome do requisito funcional:** descrição do requisito.

  - **Dados necessários:** dado 1, dado 2, dado 3.
  - **Usuários:** todos os níveis de usuário.

- **R.F. 02 - Nome do requisito funcional:** descrição do requisito.
  - **Dados necessários:** dado 1, dado 2, dado 3.
  - **Usuários:** todos os níveis de usuário.

**Processamento:**

- **R.F. 03 - Nome do requisito funcional:** descrição do requisito.

  - **Dados necessários:** dado 1, dado 2, dado 3.
  - **Usuários:** todos os níveis de usuário.

- **R.F. 04 - Nome do requisito funcional:** descrição do requisito.
  - **Dados necessários:** dado 1, dado 2, dado 3.
  - **Usuários:** todos os níveis de usuário.

**Saídas:**

- **R.F. 05 - Nome do requisito funcional:** descrição do requisito.

  - **Dados necessários:** dado 1, dado 2, dado 3.
  - **Usuários:** todos os níveis de usuário.

- **R.F. 06 - Nome do requisito funcional:** descrição do requisito.
  - **Dados necessários:** dado 1, dado 2, dado 3.
  - **Usuários:** todos os níveis de usuário.

# 6. Requisitos não funcionais

Requisitos não funcionais (**RNFs**) são as restrições impostas a um sistema que definem seus atributos de qualidade.

Eles geralmente são indicados por adjetivos como **segurança**, **desempenho** e **escalabilidade**.

**6.1 Categorias de requisitos não funcionais**

Os requisitos não funcionais são importantes porque ajudam a garantir que o sistema atenda às necessidades do usuário.

Os Requisitos Não Funcionais explicam as limitações e restrições do sistema a ser projetado. **Esses requisitos não têm nenhum
impacto na funcionalidade do aplicativo.** Além disso, existe uma prática comum de subclassificar os requisitos não funcionais em várias categorias:

- Interface de Usuário
- Confiabilidade
- Segurança
- Atuação
- Manutenção

Os requisitos não funcionais podem ser divididos em duas categorias:

1. **Atributos de qualidade:** Estas são as características do sistema que determinam sua qualidade geral. Exemplos de atributos de qualidade incluem segurança, desempenho e usabilidade.
2. **Restrições:** Estas são as limitações impostas ao sistema.
   Exemplos de restrições incluem tempo, recursos e ambiente.

**6.2 Vantagens dos requisitos não funcionais**

Os requisitos não funcionais ajudam a garantir que o sistema seja:

1. Adaptado às necessidades do usuário.
2. Adequado à finalidade.
3. Escalável, seguro e confiável.
4. Fácil de usar e manter.

**6.3 Exemplos de requisitos não funcionais**

Aqui estão alguns exemplos de requisitos não funcionais:

1. **Segurança**: O sistema deve ser protegido contra acesso não
   autorizado.
2. **Atuação**: O sistema deve ser capaz de lidar com o número necessário
   de usuários sem qualquer degradação no desempenho.
3. **Escalabilidade**: O sistema deve ser capaz de aumentar ou diminuir
   conforme necessário.
4. **Disponibilidade**: O sistema deve estar disponível quando necessário.
5. **Manutenção**: O sistema deve ser fácil de manter e atualizar.
6. **Portabilidade**: O sistema deve ser capaz de rodar em diferentes
   plataformas com alterações mínimas.
7. **Confiabilidade**: O sistema deve ser confiável e atender aos requisitos
   do usuário.
8. **Usabilidade**: O sistema deve ser fácil de usar e entender.
9. **Compatibilidade**: O sistema deve ser compatível com outros sistemas.
10. **Conformidade**: O sistema deve cumprir todas as leis e regulamentos
    aplicáveis.

**6.4 Exemplo de organização dos requisitos não funcionais**

(_A seguir, um exemplo de organização de requisitos não funcionais._)

**Requisitos não funcionais:**

- **R.N.F. 01 - Nome do requisito não funcional:** descrição do requisito.
- **R.N.F. 02 - Nome do requisito não funcional:** descrição do requisito.

**Exemplos de requisitos não funcionais:**

**Sistema de Padaria**:

- **R.N.F. 01 - Navegador homologado:** O sistema deverá ser homologado para os navegadores Google Chrome e Mozilla Firefox.
- **R.N.F. 02 - Processador:** É recomendado para o sistema no mínimo um processador Intel i3, similar ou superior a geração 7100 ou AMD Ryzen 3 da geração similar ou superior ao 3100, para que o servidor funcione em sua melhor performance.
- **R.N.F. 03 - Memória RAM:** é recomendável que o sistema possua no mínimo 2GB de RAM para melhor performance.
- **R.N.F. 04 - Arquitetura:** Será utilizada a arquitetiura MVC para o desenvolvimento do sistema, com uso de uma API REST para comunicação com o banco de dados.
- **R.N.F. 05 - Banco de dados:** O sistema será implementado com o banco de dados MySQL.
- **R.N.F. 06 - Conexão com banco de dados:** Para conexão com o banco de dados, o sistema utilizará a ferramenta de MySQL Connector.
- **R.N.F. 07 - Implementação:** O sistema deverá ser desenvolvido com linguagem Python, Javascript, HTML5, CSS3 e SQL.
- **R.N.F. 08 - Segurança:** Ficará a critério do responsável do estabelecimento a segurança dos acessos ao sistema, tendo consciência das pessoas que possua permissão para acesso.
- **R.N.F. 09 - Ambiente de Desenvolvimento Integrado (IDE):** Para criação do sistema, será utilizado o editor de texto Visual Studio Code.
- **R.N.F. 10 - Disponibilidade:** O sistema irá atender 99% do tempo de uso, somente ocorreria problemas de cadastro, remoção, inserção ou alteração em casos de falta de rede ou energia.
- **R.N.F. 11 - Legais:** O sistema deve atender às exigências da LGPD (Leis Gerais da Proteção de Dados).

**Sistema de Ordem de Serviço:**

- **R.N.F. 01 - Navegadores homologados:** o sistema deverá ser homologado para os navegadores Google Chrome e Mozilla Firefox.
- **R.N.F. 02 - Tecnologia Front-end:** Para a exibição em front-end, o software utilizará o CSS3 e o HTML5, além do framework Vue.js.
- **R.N.F. 03- Tecnologia Back-end:** O software será desenvolvido pela linguagem de programação Python, com o framework Django e a API REST com Django REST Framework.
- **R.N.F. 04 - Interoperabilidade:** O banco de dados será o MySQL, com a linguagem SQL de banco, sendo todo produzido através do MySQL Workbench .
- **R.N.F. 05 - Forma de uso do software:** O sistema por fazer parte de um ambiente interno, provavelmente será utilizado de acordo com as horas de trabalho da empresa, mas estará ativo 24 horas por dia em 7 dias por semana.
- **R.N.F. 06 - Desempenho:** Para a utilização correta e com uma qualidade e eficiência melhor, é recomendado que se use o SO mais atualizado, com recursos de hardware equivalentes a um processador intel i3 5°Gen ou semelhante, e 8GB de memória RAM, assim como os navegadores homologados.
- **R.N.F. 07- Autenticação:** Para realizar o acesso ao sistema é necessário ter um usuário de autenticação criado pelo administrador, além da possibilidade de solicitar um envio de redefinição de senha.
- **R.N.F. 08 - Web Server:** O servidor web utilizado será o Apache Tomcat, nas versões mais atualizadas.
- **R.N.F. 09 - Níveis de segurança:** O software terá diferentes tipos de acesso para cada tipo de login, tendo as permissões ideais a função de cada um.

**6.6 Conclusão**

Requisitos não funcionais são essenciais para qualquer sistema. Eles ajudam a garantir que o sistema atenda às necessidades do usuário e seja capaz de funcionar como pretendido.

É importante considerar cuidadosamente todos os requisitos não funcionais antes de projetar e desenvolver um sistema.
Eles ajudam a garantir que o sistema atenda às necessidades do usuário e seja capaz de funcionar como pretendido.

# 7. Diagrama de Caso de Uso

**7.1 Introdução**

O diagrama de caso de uso é uma ferramenta de modelagem que descreve o comportamento de um sistema a partir da perspectiva do usuário. Ele é usado para capturar os requisitos funcionais de um sistema.

- Especificam a visão externa do sistema.
- Descrevem como o sistema é percebido por seus usuários.
- Descrevem as interações entre os usuários e o sistema.

![Diagrama de Caso de Uso](img/dcu1.png "Diagrama de Caso de Uso")

**Os casos de uso:**

- Descrevem como os **usuários interagem com o sistema** (as funcionalidades do sistema)
- Facilitam a **organização dos requisitos** de um sistema.
- Dão uma **visão externa** do sistema
- O conjunto de casos de uso deve ser capaz de comunicar a **funcionalidade** e o **comportamento** do sistema para o cliente.
- Descrevem **o que** o sistema faz, mas **não** especificam **como** isso deve ser feito.

**7.2 Elementos do diagrama de caso de uso**

7.2.1 **Atores**

- Representam os papéis desempenhados por **elementos externos** ao sistema
  - Ex: humano (usuário), dispositivo de hardware ou outro sistema (cliente)
- Elementos que **interagem** com o sistema

Notação:

![Atores Notação](img/dcu_atores_notacao.png "Atores Notação")

**Exemplo: Loja de CDs**

**Identificando os atores**

- Uma loja de CDs possui discos para venda. Um cliente pode comprar uma quantidade ilimitada de discos para isto ele deve se dirigir à loja.
- A loja possui um **atendente** cuja função é atender os clientes durante a venda dos discos. A loja também possui um **gerente** cuja função é administrar o estoque para que não faltem discos. Além disso é ele quem dá folga ao atendente, ou seja, ele também atende os clientes durante a venda dos discos.

![Identificando os atores](img/dcu_identificando_atores.png "Identificando os atores")

**E o cliente?**

- Não é ator pois ele **não interage** com o sistema!

**7.2.2 Casos de uso**

- Representam **funcionalidades** do sistema (requisitos funcionais).
- São iniciados por **atores** ou por outros casos de uso.

> **Dica**: nomeie os casos de uso com **verbos** no **infinitivo**.

Notação:

![Casos de uso Notação](img/dcu_casos_de_uso_notacao.png "Casos de uso Notação")

**Exemplo: Loja de CDs**

**Identificando os casos de uso**

- Uma loja de CDs possui discos para venda. Um cliente pode comprar uma quantidade ilimitada de discos para isto ele deve se dirigir à loja. A loja possui um atendente cuja função é atender os clientes durante a **venda dos discos**.
- A loja também possui um gerente cuja função é **administrar o estoque** para que não faltem discos. Além disso é ele quem dá folga ao atendente, ou seja, ele também atende os clientes durante a **venda dos discos**.

![Identificando os casos de uso](img/dcu_identificando_casos_de_uso.png "Identificando os casos de uso")

**7.2.3 Relacionamentos**

**7.2.3.1 Relacionamento de associação**

- Indica que um ator **participa** de um caso de uso, ou seja, o ator **interage** (comunica-se) com o caso de uso.
- É representado por uma **linha sólida**.
- Um ator pode se relacionar com **um ou mais casos de uso**.

> Dicas:
>
> - Não use setas nas linhas de associação.
> - Associações não representam fluxo de informação.

![Relacionamento de associação](img/dcu_relacionamento_de_associacao.png "Relacionamento de associação")

**Exemplo: Loja de CDs**

**Identificando os relacionamentos de associação**

- Uma loja de CDs possui discos para venda. Um cliente pode comprar uma quantidade ilimitada de discos para isto ele deve se dirigir à loja. A loja possui um _atendente_ cuja função é atender os clientes durante a **venda dos discos**.
- A loja também possui um _gerente_ cuja função é **administrar o estoque** para que não faltem discos. Além disso é ele quem dá folga ao _atendente_, ou seja, ele também atende os clientes durante a **venda dos discos**.

![Identificando os relacionamentos de associação](img/dcu_identificando_relacionamentos_de_associacao.png "Identificando os relacionamentos de associação")

**7.2.3.2 Relacionamento de generalização/especialização**

**Generalização de atores**

- Quando dois ou mais atores podem se **comunicar com o mesmo conjunto de casos de uso**.
- Indica que um ator **herda** as características de outro ator.
  – Um filho (herdeiro) pode se comunicar com todos os casos de uso que seu pai se comunica.

> **Dica:** coloque os herdeiros **embaixo**.

**Notação:**

![Relacionamento de generalização/especialização de atores - notação](img/dcu_relacionamento_de_generalizacao_especializacao_notacao_de_atores.png "Relacionamento de generalização/especialização de atores - notação")

**Exemplo: Loja de CDs**

**Identificando os relacionamentos de generalização/especialização de atores**

![Identificando os relacionamentos de generalização/especialização de atores](img/dcu_identificando_relacionamentos_de_generalizacao_especializacao_de_atores.png "Identificando os relacionamentos de generalização/especialização de atores")

**Generalização de casos de uso**

– O caso de uso filho herda o comportamento e o significado do caso de uso pai.
– O caso de uso filho pode incluir ou sobrescrever o comportamento do caso de uso pai.
– O caso de uso filho pode substituir o caso de uso pai em qualquer lugar que ele apareça.

> **Dica:** deve ser aplicada quando uma condição resulta na definição de
> diversos fluxos alternativos.

Notação:

![Relacionamento de generalização/especialização de casos de uso - notação](img/dcu_relacionamento_de_generalizacao_especializacao_notacao_de_casos_de_uso.png "Relacionamento de generalização/especialização de casos de uso - notação")

**Exemplo: Loja de CDs**

**Identificando os relacionamentos de generalização/especialização de casos de uso**

**Novos requisitos:**

- As vendas podem ser **à vista** ou **a prazo**. Em ambos os casos o estoque é
  atualizado e uma nota fiscal, entregue ao consumidor.
- No caso de uma **venda à vista**, clientes cadastrados na loja e que compram mais de 5 CDs de uma só vez ganham um desconto de 1% para cada ano de cadastro.
- No caso de uma **venda a prazo**, ela pode ser parcelada em 2 pagamentos com um
  acréscimo de 20%. As vendas a prazo podem ser pagas no **cartão** ou no **boleto**.
  - Para pagamento com **boleto**, são gerados boletos bancários que são entregues ao cliente e armazenados no sistema para lançamento posterior no caixa.
  - Para pagamento com **cartão**, os clientes com mais de 10 anos de cadastro na loja ganham o mesmo desconto das compras à vista.

![Identificando os relacionamentos de generalização/especialização de casos de uso](img/dcu_identificando_relacionamentos_de_generalizacao_especializacao_de_casos_de_uso.png "Identificando os relacionamentos de generalização/especialização de casos de uso")

**Identificando mais relacionamentos de generalização/especialização de casos de uso**

![Identificando mais relacionamentos de generalização/especialização de casos de uso](img/dcu_identificando_mais_relacionamentos_de_generalizacao_especializacao_de_casos_de_uso.png "Identificando mais relacionamentos de generalização/especialização de casos de uso")

**7.2.3.3 Relacionamento de dependência**

**Extensão**

- Representa uma variação/extensão do comportamento do caso de uso base.
- O caso de uso estendido só é executado sob certas circunstâncias.
- Separa partes obrigatórias de partes opcionais.
  - Partes obrigatórias: caso de uso base.
  - Partes opcionais: caso de uso estendido.
- Fatorar comportamentos variantes do sistema (podendo reusar este comportamento
  em outros casos de uso).

**Notação:**

![Relacionamento de dependência (extensão) - notação](img/dcu_relacionamento_de_dependencia_extensao_notacao.png "Relacionamento de dependência (extensão) - notação")

**Exemplo: Loja de CDs**

**Identificando os relacionamentos de dependência (extensão)**

**Novos requisitos:**

- No caso de uma venda à vista, clientes cadastrados na loja e que compram mais
  de 5 CDs de uma só vez ganham um **desconto** de 1% para cada ano de cadastro.
- No caso de uma venda a prazo...
  - ...Para pagamento com cartão, os clientes com mais de 10 anos de cadastro na loja ganham o mesmo **desconto** das compras à vista.

![Identificando os relacionamentos de dependência (extensão)](img/dcu_identificando_relacionamentos_de_dependencia_extensao.png "Identificando os relacionamentos de dependência (extensão)")

**Inclusão**

- Evita repetição ao fatorar uma atividade
  comum a dois ou mais casos de uso.
- Um caso de uso pode incluir vários casos de uso.

**Notação:**

![Relacionamento de dependência (inclusão) - notação](img/dcu_relacionamento_de_dependencia_inclusao_notacao.png "Relacionamento de dependência (inclusão) - notação")

**Exemplo: Loja de CDs**

**Novos requisitos:**
Para efetuar vendas ou administrar estoque, atendentes e gerentes terão que **validar** suas respectivas senhas de
acesso ao sistema.

![Identificando os relacionamentos de dependência (inclusão)](img/dcu_identificando_relacionamentos_de_dependencia_inclusao.png "Identificando os relacionamentos de dependência (inclusão)")

**7.2.4 Fronteira do sistema**

- Elemento opcional (mas essencial para um bom
  entendimento).
- Serve para definir a área de atuação do sistema, ou seja, seus limites.

**Identificando a fronteira do sistema**

![Identificando a fronteira do sistema](img/dcu_identificando_a_fronteira_do_sistema.png "Identificando a fronteira do sistema")

---
