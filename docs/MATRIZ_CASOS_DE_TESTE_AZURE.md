# 🐾 Matriz Completa de Casos de Testes Manuais — Azure Boards
> **Sincronização Oficial:** Dados extraídos diretamente da API do Azure DevOps.
> **Organização:** `PetGuardian` | **Projeto:** `Sprint 4 – Azure DevOps`

---

## 📋 Plano de Teste: Usuários (ID: 1869)

### 📁 Suíte: Usuários (ID: 1870)

| ID Azure | Título do Caso de Teste | Status Atual | Passos Cadastrados |
| :---: | :--- | :---: | :---: |
| **#1871** | Criar usuário válido | 🟢 Passed | 11 passos |
| **#1872** | Criar usuário inválido | 🔴 Failed | 11 passos |
| **#1879** | Realizar logout de conta ativa | 🟢 Passed | 6 passos |
| **#1873** | Entrar com conta existente | 🟢 Passed | 5 passos |
| **#1874** | Tentativa de login com credenciais inválidas | 🟢 Passed | 5 passos |
| **#1875** | Editar própria conta com credenciais válidas | 🟢 Passed | 12 passos |
| **#1876** | Editar própria conta com credenciais inválidas | 🔴 Failed | 12 passos |
| **#1877** | Mudar tema do aplicativo | 🟢 Passed | 5 passos |
| **#1878** | Ativar notificações | 🟢 Passed | 10 passos |
| **#1880** | Fazer upgrade para Premium | 🟢 Passed | 6 passos |
| **#1881** | Excluir própria conta | 🟢 Passed | 6 passos |

#### 🔍 Detalhamento das Etapas e Dados Controlados:

##### 🧪 TC #1871: Criar usuário válido
**Objetivo:** Criação de um usuário no sistema com credenciais válidas.

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir o sistema` | Usuário entra na página inicial |
| 2 | `Clicar no botão &quot;Criar conta grátis&quot;` | Usuário é direcionado ao formulário de criação de conta |
| 3 | `Inserir um @nome válido no campo de nome` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 4 | `Inserir um @email válido no campo de email` | O campo recebe o email informado; a validação de formato é aplicada quando o usuário tenta prosseguir. |
| 5 | `Inserir um @ddd válido no campo de DDD` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 6 | `Inserir um @telefone válido no campo de telefone` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 7 | `Inserir um @cep válido no campo de CEP` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 8 | `Inserir um @numero válido no campo de número` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 9 | `Inserir uma @senha válida  no campo de senha` | O campo recebe o valor informado e o valor fica mascarado conforme o comportamento padrão de senha. |
| 10 | `Inserir a mesma @senha no campo de confirmar senha` | O campo recebe o valor informado e o valor fica mascarado conforme o comportamento padrão de senha. |
| 11 | `Clickar no botão de concluir cadastro` | Conta é criada e usuário é redirecionado a home. |

##### 🧪 TC #1872: Criar usuário inválido
**Objetivo:** Tentativa de erro ao criar usuário com credenciais invalidas

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir o sistema` | Usuário é direcionado a página inicial |
| 2 | `Clicar no botão &quot;Criar conta grátis&quot;` | Usuário é direcionado ao formulário de criação de conta |
| 3 | `Inserir um @nome no campo de nome` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 4 | `Inserir um @email inválido no campo de email` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 5 | `Inserir um @ddd inválido no campo de DDD` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 6 | `Inserir um @telefone inválido no campo de telefone` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 7 | `Inserir um @cep inválido no campo de CEP` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 8 | `Inserir um @numero inválido no campo de número` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 9 | `Inserir uma @senha inválida no campo de senha` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 10 | `Inserir uma @senha2 inválida diferente no campo de senha` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 11 | `Clickar no botão de concluir cadastro` | Conta não é criada e aparece um erro de credencial inválida. |

