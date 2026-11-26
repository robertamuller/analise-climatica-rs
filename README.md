# Projeto da disciplina de **Análise Exploratória de Dados e Visualização** (FGV EMAp, 2026.2).

A ideia deste projeto surgiu a partir da preocupação com os eventos climáticos extremos no Rio Grande do Sul, que parecem se tornar cada vez mais frequentes, principalmente as enchentes, que marcaram o estado em 2024. Além de buscar compreender melhor os padrões de temperatura e precipitação do estado, suas variações espaciais e temporais e a ocorrência de eventos extremos, tenho interesse em aprender a trabalhar com bases de dados climáticas e explorar como o clima se relaciona com outros problemas. Em particular, me interessa entender como as condições climáticas podem influenciar a dinâmica de transmissão de doenças transmitidas por vetores, tema diretamente relacionado à minha pesquisa de Trabalho de Conclusão de Curso (TCC).

## Dados

**ERA5-Land mensal (1990–2025)**, do Copernicus: temperatura a 2 m e precipitação total

**Malhas do IBGE**: estado, 497 municípios e mesorregiões

## O que tem no notebook

1. Padrões espaciais de temperatura e chuva (mapas)
2. Ciclo anual e comparação entre 5 cidades (Porto Alegre, Pelotas, Uruguaiana, Arroio do Sal e Santa Rosa)
3. Variabilidade entre anos (desvio-padrão e CV)
4. Extremos usando percentis (P90 e P95), com foco em maio/2024 em POA
5. Evolução ao longo dos anos
6. e 7. Agrupamento dos municípios com K-Means
8. Municípios atípicos com DBSCAN

## Como rodar

Instalar as bibliotecas:

```bash
pip install numpy pandas xarray rioxarray netCDF4 geopandas shapely matplotlib seaborn scikit-learn scipy requests jupyter
```

E depois é só abrir e rodar o `analise_climatica.ipynb` do começo ao fim.

As malhas do IBGE são baixadas automaticamente. O arquivo do ERA5 fica em `dados_era5/`. Se ele não estiver lá, o notebook tenta baixar pela API do Copernicus (aí precisa do `cdsapi` instalado e de uma conta no CDS com a chave configurada).

---

Roberta Müller Nuñes
