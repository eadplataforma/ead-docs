# Regra de Negócio: C4 - Ordenação de Cursos, Módulos e Aulas

## Descrição

Esta regra define como funciona a ordenação automática de cursos, módulos e aulas na plataforma, tanto em ações de exclusão quanto de restauração, cópia ou movimentação de itens.

---

## 📘 Ordenação de Cursos

- A ordenação de cursos é independente do status (Publicado ou Rascunho).
- Exemplo de ordenação inicial:
  - Curso A: ordem 1
  - Curso B: ordem 2
  - Curso C: ordem 3
- Se o **Curso A for deletado**:
  - Curso B assume a ordem 1
  - Curso C assume a ordem 2
- Se o **Curso A for restaurado**:
  - Curso A retoma a **ordem 1**
  - Curso B e Curso C retornam às suas **ordens originais** (2 e 3)

---

## 📗 Ordenação de Módulos

- A lógica de ordenação dos módulos segue o mesmo princípio dos cursos.
- Exemplo de ordenação inicial:
  - Módulo A: ordem 1
  - Módulo B: ordem 2
  - Módulo C: ordem 3
- Se o **Módulo A for deletado**:
  - Módulo B assume a ordem 1
  - Módulo C assume a ordem 2
- Se o **Módulo A for restaurado**:
  - Módulo A volta à **ordem 1**
  - Módulo B e Módulo C retornam às **posições anteriores**


## 📙 Ordenação de Aulas

- A ordenação de aulas funciona de forma similar, com a diferença de que está **associada ao módulo** em que a aula está inserida.
- Exemplo dentro do Módulo "Teste":
  - Aula A: ordem 1
  - Aula B: ordem 2
  - Aula C: ordem 3
- No Módulo "Teste 2", a ordenação pode ser a mesma ou diferente, pois a ordenação é **local para cada módulo**.

### Casos Específicos:

1. **Movimentação de Aula entre Módulos do Mesmo Curso**  
   - Ao mover uma aula para outro módulo do **mesmo curso**, ela será posicionada automaticamente como **última aula** do módulo de destino.

2. **Cópia de Aula entre Cursos**  
   - Ao copiar uma aula de um curso para outro, ela será inserida no módulo de destino na **última posição**.

3. **Cópia ou Movimentação de Módulos**  
   - O mesmo comportamento se aplica à movimentação ou cópia de módulos: eles serão posicionados no **final da lista** do novo curso.

---

## Observações

- A ordenação é sempre recalculada automaticamente pelo sistema ao excluir ou restaurar itens.
- Esse comportamento garante uma visualização consistente e organizada dos conteúdos, mesmo após operações de manutenção feitas pelo administrador.


# Regra: C4 - Ordenação de Cursos

## Descrição

Define como os cursos são ordenados na plataforma, independentemente do status (Publicado ou Rascunho).

---

## Funcionamento da Ordenação

- Os cursos são ordenados com base em um campo numérico de ordem crescente (1, 2, 3...).
- Ao excluir um curso, os cursos abaixo na lista sobem uma posição para preencher a lacuna.
- Ao restaurar um curso excluído, ele **retorna à posição original** na ordem e os outros cursos são reorganizados.

---

## Exemplo

1. Curso A (ordem 1)  
2. Curso B (ordem 2)  
3. Curso C (ordem 3)

Se o **Curso A** for excluído:

- Curso B → ordem 1  
- Curso C → ordem 2

Ao **restaurar o Curso A**:

- Curso A → volta à ordem 1  
- Curso B → volta à ordem 2  
- Curso C → volta à ordem 3

---

## 🧩 Local de Implementação

- Na listagem de cursos, módulos e aulas para o aluno e administrador.
- Nos fluxos de exclusão, restauração, cópia e movimentação de cursos, módulos e aulas.
- No painel administrativo de organização de conteúdos.

---

## 📄 Fonte da Regra

- Especificação da Plataforma EAD

---

## 🔐 Requisitos de Plano

- Disponível para todos os planos.

---

## 🔗 Tags

`ordenação` `curso` `módulo` `aula` `organização` `administração` `ead`