##### 🧪 TC #1879: Realizar logout de conta ativa

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir no sistema` | Usuário é direcionado a página inicial |
| 2 | `Criar conta ou entrar em uma conta existente` | Usuário é direcionado a Home |
| 3 | `Ir a aba &quot;Perfil&quot;` | Usuário é direcionado a aba Perfil |
| 4 | `Ir até o botão &quot;Encerrar Sessão (Logout)&quot;` | A seção ou controle indicado fica visível e acessível. |
| 5 | `Clicar no botão &quot;Encerrar Sessão (Logout)&quot;` | Aparece um popup perguntando se o usuário realmente deseja fazer logout |
| 6 | `Clicar no botão &quot;SAIR&quot;` | Usuário sai de sua conta e é redirecionado a tela inicial da aplicação. |

##### 🧪 TC #1873: Entrar com conta existente
**Objetivo:** Entrar em uma conta criada anteriormente com suas credenciais.

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir o sistema` | Usuário é direcionado a página inicial |
| 2 | `Clicar em &quot;Já tenho conta (Entrar)&quot;` | Usuário é direcionado ao formulário de login |
| 3 | `inserir @email existente no campo de email` | O campo recebe o email informado; a validação de formato é aplicada quando o usuário tenta prosseguir. |
| 4 | `inserir @senha existente no campo de senha` | O campo recebe o valor informado e o valor fica mascarado conforme o comportamento padrão de senha. |
| 5 | `clicar em entrar na conta` | Entra na conta existente e é redirecionado a home. |

##### 🧪 TC #1874: Tentativa de login com credenciais inválidas
**Objetivo:** Verificação de erro caso o usuário tente entrar em uma conta com credenciais inválidas.

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir o sistema` | Usuário é direcionado a página inicial |
| 2 | `clicar em &quot;Já tenho conta (Entrar)&quot;` | Usuário é direcionado ao formulário de login |
| 3 | `Digitar @email inválido no campo de email` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 4 | `Digitar @senha inválida no campo de senha` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 5 | `Clicar em entrar na conta` | Não entra em uma conta e ocorre um erro de credencial incorreta. |

##### 🧪 TC #1875: Editar própria conta com credenciais válidas
**Objetivo:** Edição das informações de um usuário no sistema com credenciais válidas.

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir o sistema` | Usuário é direcionado à página inicial |
| 2 | `Criar uma conta ou entrar em uma conta existente` | Usuário é direcionado a Home |
| 3 | `Clicar na aba &quot;Perfil&quot;` | Usuário é direcionado a aba Perfil |
| 4 | `Clicar no botão &quot;Editar Dados Cadastrais&quot;` | Usuário é direcionado a um formulário de edição de credenciais |
| 5 | `Substituir seu nome antigo por um @nome válido no campo de nome` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 6 | `Substituir seu email antigo por um @email válido no campo de email` | O campo recebe o email informado; a validação de formato é aplicada quando o usuário tenta prosseguir. |
| 7 | `Substituir seu DDD antigo por um @ddd válido no campo de DDD` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 8 | `Substituir seu telefone antigo por um @telefone válido no campo de telefone` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 9 | `Substituir seu telefone antigo por um @cep válido no campo de CEP` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 10 | `Substituir seu telefone antigo por um @numero válido no campo de número` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 11 | `Inserir sua senha @senha  no campo de senha` | O campo recebe o valor informado e o valor fica mascarado conforme o comportamento padrão de senha. |
| 12 | `Clicar no botão de salvar alterações` | Credênciais são alteradas |

##### 🧪 TC #1876: Editar própria conta com credenciais inválidas
**Objetivo:** Edição das informações de um usuário no sistema com credenciais inválidas.

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir o sistema` | Usuário é direcionado a página inicial |
| 2 | `Criar conta ou entrar em uma conta existente` | Usuário é direcionado a Home |
| 3 | `Clicar na aba &quot;Perfil&quot;` | Usuário é direcionado a aba Perfil |
| 4 | `Clicar no botão &quot;Editar Dados Cadastrais&quot;` | Usuário é direcionado a um formulário de edição de credenciais |
| 5 | `Substituir seu nome antigo por um @nome inválido no campo de nome` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 6 | `Substituir seu email antigo por um @email inválido no campo de email` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 7 | `Substituir seu DDD antigo por um @ddd inválido no campo de DDD` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 8 | `Substituir seu telefone antigo por um @telefone inválido no campo de telefone` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 9 | `Substituir seu telefone antigo por um @cep inválido no campo de CEP` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 10 | `Substituir seu telefone antigo por um @numero inválido no campo de número` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 11 | `Inserir @senha inválida  no campo de senha` | O sistema identifica o dado inválido/diferente e apresenta validação quando aplicável; o valor não deve ser aceito silenciosamente. |
| 12 | `Clicar no botão de salvar alterações` | Credênciais não são alteradas e aparece um alerta de credencial inválida |

##### 🧪 TC #1877: Mudar tema do aplicativo
**Objetivo:** Mudança do tema da interface do aplicativo para um usuário

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir o sistema` | Usuário é direcionado a Tela inicial |
| 2 | `Criar conta ou entrar em uma conta existente` | Usuário é direcionado a Home |
| 3 | `Ir na aba &quot;perfil&quot;` | Usuário é direcionado a aba Perfil |
| 4 | `Clicar no botão &quot;Tema do Aplicativo&quot;` | Aplicativo muda para tema escuro |
| 5 | `Clicar no botão &quot;Tema do aplicativo&quot; novamente` | Aplicativo muda para tema claro |

