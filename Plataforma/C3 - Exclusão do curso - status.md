# Regra de Negócio: C3 - Exclusão de Curso e Comportamento de Status na Restauração

## Descrição

Esta regra define o comportamento do sistema ao excluir e restaurar cursos, módulos e aulas, com foco na preservação ou alteração do status de publicação.

## Regra

- Ao **excluir um curso com status "Publicado"**, ele será removido da área ativa da plataforma.
- Se o curso for **restaurado**, seu status será alterado automaticamente para **"Rascunho"**, independentemente do status anterior.
- Já os **módulos e aulas** pertencentes ao curso:
  - Serão restaurados com o **mesmo status que possuíam antes da exclusão**.
  - Ou seja, **não terão o status alterado** após a restauração.

## Exemplo

1. Curso "Matemática Básica" está com status **Publicado**.
2. O curso é excluído.
3. Posteriormente, o curso é restaurado:
   - O curso volta com status **Rascunho**.
   - Os módulos e aulas que estavam **Publicados** ou **Em Rascunho** antes da exclusão **mantêm seu status original**.

## Observação

Essa regra visa garantir que cursos restaurados passem por uma nova validação antes de voltarem a ser publicados, ao mesmo tempo em que preserva a configuração original de seus conteúdos internos (módulos e aulas).
