# Exemplos de aplicação

## Exemplo 1 — Feature de produto (com anti-âncora + agentes paralelos)

**Input do usuário:** "Estou decidindo se adiciono comentários em thread no meu SaaS para nutricionistas. Meus usuários pedem, acho que é o melhor."

### 🛡️ Fase 0 — Anti-Âncora

**Detecção:** o usuário diz "acho que é o melhor". Vem ancorado em "sim, tem que fazer". Sinal claro.

**Reformulação pura:** "Tenho um SaaS de gestão para nutricionistas com 23 usuários ativos. 4 pediram funcionalidade colaborativa. Preciso decidir como (ou se) melhorar a comunicação dentro da plataforma."

**Suposição fundacional:** "Os usuários que pedem features são representativos da base total." Teste de falsificação: seria falso se os 4 forem power users e os 19 restantes não usarem nem metade das features atuais.

**Steel-man do oposto:** "Não adicionar nada e dedicar essas 6 semanas a conseguir 20 usuários a mais. Com 23 usuários, qualquer feature nova é otimização prematura. O problema real não é retenção, é aquisição."

---

### Chapéus (executados em paralelo, cada um sem ver os outros)

### ⚪ Branco
**Verificados:** 4 pedidos sobre 23 usuários ativos (17%), não há concorrente com essa função, equipe de 1 dev.
**Não verificados:** "aumentaria a retenção" (sem dados), "todos querem" (só 4 de 23).
**Lacunas:** tempo real de desenvolvimento, disposição a pagar mais, churn atual.

### 🟡 Amarelo
1. Retenção por engajamento social — plausível: features colaborativas aumentam uso diário em SaaS B2B.
2. Diferenciação competitiva — plausível: ninguém no nicho tem.
3. Dados orgânicos — plausível: threads geram conteúdo aproveitável para recomendações.

### ⚫ Preto
1. Moderação legal — Alto/Alto — dados de saúde são LGPD categoria especial, obrigação de moderar conteúdo.
2. Scope creep — Alto/Alto — comentários arrastam notificações, menções, edição, remoção, denúncias: 6-8 semanas no mínimo.
3. Sinal fraco — Médio/Médio — 4/23 é 17%, amostra pequena demais para decidir.
4. Custo de oportunidade — Alto/Alto — 6 semanas sem captar novos usuários com apenas 23 ativos.

### 🟢 Verde
**Alt 1 — Canal externo** *(Marco: J-Eliminação)* — Slack/Discord gerenciado por você, custo zero, 1 hora. Insight: elimina o problema técnico por completo.
**Alt 2 — Mensagens 1:1 nutri↔paciente** *(Marco: E-SCAMPER/Eliminar)* — Sem thread pública, sem moderação legal, 1 semana. Insight: cobre a necessidade real sem o risco regulatório.
**Alt 3 — Pesquisa antes** *(Marco: D-Primeiros princípios)* — Antes de construir, validar com os 23 se pagariam mais. Insight: a verdade irredutível é que você não sabe se isto gera receita.
**Alt 4 — Provocação: o SaaS sem tela** *(Marco: G-Random concept: "telefone")* — E se a comunicação fosse por áudio/voz integrado em vez de texto? Insight: nutricionistas preferem falar, não escrever.
**Alt 5 — Double down em aquisição** *(Marco: A-Inversão)* — O que garantiria fracassar? Continuar adicionando features para 23 usuários. Insight: investir as 6 semanas em marketing/vendas.

### 🔴 Vermelho
- Isto cheira a agradar os mais barulhentos.
- Entusiasmo pela Alt 2 (mensagens 1:1).
- "Todo mundo pede" soa a desculpa para não fazer o desconfortável: vender.
- Cansaço antecipado de ler "moderação LGPD".

### 🔵 Azul (síntese)

**Mapa:** 4 usuários de 23 pedem feature complexa, sem dados de retenção, risco legal alto, escopo grande para 1 dev só, custo de oportunidade crítico.

**Tensões:** Amarelo vende diferenciação, mas Preto desmonta com custo real. Vermelho confirma entusiasmo pela alternativa menor.

**Matriz:**

| Alternativa | Tempo dev | Risco legal | Receita potencial | Trade-off |
|---|---|---|---|---|
| Alt 1 (Slack) | Baixo | Baixo | Baixo | Sem controle, fragmenta a experiência |
| Alt 2 (1:1) | Médio | Médio | Médio | Cobre necessidade sem risco, mas não diferencia |
| Alt 3 (Pesquisa) | Muito baixo | Nenhum | Alto | Atrasa decisão, mas a baseia em dados |
| Alt 5 (Aquisição) | N/A | Nenhum | Alto | Ignora pedido de usuários atuais |

**Recomendação:** Alt 3 (pesquisa) esta semana + Alt 2 (mensagens 1:1) se a pesquisa confirmar demanda. Custo total: 1 semana.
**Plano B:** se a pesquisa mostrar <30% de interesse, pivotar para Alt 5 (aquisição pura).
**Métrica de revisão:** em 3 meses, se a base passar de 100 usuários e >30% pedir discussão em grupo, reconsiderar threads.

---

## Exemplo 2 — Conflito de equipe (resumo)

**Input:** "Meu colaborador não entregou no prazo e está jogando a culpa em mim na frente do cliente."
**Variante:** 3 (conflito → Vermelho primeiro)

Fase 0 detecta âncora em "quero cortar a relação". Reformula: "Preciso decidir como gerenciar um descumprimento de um colaborador que escalou publicamente."

Os 6 agentes operam em paralelo. O Vermelho (executado primeiro na apresentação mas em paralelo na execução) captura raiva, traição e vergonha sem justificativas. O Branco reúne datas e mensagens. O Verde gera opções desde conversa privada até saída limpa com cliente intacto.

Síntese: conversa privada em 24h com 3 pontos preparados por escrito. Se não houver reconhecimento, saída ordenada em 48h.