##### 🧪 TC #1878: Ativar notificações
**Objetivo:** Ativação das notificações de lembretes para a conta do usuário.

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | Usuário é direcionado a tela inicial |
| 2 | `Criar conta ou entrar em uma conta existente` | Usuário é direcionado a home |
| 3 | `Ir na aba &quot;Perfil&quot;` | Usuário é direcionado a aba Perfil |
| 4 | `Clicar no botão &quot;lembretes e notificações&quot;` | Usuário é direcionado a um menu de configurações de notificação |
| 5 | `Clicar no botão &quot;Abrir configurações do celular&quot;` | Aplicação redireciona usuário para as configurações do seu celular |
| 6 | `Ativar notificações na configuração do celular` | Usuário ativa as configuração de permissão de notificação da aplicação |
| 7 | `Voltar a tela do petguardian` | Usuário retorna a tela do petguardian |
| 8 | `Clicar no slider de &quot;Lembretes de Tarefas&quot;` | Notificações da aplicação são ativadas |
| 9 | `Escolher entre as 5 opções de @tempo` | Opção fica marcada com um check |
| 10 | `Clicar em salvar preferências` | Notificações de lembretes são ativadas com @tempo de antecedência. |

##### 🧪 TC #1880: Fazer upgrade para Premium
**Objetivo:** Promoção da conta do usuário para premium, disponibilizando acesso a funcionalidades.

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | Usuário é direcionado a página inicial |
| 2 | `Criar conta ou entrar em uma conta existente` | Usuário é direcionado a Home |
| 3 | `Ir a aba &quot;Perfil&quot;` | Usuário é direcionado a aba Perfil |
| 4 | `Clicar no botão &quot;Fazer Upgrade para Premium&quot;` | Usuário é direcionado a um menu listando beneficios de ser Premium |
| 5 | `Clicar no botão &quot;Confirmar e Ativar Premium&quot;` | Usuário é direcionado ao processo de pagamento |
| 6 | `Realizar processo de pagamento` | Usuário tem sua conta promovida para Premium |

##### 🧪 TC #1881: Excluir própria conta
**Objetivo:** Exclusão da conta do usuário no sistema

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | Usuário é direcionado a página inicial |
| 2 | `Criar conta ou entrar em uma conta existente` | Usuário é direcionado a Home |
| 3 | `Ir a aba &quot;Perfil&quot;` | Usuário é direcionado a aba Perfil |
| 4 | `Ir ao botão &quot;Excluir Minha Conta&quot;` | Usuário encontra o botão |
| 5 | `Clicar no botão &quot;Excluir Minha Conta&quot;` | Aparece um popup perguntando se o usuário tem certeza que quer excluir sua conta |
| 6 | `Clicar em &quot;EXCLUIR DEFINITIVAMENTE&quot;` | Conta do usuário é excluida do sistema. |

---

## 📋 Plano de Teste: Familia (ID: 1882)

### 📁 Suíte: Familia (ID: 1883)

