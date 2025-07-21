# ⏳ Regra de Negócio CL-AC3 - Tempo de Permanência na Aula

> Define o tempo mínimo que o aluno deve permanecer na aula antes de poder marcá-la como concluída. Essa lógica impacta diretamente o desbloqueio de aulas seguintes quando há requisitos.

---

## ✅ Descrição

Se a aula possuir o campo **"tempo de permanência"** configurado (no formato `horas:minutos`), o sistema exige que o aluno permaneça ativamente na aula por esse período antes de considerá-la como **concluída**.

A aula **somente será marcada como concluída automaticamente após o tempo ser atingido**, mesmo que todo o conteúdo tenha sido visualizado. Isso afeta diretamente aulas marcadas como **requisito**, impedindo a liberação das próximas até o tempo ser cumprido.

---

## ⚙️ Condições de Aplicação

- O campo `tempo de permanência` deve estar definido na aula
- O recurso está disponível apenas para usuários com plano **Basic ou superior**
- O tempo começa a contar de acordo com o tipo de conteúdo da aula:
  - **Vídeo**: o tempo **só começa após o aluno dar play**
  - **Outros tipos (texto, PDF, embed)**: o tempo começa **no momento do acesso**

---

## 🎯 Ação Esperada

| Tipo de Aula | Início da Contagem | Condição para conclusão |
|--------------|--------------------|--------------------------|
| Vídeo | Após o aluno clicar em "play" | Tempo total configurado deve ser atingido |
| Texto / PDF / Embed | Ao abrir a aula | Tempo total configurado deve ser atingido |

- Se o tempo **não for cumprido**:
  - ❌ Aula não é marcada como concluída
  - ❌ Aulas seguintes (se houver requisito) permanecem bloqueadas
- Se o tempo for cumprido:
  - ✅ Aula marcada como concluída
  - ✅ Aulas seguintes podem ser liberadas (se o requisito for esta aula)

---

## 🧪 Exemplos

| Aula | Tipo | Tempo Configurado | Ação do Aluno | Resultado |
|------|------|-------------------|----------------|-----------|
| Aula 3 | Vídeo | 00:10 | Aluno dá play e assiste 4 min | ❌ Aula não concluída |
| Aula 5 | Texto | 00:15 | Aluno acessa e sai em 5 min | ❌ Aula não concluída |
| Aula 2 | Vídeo | 00:05 | Aluno assiste 5 min após dar play | ✅ Aula concluída |
| Aula 1 | PDF | 00:00 | Sem tempo configurado | ✅ Aula concluída imediatamente |

---

## 🚫 Restrições

- **Recurso exclusivo para o plano Basic ou superior**
- Aula **sem tempo configurado** não sofre restrição adicional
- O sistema deve impedir **"conclusões forçadas"** por manipulação de requisição ou timer

---

## 🧩 Local de Implementação

- Acesso do aluno ao conteúdo

---

## 📄 Fonte da Regra

- Especificação EAD Plataforma

---

## 🔐 Requisitos de Plano

- Recurso disponível apenas a partir do **plano Basic**

---

## 🔗 Tags

`tempo-de-permanencia` `controle-de-acesso` `aula` `conclusao` `requisito` `plano-basic`
