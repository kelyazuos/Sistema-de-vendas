# Especificações do projeto

Será construido um sistema de vendas com cadastro de funcionários na base de dados, cadastro de produtos, venda com base nos produtos cadastrados. Serão feitas validações de login a partir dos usuários cadastrados na base de dados através de consultas sql. Será possível fazer CRUD (create, read, update, delete), na maioria das informações e diversas tabelas relacionais, do projeto, além de trabalhar diversos conceitos de SQL como joins, foreign key. primary key, dentre outros. Dentro da aplicação será possível executar vendas, que serão realizadas através de produtos cadastrados, onde suas informações vão servir para trazer um processo totalmente automatizado de cálculos de valor total, descontos e trocos. Além disso todas as vendas finalizadas irão gerar notas fiscais e também vão gerar registros na base de dados onde serão armazenadas informações sobre as vendas como: horário, data, usuário que efetuou a venda vendas daquele dia, lucros e gastos.

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


  
  

 
