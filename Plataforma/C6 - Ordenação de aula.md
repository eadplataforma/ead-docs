# Regra: C6 - Ordenação de Aula

## Descrição

Define como as aulas são ordenadas dentro de um **módulo**, respeitando uma ordem numérica, independentemente do status.

---

## Funcionamento da Ordenação

- As aulas são organizadas dentro do módulo com base em uma ordem (1, 2, 3...).
- Ao excluir uma aula, as demais são reordenadas para preencher a lacuna.
- Ao restaurar a aula, ela retorna à posição original dentro do módulo.

---

## Exemplo

**Módulo "Teste"**  
1. Aula A (ordem 1)  
2. Aula B (ordem 2)  
3. Aula C (ordem 3)

Se a **Aula A** for excluída:

- Aula B → ordem 1  
- Aula C → ordem 2

Ao **restaurar a Aula A**:

- Aula A → volta à ordem 1  
- Aula B → volta à ordem 2  
- Aula C → volta à ordem 3

---

## Casos Específicos

1. **Movimentação de Aula entre Módulos do Mesmo Curso**  
   - Ao mover uma aula para outro módulo do **mesmo curso**, ela será posicionada automaticamente como **última aula** do módulo de destino.

2. **Cópia de Aula entre Cursos**  
   - Ao copiar uma aula de um curso para outro, ela será inserida no módulo de destino na **última posição**.

> ✅ **Observação importante:**  
> Aulas podem ter **a mesma ordem** (ex: ordem 1) quando estão em **módulos diferentes**, pois a ordenação é sempre relativa ao **módulo em que estão inseridas**.

## 🧩 Local de Implementação

- Na listagem de aulas dentro de cada módulo (aluno e administrador).
- Nos fluxos de exclusão, restauração, cópia e movimentação de aulas.
- No painel administrativo de organização de aulas.

---

## 📄 Fonte da Regra

- Especificação da Plataforma EAD

---

## 🔐 Requisitos de Plano

- Disponível para todos os planos.

---

## 🔗 Tags

`ordenação` `aula` `módulo` `organização` `administração` `ead`
