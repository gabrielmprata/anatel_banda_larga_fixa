# 🧮 Medidas Desenvolvidas

* Criar tabela de medidas 
  
Para Organizar melhor as medidas no projeto, vá no menu principal > Página Inicial > Inserir dados

Coloque o nome da tabela de *medidas*, não precisa colocar o nome da coluna

No menu direito de DADOS, selecionar a tabela de MEDIDAS e escolher a opção de **criar nova medida**

Agora, podemos criar as medidas de maneira organizada

---

🧮 Total de acessos
```
acessos_total = SUM(df_acessos_bl_fixa[acessos])
```

🧮 Total de acessos (panorama)
```
acessos_panorama = SUM(df_panorama_bl_fixa[acessos])
```

🧮 Total de população projetada
```
populacao = sum(dm_populacao[populacao])
```

🧮 Quantidade de acessos do mês anterior (panorama)
```
ant_acessos_pan = CALCULATE([acessos_panorama],DATEADD(dm_calendario[data],-1,MONTH))
```

---
🧮 Faixa de velocidade
```
faixa_velocidade = 
SWITCH(
    TRUE(),
    'df_acessos_bl_fixa'[velocidade] <= 34, "< 34Mbps",
    'df_acessos_bl_fixa'[velocidade] <= 50, "Entre 34 e 50Mbps",
    'df_acessos_bl_fixa'[velocidade] <= 100, "Entre 50 e 100Mbps",
    'df_acessos_bl_fixa'[velocidade] <= 200, "Entre 100 e 200Mbps",
	'df_acessos_bl_fixa'[velocidade] <= 300, "Entre 200 e 300Mbps",
	'df_acessos_bl_fixa'[velocidade] <= 400, "Entre 300 e 400Mbps",
	'df_acessos_bl_fixa'[velocidade] <= 500, "Entre 400 e 500Mbps",
	'df_acessos_bl_fixa'[velocidade] <= 600, "Entre 500 e 600Mbps",
	'df_acessos_bl_fixa'[velocidade] <= 700, "Entre 600 e 700Mbps",
	'df_acessos_bl_fixa'[velocidade] <= 800, "Entre 700 e 800Mbps",
	'df_acessos_bl_fixa'[velocidade] <= 900, "Entre 800 e 900Mbps",
	'df_acessos_bl_fixa'[velocidade] <= 1000, "Entre 900 e 1Gb",
    "1Gb+"
)
```
🧮 Tabela calendario 📅
``` 
dm_calendario = 
VAR DataInicio = DATE(2024, 12, 1)
VAR DataFim = DATE(2025,12,31)
RETURN
    ADDCOLUMNS (
        CALENDAR (DataInicio, DataFim),
        "ano", YEAR([Date]),
        "mes", MONTH([Date]),
        "mes_desc", FORMAT([Date], "MMMM")
        )
```
🧮 Acessos mês anterior
```
ant_acessos = CALCULATE([acessos_total],DATEADD(dm_calendario[data],-1,MONTH))
```
🧮 Variação Acessos
```
var_acessos_tot = IF(ISBLANK([ant_acessos]),BLANK(),DIVIDE([acessos_total],[ant_acessos],0)-1)
```
🧮 Detalhe para Variação Acessos
```
det_var_acessos = (FORMAT([var_acessos_pan],"+;-"))
```
🧮 Market Share
```
Market Share = 

DIVIDE(
    [acessos_total],

    CALCULATE(
        [acessos_total],
        ALL(df_acessos_bl_fixa[empresa])
    )
)
```
🧮 Crescimento MoM
```
Crescimento_MoM = 
DIVIDE(
    [acessos_panorama] - [ant_acessos_pan],
    [ant_acessos_pan]
)
```
🧮 Tendência Estrutural
```
Tendencia_Estrutural = 
[Media_Movel_3M] -
[Media_Movel_12M]
```
🧮 Desvio Padrão
```
Desvio_Padrao_12M = 
VAR Periodo =
    DATESINPERIOD(
        dm_calendario[data],
        MAX(dm_calendario[data]),
        -12,
        MONTH
    )

RETURN

CALCULATE(
    STDEV.P(df_acessos_bl_fixa[acessos]),
    Periodo
)
```
🧮 Média Móvel 3M
```
Media_Movel_3M = 
AVERAGEX(
    DATESINPERIOD(
        dm_calendario[data],
        MAX(dm_calendario[data]),
        -3,
        MONTH
    ),
    [acessos_total]
)
```
🧮 Média Móvel 6M
```
Media_Movel_6M = 
AVERAGEX(
    DATESINPERIOD(
        dm_calendario[data],
        MAX(dm_calendario[data]),
        -6,
        MONTH
    ),
    [acessos_total]
)
```
🧮 Média Móvel 12M
```
Media_Movel_12M = 
AVERAGEX(
    DATESINPERIOD(
        dm_calendario[data],
        MAX(dm_calendario[data]),
        -12,
        MONTH
    ),
    [acessos_total]
)
```
🧮 Forecast Ensemble
```
Forecast_Ensemble = 
(
    [Media_Movel_3M] * 0.5
)
+
(
    [Media_Movel_12M] * 0.5
)
+
(
    [Tendencia_Estrutural] * 0.3
)
```
🧮 Forecast Híbrido
```
Forecast_Hibrido = 
(
    [Media_Movel_3M] * 0.5
) +
(
    [Media_Movel_6M] * 0.3
) +
(
    [Media_Movel_12M] * 0.2
)
```
🧮 Forecast Real
```
Forecast_Real = 
 (
(
    [Media_Movel_3M] * 0.5
) +
(
    [Media_Movel_6M] * 0.3
) +
(
    [Media_Movel_12M] * 0.2
)

+

(
    ([Media_Movel_3M] -
	 [Media_Movel_12M]) * 0.5
)
)
* [Percentual_Do_Pico]
```
🧮 Percentual do Pico
```
Percentual_Do_Pico = 
DIVIDE(
    [acessos_total],

    CALCULATE(
        MAXX(
            ALL(dm_calendario),
            [acessos_total]
        )
    )
)
```
