# Regra: Curso em Rascunho

## Descrição

Esta regra define o comportamento do sistema em relação à matrícula de alunos em cursos com status **Rascunho**.

## Regra

- Cursos com status **Rascunho** não estão disponíveis para matrícula de alunos.
- Enquanto o curso permanecer em rascunho:
  - **Não será possível realizar matrículas** de forma manual ou automatizada.
  - O curso também **não será exibido** para os alunos.
  - Somente administradores ou permissões que tenham acesso ao curso, conseguirão manuseá-lo.

## Objetivo

Evitar que alunos tenham acesso a cursos que ainda estão em fase de configuração, edição ou aprovação, garantindo que somente conteúdos prontos e revisados estejam acessíveis.

## Exemplo

Se um curso "Excel Intermediário" estiver com status **Rascunho**:
- Tentativas de matrícula via painel do aluno, integração ou administrativa **não serão permitidas**.
- Para permitir a matrícula, o curso deve ser alterado para o status **Publicado**.

## Observação

Essa regra contribui para o controle de qualidade dos cursos disponíveis na plataforma, evitando o acesso a materiais incompletos ou em revisão.

## 🧩 Local de Implementação

- Na listagem de cursos disponíveis/meus cursos para o aluno.
- No fluxo de matrícula (manual, automatizada ou via integração).
- No painel administrativo de cursos.

---

## 📄 Fonte da Regra

- Especificação da Plataforma EAD

---

## 🔐 Requisitos de Plano

- Disponível para todos os planos de aluno.

---

## 🔗 Tags

`curso-rascunho` `matrícula-bloqueada` `controle-de-qualidade` `administração` `ead`

