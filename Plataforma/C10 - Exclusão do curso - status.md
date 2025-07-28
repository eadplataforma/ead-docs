# Regra: C3 - Exclusão de Curso

## Descrição

Define o comportamento do sistema ao **excluir um curso**, incluindo os efeitos sobre grupos, matrículas, módulos, aulas, produtos vinculados e status.

---

## Comportamento ao Excluir o Curso

- O curso é movido para a **Lixeira** da plataforma.
- O curso é **removido dos grupos** aos quais estava associado.
- Todas as **matrículas** dos alunos são **excluídas**.
- Todos os **módulos e aulas** vinculados ao curso são **excluídos**.
- **Produtos vinculados** ao curso são **desassociados**.
- O **status do curso (Publicado ou Rascunho)** é registrado para referência futura.

> Importante: embora os dados sejam removidos da área ativa do sistema, ficam armazenados e podem ser restaurados posteriormente.

---

## Exemplo

1. Curso "Excel Avançado", com status **Publicado**, pertence ao grupo "Pacote Office" e está vinculado ao produto "Curso Premium".
2. Alunos estão matriculados, e o curso possui vários módulos e aulas.
3. Ao excluir o curso:
   - Vai para a **Lixeira**
   - É **removido do grupo**
   - Matrículas são **excluídas**
   - Módulos e aulas são **excluídos**
   - Produto é **desvinculado**

---

## Observações

- A exclusão é **reversível** para: curso, grupos, matrículas, módulos, aulas e produtos vinculados.
- Ao restaurar o curso, o status será sempre **Rascunho**, mesmo que antes fosse Publicado.

## 🧩 Local de Implementação

- No painel administrativo de cursos (exclusão e Lixeira).
- Nos fluxos de exclusão de cursos, módulos, aulas, grupos, matrículas e produtos vinculados.
- Nos processos de reversão/restauração de dados excluídos.

---

## 📄 Fonte da Regra

- Especificação da Plataforma EAD

---

## 🔐 Requisitos de Plano

- Disponível para todos os planos.

---

## 🔗 Tags

`exclusão` `curso` `módulo` `aula` `matrícula` `produto` `grupo` `lixeira` `ead`
