# 🛡️ Regra de Negócio CL-AC1 - Controle de Acesso de Aula 1: Exibir Identificação do Aluno

> Exibição de marca d'água com identificação do aluno em conteúdos de aula, como medida de segurança e rastreabilidade.

---

## ✅ Descrição

Quando o **recurso de identificação do aluno estiver ativo na aula e na configuração global do sistema**, será exibida uma **marca d'água** com o nome e/ou e-mail do aluno sobre os **conteúdos de vídeo e PDF** da aula, como forma de controle de acesso e inibição de compartilhamentos indevidos.

A marca d'água segue o estilo definido na configuração global (ex: cor, posição, opacidade, rotação, etc.).

---

## ⚙️ Condições de Aplicação

- A configuração **global de marca d’água** deve estar ativada
- O recurso **de identificação de aluno na aula específica** também deve estar ativado
- O plano do usuário deve ser **Basic ou superior**

---

## 🎯 Ação Esperada

- Exibir a marca d’água com os dados do aluno (ex: `João Silva - joao@email.com`) sobre os conteúdos de **vídeo** e **PDF**
- Aplicar o **estilo global configurado** da marca
- **Não exibir** marca d’água nos seguintes conteúdos:
  - Texto
  - Embed (YouTube, Vimeo, etc.)
  - Live
  - Google Meet

---

## 🚫 Restrições e Exceções

| Conteúdo | Exibe marca d’água? |
|----------|---------------------|
| Vídeo | ✅ Sim |
| PDF | ✅ Sim |
| Texto | ❌ Não |
| Embed (ex: YouTube) | ❌ Não |
| Live | ❌ Não |
| Meet | ❌ Não |

---

## 🧪 Exemplos

| Situação | Plano | Config Global | Config na Aula | Resultado |
|---------|-------|----------------|----------------|-----------|
| Vídeo com todas as condições atendidas | Basic | Ativa | Ativa | ✅ Marca exibida |
| PDF com config global desativada | Pro | ❌ Inativa | Ativa | ❌ Marca não exibida |
| Texto com todas as condições ativas | Pro | Ativa | Ativa | ❌ Marca não exibida |
| Vídeo com plano Free | Free | Ativa | Ativa | ❌ Marca não exibida |

---

## 🧩 Local de Implementação

- No player em que o aluno acessa o conteúdo de uma aula.
- No player em que o aluno visualiza a solução de uma questão.

---

## 📄 Fonte da Regra

- Especificação da Plataforma EAD

---

## 🔐 Requisitos de Plano

- Recurso disponível apenas a partir do **plano Basic**

---

## 🔗 Tags

`controle-de-acesso` `aula` `identificação` `marca-dagua` `plano-basic` `segurança` `restrição`

