# <img loading="lazy" src="https://img.icons8.com/?size=100&id=8gfeOoqrHqJU&format=png&color=000000" width="40" height="40"/> Estrutura no Figma

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

---

## 03_HEADER

Componentes:

* Logo
* Título
* Ícones topo
* Data/Hora

---

## 04_KPIs

Criar 2 componente reutilizável:

* Título
* Valor
* Crescimento

Depois usar Auto Layout.

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


# Sistema de Cores

## Styles

### Background

* ![#FF5733](https://placehold.co/30x30/020B1C/020B1C/png) `#020B1C`

### Blue Primary

* ![#FF5733](https://placehold.co/30x30/00A3FF/00A3FF/png) `#00A3FF`

### Blue Deep

* ![#FF5733](https://placehold.co/30x30/013681/013681/png) `#013681`

### Text Primary

* ![#FF5733](https://placehold.co/30x30/FFFFFF/FFFFFF/png) `#FFFFFF`

### Text Secondary

* ![#FF5733](https://placehold.co/30x30/B7C4D8/B7C4D8/png) `#B7C4D8`

### Success

* ![#FF5733](https://placehold.co/30x30/00FF85/00FF85/png) `#00FF85`

### Danger

* ![#FF5733](https://placehold.co/30x30/FF3B3B/FF3B3B/png) `#FF3B3B`

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

# Exportação para Power BI

## Background

Export:

* PNG
* 1920x1080

Exportar separado:

* OFF
* ON

