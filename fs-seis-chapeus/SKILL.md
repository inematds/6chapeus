---
name: fs-seis-chapeus
description: Análise estruturada pelos Seis Chapéus de De Bono com sistema anti-âncora integrado e isolamento estrito entre fases. Use SEMPRE que o usuário quiser analisar uma funcionalidade complexa, avaliar uma decisão difícil, desbloquear um conflito de equipe, validar uma proposta técnica ou comercial, fazer um pre-mortem, sair de um bloqueio de pensamento, ou pedir "seis chapeus", "seis chapéus", "six hats", "análise multi-perspectiva", "me ajuda a pensar", "quebra a âncora", "prós e contras de verdade". Ative também diante de "devo fazer X?" ou tensão emocional+técnica+estratégica misturadas.
---

# fs-seis-chapeus — Seis Chapéus + Anti-Âncora

Implementação operacional do método de Edward de Bono com duas camadas:

1. **Sistema anti-âncora** — ruptura obrigatória do viés antes de pensar.
2. **Seis chapéus sequenciais com isolamento estrito** — um modo por vez, sem contaminação cruzada.

---

## Quando NÃO usar esta skill

- Perguntas factuais simples.
- Tarefas de execução pura (escrever código, redigir um e-mail).
- Decisões triviais ou reversíveis de baixo custo.
- Quando o usuário pede opinião rápida sem querer processo.

Se o problema cabe em 3 linhas, não acione esta skill.

---

## Fase 0 — Sistema Anti-Âncora (obrigatória)

Executada ANTES dos chapéus, sempre. Não pule mesmo com pressa.

### 0.1 Detecção de âncora

Avaliar se o usuário vem com solução pré-escolhida. Sinais:
- Verbaliza solução ("vou fazer X", "acho que o melhor é Y")
- Já iterou 3+ turnos sobre a mesma abordagem
- Vocabulário de compromisso ("já decidi", "só preciso de confirmação")
- Pattern-matching do próprio modelo (a primeira ideia que veio à cabeça)

Se detectar âncora, declarar: "Detecto que você vem ancorado em [X]. Vou quebrar essa âncora antes de analisar."

Se não detectar âncora, declarar também: "Não detecto âncora clara. Executo a ruptura mesmo assim como medida preventiva."

### 0.2 Ruptura da âncora — 4 movimentos em ordem

**Movimento 1 — Reformulação pura:**
Reescrever o problema SEM assumir a abordagem atual. Só objetivo + restrições. Proibido incluir a solução implícita. Teste: alguém que lesse a reformulação poderia chegar a uma solução completamente distinta? Se não, reescrever.

**Movimento 2 — Suposição fundacional:**
Identificar a crença invisível que sustenta a abordagem do usuário. Formular teste de falsificação: "Esta suposição seria falsa se...".

**Movimento 3 — Steel-man do oposto:**
Construir o melhor argumento possível a favor de NÃO fazer o proposto, ou de fazer o contrário. Versão forte, não caricatura. Teste: alguém inteligente que defendesse essa posição se sentiria representado?

**Movimento 4 — Pre-mortem rápido:**
Imaginar que a abordagem fracassou em 6-12 meses. Identificar os 3 modos de falha mais prováveis.

### 0.3 Classificação do problema

Determinar variante de chapéus conforme o tipo. Ver `references/variants.md`:
- Funcionalidade de produto → Variante 2
- Conflito entre pessoas → Variante 3
- Pre-mortem → Variante 4
- Desbloqueio criativo → Variante 5
- Decisão irreversível de alto custo → Variante 6
- Geral → Variante 1

---

## Regras de isolamento (não negociáveis)

1. **Um chapéu por vez.** Nunca misturar dois modos na mesma seção.
2. **Isolamento estrito.** Enquanto se usa um chapéu, os demais NÃO existem. Se aparecer conteúdo de outro chapéu, descartar ou guardar para sua fase. Cada chapéu deve ser monolítico.
3. **O Azul abre e fecha sempre.** Sem Azul de abertura não se começa.
4. **Sem justificativa no Vermelho.** Se aparecer "porque..." no Vermelho, a frase é inválida.
5. **O Preto é lógica negativa, não pessimismo.** Apenas riscos verificáveis. Não "não gosto" (isso é Vermelho).
6. **O Amarelo exige respaldo lógico.** Cada benefício deve poder ser defendido com um argumento.
7. **O Verde usa marcos divergentes.** Ver `references/divergence-frameworks.md`. Mínimo de 3 marcos distintos, mínimo 1 provocação radical.
8. **Não trocar de chapéu no meio da fase.** Se uma fase ficar curta, fecha e passa.
9. **Se não houver material para uma fase, declarar.** "Não encontro riscos sólidos" é informação valiosa. Não preencher com conteúdo falso.

---

## Chapéu Azul (abertura)

Definir:
- **Pergunta exata** reformulada pelo Claude (não copiada do usuário).
- **Restrições** conhecidas.
- **Critério de sucesso**: como saberemos que a conclusão é boa?
- **Ordem dos chapéus** escolhida e por quê.

Fase curta (4-8 linhas). Se faltar contexto, parar e perguntar.

---

## Chapéu Branco

Apenas fatos, em duas categorias:
- **Fatos verificados** (dados, métricas, restrições objetivas do contexto do usuário).
- **Fatos acreditados mas não verificados** (suposições não comprovadas).

