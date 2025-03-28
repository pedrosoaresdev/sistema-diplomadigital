# Sistema Web: Gerador de Diplomas Digitais

## Descrição

O **Sistema Web: Gerador de Diplomas Digitais** é uma plataforma online que estou desenvolvendo desenvolvimento que visa gerar diplomas digitais para cursos e treinamentos de forma prática e segura. O sistema possibilitará a criação, validação e distribuição de diplomas no formato digital, com total segurança e verificação da autenticidade através de códigos únicos. Seguindo a lógica de regra de négocios, sendo assim otimizando processos na educação.

## Funcionalidades

### 1. **Cadastro de Cursos**
   - **Descrição**: Administradores podem cadastrar novos cursos com detalhes como nome do curso, descrição, carga horária, entre outros.
   - **Regras de Negócio**:
     - Cada curso deve ter um nome único.
     - A carga horária deve ser um número positivo.
     - O curso só pode ser cadastrado se todos os campos obrigatórios forem preenchidos.

### 2. **Geração de Diplomas Digitais**
   - **Descrição**: O sistema gerará diplomas digitais automaticamente após a conclusão de um curso. O diploma conterá informações como nome do aluno, curso, carga horária, e data de emissão.
   - **Regras de Negócio**:
     - O diploma será gerado automaticamente após a conclusão do curso.
     - Cada diploma gerado terá um código único que permitirá sua validação.
     - O diploma será exportado no formato PDF.

### 3. **Validação de Diplomas**
   - **Descrição**: O sistema permitirá que qualquer pessoa valide a autenticidade de um diploma digital usando o código único gerado.
   - **Regras de Negócio**:
     - O código único do diploma deve ser utilizado para validar sua autenticidade.
     - A validação retorna informações sobre a instituição que emitiu o diploma, nome do aluno e curso.

### 4. **Distribuição de Diplomas**
   - **Descrição**: Após a geração do diploma, o sistema permitirá o envio automático por e-mail para o aluno, com um link para o download do diploma digital.
   - **Regras de Negócio**:
     - O e-mail do aluno deve estar correto para que o envio seja realizado com sucesso.
     - O aluno receberá um link para baixar o diploma em PDF.

### 5. **Acesso ao Histórico de Diplomas**
   - **Descrição**: Os alunos poderão acessar seu histórico de diplomas gerados através de um painel de usuário.
   - **Regras de Negócio**:
     - Somente alunos autenticados poderão acessar seus diplomas.
     - O histórico de diplomas será exibido por ordem de geração, permitindo que o aluno baixe ou visualize diplomas passados.

## Tecnologias

O sistema será desenvolvido utilizando as seguintes tecnologias:

- **Back-End**:
  - **Java**: Usado para a implementação da lógica de negócios, criação de APIsREST e manipulação dos dados.
  - **Spring Boot**: Framework para construção de aplicações Java, fornecendo uma estrutura robusta e escalável.
  - **JPA/Hibernate**: Para integração com banco de dados e manipulação de dados de forma eficiente.

- **Front-End**:
  - **TypeScript**: Para garantir que o código seja robusto e fácil de manter, com forte tipagem e verificação de erros em tempo de compilação.
  - **Angular**: Framework para construir interfaces ricas e dinâmicas, facilitando a interação do usuário com o sistema.
  - **HTML/CSS**: Para construção da interface do usuário, com um design responsivo e intuitivo.

- **Banco de Dados**:
  - **PostgreSQL**: Banco de dados relacional que será utilizado para armazenar dados sobre cursos, alunos, e diplomas.

- **Outras Tecnologias**:
  - **Docker**: Para garantir que o ambiente de desenvolvimento seja replicável e para facilitar o deploy em diferentes ambientes.
  - **JUnit**: Para testes unitários no back-end, garantindo que a lógica de negócios funcione corretamente.
  - **AWS S3**: Para armazenamento de arquivos como os PDFs dos diplomas gerados.

## Status do Projeto

O projeto está atualmente em **desenvolvimento**. As funcionalidades principais estão sendo implementadas, e a primeira versão está prevista para lançamento dentro de algumas semanas. Ainda existem algumas funcionalidades a serem finalizadas, como a validação de diplomas e o envio automático de e-mails, mas o desenvolvimento está progredindo bem.

## Representação do armazenamento
As informações dos diplomas, incluindo o código de validação, no banco de dados:

| **ID** | **Nome do Aluno**   | **Curso**             | **Carga Horária** | **Data de Emissão** | **Código de Validação**            |
|--------|---------------------|-----------------------|-------------------|---------------------|------------------------------------|
| 1      | João da Silva       | Desenvolvimento Web   | 80                | 2025-03-28          | E1A3F5G2H9-J7D3K0L5M8N9P1         |
| 2      | Maria Oliveira      | Design Gráfico        | 60                | 2025-03-29          | A7C3F1G9H4-J9E3K0M7N9O2           |

