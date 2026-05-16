O melhor fluxo para reproduzir esse dashboard no Figma e depois levar para o Power BI seria:

# Estrutura Ideal no Figma

## Frame Principal

* Desktop:

  * `1920x1080`
* Layout Grid:

  * 12 colunas
  * Margem: `32px`
  * Gutter: `24px`

---

# Organização das Camadas

## 01_BACKGROUND

Contém:

* Fundo gradiente
* Grid
* Glow
* Wi-Fi HUD

---

## 02_SIDEBAR

Componentes:

* Sidebar base
* Menu OFF
* Menu ON
* Ícones
* Status sistema

---

## 03_HEADER

Componentes:

* Logo
* Título
* Ícones topo
* Data/Hora

---

## 04_KPIs

Criar 1 componente reutilizável:

* Ícone
* Título
* Valor
* Crescimento

Depois usar Auto Layout.

---

## 05_CHARTS

Separar:

* Chart principal
* Donut 1
* Donut 2
* Atividade
* Mapa

---

# Componentes Essenciais

## Sidebar Item

Criar Component + Variants:

### Variant OFF

* Texto `#E1E8ED`
* Sem glow

### Variant ON

* Fundo azul
* Glow
* Texto branco

Isso facilita MUITO no Power BI depois.

---

# Sistema de Cores

## Styles

### Background

* `#020B1C`

### Blue Primary

* `#00A3FF`

### Blue Deep

* `#013681`

### Text Primary

* `#FFFFFF`

### Text Secondary

* `#B7C4D8`

### Success

* `#00FF85`

### Danger

* `#FF3B3B`

---

# Efeitos no Figma

## Glow Azul

Effects:

* Drop Shadow
* X: 0
* Y: 0
* Blur: 18
* Cor:

  * `#00A3FF`
* Opacidade:

  * `35%`

---

# Auto Layout

Use Auto Layout em:

* Sidebar
* KPI Cards
* Header
* Lista Atividade

Facilita:

* alinhamento
* responsividade
* exportação

---

# Exportação para Power BI

## Background

Export:

* PNG
* 1920x1080

---

## Sidebar

Exportar separado:

* OFF
* ON

---

## Ícones

Preferência:

* SVG

Power BI renderiza melhor.

---

# Estrutura Recomendada do Arquivo

```text
📁 Dashboard
 ┣ 📁 Background
 ┣ 📁 Sidebar
 ┣ 📁 Header
 ┣ 📁 Cards
 ┣ 📁 Charts
 ┣ 📁 Assets
 ┗ 📁 Icons
```

---

# Plugins Figma que vão ajudar MUITO

## Icons

* Iconify

## Gráficos

* Charts
* Datavizer

## UI

* UI Prep
* Design System Organizer

---

# Fluxo Profissional

## Etapa 1

Montar tudo no Figma

## Etapa 2

Exportar:

* fundos
* botões
* assets

## Etapa 3

Montar no Power BI

## Etapa 4

Criar:

* bookmarks
* navegação
* estados ON/OFF

---
* pronto para portfólio
* extremamente diferenciado no LinkedIn/GitHub.
