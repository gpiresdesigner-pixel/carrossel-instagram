# 🎠 instagram-carousel — Claude Skill

> Skill para o Claude criar carrosséis profissionais para o Instagram automaticamente — do briefing ao PNG 1080×1350px pronto para postar.

Criada por [@estrategistagabriel](https://instagram.com/estrategistagabriel)

---

## O que essa skill faz

Com ela instalada, o Claude vira um designer de carrosséis completo. Você descreve o tema, ele gera:

- **Paleta de cores** derivada automaticamente da sua cor principal (6 tokens)
- **Tipografia profissional** com pares do Google Fonts
- **HTML interativo** com frame do Instagram e swipe real para preview
- **Script Python** para exportar cada slide como PNG 1080×1350px

Tudo isso a partir de um único prompt.

---

## Fontes de conteúdo suportadas

| Fonte | Como usar |
|-------|-----------|
| Tema livre | Diga o assunto — o Claude estrutura os slides |
| Blog / artigo | Cole o texto ou envie a URL |
| Vídeo | URL do YouTube, TikTok ou Instagram Reels |
| Modelo de design | Envie uma imagem — o Claude extrai cores e estilo |

---

## Como instalar

### Pré-requisito
Você precisa ter o [Claude.ai](https://claude.ai) com suporte a skills (Projects ou plano Pro).

### Passo a passo

**1. Clone ou baixe este repositório**

```bash
git clone https://github.com/estrategistagabriel/instagram-carousel-skill.git
```

**2. Faça upload da skill no Claude**

No Claude.ai, vá em **Projects → Skills → Upload Skill** e selecione a pasta `instagram-carousel/`.

Ou, se estiver usando o Claude Code:

```bash
claude skills install ./instagram-carousel
```

**3. Pronto.** A skill é ativada automaticamente quando você mencionar carrossel, slides para Instagram ou transformar conteúdo em post.

---

## Como usar

Abra o Claude e diga algo como:

```
Cria um carrossel sobre os 5 erros mais comuns no tráfego pago
```

```
Transforma esse vídeo em carrossel: youtube.com/...
```

```
Quero um carrossel com o estilo dessa imagem [anexo]
```

O Claude vai perguntar os dados da sua marca (cor, @handle, fonte, tom) e gerar o HTML completo para você revisar antes de exportar.

---

## Exportando os slides

Após aprovar o preview, peça o script de exportação:

```
Agora gera o script Python para exportar os slides
```

O Claude entrega um script pronto. Para rodar:

```bash
pip install playwright
playwright install chromium
python export_slides.py
```

Os PNGs ficam salvos em `./slides/` com 1080×1350px — prontos para upload direto no Instagram.

---

## Estrutura da skill

```
instagram-carousel/
├── SKILL.md                        ← Instruções principais do fluxo
└── references/
    ├── slide-architecture.md       ← Componentes HTML e estrutura base
    ├── typography.md               ← Pares de fontes e escala tipográfica
    ├── export-script.md            ← Script Python de exportação
    ├── video-content.md            ← Extração de conteúdo de vídeos
    └── model-extraction.md         ← Extração de estilo de modelos de design
```

---

## Exemplo de output

O carrossel gerado tem 7 slides com sequência narrativa completa:

| # | Tipo | Objetivo |
|---|------|----------|
| 1 | Hero | Hook — frase de impacto que para o scroll |
| 2 | Problema | A dor do seu público |
| 3 | Solução | O que resolve |
| 4 | Recursos | O que você entrega |
| 5 | Detalhes | Diferenciais e provas |
| 6 | Passo a passo | Como funciona na prática |
| 7 | CTA | Chamada para ação clara |

Todos os slides têm barra de progresso, seta de swipe e são exportados individualmente como PNG.

---

## Requisitos técnicos

| Ferramenta | Versão mínima |
|-----------|--------------|
| Python | 3.8+ |
| Playwright | 1.40+ |
| Chromium | instalado via `playwright install chromium` |
| Claude | Plano Pro ou Team com suporte a skills |

---

## Contribuindo

Encontrou um bug ou quer sugerir uma melhoria? Abre uma [issue](../../issues) ou manda um PR.

Ideias bem-vindas:
- Novos temas visuais (dark mode, editorial, minimalista)
- Suporte a mais fontes de conteúdo
- Integração com agendadores de post

---

## Licença

MIT — use, modifique e distribua à vontade. Crédito é bem-vindo mas não obrigatório.

---

## Autor

Feito com ☕ e Claude por **Gabriel Pires**

- Instagram: [@estrategistagabriel](https://instagram.com/estrategistagabriel)
