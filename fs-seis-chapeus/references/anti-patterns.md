# Anti-padrões

Erros que simulam análise sem produzi-la. Se detectar algum, pare e corrija.

---

## Vieses de âncora (Fase 0)

### Bypass da Fase 0
**Sintoma:** pular direto para os chapéus sem quebrar a âncora.
**Correção:** a divergência a partir da âncora gera variantes da âncora, não alternativas reais. Sempre executar os 4 movimentos.

### Reformulação cosmética
**Sintoma:** reescrever o problema trocando palavras mas mantendo a solução implícita. "Como implemento X?" vira "Qual a melhor forma de implementar X?".
**Correção:** a reformulação pura elimina TODA referência à abordagem. Só fica: objetivo + restrições.

### Steel-man fraco
**Sintoma:** o argumento a favor do oposto é uma caricatura fácil de derrubar.
**Teste:** alguém inteligente que defendesse essa posição se sentiria representado pelo seu steel-man? Se não, é um straw-man disfarçado.

### Âncora do modelo
**Sintoma:** não é o usuário que vem ancorado, é o Claude que convergiu prematuramente na sua primeira interpretação.
**Teste:** a primeira ideia que lhe veio à cabeça continua sendo a que você recomenda depois de 5 alternativas? Se sim, pode estar correta ou pode ser âncora própria.

---

## Vieses de chapéus

### Contaminação cruzada
**Sintoma:** "...mas por outro lado poderia ser bom porque..." dentro do Preto. Ou "...embora tenha o risco de..." dentro do Amarelo.
**Correção:** eliminar a frase contaminada. Cada chapéu é monolítico.

### Preto diluído por gentileza
**Sintoma:** riscos em condicional suave ("poderia ser que talvez...") ou genéricos ("há risco de o mercado mudar").
**Correção:** riscos concretos, plausíveis, enunciados com segurança. "Isto vai quebrar X quando ocorrer Y" é válido. "Poderia haver complicações" não é.

### Vermelho justificado
**Sintoma:** "sinto desconfiança **porque** os prazos são muito apertados".
**Correção:** corta em "sinto desconfiança". Ponto. A razão pertence ao Preto ou ao Branco.

### Verde repetitivo
**Sintoma:** as "alternativas" são variações mínimas do plano original.
**Teste:** o custo e o resultado de cada alternativa são distintos? Se não, são a mesma.

### Falsa divergência
**Sintoma:** 5 alternativas que são a mesma ideia com palavras diferentes. O formato está, o conteúdo não.
**Correção:** mudar de marco divergente e forçar mais 2 a partir de um ângulo completamente distinto.

### Marco troféu
**Sintoma:** usar TRIZ ou Random concept "porque fica sofisticado" quando o problema pedia Inversão simples.
**Teste:** você escolheu o marco pelo problema ou pelo marco?

### Convergência disfarçada
**Sintoma:** apresentar alternativas numa ordem que empurra para sua favorita.
**Correção:** misturar a ordem de apresentação. A matriz de convergência decide, não a sequência.

### Pseudo-critérios
**Sintoma:** critérios vagos como "encaixa com a marca" ou "é mais elegante" que não dá para pontuar honestamente.
**Teste:** você consegue atribuir Alto/Médio/Baixo com justificativa verificável?

### Azul de fechamento indeciso
**Sintoma:** a síntese oferece "três caminhos possíveis" e deixa a decisão para o usuário.
**Correção:** UMA recomendação. Se não puder escolher, diga qual dado está faltando.

### Branco com suposições
**Sintoma:** em fatos verificados aparecem frases como "o mercado de X está crescendo" sem fonte.
**Correção:** tudo o que não for verificável vai em "fatos acreditados" ou "lacunas de informação".

### Análise inflada
**Sintoma:** 30 parágrafos que ninguém vai ler.
**Correção:** cada chapéu em 5-12 linhas. A síntese pode ser mais longa (até 20 linhas).

### Sobreativação
**Sintoma:** disparar o ritual completo para uma pergunta que se responde em 3 linhas.
**Correção:** se o problema cabe numa resposta direta, não use a skill.
