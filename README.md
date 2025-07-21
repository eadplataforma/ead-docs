# 📘 Regras de Negócio do Sistema Plataforma

Este diretório contém a documentação oficial das **regras de negócio** aplicadas no sistema de gestão de cursos.  
O objetivo é garantir clareza, rastreabilidade e padronização no entendimento e evolução do sistema.

---

## 🧭 Índice de Regras

| Código | Nome | Tipo | Link |
|--------|------|------|------|
| A-C1 | Exibir identificação do aluno (marca d’água) | Controle de Acesso | [Ver Regra](./Plataforma/Curso/Aula/Controle%20de%20Acesso/A-C1%20-%20Identificação%20do%20aluno.md) |
| A-C2 | Aula Requisito | Controle de Acesso | [Ver Regra](Plataforma/Curso/Aula/Controle%20de%20Acesso/A-C2%20-%20Requisito.md) |
| A-C3 | Tempo de Permanência na Aula | Controle de Acesso | [Ver Regra](Plataforma/Curso/Aula/Controle%20de%20Acesso/A-C3%20-%20Tempo%20de%20Permanência.md) |

---

## 📝 Padrão de Documentação

Cada regra segue um modelo padronizado com as seguintes seções:

### 🆔 Identificação
- Código da regra (ex: `RB002`, `CA-CA1`)
- Nome descritivo e objetivo da regra

### ✅ Descrição
- O que a regra faz, por que existe, e em que contexto se aplica

### ⚙️ Condições de Aplicação
- Quando a regra entra em ação (ex: ao cadastrar, ao acessar, ao concluir aula)

### 🎯 Ação Esperada
- O que deve acontecer quando a regra é ativada ou violada

### 🚫 Restrições/Exceções
- Situações onde a regra não se aplica ou possui exceções

### 🧪 Exemplos
- Casos reais ou simulados para fácil entendimento

### 🧩 Local de Implementação
- Onde a lógica está (ou deve estar) no código: arquivos, serviços, componentes

### 📄 Fonte da Regra
- Origem do requisito (ex: equipe pedagógica, jurídico, documentação de produto)

### 🔐 Requisitos de Plano
- Planos que permitem acesso ao recurso, se aplicável

### 🔗 Tags
- Palavras-chave para facilitar busca e agrupamento de regras

---

## 🧑‍💻 Como contribuir

- Adicione novas regras no diretório `/rules/` usando o padrão de nomenclatura:  
  `CÓDIGO-descricao-curta.md`  
  Ex: `CA-CA4-bloqueio-download.md`

- Atualize este `README.md` com o link para a nova regra

- Mantenha o padrão de estrutura das seções

---

## 🛠️ Observações

- As regras impactam diretamente o comportamento do sistema e devem ser revisadas em mudanças de produto
- Em caso de conflito entre regras, a mais restritiva ou explícita deve prevalecer, salvo exceção documentada

---

**Última atualização:** 2025-07-21  
**Responsável:** Equipe de Produto
