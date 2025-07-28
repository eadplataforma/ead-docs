# Recurso: Banco de Questões

## Descrição

O **Banco de Questões** é o espaço destinado para que o administrador possa **criar manualmente** ou **importar** questões que serão utilizadas em **provas** e **quizzes**.

Também é possível **exportar uma planilha** contendo as questões cadastradas, facilitando a organização e edição externa.

---

## Tipos de Questões Suportados

O sistema permite três tipos de questões:

- **Dissertativas**
- **Múltipla Escolha**
- **Alternativas Simples** (resposta única)

---

## Campos Adicionais

### Observação

- Campo opcional onde o administrador pode inserir **informações complementares para os alunos**, como dicas ou instruções específicas.

### Solução

- Campo destinado à **explicação ou resolução da questão**.
- A solução **é exibida ao aluno apenas ao final da prova**, desde que a opção **"Exibir o gabarito"** esteja habilitada nas configurações da prova.

#### Comportamento do campo "Solução":

- Se a prova **permite mais de uma tentativa**: a solução será exibida **apenas na última tentativa do aluno**.
- Se a prova **possui apenas uma tentativa**: a solução será exibida **logo após essa tentativa**, **independente** de aprovação ou reprovação.

---

## Limite de Alternativas

- Para questões do tipo **Múltipla Escolha** e **Alternativas Simples**, o número máximo de alternativas por questão é **8**.

---

## Ordenação de Questões

- A ordenação das questões no banco é sequencial.
- Quando uma questão é **excluída** e posteriormente **restaurada**, ela retorna para a **última posição** da lista.

---

## Exemplo de Uso

1. O administrador importa um conjunto de 20 questões em uma planilha.
2. Ele edita algumas delas, adicionando observações e soluções explicativas.
3. Habilita a opção "Exibir o gabarito" na configuração da prova.
4. Ao final da tentativa (única ou última), os alunos visualizam as soluções das questões resolvidas.

---

## Observações

- O Banco de Questões permite o reaproveitamento de conteúdos em múltiplas avaliações.
- A utilização dos campos de observação e solução **enriquece a experiência pedagógica** do aluno.
- A limitação de 8 alternativas por questão ajuda a manter a clareza e objetividade das avaliações.

## 🧩 Local de Implementação

- No painel administrativo de Banco de Questões.
- Nos fluxos de criação, importação, exportação, edição, exclusão e restauração de questões.
- Nas telas de configuração e exibição de provas/quizzes.

---

## 📄 Fonte da Regra

- Especificação da Plataforma EAD

---

## 🔐 Requisitos de Plano

- Disponível a partir do plano starter.

---

## 🔗 Tags

`banco-de-questões` `prova` `quiz` `questão` `importação` `exportação` `ordenação` `ead`

