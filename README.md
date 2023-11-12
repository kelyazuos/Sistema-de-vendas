# Especificações do projeto

Será construido um sistema de vendas com cadastro de funcionários na base de dados, cadastro de produtos, venda com base nos produtos cadastrados. Serão feitas validações de login a partir dos usuários cadastrados na base de dados através de consultas sql. Será possível fazer CRUD (create, read, update, delete), na maioria das informações e diversas tabelas relacionais, do projeto, além de trabalhar diversos conceitos de SQL como joins, foreign key. primary key, dentre outros. Dentro da aplicação será possível executar vendas, que serão realizadas através de produtos cadastrados, onde suas informações vão servir para trazer um processo totalmente automatizado de cálculos de valor total, descontos e trocos. Além disso todas as vendas finalizadas irão gerar notas fiscais e também vão gerar registros na base de dados onde serão armazenadas informações sobre as vendas como: horário, data, usuário que efetuou a venda vendas daquele dia, lucros e gastos.

# Sistema de Gestão de Vendas

## Introdução

A eficiência e automação são pilares fundamentais no ambiente empresarial moderno, impulsionados pela incessante busca por otimização de processos e aprimoramento da gestão. Diante dessa demanda, apresentamos o Sistema de Gestão de Vendas, uma solução abrangente que visa integrar desde o cadastro de funcionários e produtos até a conclusão de vendas e o registro minucioso de transações.

Este projeto emprega conceitos avançados de bancos de dados relacionais, como chaves primárias e estrangeiras, e implementa funcionalidades essenciais, incluindo autenticação de usuários, geração automática de notas fiscais e um sistema de registros para análise detalhada das operações comerciais.

## Funcionalidades Principais

- Cadastro eficiente de funcionários e produtos.
- Realização de vendas com cálculos automáticos de valores totais, descontos e trocos.
- Geração automática de notas fiscais eletrônicas para conformidade com regulamentações fiscais.
- Registros detalhados de transações para análise de desempenho, lucratividade e tomada de decisões estratégicas.

## Tecnologias Utilizadas

- Linguagem: Python
- Banco de Dados: SQL Sever
- ORM: SQLAlchemy
- Criptografia: [Inserir Biblioteca]
- Outras dependências especificadas no arquivo `requirements.txt`

## Instalação

1. Clone o repositório: `git clone https://github.com/kelyazuos/Sistema-de-vendas.git`
2. Instale as dependências: `pip install -r requirements.txt`
3. Configure o ambiente e o banco de dados conforme necessário.

## Uso

1. Execute o sistema: `python main.py`
2. Acesse a aplicação pelo navegador ou cliente.

## Contribuição

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues ou enviar pull requests.

# Objetivo do Projeto

O principal objetivo deste projeto é desenvolver um sistema abrangente de gestão de vendas que ofereça uma solução completa e integrada para otimizar os processos comerciais. Através da implementação de um conjunto de funcionalidades, o sistema visa atender às seguintes metas:

## 1. Automação Operacional:
- Automatizar as principais operações comerciais, desde o cadastro de funcionários e produtos até a conclusão de vendas, proporcionando eficiência e redução de erros manuais.

## 2. Controle de Acesso Seguro:
- Implementar um sistema de autenticação seguro para controlar o acesso de usuários, garantindo a confidencialidade das informações e a integridade do sistema.

## 3. Gestão Eficiente de Produtos:
- Facilitar o gerenciamento de produtos através de funcionalidades CRUD (Create, Read, Update, Delete), possibilitando a rápida adaptação às mudanças no catálogo.

## 4. Operações Comerciais Avançadas:
- Possibilitar a realização de vendas através de produtos cadastrados, com cálculos automatizados de valores totais, descontos e trocos, proporcionando uma experiência de compra eficiente.

## 5. Registro Detalhado de Transações:
- Registrar informações detalhadas sobre cada venda, incluindo data, horário, produtos vendidos e usuário responsável, para análises precisas de desempenho e tomada de decisões informada.