| ID Azure | Título do Caso de Teste | Status Atual | Passos Cadastrados |
| :---: | :--- | :---: | :---: |
| **#1884** | Adicionar pet | 🟢 Passed | 11 passos |
| **#1885** | Convidar familiar | 🟢 Passed | 7 passos |
| **#1886** | Editar ficha do pet | 🟢 Passed | 13 passos |
| **#1887** | Criar um registro de saúde | 🟢 Passed | 8 passos |
| **#1888** | Editar registro de saúde | 🟢 Passed | 7 passos |
| **#1889** | Excluir registro de saúde de pet | 🟢 Passed | 7 passos |
| **#1890** | Transferir titularidade de pet | 🟢 Passed | 7 passos |
| **#1892** | Deixar de cuidar de um pet | 🟢 Passed | 7 passos |
| **#1894** | Criar tarefa válida para pet | 🟢 Passed | 10 passos |
| **#1895** | Concluir tarefa existente | 🟢 Passed | 5 passos |
| **#1896** | Editar tarefa existente | 🟢 Passed | 10 passos |
| **#1897** | Excluir tarefa existente | 🟢 Passed | 6 passos |
| **#1891** | Excluir Co-cuidador do pet | 🟢 Passed | 7 passos |
| **#1893** | Excluir pet | 🟢 Passed | 6 passos |

#### 🔍 Detalhamento das Etapas e Dados Controlados:

##### 🧪 TC #1884: Adicionar pet
**Objetivo:** Adição de um pet a uma familia existente.

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | Usuário é direcionado a página inicial |
| 2 | `Criar conta ou entrar em uma conta existente` | Usuário é direcionado a Home |
| 3 | `Ir a aba &quot;Family&quot;` | Usuário é direcionado a aba &quot;Family&quot; |
| 4 | `Clicar no botão &quot;Adicionar Pet&quot;` | Usuário é direcionado a um formulário de cadastro de pet |
| 5 | `Inserir @nome_pet válido` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 6 | `Inserir @raça válida` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 7 | `Inserir @data_nascimento válida` | O campo recebe a data/horário informado e permite prosseguir apenas se o valor atender às regras de validação. |
| 8 | `Escolher @porte_pet` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 9 | `Inserir @sexo_pet` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 10 | `Escolher se pet é @castrado ou não` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 11 | `Clicar em &quot;Cadastrar Pet&quot;` | Pet é adicionado e usuário vira seu &quot;Tutor Principal&quot;. |

##### 🧪 TC #1885: Convidar familiar
**Objetivo:** Convida um familiar como tutor para a familia.

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | Usuário é direcionado à página inicial |
| 2 | `Criar conta ou entrar em uma conta existente` | Usuário é direcionado à Home |
| 3 | `Ir a aba &quot;Family&quot;` | Usuário é direcionado à aba &quot;Family&quot; |
| 4 | `Clicar no botão &quot;Convidar&quot;` | Aparece um form pedindo que o usuário insira o email do convidado. |
| 5 | `Inserir @email da conta existente` | O campo recebe o email informado; a validação de formato é aplicada quando o usuário tenta prosseguir. |
| 6 | `Selecionar um @pet que está na familia` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 7 | `Clicar no botão &quot;Enviar Convite&quot;` | Usuário aparece como &quot;Co-cuidador&quot; do @pet escolhido. |

##### 🧪 TC #1886: Editar ficha do pet
**Objetivo:** Informações do pet são editadas pelo &quot;Tutor Principal&quot;

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | Usuário é direcionado a página inicial |
| 2 | `Criar ou entrar em uma conta existente` | Usuário é direcionado à página Home |
| 3 | `Ter o vínculo de &quot;Tutor Principal&quot; sobre um @pet existente` | O sistema executa a ação indicada e apresenta o resultado esperado do fluxo, sem erro inesperado. |
| 4 | `Ir a aba &quot;Family&quot;` | Usuário é direcionado à aba &quot;Family&quot; |
| 5 | `Clicar em um @pet` | O controle selecionado responde à interação e a próxima tela/diálogo esperado é exibido. |
| 6 | `Clicar em &quot;Editar Ficha&quot;` | Usuário é direcionado à um form de credenciais do pet |
| 7 | `Substituir o nome do @pet por um @nome_pet novo` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 8 | `Substituir a raça do @pet por uma @raca nova` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 9 | `substituir a data de nascimento do @pet por uma @data_nascimento nova` | O campo recebe a data/horário informado e permite prosseguir apenas se o valor atender às regras de validação. |
| 10 | `Substituir o porte do @pet por um @porte novo` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 11 | `Substituir o sexo do @pet por um @sexo movo` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 12 | `Substituir a escolha do @castrado para a outra opção` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 13 | `Clicar em &quot;Salvar Alterações&quot;` | Credênciais do pet são alteradas. |

