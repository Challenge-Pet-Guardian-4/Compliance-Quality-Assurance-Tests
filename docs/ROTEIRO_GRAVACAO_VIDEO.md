# 🎬 Roteiro de Gravação de Vídeo — Compliance, Quality Assurance & Tests
> **FIAP Challenge 2026 — Sprint 4 | Turma: 2TDSPG**  
> **Projeto:** PetGuardian (Clyvo Vet)  
> **Duração estimada:** 3 a 5 minutos  
> **Objetivo:** Demonstrar a conformidade total dos Testes Manuais no Azure DevOps (80%) e a Automação de Integração de APIs no Postman (20%).

---

## 🛠️ Checklist Pré-Gravação (Deixe pronto antes de apertar REC)

1. **Aba 1 do Navegador:** Azure DevOps aberto em `Test Plans` > `Test plans` (Projeto: `Sprint 4 – Azure DevOps`).
2. **Aba 2 do Navegador:** Azure DevOps aberto em `Test Plans` > `Progress report` (onde o círculo já está 100% verde!).
3. **Aba 3 do Navegador:** Repositório GitHub aberto na branch `develop` mostrando o `README.md`.
4. **Postman Desktop Aberto:**
   - Coleção `PetGuardian — QA Automated Integration Tests (Sprint 4)` visível no painel esquerdo.
   - Ambiente `PetGuardian — Environment (Cloud Production)` selecionado no canto superior direito.
   - Janela do **Runner** pronta para clicar no botão azul de executar.

---

## ⏱️ Minuto a Minuto com Fala Sugerida

### 📍 [00:00 - 00:35] Bloco 1: Abertura e Apresentação
**Na tela:** Slide inicial ou tela do repositório GitHub com os nomes e RMs.

> *"Olá, professores! Somos a equipe do PetGuardian, turma 2TDSPG, composta por Enzo Okuizumi, Gustavo Okada, Lucas Barros Gouveia, Luna Guimarães e Milton Marcelino.*  
> *Neste vídeo, vamos apresentar a entrega oficial da Sprint 4 para a disciplina de Compliance, Quality Assurance & Tests, demonstrando a cobertura completa de testes manuais no Azure DevOps e a automação de testes de integração da nossa API em nuvem utilizando o Postman."*

---

### 📍 [00:35 - 01:50] Bloco 2: Testes Manuais de Software no Azure DevOps (Parte A — 80%)
**Na tela:** Mudar para o navegador na aba **Test Plans** > **Test plans**.

> *"Iniciando pela Parte A, estruturamos nossos testes de validação no nível de sistema diretamente no **Azure Test Plans**. Dividimos a solução em 4 grandes Planos de Testes: **Usuários**, **Família**, **Educação** e **IA**, cobrindo 33 casos de teste rigorosos."*

*(Ação: Clicar no plano 'Usuários' e abrir o caso de teste #1871 ou #1884)*

> *"Como exigido no edital e demonstrado nas aulas do Prof. Paulo Sampaio, trabalhamos com a técnica de **dados controlados**. Definimos parâmetros dinâmicos usando o prefixo `@` — como `@nome`, `@email`, `@ddd`, `@telefone` e `@cep` —, com ações claras e saídas esperadas estritas para cada etapa de execução."*

*(Ação: Clicar na aba **Chart** e depois na aba **Progress report**)*

> *"Na aba **Chart**, configuramos os gráficos analíticos de controle: um gráfico por **Outcome** para monitorar o status dos testes e outro por **Run by** para garantir a rastreabilidade do QA responsável. Como podemos ver também no **Progress report**, 100% dos testes da suíte estão executados e devidamente validados."*

---

### 📍 [01:50 - 03:50] Bloco 3: Automação de Testes de Integração com Postman (Parte B — 20%)
**Na tela:** Mudar para o software **Postman Desktop**.

> *"Agora, para a Parte B de automação de testes funcionais e de integração, implementamos uma suíte completa no **Postman**, apontando diretamente para a nossa API Java Spring Boot em produção na nuvem Azure no App Service.*  
> *No ambiente do Postman, configuramos a variável `baseUrl` para a URL da nuvem e as credenciais de teste."*

*(Ação: Passar rapidamente o mouse ou abrir as requisições 1 a 7)*

> *"Nossa coleção possui 7 requisições encadeadas que testam o ciclo de vida real da aplicação com asserções em JavaScript (`pm.test`):*  
> 1. *Primeiro, realizamos o login com credenciais válidas (`POST /login`), validando status 200, extraindo o token Bearer JWT e salvando na variável de ambiente;*  
> 2. *Em seguida, cadastramos um Pet dependente (`POST /pets`), validando HTTP 201 e persistência relacional no Oracle;*  
> 3. *Criamos uma tarefa preventiva de cuidados (`POST /tarefas`) valendo 10 pontos de saúde no status `PENDENTE`;*  
> 4. *Concluímos a tarefa (`PATCH /concluir`), mudando atonicamente o estado para `CONCLUIDO`;*  
> 5. *Invocamos a **Stored Procedure Oracle** `PKG_PETGUARDIAN.CALCULAR_PONTOS_PET` via endpoint `/pets/{{id}}/pontos`, comprovando que a procedure computou os 10 pontos em tempo real no banco de dados;*  
> 6. *Testamos a resiliência e validação da API com payload quebrado (`POST /pets`), verificando o status `400 Bad Request` retornado pelo `GlobalExceptionHandler`;*  
> 7. *E, por fim, executamos um **Teardown limpo** (`DELETE /pets/{{id}}`), que apaga o pet de teste com status 204, garantindo uma suíte 100% idempotente que não polui o banco de produção."*

*(Ação: Clicar com o botão direito na coleção > **Run Collection** > Clicar no botão azul **Run PetGuardian**)*

> *"Vamos executar a coleção inteira em tempo real no Collection Runner..."*  
*(Aguardar os 4 a 5 segundos enquanto as barras verdes vão subindo)*  
> *"Como podemos observar, todas as **15 asserções** foram executadas com sucesso: 100% de aprovação, tempo médio de resposta abaixo de 1 segundo e zero falhas!"*

---

### 📍 [03:50 - 04:30] Bloco 4: Conclusão e Repositório GitHub
**Na tela:** Mudar para o repositório GitHub (`branch develop`).

> *"Para finalizar, todos os artefatos — incluindo o arquivo da coleção e ambiente do Postman, a matriz detalhada dos 33 casos de teste, o script utilitário de sincronização em Python e a documentação completa — estão versionados e públicos no nosso repositório oficial do GitHub na branch obrigatória **`develop`**.*  
> *Além disso, o professor já possui acesso configurado como membro Basic e Administrador no nosso Azure DevOps para auditoria.*  
> *Muito obrigado a todos!"*

---

## 💡 Dicas Importantes para o Dia da Gravação

1. **Resolução de Tela:** Grave em 1080p (Full HD) para que os textos do Postman e do Azure fiquem perfeitamente legíveis.
2. **Postman:** Se a letra estiver pequena no Postman, pressione `Ctrl` + `+` uma ou duas vezes para dar zoom antes de começar a gravar.
3. **Sem Pressa:** Fale pausadamente; o tempo do roteiro dá exatamente entre 3:30 e 4:30 minutos.
4. **Publicação no YouTube:** Suba o vídeo como **Não Listado** (Unlisted) ou **Público**, copie o link e cole na linha 23 do [`Compliance-Quality-Assurance-Tests/README.md`](file:///c:/Users/Enzo/new_backup/FIAP/_Projetos/Challenge_Clyvo_4/Compliance-Quality-Assurance-Tests/README.md).
