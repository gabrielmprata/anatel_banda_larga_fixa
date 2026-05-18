# 🧮 Métricas Desenvolvidas

* Faixa de velocidade
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