##### 🧪 TC #1887: Criar um registro de saúde
**Objetivo:** Cria um registro de saúde do pet

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Criar conta ou entrar em uma conta existente` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Possuir vinculo com o pet em uma familia` | O sistema executa a ação indicada e apresenta o resultado esperado do fluxo, sem erro inesperado. |
| 4 | `Ir a aba &quot;Family&quot;` | A seção ou controle indicado fica visível e acessível. |
| 5 | `Clicar em um pet` | O controle selecionado responde à interação e a próxima tela/diálogo esperado é exibido. |
| 6 | `Clicar no botão &quot;Registrar&quot;` | O formulário de registro de saúde é aberto para inserir os dados do evento/atendimento. |
| 7 | `Escrever tipo de @evento ou usar uma das sugestões no campo de evento / atendimento` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 8 | `Inserir @data_evento no campo de data do evento` | O campo recebe a data/horário informado e permite prosseguir apenas se o valor atender às regras de validação. |

##### 🧪 TC #1888: Editar registro de saúde
**Objetivo:** Usuário de uma familia realiza a edição de um registro de saúde do pet

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Criar conta ou entrar em uma conta existente` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Ir a aba &quot;Family&quot;` | A seção ou controle indicado fica visível e acessível. |
| 4 | `Clicar em um pet` | O controle selecionado responde à interação e a próxima tela/diálogo esperado é exibido. |
| 5 | `Clicar no icone de lápis do lado de um registro de saúde existente` | O controle selecionado responde à interação e a próxima tela/diálogo esperado é exibido. |
| 6 | `Substituir campo de evento / atendimento por um novo @evento ou usar as &quot;Sugestões Rápidas&quot;` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 7 | `Substituir campo de data do evento por uma @data_evento nova` | O campo recebe a data/horário informado e permite prosseguir apenas se o valor atender às regras de validação. |

##### 🧪 TC #1889: Excluir registro de saúde de pet
**Objetivo:** Cuidador de um pet vinculado a sua conta exclui seu registro de saúde

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Criar conta ou entrar em conta existente` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Ir a aba &quot;Family&quot;` | A seção ou controle indicado fica visível e acessível. |
| 4 | `Clicar em um pet existente` | O controle selecionado responde à interação e a próxima tela/diálogo esperado é exibido. |
| 5 | `Ir até &quot;Prontuario e Saúde&quot;` | A seção ou controle indicado fica visível e acessível. |
| 6 | `Clicar no ícone de &quot;Excluir&quot; abaixo do botão &quot;Registrar&quot;` | O formulário de registro de saúde é aberto para inserir os dados do evento/atendimento. |
| 7 | `Clicar em &quot;EXCLUIR&quot;` | O item selecionado é removido após a confirmação e deixa de aparecer na lista. |