## 6. Geração Automática de Notas Fiscais:
- Implementar um mecanismo de geração automática de notas fiscais eletrônicas, garantindo conformidade com regulamentações fiscais locais e simplificando processos burocráticos.

## 7. Análise de Desempenho e Lucratividade:
- Fornecer ferramentas para análise de desempenho comercial, permitindo a avaliação de lucros, gastos e outras métricas relevantes.

## 8. Adoção de Boas Práticas de Desenvolvimento:
- Seguir boas práticas de desenvolvimento de software, como o uso de testes unitários, documentação adequada, e otimização de consultas SQL para garantir a confiabilidade, manutenibilidade e desempenho do sistema.

# ESQUELETO GERAL DO PROJETO 

1. Configuração do Banco de Dados: 

   - Escolha um banco de dados SQL, como MySQL, PostgreSQL ou SQLite. 

   - Crie as tabelas necessárias para armazenar informações sobre funcionários, produtos, vendas, notas fiscais e registros. 

2. Cadastro de Funcionários: 

   - Crie um formulário para adicionar funcionários à base de dados. 

   - Valide os campos do formulário, como nome, sobrenome, senha, etc. 

   - Armazene informações do funcionário na tabela apropriada. 

3. Cadastro de Produtos: 

   - Crie um formulário para adicionar produtos à base de dados. 

   - Valide os campos do formulário, como nome do produto, preço, estoque, etc. 

   - Armazene informações do produto na tabela apropriada. 

4. Sistema de Login: 

   - Implemente um sistema de login que verifica as credenciais do usuário na base de dados. 

5. Vendas: 

   - Crie uma interface para realizar vendas, onde você pode selecionar produtos e quantidades. 

   - Calcule o valor total, descontos e troco automaticamente. 

   - Atualize o estoque dos produtos após uma venda. 

   - Gere notas fiscais e registre informações da venda. 

6. Registros e Relatórios: 

   - Registre informações de cada venda, incluindo horário, data, funcionário, produtos vendidos, valor total, descontos, etc. 

   - Crie relatórios para analisar as vendas diárias, lucros, gastos, etc. 

   - Utilize consultas SQL com junções (joins) para obter dados relacionais entre tabelas. 

7. CRUD (Create, Read, Update, Delete): 

   - Implemente operações CRUD para funcionários e produtos, permitindo adicionar, ler, atualizar e excluir registros. 

8. Outros Conceitos SQL: 

   - Use conceitos como chaves primárias (primary keys) e chaves estrangeiras (foreign keys) para manter integridade referencial. 

   - Utilize junções (joins) para buscar dados de tabelas relacionadas.
  
   Certamente! Baseando-me nas informações fornecidas anteriormente, aqui está uma lista consolidada de requisitos funcionais e não funcionais para o sistema de vendas em C#:

### Requisitos Funcionais:

#### 1. Autenticação e Autorização:
   - **RF1:** O sistema deve permitir que os usuários façam login usando credenciais válidas (nome de usuário e senha).
   - **RF2:** O sistema deve autenticar os usuários com base nas informações armazenadas no banco de dados.

#### 2. Cadastro de Funcionários:
   - **RF3:** O sistema deve permitir o cadastro de novos funcionários, incluindo informações como nome, cargo e credenciais de login.
   - **RF4:** O sistema deve permitir a atualização das informações dos funcionários.
   - **RF5:** O sistema deve permitir a exclusão de funcionários do banco de dados.

#### 3. Cadastro de Produtos:
   - **RF6:** O sistema deve permitir o cadastro de novos produtos, incluindo informações como nome, descrição, preço e quantidade em estoque.
   - **RF7:** O sistema deve permitir a atualização das informações dos produtos.
   - **RF8:** O sistema deve permitir a exclusão de produtos do banco de dados.