Listar **lacunas de informação** se faltarem dados críticos. Não preencher com suposições. Tudo o que não estiver no contexto explícito do usuário vai em "acreditados" ou em "lacunas".

---

## Chapéu Amarelo

Benefícios com respaldo lógico:

> **Benefício:** [descrição] — **Por que é plausível:** [raciocínio]

Mínimo 3, máximo 7. Se não houver 3 defensáveis, declarar. PROIBIDO mencionar riscos, ponderar com "embora..." ou adicionar advertências. Isso pertence ao Preto.

---

## Chapéu Preto

Riscos concretos com avaliação:

> **Risco:** [descrição] — **Probabilidade/impacto:** [baixo/médio/alto] — **Por quê:** [raciocínio]

Mínimo 3, máximo 7. Seja severo. Este é o chapéu mais valioso e o que mais se dilui por instinto de complacência. PROIBIDO suavizar com condicional ("poderia talvez..."). Enunciar com segurança: "Isto vai falhar quando...". PROIBIDO mencionar benefícios ou oportunidades.

---

## Chapéu Verde

Alternativas criativas usando marcos divergentes de `references/divergence-frameworks.md`.

Regras:
- Mínimo de **5 alternativas executivamente distintas** (mudam o quê ou o como fundamental, não apenas o stack ou a cor do botão).
- Usar no mínimo **3 marcos diferentes** do catálogo de 10.
- Pelo menos **1 provocação radical** (inversão total, eliminação do problema, constraint shock extremo).
- **Não pré-julgar.** A crítica não é trabalho do Verde. PROIBIDO dizer "esta não é viável" ou "esta é a melhor".
- Teste de distinção: o custo e o resultado de duas alternativas são distintos? Se não, são a mesma. Eliminar duplicatas.

Formato por alternativa:
> **Alt N — [Nome curto]** *(Marco: [letra+nome])* — [2-3 linhas de descrição] — Insight-chave: [1 linha].

---

## Chapéu Vermelho

Reações emocionais e intuitivas sem justificativa. Frases curtas, diretas, viscerais.

Exemplos válidos:
- "Isto cheira a armadilha."
- "Algo na opção 3 me entusiasma sem eu saber por quê."
- "Cansaço antecipado só de ler o escopo."
- "Não confio."

**Proibido escrever "porque..." nesta fase.** Se aparecer, a frase é inválida. Máximo 8 frases.

---

## Chapéu Azul (síntese) — Convergência com matriz

Estrutura fixa:

### 1. Mapa do terreno
3-5 linhas resumindo o que sabemos após os 6 chapéus.

### 2. Tensões detectadas
Onde o Preto e o Amarelo colidem. Onde o Vermelho não encaixa com a lógica.

### 3. Matriz de decisão
Definir 3-5 critérios **específicos do problema** (não genéricos como "viabilidade"). Pontuar as alternativas do Verde:

| Alternativa | Critério 1 | Critério 2 | Critério 3 | Trade-off principal |
|---|---|---|---|---|
| Alt 1 | Alto | Médio | Baixo | [trade-off] |

Teste de critérios: você consegue atribuir Alto/Médio/Baixo com justificativa verificável? Se não, operacionalize melhor o critério.

### 4. Recomendação acionável
UMA opção priorizada + próximos passos concretos. Não três opções. Uma. Se não puder escolher, declare qual dado está faltando.

### 5. Plano B
Segunda opção + condição de ativação ("ativar Plano B se...").

### 6. Métricas de revisão
Evidência concreta que faria revisar a escolha em 1-3 meses.

### 7. Lacunas pendentes
Informação do Branco que ainda falta e deveria ser obtida antes de executar.

---

## Formato de saída

```
## 🛡️ Fase 0 — Anti-Âncora
[detecção + 4 movimentos de ruptura]

## 🔵 Chapéu Azul (abertura)
[definição do problema]

## ⚪ Chapéu Branco
[fatos]

## 🟡 Chapéu Amarelo
[benefícios]

## ⚫ Chapéu Preto
[riscos]

## 🟢 Chapéu Verde
[alternativas com marcos]

## 🔴 Chapéu Vermelho
[emoções]

## 🔵 Chapéu Azul (síntese)
[mapa + tensões + matriz + recomendação + plano B + métricas]
```

A ordem de apresentação varia conforme a variante escolhida (ver `references/variants.md`).

---

## Checklist antes de entregar

- [ ] Fase 0 (anti-âncora) executada com os 4 movimentos?
- [ ] Âncora detectada e declarada (ou ausência declarada)?
- [ ] As 7+ seções presentes e na ordem correta da variante?
- [ ] O Preto tem pelo menos 3 riscos reais e não diluídos?
- [ ] O Verde tem pelo menos 5 alternativas com 3+ marcos distintos?
- [ ] O Verde inclui pelo menos 1 provocação radical?
- [ ] O Vermelho está livre de "porque..."?
- [ ] A síntese inclui matriz com critérios operacionalizáveis?
- [ ] A síntese dá UMA recomendação + Plano B?
- [ ] Há contaminação cruzada entre chapéus? Se houver, reescrever a seção.

Se algum ponto falhar, reescrever antes de entregar.

---

## Referências

- `references/variants.md` — Ordens alternativas conforme o tipo de problema.
- `references/divergence-frameworks.md` — Catálogo de 10 marcos para o Chapéu Verde.
- `references/anti-patterns.md` — Erros comuns (âncora + chapéus).
- `references/examples.md` — Exemplos completos de aplicação.
