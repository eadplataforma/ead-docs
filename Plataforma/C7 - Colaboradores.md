# Recurso: Colaboradores

## Descrição

O recurso de **Colaboradores** permite ao administrador adicionar usuários que irão atuar como **professores** ou **tutores** em um curso. Esses colaboradores podem ser atribuídos a **módulos** e **aulas**, conforme a necessidade do conteúdo.

---

## Funcionalidades

- Adição de colaboradores no curso.
- Associação de colaboradores a módulos e aulas específicas.
- Definição de papéis (professor ou tutor) para facilitar a organização pedagógica e administrativa.

---

## Regra: Adição de Colaborador no Curso

- Apenas **usuários com perfil de Professor ou Administrador** podem ser atribuídos como **Coordenador do Curso**.
- Usuários com perfil de Tutor **não podem ser coordenadores**.
- Um mesmo curso pode ter múltiplos colaboradores, com diferentes papéis, desde que respeitem os perfis permitidos.

---

## Exemplo

1. O administrador acessa o curso "Matemática Aplicada".
2. Ele adiciona:
   - João (perfil: Professor) como colaborador e o define como **Coordenador do Curso**.
   - Maria (perfil: Tutor) como colaboradora, associando-a a dois módulos.
3. A plataforma **aceita João como coordenador**, mas **não permitiria associar Maria como coordenadora**, pois seu perfil é Tutor.

---

## Observação

Essa regra garante que apenas usuários com os níveis apropriados de permissão e conhecimento gerencial sejam responsáveis pela coordenação dos cursos, mantendo a estrutura organizacional clara e funcional.

## 🧩 Local de Implementação

- No painel administrativo de cursos.
- Nas telas de gerenciamento de colaboradores, módulos e aulas.
- Nos fluxos de atribuição de papéis e permissões em cursos.

---

## 📄 Fonte da Regra

- Especificação da Plataforma EAD

---

## 🔐 Requisitos de Plano

- Disponível para todos os planos.

---

## 🔗 Tags

`colaboradores` `curso` `professor` `tutor` `coordenador` `permissão` `ead`