#### 4. Vendas:
   - **RF9:** O sistema deve permitir que os funcionários selecionem produtos para venda.
   - **RF10:** O sistema deve calcular o valor total da venda com base nos produtos selecionados, aplicando descontos, se houver.
   - **RF11:** O sistema deve permitir a finalização da venda, incluindo a geração de nota fiscal.
   - **RF12:** O sistema deve calcular o troco, se o cliente pagar com um valor superior ao total da compra.
   - **RF13:** O sistema deve registrar a venda no banco de dados, incluindo informações como horário, data, produtos vendidos, valor total e funcionário responsável.

#### 5. Relatórios:
   - **RF14:** O sistema deve permitir a geração de relatórios diários de vendas, incluindo informações sobre vendas, lucros e gastos.
   - **RF15:** O sistema deve permitir a visualização de histórico de vendas por funcionário.

### Requisitos Não Funcionais:

#### 1. **Desempenho:**
   - **RNF1:** O sistema deve ser responsivo, fornecendo feedback ao usuário dentro de 5 segundos para qualquer operação.
   - **RNF2:** O sistema deve ser capaz de lidar com pelo menos 50 usuários simultâneos sem degradação significativa no desempenho.

#### 2. **Segurança:**
   - **RNF3:** As senhas dos usuários devem ser armazenadas de forma segura, utilizando algoritmos de hash seguros com salt para proteger contra ataques de força bruta.
   - **RNF4:** O sistema deve ter controle de acesso baseado em papéis (RBAC), garantindo que apenas usuários autorizados tenham permissões específicas.

#### 3. **Confiabilidade:**
   - **RNF5:** O sistema deve ter um backup diário dos dados para evitar a perda de informações em caso de falha.
   - **RNF6:** O sistema deve ser capaz de se recuperar automaticamente de falhas, minimizando o tempo de inatividade.

#### 4. **Usabilidade:**
   - **RNF7:** A interface do usuário deve ser intuitiva e fácil de usar, exigindo o mínimo de treinamento para os usuários.
   - **RNF8:** O sistema deve fornecer feedback claro e mensagens de erro compreensíveis para orientar os usuários em caso de problemas.

#### 5. **Manutenibilidade:**
   - **RNF9:** O código fonte deve ser bem organizado e seguir as melhores práticas de programação para facilitar a manutenção e extensibilidade do sistema.
   - **RNF10:** O sistema deve ser modular, permitindo a fácil adição ou remoção de funcionalidades sem afetar outras partes do sistema.

#### 6. **Compatibilidade:**
   - **RNF11:** O sistema deve ser compatível com os principais navegadores web, como Chrome, Firefox, Safari e Edge.
   - **RNF12:** O sistema deve ser compatível com sistemas operacionais Windows, macOS e Linux.

#### 7. **Documentação:**
   - **RNF13:** O sistema deve ter uma documentação abrangente, incluindo manual do usuário, guia de instalação e documentação técnica para facilitar o entendimento e a manutenção do sistema.

#### 8. **Escalabilidade:**
   - **RNF15:** O sistema deve ser escalável, permitindo a adição de mais usuários, produtos e transações sem comprometer o desempenho.


     Com base nos requisitos funcionais fornecidos, é possível identificar vários casos de uso para o sistema de vendas em C#. Aqui estão alguns exemplos de casos de uso:

## Casos de Uso do Sistema de Vendas:

#### 1. **Autenticação do Usuário:**
   - **Ator:** Funcionário
   - **Descrição:** O funcionário fornece suas credenciais (nome de usuário e senha) para acessar o sistema.
   - **Fluxo Principal:**
     1. O sistema exibe a tela de login.
     2. O funcionário insere seu nome de usuário e senha.
     3. O sistema valida as credenciais.
     4. Se as credenciais forem válidas, o funcionário é autenticado e pode acessar o sistema.

#### 2. **Gerenciamento de Funcionários:**
   - **Ator:** Administrador
   - **Descrição:** O administrador pode adicionar, visualizar, atualizar e excluir informações de funcionários no sistema.
   - **Fluxo Principal:**
     1. O administrador seleciona a opção de gerenciamento de funcionários.
     2. O sistema exibe a lista de funcionários.
     3. O administrador pode adicionar um novo funcionário, editar as informações de um funcionário existente ou excluir um funcionário.

