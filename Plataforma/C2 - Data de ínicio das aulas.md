# Regra de Negócio: C2 - Exibição de Curso com Data Futura de Início

## Descrição

Esta regra define o comportamento da exibição de cursos na área "Meus Cursos", com base na data de início das aulas.

## Regra

Quando a data de início das aulas de um curso for futura (ou seja, ainda não tiver chegado):

- O curso **não será exibido** na área "Meus Cursos" do aluno.
- O curso **só será exibido** a partir da data definida como início das aulas.
- Mesmo que o curso não apareça na área "Meus Cursos", a matrícula do aluno **já estará registrada** e visível nos relatórios administrativos.

## Exemplo

Se um aluno for matriculado no dia 10 de agosto, em um curso com data de início marcada para o dia 20 de agosto:

- Entre os dias 10 e 19 de agosto: o curso **não aparecerá** na área "Meus Cursos".
- A partir do dia 20 de agosto: o curso **passará a aparecer** automaticamente na área "Meus Cursos".

## Observação

Esta lógica, evita que alunos acessem conteúdos, antes da data oficial de início definida para o curso.
