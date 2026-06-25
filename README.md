# 🛜 Anatel - Acessos de Banda Larga Fixa no Brasil :chart_with_upwards_trend:

<p align="left">
<img src="http://img.shields.io/static/v1?label=STATUS&message=EM%20DESENVOLVIMENTO&color=RED&style=for-the-badge" #vitrinedev/>  

<img src="http://img.shields.io/static/v1?label=vers%C3%A3o%20do%20projeto&message=v4.0&color=red&style=for-the-badge&logo=github"/>
</p>
<br><br>

## 🖥️ Demo App

<img loading="lazy" src="https://img.icons8.com/?size=100&id=3sGOUDo9nJ4k&format=png&color=000000" width="30" height="30"/>[![PowerBI App](https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=Power%20BI&logoColor=white)](https://app.powerbi.com/view?r=eyJrIjoiZDNjYjdmMzItOGZkNy00NWI0LTk5NmQtZDhmMGRjZWZlYjNiIiwidCI6IjY1OWNlMmI4LTA3MTQtNDE5OC04YzM4LWRjOWI2MGFhYmI1NyJ9)






![Dashboard Demo](assets/demo.gif)

# 📶 Introdução

Os dados apresentados nesse estudo acadêmico, referem-se aos acessos de Banda Larga Fixa (**SCM** - Serviço de Comunicação Multimídia), enviados pelas prestadoras do serviço.

O Serviço de Comunicação Multimídia é um serviço fixo de telecomunicações de interesse coletivo, prestado em âmbito nacional e internacional, no regime privado, que possibilita a oferta de capacidade de transmissão, emissão e recepção de informações multimídia, permitindo inclusive o provimento de conexão à internet, utilizando quaisquer meios, a Assinantes dentro de uma Área de Prestação de Serviço.
<br><br>
# 🛜 Sobre o Mercado
>
O mercado de banda larga fixa vem crescendo cada vez mais no Brasil, gerando uma grande concorrência entre empresas de telecomunicações.
>
Cada vez mais, os brasileiros desejam ter em casa uma conexão de alta velocidade e de grande estabilidade, e esse cenário é um efeito da modernização da infraestrutura de telecomunicações no país.
>
Trata-se de um movimento cujo início beneficiou principalmente grandes centros urbanos, mas que foi expandindo gradualmente para cidades pequenas e bairros mais afastados.
Não resta dúvida hoje em dia, que **a banda larga mais eficaz é a Fibra óptica**.
>
A ANATEL(Agência Nacional de Telecomunicações) divulgou em seu portal de dados, que em 2025 o Brasil registrou **55,4 milhões de acessos de banda larga fixa**, e que 79% desses acessos, são de Fibra Óptica.
>
Com os dados disponibilizados pela ANATEL, iremos entender o cenário de Banda Larga no Brasil.
<br><br>
# 🎯 Objetivo do Projeto

Demonstrar capacidade em:

* Data Analytics
* Data Science
* Power BI avançado
* Estatística aplicada
* Storytelling analítico
* UX para dashboards

# 🛠️ Tecnologias

* <img src="https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue"  width="80" height="20"/>
* <img loading="lazy" src="https://img.icons8.com/?size=100&id=3sGOUDo9nJ4k&format=png&color=000000" width="20" height="20"/><img loading="lazy" src="https://img.shields.io/badge/PowerBI-F2C811?style=for-the-badge&logo=Power%20BI&logoColor=white" width="80" height="20"/>
* DAX
* Power Query
* Estatística Aplicada
* Forecasting Analytics
* 🐍 Python

# 🧠 Técnicas Utilizadas

| Categoria        | Técnicas                      |
| ---------------- | ----------------------------- |
| Estatística      | Média, Desvio Padrão, Z-score |
| Séries Temporais | Média Móvel, Tendência Linear |
| Analytics        | Market Share, Volatilidade    |
| Forecast         | Previsão temporal             |
| BI               | KPIs executivos               |
| UX/UI            | UX para dashboards          |

# 📈 Principais Visuais

* KPIs
  * Total de acessos com variação MoM
  * Densidade
  * Total de reclamações com variação MoM

* Linhas com o historico de acessos dos últimos 10 anos
* Barras horizontal com o MarketShare por operadora com a opção de "Outros"(agrupa todas as outraas que não estão entre as Top 12)
* Mapa do Brasil
* Barras com adições liquidas de fibra(net-add)
* Barras com maiores perdas de acessos(Churn)
* Último 6 meses baseado no filtro de segmentação
* Forecast Temporal

# 📌 Insights Gerados

O projeto permite identificar:

* Operadoras com crescimento anômalo
* Expansão agressiva de ISPs regionais
* Concentração de mercado
* Volatilidade operacional
* Tendência de crescimento
* Ganho/perda de market share
* Risco competitivo
* Aceleração regional
* Operadoras com mais reclamações na ANATEL

# 📊 Principais Métricas Estatísticas

## Média dos Últimos 3/6/12 Meses
Utilizada para identificar o comportamento médio do mercado.

$$
\mu = \frac{\sum x}{n}
$$  

## Desvio Padrão

Mede a dispersão dos acessos entre operadoras.

$$
\sigma = \sqrt{\frac{\sum (x-\mu)^2}{n}}
$$


## Z-Score

Detecta operadoras fora do padrão estatístico.

$$
Z = \frac{x - \mu}{\sigma}
$$

# 🚀 Próximos Passos

* Implementar Prophet Forecast
* Previsto x Realizado
* Churn prediction
* Forecast por UF

# 🎨 UX/UI Design
Acesse o design de interface no Figma!

<a href="https://www.figma.com/design/OO6KSzkn8NwiGCw3pkBMSb/Dash_Banda_Larga_Fixa?node-id=0-1&m=dev&t=68cCvjjaU9CvstNc-1"><img src="https://img.icons8.com/?size=100&id=8gfeOoqrHqJU&format=png&color=000000" width="40" height="40" alt="Acesse"></a>

# 📊 Modelo Analítico

## Fluxo da análise

```text id="t2f44f"
Dados → Tratamento → Estatística → Anomalias → Forecast → Insights
```

# 🧱 Arquitetura de Dados

O projeto utiliza modelagem dimensional no padrão **Star Schema**, garantindo:

* melhor performance;
* escalabilidade;
* facilidade analítica.

# 📚 Aprendizados

Durante o desenvolvimento deste projeto foram aplicados conceitos de:

* Estatística descritiva
* Séries temporais
* Engenharia analítica
* UX para BI
* Design orientado a dados
* Storytelling executivo
* Telecom Analytics

# 👨‍💻 Autor

**Gabriel Prata**

Especialista em Business Intelligence (BI) | Cientista de Dados | Data Viz Developer | Analytics Engineer

📍 Rio de Janeiro - Brasil

💼 Focado em Analytics, Ciência de Dados, Forecasting e Business Intelligence

Built with Data, Analytics & Coffee