#### 3. **Gerenciamento de Produtos:**
   - **Ator:** Administrador
   - **Descrição:** O administrador pode adicionar, visualizar, atualizar e excluir informações de produtos no sistema.
   - **Fluxo Principal:**
     1. O administrador seleciona a opção de gerenciamento de produtos.
     2. O sistema exibe a lista de produtos disponíveis.
     3. O administrador pode adicionar um novo produto, editar as informações de um produto existente ou excluir um produto.

#### 4. **Realização de Vendas:**
   - **Ator:** Funcionário
   - **Descrição:** O funcionário pode selecionar produtos para venda, calcular o total, aplicar descontos, finalizar a venda e gerar uma nota fiscal.
   - **Fluxo Principal:**
     1. O funcionário seleciona produtos da lista de produtos disponíveis.
     2. O sistema calcula o valor total da compra.
     3. O funcionário aplica descontos, se houver.
     4. O funcionário finaliza a venda, indicando o método de pagamento.
     5. O sistema gera uma nota fiscal para a venda.

#### 5. **Geração de Relatórios:**
   - **Ator:** Funcionário
   - **Descrição:** O funcionário pode gerar relatórios diários de vendas e visualizar o histórico de vendas por funcionário.
   - **Fluxo Principal:**
     1. O funcionário seleciona a opção de geração de relatórios.
     2. O sistema permite ao funcionário escolher entre relatório diário ou histórico de vendas por funcionário.
     3. O sistema gera o relatório solicitado e o exibe para o funcionário.

As regras de negócio definem as políticas, diretrizes e restrições que guiam o comportamento do sistema. Elas ajudam a garantir a consistência dos dados e a lógica de negócios em toda a aplicação. Com base nos requisitos apresentados, aqui estão algumas regras de negócio para o sistema de vendas em C#:

### Regras de Negócio:

#### 1. **Autenticação de Usuários:**
   - **RN1:** Apenas usuários cadastrados no sistema podem fazer login.
   - **RN2:** As credenciais de login (nome de usuário e senha) devem ser validadas antes de permitir o acesso ao sistema.

#### 2. **Gerenciamento de Funcionários:**
   - **RN3:** O nome de usuário de um funcionário deve ser único no sistema.
   - **RN4:** Todos os funcionários devem ter um cargo atribuído (por exemplo, vendedor, gerente).
   - **RN5:** Um funcionário não pode ser excluído se tiver registros de vendas associados a ele.

#### 3. **Gerenciamento de Produtos:**
   - **RN6:** O código de identificação único de um produto (SKU) deve ser único no sistema.
   - **RN7:** O preço de um produto não pode ser negativo ou zero.
   - **RN8:** A quantidade em estoque de um produto não pode ser negativa.

#### 4. **Realização de Vendas:**
   - **RN9:** O sistema deve calcular corretamente o valor total da venda com base nos produtos selecionados e nos descontos aplicados.
   - **RN10:** O sistema deve calcular corretamente o troco, se o cliente pagar com um valor superior ao total da compra.
   - **RN11:** A venda só pode ser finalizada se houver pelo menos um produto na lista de itens vendidos.

#### 5. **Geração de Relatórios:**
   - **RN12:** Os relatórios diários de vendas devem incluir informações precisas sobre vendas, lucros e gastos do dia.
   - **RN13:** O histórico de vendas por funcionário deve ser preciso e mostrar todas as vendas realizadas por um funcionário específico.

#### 6. **Segurança:**
   - **RN14:** A senha do usuário deve ser armazenada de forma segura, utilizando técnicas de hash e salt para proteger contra acesso não autorizado.
   - **RN15:** As transações devem ser protegidas contra acessos não autorizados. Apenas usuários autenticados têm permissão para realizar vendas ou acessar informações confidenciais.

#### 7. **Outras Regras:**
   - **RN16:** O sistema deve manter um registro de todas as transações de vendas, incluindo informações sobre produtos vendidos, horário da venda, valor total, descontos aplicados e funcionário responsável.


  
  

 
