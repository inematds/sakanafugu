# Blueprint — Curso "LLMs Orquestradas"

Foco (trava do usuário): **mostrar uma nova forma de ter múltiplas LLMs orquestradas.**
Fugu Ultra e OpenRouter Fusion entram como os DOIS exemplos concretos do padrão.

- courseId (`<meta name="inema-course">` + manifesto `course`): **llms-orquestradas**
- Emoji do curso: 🐟  (Sakana = peixe; "vários peixinhos → um peixe maior")
- Título: **LLMs Orquestradas**
- Subtítulo: "A nova forma de rodar vários modelos de IA juntos — do conceito ao Fugu e ao Fusion"
- Fonte de dados: `/tmp/.../scratchpad/fontes-curso.md` (transcript + lesson.html). Números do benchmark = lesson.html.

## Trilhas (3) + módulos (6) — 6 tópicos por módulo

### T1 — Fundamentos (Emerald) `curso/trilha1/`
A "nova forma" e o vocabulário. Trilha de FUNDAMENTO → define CADA termo inline (#31).
- **1-1 — O que é orquestrar várias LLMs** 🧩  (frase-marca: "Quem faz / como combina")
  Tópicos: 1) O que é uma LLM (e por que uma só tem teto) · 2) Orquestração: as 2 perguntas
  (quem faz cada parte / como combina) · 3) Maestro + especialistas + quem funde · 4) "Mixture
  of experts" entregue como 1 API · 5) Você já orquestra (Claude Code + sub-agents) · 6) O custo
  escondido da orquestração (tokens do time, latência).
- **1-2 — O espectro: da mão ao modelo-maestro** 🎚️  (frase-marca: "Da mão ao automático")
  Tópicos: 1) Eixo de quem decide (você ↔ modelo) · 2) Ponta esquerda: você fia na mão
  (Codex+Claude) · 3) Meio: sub-agents/workflows de um provider · 4) Ponta direita: orquestração
  dentro de um modelo treinado (Fugu) · 5) Roteamento: o "conductor" que decide · 6) Trade-offs
  do espectro (controle × esforço × custo).

### T2 — Fugu Ultra: o maestro (Blue) `curso/trilha2/`
Orquestração por DECOMPOSIÇÃO. Usa os dados reais do lesson.html.
- **2-1 — Como o Fugu funciona** 🐡  (frase-marca: "Decompõe, delega, funde")
  Tópicos: 1) "Não é mais inteligente, é um gerente" · 2) O conductor pequeno (decide alone vs
  team) · 3) O pool secreto de modelos frontier · 4) Decompor → delegar → fundir (1 endpoint) ·
  5) Fugu vs Fugu Ultra + preço ($5 in/$30 out, 22 jun 2026) · 6) O que o time NUNCA viu (sua
  resposta cara).
- **2-2 — O veredito: 38 testes, e quando vale a pena** 📊  (frase-marca: "36/38 empate, 5× o preço")
  Tópicos: 1) O exame (38 tarefas, 4 waves, graded por código) · 2) Quem foi mais correto
  (36 empates, 0 do time) · 3) O relógio (4.5× mais lento) · 4) A conta (5× mais caro) · 5) As 2
  derrotas do time (stats 80%, romano 4/5) · 6) O ladder de decisão (quando o orquestrador ganha).
  PRÁTICO: topico de setup conceitual no Claude Code (1 endpoint + API key, pay-as-you-go) —
  honesto que os passos exatos vêm da doc da Sakana / do .md do autor.

### T3 — OpenRouter Fusion: o ensemble (Purple) `curso/trilha3/`
Padrão DIFERENTE: ensemble paralelo + juiz. Enriquecer com conhecimento geral (self-consistency,
LLM-as-judge, mixture-of-agents) definindo termos.
- **3-1 — Mesmo prompt, N modelos, um juiz** ⚖️  (frase-marca: "Paralelo, não decomposição")
  Tópicos: 1) O que a Fusion faz (1 prompt → N modelos) · 2) O juiz que funde · 3) Por que isso
  melhora (perspectivas diversas) · 4) Fusion × Fugu (ensemble × decomposição) · 5) Parentes:
  self-consistency, LLM-as-judge, mixture-of-agents · 6) O custo do paralelo (N respostas + juiz).
- **3-2 — Fusion na prática e o futuro da skill** 🚀  (frase-marca: "Otimizar custo × qualidade")
  Tópicos: 1) Quando paralelo-e-fundir ganha · 2) Quando 1 modelo forte basta · 3) Montar você
  mesmo (padrão judge no Claude Code) · 4) Unit economics da orquestração · 5) Hedge de vendor /
  não travar em 1 provider · 6) A skill do futuro: orquestrar com consciência de custo.

## Manifesto (idêntico em TODA página — só muda o caminho relativo do learn.css/js e a trilha ativa)
```json
{
  "course": "llms-orquestradas",
  "tracks": [
    { "n": "1", "title": "Fundamentos", "modules": [
      { "id": "1-1", "title": "O que é orquestrar várias LLMs", "topics": 6, "href": "curso/trilha1/modulo-1-1.html" },
      { "id": "1-2", "title": "O espectro: da mão ao modelo-maestro", "topics": 6, "href": "curso/trilha1/modulo-1-2.html" }
    ]},
    { "n": "2", "title": "Fugu Ultra", "modules": [
      { "id": "2-1", "title": "Como o Fugu funciona", "topics": 6, "href": "curso/trilha2/modulo-2-1.html" },
      { "id": "2-2", "title": "O veredito: 38 testes", "topics": 6, "href": "curso/trilha2/modulo-2-2.html" }
    ]},
    { "n": "3", "title": "OpenRouter Fusion", "modules": [
      { "id": "3-1", "title": "Mesmo prompt, N modelos, um juiz", "topics": 6, "href": "curso/trilha3/modulo-3-1.html" },
      { "id": "3-2", "title": "Fusion na prática", "topics": 6, "href": "curso/trilha3/modulo-3-2.html" }
    ]}
  ]
}
```

## Caminhos relativos para assets
- landing `index.html`: `assets/learn.css` · `assets/learn.js`
- `curso/trilhaX/*.html`: `../../assets/learn.css` · `../../assets/learn.js`

## Cores: T1 Emerald (#059669 light), T2 Blue (#2563eb), T3 Purple (#7c3aed / violet-600).
