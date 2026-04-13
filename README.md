# Operação Controlo Total — Dia 1

**Missão de Orientação, Resiliência e Evacuação**  
Cenário: Apagão Global · Miguel Delgado · 17 Abril 2026

---

## Estrutura do Projeto

```
controlo-total-site/
├── render.yaml              ← Blueprint para Render (auto-deploy)
├── .gitignore
├── README.md
└── public/                  ← Ficheiros estáticos servidos pelo Render
    ├── index.html           ← Site responsivo (mobile + desktop)
    └── missao_dia1.pdf      ← PDF para impressão (5 págs A4, fundo preto)
```

## Secções do Site

| # | Secção | Banner | Destinatário | Entrega |
|---|--------|--------|--------------|---------|
| 1 | Carta de Missão | 🟢 Entregar CP1 | Toda a equipa | Envelope selado, 17:30 |
| 2 | Protocolo Rádio | 🔵 Entregar CP2 | Transmissões | Após código no Coreto |
| 3 | Mapa Tático | 🟠 CP2 Opcional | Orientação | Decisão do Comandante |
| 4 | Materiais Facilitador | 🔴 Não Entregar | Facilitador | Nunca chega à equipa |
| 5 | Timeline + Scripts | 🔴 Não Entregar | Facilitador | Nunca chega à equipa |

---

## Deploy no Render

### Opção A — Blueprint (Automático)

1. Criar repo no GitHub com estes ficheiros
2. No [Render Dashboard](https://dashboard.render.com), clicar **New → Blueprint**
3. Conectar o repo → Render lê o `render.yaml` e cria o static site
4. Deploy automático a cada push

### Opção B — Manual

1. No [Render Dashboard](https://dashboard.render.com), clicar **New → Static Site**
2. Conectar o repo GitHub
3. Configurar:
   - **Name:** `controlo-total`
   - **Branch:** `main`
   - **Publish Directory:** `public`
   - **Build Command:** *(deixar vazio)*
4. Clicar **Create Static Site**

### URLs após deploy

- Site: `https://controlo-total.onrender.com`
- PDF: `https://controlo-total.onrender.com/missao_dia1.pdf`

---

## Deploy no GitHub Pages

1. Settings → Pages
2. Source: **Deploy from a branch**
3. Branch: `main`, Folder: `/public`  
   *(ou mover os ficheiros de `public/` para a raiz e selecionar `/`)*
4. O site fica em `https://<username>.github.io/<repo>/`

---

## Setup Local

```bash
git clone https://github.com/<username>/controlo-total-site.git
cd controlo-total-site
# Abrir diretamente no browser:
open public/index.html
```

Sem dependências. Sem build. Sem frameworks. Apenas HTML + CSS + SVG.

---

## Contexto

Materiais para a formação **Controlo Total** — programa certificado pela [European Security Academy](https://www.instagram.com/euseca_portugal/), liderado por [Miguel Delgado](https://migueldelgado.pt) ([@miguel26delgado](https://www.instagram.com/miguel26delgado/)).

---

*CLASSIFICAÇÃO: CONFIDENCIAL — DISTRIBUIÇÃO LIMITADA*
