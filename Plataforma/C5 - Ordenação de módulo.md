# Regra: C5 - Ordenação de Módulo

## Descrição

Define como os módulos são ordenados dentro de um curso, independentemente do status (Publicado ou Rascunho).

---

## Funcionamento da Ordenação

- Os módulos dentro de um curso seguem uma ordem numérica (1, 2, 3...).
- Ao excluir um módulo, os módulos seguintes sobem de posição para preencher a lacuna.
- Ao restaurar um módulo, ele **retorna à posição original** na ordem.

---

## Exemplo

1. Módulo A (ordem 1)  
2. Módulo B (ordem 2)  
3. Módulo C (ordem 3)

Se o **Módulo A** for excluído:

- Módulo B → ordem 1  
- Módulo C → ordem 2

Ao **restaurar o Módulo A**:

- Módulo A → volta à ordem 1  
- Módulo B → volta à ordem 2  
- Módulo C → volta à ordem 3

---

## Casos Específicos

- **Cópia ou Movimentação de Módulos entre Cursos**  
  - Quando um módulo é **movido** ou **copiado** para outro curso, ele será automaticamente posicionado na **última posição** da lista de módulos do curso de destino.

## 🧩 Local de Implementação

- Na listagem de módulos dentro de cada curso (aluno e administrador).
- Nos fluxos de exclusão, restauração, cópia e movimentação de módulos.
- No painel administrativo de organização de módulos.

---

## 📄 Fonte da Regra

- Especificação da Plataforma EAD

---

## 🔐 Requisitos de Plano

- Disponível para todos os planos.

---

## 🔗 Tags

`ordenação` `módulo` `curso` `organização` `administração` `ead`

