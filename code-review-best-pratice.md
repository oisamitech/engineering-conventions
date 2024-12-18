
# Convenções para Revisão de Código

Este documento descreve as convenções e melhores práticas que devem ser seguidas durante o processo de revisão de código. O objetivo é garantir qualidade, consistência e colaboração eficaz dentro do time.

## Propósito das Revisões de Código
As revisões de código têm como objetivos principais:
- Garantir a **qualidade do código**.
- **Promover aprendizado** entre os membros do time.
- Melhorar a **consistência** com padrões e boas práticas.
- Aumentar a **colaboração** e a visão compartilhada do sistema.

---

## Convenções para Formatar Pull Requests

### Título Claro e Conciso
Use títulos que descrevam o propósito da mudança:
- **Bom:** "Adiciona endpoint para listar pedidos do cliente."
- **Ruim:** "Alterações nos pedidos."

### Descrição Detalhada
Explique o contexto e o que foi feito. Use o template abaixo:
```markdown
### Problema
Descreva o problema que a mudança resolve.

### Solução
- Explique a solução implementada.
- Destaque pontos importantes, como lógica ou design escolhido.

### Testes
Inclua informações sobre os testes realizados.
```

### Referências
Adicione links ou IDs relacionados:
- **Exemplo:** "Closes #123" ou "Relacionado ao ticket ABC-456".

---

## Convenções para o Código

### Tamanho e Escopo de Pull Requests
- Evite mudanças muito grandes. Divida em PRs menores e mais gerenciáveis.
- **Regra prática:** No máximo 300 linhas modificadas (dependendo do contexto).

### Nomeação de Variáveis e Funções
- Use nomes descritivos e consistentes.
- Prefira inglês para manter uniformidade.
  - **Exemplo:** `customerOrders` ao invés de `co` ou `pedidos`.

### Comentários
- Evite comentários óbvios, mas documente lógica complexa.
- **Exemplo:**
  ```javascript
  // Valida que o usuário está autenticado antes de processar a requisição.
  ```

### Boas Práticas
- Mantenha funções curtas: uma função deve fazer apenas uma coisa.
- Siga o princípio DRY (Don't Repeat Yourself).
- Adicione testes unitários e/ou de integração para novas funcionalidades.

---

## Convenções para Revisores

### Checklist para Revisão
Antes de aprovar um PR, verifique:
- [ ] A lógica do código está clara?
- [ ] Segue os padrões do time (nomenclatura, formatação)?
- [ ] Testes foram escritos e passaram?
- [ ] Há impacto negativo em performance ou segurança?

### Feedback Construtivo
- Use uma linguagem objetiva e respeitosa:
  - **Construtivo:** "Essa função poderia ser dividida para melhorar a legibilidade."
  - **Evite:** "Isso está errado."
- Reconheça pontos positivos:
  - **Exemplo:** "Ótima escolha para resolver esse problema!"

### Responsabilidade Compartilhada
- Todos os membros devem participar e aprender com as revisões.
- Questione com curiosidade: "Poderia explicar por que escolheu essa abordagem?"

---

## Ferramentas e Automação

### Linters e Formatação Automática
Configure ferramentas como **ESLint**, **Prettier** ou **Black** para garantir consistência no estilo do código.

### Estrutura de Commits
Siga o padrão:
```
[Tipo]: [Descrição breve]
Exemplo: fix: Corrige bug na listagem de pedidos
```

### Integrações de CI/CD
- O PR só deve ser aprovado se os testes automatizados e ferramentas de validação passarem.

---

## Boas Práticas para Colaboração

### Rotatividade de Revisores
- Rotacione as revisões para evitar silos de conhecimento.
- Garanta que todos revisem diferentes partes do sistema.

### Revisões Assíncronas e Pontuais
- Estabeleça prazos realistas para revisão (ex.: responder PRs em até dois dias úteis).
- Priorize PRs que bloqueiam outros desenvolvimentos.

### Documentação Contínua
- Atualize este documento regularmente para refletir práticas e padrões adotados pelo time.

---

**Dúvidas ou sugestões?** Abra um Pull Request para discutir melhorias neste documento.