##### 🧪 TC #1890: Transferir titularidade de pet
**Objetivo:** Transfere vínculo de &quot;Tutor principal&quot; para um co-cuidador de um pet.

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Entrar em conta vínculada a um pet como &quot;Tutor principal&quot;` | O sistema executa a ação indicada e apresenta o resultado esperado do fluxo, sem erro inesperado. |
| 3 | `Ir a aba &quot;Family&quot;` | A seção ou controle indicado fica visível e acessível. |
| 4 | `Clicar em um pet` | O controle selecionado responde à interação e a próxima tela/diálogo esperado é exibido. |
| 5 | `Ir a rede de cuidado` | A seção ou controle indicado fica visível e acessível. |
| 6 | `Clicar no ícone de coroa do lado de um &quot;Co-cuidador&quot;` | A titularidade é transferida após confirmação; a rede de cuidado mostra o novo Tutor Principal. |
| 7 | `Clicar em &quot;TRANSFERIR&quot;` | A titularidade é transferida após confirmação; a rede de cuidado mostra o novo Tutor Principal. |

##### 🧪 TC #1892: Deixar de cuidar de um pet
**Objetivo:** Cuidador de um pet saí de sua rede de cuidado

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Entrar em uma conta vínculada a um pet como &quot;Co-cuidador&quot;` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Ir a aba &quot;Family&quot;` | A seção ou controle indicado fica visível e acessível. |
| 4 | `Clicar em um pet` | O controle selecionado responde à interação e a próxima tela/diálogo esperado é exibido. |
| 5 | `Ir a &quot;Rede de Cuidado&quot;` | A seção ou controle indicado fica visível e acessível. |
| 6 | `Clicar no ícone de &quot;Sair&quot; do lado de seu perfil` | A seção selecionada é exibida corretamente. |
| 7 | `Clicar em &quot;SAIR&quot;` | O item selecionado é removido após a confirmação e deixa de aparecer na lista. |

##### 🧪 TC #1894: Criar tarefa válida para pet
**Objetivo:** Usuário vinculado a um pet cria tarefa para sua rede de cuidado realizar

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Entrar em uma conta vinculada a um pet` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Ir a aba &quot;Family&quot;` | A seção ou controle indicado fica visível e acessível. |
| 4 | `Clicar em &quot;Nova Tarefa&quot;` | O controle selecionado responde à interação e a próxima tela/diálogo esperado é exibido. |
| 5 | `Selecionar @pet` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 6 | `Inserir @titulo da tarefa` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 7 | `Inserir @descricao da tarefa` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 8 | `Inserir @xp de recompensa, com valor de 0 a 10` | O valor é preenchido; o sistema aceita somente um número dentro do intervalo indicado no caso de teste. |
| 9 | `Inserir @data e @horario de prazo` | O campo recebe a data/horário informado e permite prosseguir apenas se o valor atender às regras de validação. |
| 10 | `Clicar em &quot;Criar Tarefa&quot;` | O controle selecionado responde à interação e a próxima tela/diálogo esperado é exibido. |

##### 🧪 TC #1895: Concluir tarefa existente
**Objetivo:** Usuário da Rede de Cuidado de um pet conclui sua tarefa

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Entrar em uma conta vinculada a um pet` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Ir a aba &quot;Family&quot;` | A seção ou controle indicado fica visível e acessível. |
| 4 | `Ir a uma tarefa existente` | A seção ou controle indicado fica visível e acessível. |
| 5 | `Clicar no icone de check ao lado da tarefa` | A tarefa passa para o estado concluído e a interface reflete a alteração. |

##### 🧪 TC #1896: Editar tarefa existente
**Objetivo:** Usuário da Rede de Cuidado de um pet edita sua tarefa

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Entrar em uma conta vinculada a um pet` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Ir a aba &quot;Family&quot;` | A seção ou controle indicado fica visível e acessível. |
| 4 | `Clicar no ícone de edição do lado do xp da tarefa` | O controle selecionado responde à interação e a próxima tela/diálogo esperado é exibido. |
| 5 | `Selecionar @pet` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 6 | `Substituir @titulo da tarefa` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 7 | `Substituir @descricao da tarefa` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 8 | `Substituir @xp da tarefa` | O valor é preenchido; o sistema aceita somente um número dentro do intervalo indicado no caso de teste. |
| 9 | `Substituir @data e @horario de prazo` | O campo recebe a data/horário informado e permite prosseguir apenas se o valor atender às regras de validação. |
| 10 | `Clicar em &quot;Salvar Alterações&quot;` | As alterações válidas são salvas e os dados atualizados aparecem no perfil. |

##### 🧪 TC #1897: Excluir tarefa existente
**Objetivo:** Usuario da Rede de Cuidado de um pet exclui sua tarefa

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Entrar em uma conta vinculada a um pet` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Ir a aba &quot;Family&quot;` | A seção ou controle indicado fica visível e acessível. |
| 4 | `Ir a uma tarefa` | A seção ou controle indicado fica visível e acessível. |
| 5 | `Clicar no ícone de exclusão do lado do ícone de edição` | O controle selecionado responde à interação e a próxima tela/diálogo esperado é exibido. |
| 6 | `Clicar em &quot;EXCLUIR&quot;` | O item selecionado é removido após a confirmação e deixa de aparecer na lista. |

##### 🧪 TC #1891: Excluir Co-cuidador do pet
**Objetivo:** &quot;Tutor principal&quot; exclui &quot;Co-cuidador&quot; da rede de cuidado de um pet

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Entrar em uma conta que está vinculada a um pet como &quot;Tutor Principal&quot;` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Ir a aba &quot;Family&quot;` | A seção ou controle indicado fica visível e acessível. |
| 4 | `Clicar em um pet vinculado` | O controle selecionado responde à interação e a próxima tela/diálogo esperado é exibido. |
| 5 | `Ir a &quot;Rede de Cuidado&quot;` | A seção ou controle indicado fica visível e acessível. |
| 6 | `Clicar no ícone de exclusão do lado de um &quot;Co-cuidador&quot;` | O controle selecionado responde à interação e a próxima tela/diálogo esperado é exibido. |
| 7 | `Clicar em &quot;REMOVER&quot;` | O item selecionado é removido após a confirmação e deixa de aparecer na lista. |

##### 🧪 TC #1893: Excluir pet
**Objetivo:** Tutor principal exclui pet do sistema

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Entrar em uma conta vinculada a um pet como &quot;Tutor principal&quot;` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Ir a aba &quot;Family&quot;` | A seção ou controle indicado fica visível e acessível. |
| 4 | `Clicar em um pet` | O controle selecionado responde à interação e a próxima tela/diálogo esperado é exibido. |
| 5 | `Clicar em &quot;Excluir&quot;` | O item selecionado é removido após a confirmação e deixa de aparecer na lista. |
| 6 | `Clicar em &quot;EXCLUIR&quot;` | O item selecionado é removido após a confirmação e deixa de aparecer na lista. |

---

## 📋 Plano de Teste: Educação (ID: 1898)

### 📁 Suíte: Educação (ID: 1899)

| ID Azure | Título do Caso de Teste | Status Atual | Passos Cadastrados |
| :---: | :--- | :---: | :---: |
| **#1902** | Realizar lição | 🟢 Passed | 8 passos |
| **#1903** | Desmarcar lição concluída | 🟢 Passed | 6 passos |

#### 🔍 Detalhamento das Etapas e Dados Controlados:

##### 🧪 TC #1902: Realizar lição
**Objetivo:** Usuário da Rede de Cuidado de um pet realiza sua lição

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Entrar em uma conta vinculada a um pet` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Ir a aba &quot;Educação&quot;` | A seção ou controle indicado fica visível e acessível. |
| 4 | `Escolher um @pet` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 5 | `Clicar em um modulo não concluido` | O módulo selecionado é aberto e seu status de conclusão é exibido corretamente. |
| 6 | `Ler &quot;Passo a Passo&quot; e seus ensinamentos` | O conteúdo indicado é exibido e pode ser consultado sem erro. |
| 7 | `Verificar &quot;Links e Recursos Recomendados&quot;` | O conteúdo indicado é exibido e pode ser consultado sem erro. |
| 8 | `Clicar no botão &quot;Concluir e Ganhar Pontos!&quot;` | O módulo passa a constar como concluído e os pontos correspondentes são contabilizados uma única vez. |

##### 🧪 TC #1903: Desmarcar lição concluída
**Objetivo:** Desmarca uma lição que estava concluída

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Entrar em uma conta que esteja vinculada a um pet` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Ir a aba &quot;Educação&quot;` | A seção ou controle indicado fica visível e acessível. |
| 4 | `Escolher um @pet` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 5 | `Clicar em modulo concluido` | O módulo selecionado é aberto e seu status de conclusão é exibido corretamente. |
| 6 | `Clicar no botão &quot;Desmarcar Aula Concluída&quot;` | O módulo deixa de constar como concluído; a pontuação é ajustada conforme as regras do aplicativo. |

---

## 📋 Plano de Teste: IA (ID: 1900)

### 📁 Suíte: IA (ID: 1901)

| ID Azure | Título do Caso de Teste | Status Atual | Passos Cadastrados |
| :---: | :--- | :---: | :---: |
| **#1904** | Realizar pergunta ao assistente desvinculado de pet | 🟢 Passed | 4 passos |
| **#1905** | Realizar pergunta ao assistente vínculado ao pet | 🟢 Passed | 5 passos |
| **#1906** | Ver histórico de conversa vinculado a um pet | 🟢 Passed | 5 passos |
| **#1908** | Criar novo chat | 🟢 Passed | 5 passos |
| **#1907** | Excluir chat anterior | 🟢 Passed | 6 passos |
| **#1909** | Realizar pergunta fora do contexto | 🟢 Passed | 4 passos |

#### 🔍 Detalhamento das Etapas e Dados Controlados:

##### 🧪 TC #1904: Realizar pergunta ao assistente desvinculado de pet
**Objetivo:** Usuário que não está vinculado a um pet realiza pergunta dentro do contexto

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Criar uma conta premium ou entrar em uma conta premium existente que não está vínculada a um pet` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Clicar no botão do chatbot no centro inferior da tela` | A ação é executada e a tela/diálogo correspondente é exibida sem erro. |
| 4 | `Relizar @pergunta para IA ou usar mensagens prontas disponibilizadas.` | A mensagem é enviada e fica visível na conversa; o assistente apresenta uma resposta relacionada à pergunta e ao contexto selecionado. |

##### 🧪 TC #1905: Realizar pergunta ao assistente vínculado ao pet
**Objetivo:** Usuário vínculado a um pet realiza pergunta a IA do sistema

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Entrar em uma conta premium vinculada a um pet` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Clicar no botão do chatbot no centro inferior` | A ação é executada e a tela/diálogo correspondente é exibida sem erro. |
| 4 | `Escolher @pet que servira de contexto` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 5 | `Realizar @pergunta ou usar mensagem pronta do sistema` | A mensagem é enviada e fica visível na conversa; o assistente apresenta uma resposta relacionada à pergunta e ao contexto selecionado. |

##### 🧪 TC #1906: Ver histórico de conversa vinculado a um pet
**Objetivo:** Usuário ve o histórico do chat de IA que está vinculado a temas do pet escolhido

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Entrar em uma conta premium vinculada a um pet` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Clicar no botão do chatbot no centro inferior` | A ação é executada e a tela/diálogo correspondente é exibida sem erro. |
| 4 | `Escolher @pet que servira para o contexto` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 5 | `Clicar no botão &quot;Histórico&quot;` | O histórico de conversas do pet selecionado é exibido, sem misturar conversas de outros pets. |

##### 🧪 TC #1908: Criar novo chat
**Objetivo:** Cria um novo chat com IA para o pet vinculado

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Entrar em uma conta premium vinculada a um pet` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Clicar no botão do chatbot localizado no centro inferior` | A ação é executada e a tela/diálogo correspondente é exibida sem erro. |
| 4 | `Escolher @pet que servira de contexto` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 5 | `Clicar no botão &quot;Nova Dúvida&quot;` | Uma nova conversa é iniciada, sem reutilizar as mensagens da conversa anterior. |

##### 🧪 TC #1907: Excluir chat anterior
**Objetivo:** Usuário exclui chat realizado com a IA vinculada ao seu pet

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Entrar em uma conta premium vinculada a um pet` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Clicar no botão do chatbot no centro inferior` | A ação é executada e a tela/diálogo correspondente é exibida sem erro. |
| 4 | `Escolher @pet que vai servir para o contexto` | O campo/controle recebe a informação selecionada ou digitada, mantendo o formulário pronto para a próxima etapa. |
| 5 | `Clicar no botão &quot;Histórico&quot;` | O histórico de conversas do pet selecionado é exibido, sem misturar conversas de outros pets. |
| 6 | `Clicar no icone de &quot;excluir&quot; do lado de um chat` | O item selecionado é removido após a confirmação e deixa de aparecer na lista. |

##### 🧪 TC #1909: Realizar pergunta fora do contexto
**Objetivo:** Usuário realiza pergunta que não está relacionada com a premissa do sistema

| # | Ação (Entrada) | Resultado Esperado (Saída) |
| :-: | :--- | :--- |
| 1 | `Abrir sistema` | A tela inicial do PetGuardian é exibida sem erro. |
| 2 | `Criar conta premium ou entrar em uma conta premium existente` | O usuário autenticado é direcionado à Home; a sessão fica ativa. |
| 3 | `Clicar no botão de chatbot localizado no centro inferior` | A ação é executada e a tela/diálogo correspondente é exibida sem erro. |
| 4 | `Realizar @pergunta fora do escopo do aplicativo` | A pergunta é enviada; o assistente responde de forma segura e orienta o usuário ao escopo do aplicativo, sem inventar orientação veterinária. |

---
