# Regra: C9 - Restauração de Curso

## Descrição

Define o comportamento do sistema ao **restaurar um curso** que foi previamente excluído (enviado à Lixeira), incluindo a recuperação de seus vínculos, conteúdos e status.

---

## Comportamento ao Restaurar o Curso

Ao restaurar um curso da Lixeira:

- O curso é restaurado com status **Rascunho**, mesmo que antes estivesse **Publicado**.
- O curso é **reassociado automaticamente** aos **grupos** aos quais estava vinculado.
- As **matrículas dos alunos** são **restauradas**.
- Os **produtos vinculados** ao curso também são **reativados** e reassociados.
- Todos os **módulos e aulas** que foram excluídos junto com o curso são **restaurados automaticamente**.
- Os **módulos e aulas mantêm o status original** (por exemplo: Publicado ou Rascunho).

---

## Exemplo

1. O curso "Marketing Digital" foi excluído com:
   - Status **Publicado**
   - Grupo: "Comunicação"
   - Produto vinculado: "Combo MKT"
   - 5 módulos (alguns em Rascunho, outros Publicados)
   - 20 aulas distribuídas entre os módulos
   - Matrículas ativas

2. Ao restaurar o curso:
   - Ele retorna com status **Rascunho**
   - Volta ao grupo "Comunicação"
   - As **matrículas são restauradas**
   - O produto "Combo MKT" é **reativado**
   - Todos os módulos e aulas são restaurados
   - Cada módulo e aula retorna com o **mesmo status** que possuíam antes da exclusão

---

## Observações

- A única alteração automática feita pelo sistema é no status do **curso**, que sempre retorna como **Rascunho**, independentemente do status original.
- Todos os demais itens — **grupos, matrículas, produtos, módulos e aulas** — são restaurados **com os mesmos vínculos e status anteriores**.
- É recomendável revisar o curso restaurado antes de publicá-lo novamente.

## 🧩 Local de Implementação

- No painel administrativo de cursos (Lixeira e restauração).
- Nos fluxos de restauração de cursos, módulos e aulas.
- Nos processos de reativação de vínculos e produtos associados.

---

## 📄 Fonte da Regra

- Especificação da Plataforma EAD

---

## 🔐 Requisitos de Plano

- Disponível para todos os planos.

---

## 🔗 Tags

`restauração` `curso` `módulo` `aula` `matrícula` `produto` `grupo` `ead`
