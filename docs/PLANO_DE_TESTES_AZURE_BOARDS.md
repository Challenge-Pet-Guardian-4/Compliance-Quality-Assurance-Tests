# 📋 Plano de Testes Manuais de Software — Azure Boards (80%)
## 🐾 Projeto: PetGuardian (Challenge 2026 — Clyvo Vet)
> **Disciplina:** Compliance, Quality Assurance & Tests — 4ª Sprint  
> **Plataforma de Gestão:** [Azure Boards](https://dev.azure.com/PetGuardian/Sprint%204%20%E2%80%93%20Azure%20DevOps)

---

## 👥 Integrantes

| Nome | RM | Turma |
| :--- | :---: | :---: |
| **Enzo Okuizumi** | **561432** | 2TDSPG |
| **Gustavo Okada** | **563428** | 2TDSPG |
| **Lucas Barros Gouveia** | **566422** | 2TDSPG |
| **Luna de Carvalho Guimarães** | **562290** | 2TDSPG |
| **Milton Marcelino** | **564836** | 2TDSPG |

---

## 🎯 Configuração de Acesso do Professor
* **Organização no Azure DevOps:** `PetGuardian`
* **Nível de Acesso na Organização:** Perfil **Basic**
* **Acesso no Projeto:** **Administrator** do Projeto `Sprint 4 – Azure DevOps`

---

## 🧪 Matriz de Casos de Testes Manuais com Dados Controlados

### Caso de Teste 01 (TC-01): Autenticação de Cuidador e Emissão de Sessão JWT
* **Objetivo:** Validar a segurança e o controle de acesso de cuidadores cadastrados no sistema PetGuardian, garantindo a geração de Bearer Token JWT válido para autenticação de APIs e sincronização mobile.
* **Pré-condições:** Usuário previamente cadastrado na base relacional Oracle (ou seed de inicialização).
* **Dados de Entrada Controlados:**
  - `email`: `"enzo.admin@petguardian.com"`
  - `senha`: `"123mudar"`
  - `metodo`: `POST /login`
* **Procedimento de Teste (Passo a Passo):**
  1. Acessar a interface de autenticação do sistema (ou endpoint `/login` via cliente HTTP/Swagger).
  2. Informar no campo de e-mail exatamente `"enzo.admin@petguardian.com"`.
  3. Informar no campo de senha exatamente `"123mudar"`.
  4. Clicar no botão "Entrar" / Enviar requisição.
  5. Observar o tempo de resposta e o cabeçalho de autorização gerado.
* **Dados de Saída Esperados:**
  - Código HTTP: `200 OK`.
  - Corpo da Resposta: JSON contendo o campo `token` preenchido com string alfanumérica JWT estruturada (`header.payload.signature`) e objeto `user` com `email: "enzo.admin@petguardian.com"`, `role: "ADMIN"`.
  - Redirecionamento bem-sucedido para o Dashboard / Home do Tutor.

---

### Caso de Teste 02 (TC-02): Cadastro de Novo Pet no Care Circle Familiar
* **Objetivo:** Validar a criação de um animal dependente vinculado ao tutor principal, garantindo integridade das regras de negócio (porte, sexo, raça e castração) e persistência relacional na tabela `PET`.
* **Pré-condições:** Usuário autenticado com token JWT ativo.
* **Dados de Entrada Controlados:**
  - `nome`: `"Rex QA Automation"`
  - `dataNasc`: `"2023-05-10"`
  - `sexo`: `"M"` (Macho)
  - `porte`: `"MEDIO"`
  - `castrado`: `true` (Sim)
  - `raca`: `"Golden Retriever"`
* **Procedimento de Teste (Passo a Passo):**
  1. No menu principal da aplicação (Mobile ou Web), acessar "Adicionar Novo Pet".
  2. Preencher o campo Nome com `"Rex QA Automation"`.
  3. Selecionar no calendário a data de nascimento `"10/05/2023"`.
  4. Selecionar o sexo `"Macho"`, porte `"Médio"` e marcar a opção "Castrado" como verdadeira (`true`).
  5. Preencher a Raça com `"Golden Retriever"`.
  6. Acionar a ação de submissão do formulário.
* **Dados de Saída Esperados:**
  - Código HTTP: `201 Created`.
  - Resposta contendo o identificador gerado dinamicamente (`id > 0`), idade calculada dinamicamente, status de castração e associação automática do usuário autenticado como `respon_princ = 'S'` na tabela `USUARIO_PET`.
  - Mensagem de sucesso na UI e exibição do card do pet na lista de animais da família.

---

### Caso de Teste 03 (TC-03): Agendamento e Conclusão de Tarefa com Gamificação de Saúde
* **Objetivo:** Validar o ciclo de vida de uma tarefa preventiva de rotina (`PENDENTE` -> `CONCLUIDO`) e o acréscimo de pontuação de bem-estar ao pet e cuidador.
* **Pré-condições:** Pet cadastrado com ID válido.
* **Dados de Entrada Controlados:**
  - `titulo`: `"Vacinação Polivalente V10"`
  - `dataPrazo`: `"2026-11-20T10:00:00"`
  - `pontos`: `50`
  - `status`: `"CONCLUIDO"`
* **Procedimento de Teste (Passo a Passo):**
  1. Acessar a aba "Tarefas e Cuidados" do pet selecionado.
  2. Criar a tarefa com título `"Vacinação Polivalente V10"` e valor de `50` pontos.
  3. Confirmar que a tarefa é exibida inicialmente no estado `PENDENTE`.
  4. Marcar a caixa de seleção de conclusão da tarefa informando a data/hora real do cumprimento.
  5. Submeter a confirmação de conclusão.
* **Dados de Saída Esperados:**
  - Código HTTP: `200 OK`.
  - Estado da tarefa atualizado para `CONCLUIDO`.
  - Acréscimo imediato de 50 pontos no saldo do pet, refletido na tabela `HISTORICO_PONTOS` e auditado no log DML do banco Oracle.

---

### Caso de Teste 04 (TC-04): Invocação de Stored Procedure Oracle para Cálculo de Pontos
* **Objetivo:** Comprovar a integração direta entre a aplicação backend e os procedimentos empacotados (`PKG_PETGUARDIAN.CALCULAR_PONTOS_PET`) no banco Oracle.
* **Pré-condições:** Pet possuindo tarefas e módulos educativos concluídos na base de dados.
* **Dados de Entrada Controlados:**
  - `Header`: `Authorization: Bearer <TOKEN_JWT>`
  - `Endpoint`: `GET /pets/me/pontos`
* **Procedimento de Teste (Passo a Passo):**
  1. Realizar requisição autenticada ao endpoint `/pets/me/pontos`.
  2. Acompanhar no console do backend a execução da chamada PL/SQL via JDBC/JPA (`PKG_PETGUARDIAN.CALCULAR_PONTOS_PET`).
  3. Verificar a agregação dos pontos computados de rotina preventiva e conteúdo educativo.
* **Dados de Saída Esperados:**
  - Código HTTP: `200 OK`.
  - Payload com `pontuacaoTotalGeral`, total de pets avaliados e distribuição analítica por animal.
  - O valor retornado na API deve ser idêntico ao resultado retornado por consulta direta:  
    `SELECT PKG_PETGUARDIAN.CALCULAR_PONTOS_PET(:id_pet) FROM DUAL;`.

---

### Caso de Teste 05 (TC-05): Consulta de Conteúdos Pedagógicos Ricos no MongoDB NoSQL
* **Objetivo:** Validar o consumo de documentos não relacionais flexíveis (trilhas educativas, dicas veterinárias e mídia de adestramento) armazenados no MongoDB.
* **Pré-condições:** Coleção `conteudos` provisionada no MongoDB via `setup_mongodb_conteudos.js`.
* **Dados de Entrada Controlados:**
  - `Endpoint`: `GET /trilhas` (ou `/conteudos/aulas`)
  - `Filtro`: Categoria `"ADESTRAMENTO_POSITIVO"`
* **Procedimento de Teste (Passo a Passo):**
  1. Acessar o módulo "Aprenda & Eduque" da aplicação.
  2. Filtrar os artigos e aulas pela categoria `"ADESTRAMENTO_POSITIVO"`.
  3. Clicar no primeiro artigo da lista para visualização de texto rico e metadados.
* **Dados de Saída Esperados:**
  - Código HTTP: `200 OK`.
  - Retorno de documento JSON contendo tags dinâmicas, tempo estimado de leitura e pontuação ao concluir o módulo.
  - Carregamento rápido sem lentidão de joins relacionais complexos.
