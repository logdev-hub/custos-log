# UC7 — Custos Logísticos (Site Didático)

> Site estático, em **HTML/CSS/JS + Bootstrap**, para apoiar a **Unidade Curricular 7 — Custos Logísticos**. Reúne estudos de caso, fórmulas, passo a passo didático, KPIs e consolidações. Pronto para publicar no **GitHub Pages**.

## 🎯 Objetivos
- Demonstrar **custos diretos e indiretos** de logística com linguagem clara e visual.
- Oferecer **exercícios guiados** com fórmulas e resultados intermediários.
- Consolidar **KPIs**: custo por pedido/linha, por m², por unidade estocada, utilização de MO, etc.

## 📦 O que já vem pronto
- **Home (`index.html`)**: navegação da UC7 e cards de conteúdos.
- **Case 1 — Armazenagem (`case1-armazenagem.html`)**: custos por área, holding, processos e KPIs.
- **Case 2 — Transporte (`case2-transporte.html`)**: fixos/variáveis, pedágio, GRIS e R$/km • R$/kg.
- **Case 3 — Produção (`case3-producao.html`)**: DM, MOD, CIF, depreciação, Tradicional × ABC.
- **Case 4 — Formação de Preço (`case4-preco.html`)**: markup, impostos, comissionamento, frete e PEQ.
- **Case 5 — Ponto de Equilíbrio (`case5-ponto-equilibirio.html`)**: PE contábil/econômico/financeiro com sensibilidade logística.
- **Case 6 — Custo de Pedido (`case6-custo-pedido.html`)**: custo/linha comprada, tempos administrativos e automação (EDI/NF-e).
- **Case 7 — Custo por Processo (CD) (`case7-processos-cd.html`)**: recebimento, put-away, picking, embalagem, expedição e inventário.
- **Case 8 — Mão de Obra Direta/Indireta (`case8-mao-de-obra.html`)**: dimensionamento, custo/h, utilização e impactos no custo logístico.
- **Sobre (`sobre.html`)**: proposta do projeto e instruções de publicação.

**Todos os cases** possuem **navbar padrão** “UC7 — Custos Logísticos” e mantêm o visual responsivo (Bootstrap via CDN).

---

## 🗂️ Estrutura de pastas (sugerida)
```
uc7-custos-logisticos/
├─ index.html
├─ sobre.html
├─ case1-armazenagem.html
├─ case2-transporte.html
├─ case3-producao.html
├─ case4-preco.html
├─ case5-ponto-equilibirio.html
├─ case6-custo-pedido.html
├─ case7-processos-cd.html
├─ case8-mao-de-obra.html
└─ README.md
```
> Dependências (Bootstrap e ícones) por **CDN** — não há node_modules.

---

## ▶️ Como rodar localmente
**Opção 1 (mais simples):**
1. Clique duas vezes em `index.html`.

**Opção 2 (servidor local):**
```bash
# Se tiver Node.js
npx serve .
# ou
python -m http.server 8080
```
Acesse `http://localhost:3000` ou `http://localhost:8080`.

---

## 🌐 Publicar no GitHub Pages
1. Crie um repositório **público** (ex.: `uc7-custos-logisticos`).
2. Envie todos os arquivos (`index.html`, `sobre.html` e `case*.html`) para a branch **main**.
3. Vá em **Settings → Pages** → **Source: Deploy from a branch**.
4. Selecione **Branch: main** e **/ (root)** → **Save**.
5. Acesse: `https://<seu-usuario>.github.io/uc7-custos-logisticos/`.

Links úteis:
- Home: `/`
- Sobre: `/sobre.html`
- Case 1: `/case1-armazenagem.html`
- Case 2: `/case2-transporte.html`
- Case 3: `/case3-producao.html`
- Case 4: `/case4-preco.html`
- Case 5: `/case5-ponto-equilibirio.html`
- Case 6: `/case6-custo-pedido.html`
- Case 7: `/case7-processos-cd.html`
- Case 8: `/case8-mao-de-obra.html`

---

## ⚙️ Parametrizações e Fórmulas (resumo)
- **Custo unitário de processo** = (min ÷ 60 × R$/h) + insumos.
- **Custo de pedido (linha)** = (horas adm. × R$/h + sistemas) ÷ linhas.
- **Holding** = base de área + deprec + fração de TI/overhead → por unidade estocada.
- **PE Contábil** = CF_contábil ÷ MC_un; **PE Econômico** = (CF + lucro alvo) ÷ MC_un; **PE Financeiro** = CF_fin ÷ MC_un.
- **Transporte**: custo viagem = fixos rateados por hora + variáveis por km + pedágio + GRIS.

---

## 🧭 Roadmap (sugestões)
- [ ] Painéis comparativos entre cases (consolidação de KPIs).
- [ ] Exportar resultados para CSV/PNG (tabelas e gráficos).
- [ ] Integração mínima com inputs via URL (query string) para cenários.

---

## 👤 Autor & Licença
- Autor: **Leandro Pereira** (UC7 — Custos Logísticos)
- Licença: **MIT**
