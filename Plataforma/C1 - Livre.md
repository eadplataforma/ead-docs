# Regra de Negócio: C1 - Curso Livre

## Descrição

A regra **C1 - Curso Livre** define o comportamento do sistema quando um curso é configurado como **curso livre**. Essa configuração tem impacto direto na disponibilidade do curso e no processo de matrícula dos alunos.

---

## Objetivo

Permitir que cursos classificados como **livres** estejam disponíveis para todos os alunos, sem necessidade de solicitação ou aprovação prévia, promovendo acesso automático e facilitado.

---

## Comportamento do Sistema

Quando a opção **Curso Livre** estiver **ativada** para um curso:

- O curso ficará **visível e disponível** para **todos os alunos** cadastrados na plataforma.
- Ao **acessar** o curso pela primeira vez, o aluno será **automaticamente matriculado**, sem a necessidade de intervenção manual por parte de administradores ou gestores.

---

## Fluxo de Execução

1. **Admin** ativa a opção **Curso Livre** nas configurações do curso.
2. O curso é exibido na área de meus cursos, acessíveis a todos os alunos.
3. Um aluno acessa o curso.
4. O sistema verifica se o aluno já está matriculado.
   - Se **não estiver matriculado**, realiza a **matrícula automaticamente**.
   - Se **já estiver matriculado**, o acesso é concedido normalmente.

---

## Regras e Restrições

- A matrícula automática ocorre **somente no primeiro acesso** ao curso.
- A regra só se aplica quando o status **Curso Livre** estiver ativado.
- Se o curso for configurado posteriormente como **não livre**, novos acessos exigirão processo de matrícula normal (caso aplicável).

---

## Casos de Uso

- Cursos de introdução ou ambientação.
- Trilhas de conhecimento abertas a toda a base de alunos.
- Conteúdos educacionais com objetivo de autoaprendizagem, sem pré-requisitos.

---

## Exemplos

| Situação                             | Resultado Esperado                     |
|-------------------------------------|----------------------------------------|
| Curso com "Curso Livre" ativado     | Aluno visualiza e se matricula ao acessar |
| Curso com "Curso Livre" desativado  | Aluno não visualiza automaticamente e precisa ser matrículado |

---

## Considerações Técnicas

- A matrícula automática deve ser registrada com data/hora do primeiro acesso.
- O evento de matrícula deve seguir o mesmo padrão dos demais tipos de matrícula (para fins de relatório e integração).
