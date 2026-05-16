# Wireframe Descritivo — Dashboard Rede & Conectividade (Power BI)

## Estrutura Geral

### Resolução Base

* Canvas: `1920 x 1080`
* Tema: Dark Futuristic / Cyber UI
* Background:

  * Azul escuro gradiente
  * Grid tecnológico discreto
  * Glow azul neon
  * Elemento visual Wi-Fi no lado direito

---

# 1. SIDEBAR ESQUERDA

## Dimensões

* Largura: `180px`
* Altura: `100%`

## Fundo

* Cor:

  * `#020B1C`
* Transparência leve
* Glow azul discreto nas bordas

## Estrutura

### Topo

#### Botão Menu Hamburger

* Ícone:

  * tamanho `26px`
* Cor OFF:

  * `#E1E8ED`
* Cor ON:

  * `#00A3FF`

---

# 2. MENU PRINCIPAL

## Itens

1. Visão Geral
2. Dispositivos
3. Redes
4. Alertas
5. Relatórios
6. Configurações

---

## Estrutura de Cada Item

### Container

* Altura: `72px`
* Border Radius: `8px`
* Padding Left: `22px`

---

## Estado OFF

### Fundo

* Transparente

### Ícone

* Cor:

  * `#E1E8ED`

### Texto

* Fonte:

  * Segoe UI / Montserrat
* Peso:

  * SemiBold
* Tamanho:

  * `16px`
* Cor:

  * `#E1E8ED`

---

## Estado ON (Selecionado)

### Fundo

* Gradiente:

  * `#013681`
  * `#0353C7`

### Glow

* Outer Glow Azul:

  * Blur `18px`
  * Opacidade `35%`

### Ícone

* Cor:

  * `#FFFFFF`
* Glow Azul

### Texto

* Cor:

  * `#FFFFFF`

---

# 3. HEADER SUPERIOR

## Altura

* `90px`

## Elementos

### Logo Shield

* Tamanho:

  * `42px`

### Título

#### DASHBOARD

* Fonte:

  * Montserrat Bold
* Tamanho:

  * `32px`
* Cor:

  * `#FFFFFF`

#### REDE E CONECTIVIDADE

* Fonte:

  * Montserrat Medium
* Tamanho:

  * `14px`
* Cor:

  * `#00A3FF`

---

## Área Direita

### Ícones

* Notificação
* Configuração

### Data/Hora

* Fonte:

  * `14px`
* Cor:

  * `#B7C4D8`

---

# 4. KPI CARDS SUPERIORES

## Quantidade

* 4 Cards

## Dimensão

* Largura:

  * `220px`
* Altura:

  * `190px`

## Fundo

* Cor:

  * `#04152D`

## Borda

* `1px solid #0F3E87`

## Border Radius

* `16px`

---

## Conteúdo Interno

### Ícone Superior

* Cor:

  * `#00A3FF`

### Valor Principal

* Fonte:

  * `42px`
* Peso:

  * Bold
* Cor:

  * Branco

### Indicador Crescimento

* Cor:

  * `#00D1FF`

---

# 5. HERO VISUAL WIFI

## Localização

* Canto superior direito

## Elementos

* Ícone Wi-Fi gigante
* Radar circular HUD
* Glow reduzido

## Opacidade Recomendada

* `20% ~ 35%`

Importante:

> Não competir visualmente com gráficos do Power BI.

---

# 6. GRÁFICO PRINCIPAL

## Tipo

* Line Area Chart

## Dimensões

* `760 x 300`

## Estilo

### Linha

* Azul neon:

  * `#00A3FF`

### Área

* Gradiente azul transparente

### Fundo

* Transparente

### Grid

* Azul escuro discreto

---

# 7. DONUT CHARTS

## Quantidade

* 2

## Dimensões

* `360 x 330`

---

## Estilo

### Centro

* Valor total grande

### Fatias

* Tons de azul:

  * `#00A3FF`
  * `#1B6DFF`
  * `#2F8CFF`
  * `#5CAEFF`

---

# 8. PAINEL ATIVIDADE TEMPO REAL

## Tipo

* Lista vertical

## Elementos

* Ícone
* Evento
* Timestamp

## Cores dos Alertas

* Verde = sucesso
* Azul = conexão
* Vermelho = crítico

---

# 9. MAPA DE COBERTURA

## Estrutura

* Mini mapa blueprint
* Glow azul
* Pings circulares

---

# 10. PALETA DE CORES

| Elemento         | Cor     |
| ---------------- | ------- |
| Background       | #020B1C |
| Azul Principal   | #00A3FF |
| Azul Escuro      | #013681 |
| Branco           | #FFFFFF |
| Texto Secundário | #B7C4D8 |
| Verde Status     | #00FF85 |
| Vermelho Alerta  | #FF3B3B |

---

# 11. TIPOGRAFIA

## Fonte Principal

* Montserrat
  ou
* Segoe UI

## Hierarquia

| Uso           | Tamanho |
| ------------- | ------- |
| Título        | 32px    |
| KPI           | 42px    |
| Subtítulo     | 16px    |
| Texto comum   | 14px    |
| Label pequena | 12px    |

---

# 12. EFEITOS VISUAIS

## Glow

* Azul Neon
* Baixa opacidade

## Sombras

* Soft Shadow
* Blur alto
* Escuro

## Bordas

* Radius:

  * `12 ~ 18px`

---

# 13. IMPLEMENTAÇÃO NO POWER BI

## Recomendado

### Navegação

* Bookmarks
* Botões transparentes
* PNGs ON/OFF

### Background

* Inserir como Canvas Background

### Cards

* Shapes + visual transparente

### Ícones

* SVG preferencialmente

### Melhor Resultado

* Usar:

  * Figma
  * PowerPoint
  * Photoshop
    para assets externos.
