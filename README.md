# UC7 — Custos Logísticos (Site Didático)

> Site estático, em **HTML/CSS/JS + Bootstrap**, para apoiar a **Unidade Curricular 7 — Custos Logísticos**. Reúne estudos de caso, fórmulas, passo a passo didático, KPIs e consolidações. Pronto para publicar no **GitHub Pages**.

## 🎯 Objetivos
- Demonstrar **custos diretos e indiretos** de logística com linguagem clara e visual.
- Oferecer **exercícios guiados** com fórmulas e resultados intermediários.
- Consolidar **KPIs**: custo por pedido, por linha, por m², por unidade estocada, utilização de MO, etc.

## 📦 O que já vem pronto
- **Home (`index.html`)**: navegação da UC7, cards de conteúdos e link para o Case de Armazenagem.
- **Case 1 — Armazenagem (`case1-armazenagem.html`)**: enunciado completo, fórmulas, cálculos passo a passo, transições (fade), resultados e KPIs.
- **Responsivo** (Bootstrap via CDN) e **zero build** (só abrir o HTML no navegador).

> Dica: Os números do Case 1 são didáticos e podem ser ajustados no objeto `params` (ver seção **Parametrização**).

---

## 🗂️ Estrutura de pastas (sugerida)
```
uc7-custos-logisticos/
├─ index.html                # Página inicial da UC7
├─ case1-armazenagem.html    # Estudo completo de custos de armazenagem (pequeno porte)
├─ assets/                   # (opcional) imagens e arquivos estáticos
│  ├─ img/
│  └─ css/ js/
└─ README.md
```

> As dependências (Bootstrap e ícones) são carregadas por **CDN** — não há node_modules.

---

## ▶️ Como rodar localmente
**Opção 1 (mais simples):**
1. Baixe/clique duas vezes em `index.html` para abrir no navegador.

**Opção 2 (servidor local):**
```bash
# Se tiver Node.js
npx serve .
# ou
python -m http.server 8080
```
Acesse: `http://localhost:3000` ou `http://localhost:8080` (conforme a ferramenta).

---

## 🌐 Publicar no GitHub Pages
1. Crie um repositório **público** (ex.: `uc7-custos-logisticos`).
2. Envie `index.html` e `case1-armazenagem.html` para a branch **main**.
3. Vá em **Settings → Pages** → **Source: Deploy from a branch**.
4. Selecione **Branch: main** e **/ (root)** → **Save**.
5. Acesse a URL: `https://<seu-usuario>.github.io/uc7-custos-logisticos/`.

Links úteis do site:
- Home: `/`
- Case 1: `/case1-armazenagem.html`

---

## ⚙️ Parametrização (Case 1 — Armazenagem)
No arquivo `case1-armazenagem.html`, ajuste o objeto **`params`** no `<script>` para simular cenários:
```js
const params = {
  areaTotal: 150,
  areaPrat: 90,
  areaPP: 30,
  areaOper: 30,
  estoqueMedio: 5000,
  pedidosMes: 250,
  linhasExpedidas: 400,
  POs: 15,
  linhasCompradas: 300,
  aluguel: 6750,
  util: 1500,
  seguros: 400,
  seguranca: 350,
  manut: 500,
  ti: 600,
  deprecEstr: 833.33,
  deprecMHE: 83.33,
  overheadAdm: 800,
  moDireta: 7040,
  moIndireta: 2640,
  consumiveis: 1350,
  adminCompras: 493.75,
  custoHoraMOD: 20,
  custoHoraMOI: 30,
  recebMinPorLinha: 3.5,
  putMinPorLinha: 2.0,
  pickMinPorLinha: 3.0,
  embMinPorPedido: 7.0,
  inventarioHoras: 24,
  expedicaoMiscHoras: 12,
  etiquetaPorLinha: 0.50,
  insumosPorPedido: 3.00,
  skusContadosMes: 80,
};
```
> Os resultados e KPIs se atualizam automaticamente quando esses valores mudam.

---

## 🧮 Fórmulas principais (sem LaTeX)
- **Custo de m²/mês** = (aluguel + utilidades + seguros + segurança + manutenção) ÷ m².
- **Prateleira (por localização/mês)** = Custo m² × 0,25 m² (4 loc/m²).
- **Porta‑palete (por posição/mês)** = Custo m² × ~1,0 m² por posição.
- **Holding (mês)** = base de área + deprec. estruturas + 50% TI + 50% (MO indireta + overhead adm.).
- **Custo por unidade estocada (mês)** = Holding ÷ estoque médio (unidades).
- **Custo unitário do processo** = (minutos ÷ 60 × custo/h) + consumíveis (se houver).
- **Custo de pedido (por linha comprada)** = (horas adm. × custo/h) ÷ linhas do mês.
- **KPIs**: custo por pedido = Total ÷ pedidos; custo por linha = Total ÷ linhas; custo por m² = base de área ÷ m²; produtividade = linhas ÷ horas.

---

## 🧭 Roadmap
- [ ] Custos de **Transporte** (fixos/variáveis, faixas, pedágio/GRIS, modais)
- [ ] Custos de **Produção** (CIF, centros de custos, rateios)
- [ ] **Formação de Preço** (markup, impostos, frete, margem)
- [ ] **Margem de Contribuição** (por item/pedido/cliente)
- [ ] **Ponto de Equilíbrio** (contábil/econômico/financeiro)
- [ ] **Custo de Pedido** (admin compras/recebimento detalhado)

Contribuições são bem-vindas! Abra uma **issue** ou envie um **pull request**.

---

## 👤 Autor & Licença
- Autor: **Leandro Pereira** (UC7 — Custos Logísticos)
- Licença: **MIT** (ajuste se preferir outra)

> Se publicar como **GitHub Pages**, lembre de manter os links relativos (`case1-armazenagem.html`) e o repositório como **público**.
