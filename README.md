# Compliance, Quality Assurance & Tests — 🐾 PetGuardian
> **Sprint 4 — Consolidação Final de Testes de Software & Qualidade**  
> Desafio 2026 (2º Ano ADS — Clyvo Vet) | Turmas de Fevereiro (2TDSPG)

---

## 👥 Integrantes

| Nome | RM | Turma | GitHub | LinkedIn |
| :--- | :---: | :---: | :--- | :--- |
| **Enzo Okuizumi** | **561432** | 2TDSPG | [EnzoOkuizumiFiap](https://github.com/EnzoOkuizumiFiap) | [Enzo Okuizumi](https://www.linkedin.com/in/enzo-okuizumi-b60292256/) |
| **Gustavo Okada** | **563428** | 2TDSPG | [Gdev3356](https://github.com/Gdev3356) | [Gustavo Okada](https://www.linkedin.com/in/gustavo-okada-53a3b8359/) |
| **Lucas Barros Gouveia** | **566422** | 2TDSPG | [LuzBGouveia](https://github.com/LuzBGouveia) | [Lucas Barros Gouveia](https://www.linkedin.com/in/lucas-barros-gouveia-09b147355/) |
| **Luna de Carvalho Guimarães** | **562290** | 2TDSPG | [lunaguima](https://github.com/lunaguima) | [Luna Guimarães](https://www.linkedin.com/in/luna-guimar%C3%A3es-b0ba82309/) |
| **Milton Marcelino** | **564836** | 2TDSPG | [MiltonMarcelino](https://github.com/MiltonMarcelino) | [Milton Marcelino](https://www.linkedin.com/in/milton-marcelino-250298142) |

---

## 🔗 Links Oficiais Obrigatórios de Entrega (Sprint 4)

| Recurso | Descrição | Link Oficial |
| :--- | :--- | :--- |
| 📋 **Azure Boards & Test Plans (QA)** | Acesso aos 4 Planos de Testes Manuais com dados controlados | [Azure Boards — Sprint 4](https://dev.azure.com/PetGuardian/Sprint%204%20%E2%80%93%20Azure%20DevOps) |
| 🐙 **Repositório Oficial (Branch `develop`)** | Código de QA, matriz de testes e scripts na branch obrigatória | [GitHub — Compliance & QA](https://github.com/Challenge-Pet-Guardian-4/Compliance-Quality-Assurance-Tests/tree/develop) |
| ☕ **Repositório Java (Branch `develop`)** | Backend Spring Boot, persistência relacional e suíte de testes | [GitHub — Java Advanced (Branch develop)](https://github.com/Challenge-Pet-Guardian-4/Java-Advanced/tree/develop) |

## 🔗 Vídeo de Demonstração (Sprint 4)

[Video QA - Challenge Pet Guardian Sprint 4](https://www.youtube.com/watch?v=rt8Ic9Sq9fI)

---

## 🌐 Links do Ecossistema Integrado (Java, DevOps & Nuvem Azure)

| Componente | Descrição | Link |
| :--- | :--- | :--- |
| 🌐 **API em Produção (Azure Web App)** | Endpoint base do App Service provisionado na nuvem | [https://app-petguardian-01bd2f0c.azurewebsites.net](https://app-petguardian-01bd2f0c.azurewebsites.net) |
| 🛡️ **Console Web Admin (Produção)** | Interface web administrativa para auditoria | [https://app-petguardian-01bd2f0c.azurewebsites.net/admin](https://app-petguardian-01bd2f0c.azurewebsites.net/admin) |
| 📖 **Swagger UI Interativo (OpenAPI 3.1)** | Documentação interativa de todos os endpoints REST | [Swagger UI PetGuardian](https://app-petguardian-01bd2f0c.azurewebsites.net/swagger-ui/index.html) |
| 🩺 **Actuator Health (Observabilidade)** | Healthcheck em tempo real (Oracle + MongoDB + Liveness) | [Healthcheck Actuator](https://app-petguardian-01bd2f0c.azurewebsites.net/actuator/health) |
| ☕ **Repositório GitHub (Java Advanced)** | Aplicação Spring Boot, Stored Procedures e testes automatizados | [GitHub — Java Advanced (Branch develop)](https://github.com/Challenge-Pet-Guardian-4/Java-Advanced/tree/develop) |
| 🚀 **Repositório GitHub (DevOps & Cloud)** | Pipelines de CI/CD, IaC Bash e infraestrutura em nuvem | [GitHub — DevOps Tools](https://github.com/Challenge-Pet-Guardian-4/DevOps-Tools-Cloud-Computing) |

---

## 📑 Estrutura da Entrega de Qualidade

A entrega de QA atende integralmente à divisão percentual e critérios do edital:

```
Compliance-Quality-Assurance-Tests/
│
├── docs/
│   ├── PLANO_DE_TESTES_AZURE_BOARDS.md     # Visão Geral da Arquitetura e 5 Test Cases Core
│   └── MATRIZ_CASOS_DE_TESTE_AZURE.md      # Matriz Completa dos 33 Test Cases Cadastrados no Azure
│
├── postman/
│   ├── PetGuardian_QA_Automation.postman_collection.json # Suíte com 7 Casos Automatizados e Teardown
│   └── PetGuardian_QA_Environment.postman_environment.json # Variáveis de Ambiente (Local & Nuvem)
│
├── scripts/
│   └── azure_qa_cli.py                     # CLI Python Oficial para Gestão e Execução no Azure DevOps
│
└── README.md                               # Documentação Oficial com Links e Instruções
```

---

## 📋 PARTE A) Teste Manual de Software no Azure Boards (80%)

O plano de testes manuais foi modelado diretamente no **Azure Boards / Test Plans**, utilizando a técnica de **dados controlados** predefinidos para garantir repetibilidade e confiabilidade.

| ID | Caso de Teste | Objetivo Principal | Dados de Entrada Controlados | Resultado Esperado | Peso |
| :---: | :--- | :--- | :--- | :--- | :---: |
| **TC-01** | Autenticação de Cuidador | Validar segurança e emissão do JWT | `email`: `"enzo.admin@petguardian.com"`<br>`senha`: `"123mudar"` | HTTP 200, JWT estruturado, redirecionamento | 20% |
| **TC-02** | Cadastro de Pet no Care Circle | Validar persistência relacional na tabela `PET` | `nome`: `"Rex QA Automation"`<br>`porte`: `"MEDIO"`, `castrado`: `true`, `raca`: `"Golden Retriever"` | HTTP 201 Created, ID gerado, vínculo `USUARIO_PET` | 20% |
| **TC-03** | Ciclo de Tarefa e Gamificação | Validar transição `PENDENTE` -> `CONCLUIDO` | `titulo`: `"Vacinação V10"`<br>`pontos`: `50` | HTTP 200, +50 pontos atribuídos, auditoria DML | 20% |
| **TC-04** | Stored Procedure Oracle | Validar cálculo via `PKG_PETGUARDIAN` | Chamada ao endpoint `/pets/me/pontos` | HTTP 200, agregação de pontos calculada por procedure | 20% |
| **TC-05** | Consulta NoSQL MongoDB | Validar documentos de trilhas pedagógicas | Categoria `"ADESTRAMENTO_POSITIVO"` | HTTP 200, documento NoSQL com mídia e metadados | - |

> 📌 *O passo a passo minucioso de cada caso de teste está documentado em [`docs/PLANO_DE_TESTES_AZURE_BOARDS.md`](./docs/PLANO_DE_TESTES_AZURE_BOARDS.md).*

---

## 🤖 PARTE B) Automação de Testes de Integração com Postman (20%)

Para a automação dos testes de integração, foi desenvolvida uma coleção Postman com **7 casos de testes automatizados encadeados** com arquitetura idempotente e teardown automático (atendendo com folga à meta de no mínimo 4 casos exigida no edital), contendo scripts em JavaScript no padrão `pm.test` com validação de status code, JSON Schema, tempo de resposta, encadeamento de variáveis dinâmicas, cálculo real via Stored Procedure Oracle e limpeza de base de dados.

### 🧪 Casos de Testes Automatizados Implementados:

1. **Teste 01: Autenticação com Credenciais Válidas (Login JWT)**
   - **Verificações:** Status `200 OK`, presença de token string não vazio, validação do e-mail do usuário e extração dinâmica do `jwt_token` para o ambiente do Postman.
2. **Teste 02: Persistência de Pet no Banco Relacional (201 Created)**
   - **Verificações:** Status `201 Created`, validação de campos obrigatórios (`id`, `nome`, `porte`, `sexo`), cabeçalho `application/json` e gravação do `created_pet_id`.
3. **Teste 03: Agendamento de Tarefa Preventiva para o Pet (201 Created)**
   - **Verificações:** Status `201 Created`, vínculo automático ao `petId` recém-criado, estado inicial `PENDENTE`, pontuação (`10` pontos) e extração do `created_tarefa_id`.
4. **Teste 04: Conclusão de Rotina e Gamificação (200 OK)**
   - **Verificações:** Invocação do endpoint `PATCH /tarefas/{{created_tarefa_id}}/concluir`, validando transição para `CONCLUIDO` e disparo da bonificação de saúde.
5. **Teste 05: Invocação de Stored Procedure Oracle (`/pets/{{created_pet_id}}/pontos`)**
   - **Verificações:** Status `200 OK`, validação da execução da Stored Procedure PL/SQL `PKG_PETGUARDIAN.CALCULAR_PONTOS_PET` comprovando que os 10 pontos da tarefa recém-concluída foram computados com exatidão (`pontosTarefas == 10` e `pontosTotais == 10`).
6. **Teste 06: Validação de Resiliência e Segurança (400 Bad Request)**
   - **Verificações:** Envio de payload inválido sem autorização e campos obrigatórios, validando interceptação pelo `GlobalExceptionHandler` e status `400 Bad Request`.
7. **Teste 07: Teardown — Limpeza Automatizada do Pet de Teste (204 No Content)**
   - **Verificações:** Envio de requisição `DELETE /pets/{{created_pet_id}}`, validando status `204 No Content` e garantindo que o banco de dados Oracle permaneça limpo e a suíte seja 100% idempotente a cada execução.

---

## 🚀 Como Executar os Testes Automatizados

### Opção 1: Via Postman Desktop
1. Abra o Postman.
2. Clique em **Import** e selecione os dois arquivos da pasta `postman/`:
   - `PetGuardian_QA_Automation.postman_collection.json`
   - `PetGuardian_QA_Environment.postman_environment.json`
3. Selecione o ambiente **PetGuardian — Environment (Local & Cloud)**.
4. Clique com o botão direito na coleção e selecione **Run Collection**.
5. Clique em **Run PetGuardian — QA Automated Integration Tests**. Todos os 4 testes devem passar com 100% de sucesso.

### Opção 2: Via Linha de Comando (Newman CLI)
```bash
# Instalar o Newman globalmente (se necessário)
npm install -g newman

# Executar a coleção com relatório no terminal
newman run postman/PetGuardian_QA_Automation.postman_collection.json \
  -e postman/PetGuardian_QA_Environment.postman_environment.json \
  --reporters cli
```

### Opção 3: Via CLI Python Oficial do Projeto (`azure_qa_cli.py`)
Para gerenciar e sincronizar a suíte do Azure Boards / Test Plans via terminal:
```bash
# Exibir resumo com percentuais de execução
python scripts/azure_qa_cli.py summary

# Listar todos os 33 casos de teste cadastrados
python scripts/azure_qa_cli.py list

# Exibir detalhes e passos de um caso específico (ex: TC 1871)
python scripts/azure_qa_cli.py show 1871

# Executar todos os testes na nuvem Azure (31 Passed, 2 Failed para evidência de bugs)
python scripts/azure_qa_cli.py run-all

# Resetar todos os testes de volta para 'Active' / 'Unspecified'
python scripts/azure_qa_cli.py reset-all
```

---

## 🔒 Configuração de Permissões para Avaliação (Azure DevOps)

Para garantir acesso irrestrito do professor sem qualquer risco de penalidade:
1. **Organization Settings > Users:** Professor adicionado com perfil **Basic**.
2. **Project Settings > Permissions > Project Administrators:** Professor adicionado ao grupo de **Administradores**.
3. **Branch de Entrega:** O repositório está configurado e publicado com a branch padrão de avaliação: **`develop`**.