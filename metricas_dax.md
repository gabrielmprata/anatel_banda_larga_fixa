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
