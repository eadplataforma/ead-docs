# 🔐 Regra de Negócio CA-CA2 - Controle de Acesso de Aula 2: Aula Requisito

> Ao ativar o recurso de aula requisito, o sistema bloqueia o acesso às aulas seguintes até que a aula obrigatória seja concluída.

---

## ✅ Descrição

Quando o recurso **"aula requisito"** está ativado em uma aula, o sistema exige que o aluno conclua essa aula antes de liberar qualquer conteúdo subsequente no curso.

Este controle é utilizado para garantir a progressão pedagógica e está disponível apenas a partir do **plano Basic**.

---

## ⚙️ Condições de Aplicação

- O **recurso de aula requisito** deve estar ativado na aula desejada
- O **plano do usuário** deve ser **Basic ou superior**
- O sistema deve verificar a **ordem das aulas** no curso
- A aula marcada como requisito deve ser **concluída pelo aluno**

---

## 🎯 Ação Esperada

- Se o aluno **não concluiu** a aula marcada como requisito:
  - ❌ Todas as aulas **posteriores** no curso ficam **bloqueadas**
  - 🧾 Exibir aviso: `Para acessar esta aula, você precisa concluir a aula: [Nome da Aula Requisito]`
- Se o aluno **concluiu** a aula requisito:
  - ✅ Conteúdo subsequente é liberado normalmente

---

## 🚫 Restrições e Exceções

- A ordem das aulas deve estar **definida corretamente** no curso
- **Múltiplas aulas** podem ser configuradas como requisito
- Aulas anteriores à aula requisito **não são bloqueadas**
- Aulas já concluídas pelo aluno **não são bloqueadas**
- Não se aplica a usuários de planos inferiores ao **Basic**

---

## 🧪 Exemplos

| Aula | Aula Requisito Ativa? | Aula Concluída? | Acesso Permitido? |
|------|------------------------|------------------|--------------------|
| Aula 2 | ✅ Aula 1 | ❌ Não | ❌ Bloqueado |
| Aula 2 | ✅ Aula 1 | ✅ Sim | ✅ Permitido |
| Aula 1 | ❌ | — | ✅ Permitido |
| Aula 3 | ✅ Aula 2 | ❌ Não | ❌ Bloqueado |
| Aula 3 | ✅ Aula 2 | ✅ Sim | ✅ Permitido |
| Aula 2 (usuário plano Free) | ✅ Aula 1 | ✅ Sim | ❌ Bloqueado (sem acesso ao recurso) |

---

## 🧩 Local de Implementação

- Navegação do aluno dentro do curso
- Hitórico de matriculas na visão do aluno
- Hitórico de matriculas na visão do admin

---

## 📄 Fonte da Regra

- Documento de Regras Acadêmicas da Plataforma, seção 8.1  
- Reunião pedagógica com coordenação – 2025-07-01

---

## 🔐 Requisitos de Plano

- Recurso **disponível apenas a partir do plano Basic**
- Clientes de planos inferioes ao Basic não tem acesso a este recurso

---

## 🔗 Tags

`controle-de-acesso` `aula-requisito` `progressao` `plano-basic` `bloqueio` `ensino`

