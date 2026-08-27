# Soluções em Energias Renováveis e Sustentáveis
> **Atividade Prática de Análise de Dados no Setor Energético**  
> **Curso:** Ciência da Computação | **Instituição:** FIAP  
> **Ferramentas:** Orange Data Mining, Python, Pandas, Matplotlib & Seaborn  

---

## Integrantes

| Nome | RM |
|:-----|:---|
| Caio Henrique Ferraz da Silva | RM568992 |
| Enzo Caruso Peter | RM570908 |
| Leonardo Figueredo dos Santos | RM573653 |
| Leonardo Robert Maulicino | RM570329 |
| Pablo Renato dos Santos Sobral de Carvalho | RM569894 |

---

## Sobre o Repositório

Este repositório contém as soluções desenvolvidas para a atividade prática da disciplina **Soluções em Energias Renováveis e Sustentáveis**. 

O objetivo principal do projeto é aplicar técnicas avançadas de preparação, inspeção, filtragem condicional e análise exploratória de dados em conjuntos de dados reais do setor elétrico e renovável. As etapas combinam amostragem e limpeza no **Orange Data Mining** com processamento e geração de diagnósticos no **Python / Pandas**.

Todos os exercícios foram consolidados em um único Jupyter Notebook (`.ipynb`), integrando código executável, visualizações gráficas e pareceres interpretativos fundamentados no contexto operacional de cada cenário energético.

---

## Tecnologias e Ferramentas

* **Orange Data Mining:** Amostragem aleatória estratificada, inspeção visual de tipos, validação de integridade e exportação de subsets.
* **Python 3.12+:** Linguagem base para desenvolvimento dos scripts de processamento.
* **Pandas:** Manipulação de DataFrames, tratamento estatístico, renomeação de atributos e filtragem condicional vetorial.
* **Matplotlib & Seaborn:** Construção de histogramas comparativos e distribuições de frequência com marcadores de limiares estatísticos.

---

## Datasets e Exercícios Analisados

O projeto abrange a análise de 6 datasets distintos do ecossistema energético global:

### Dataset 1 — Appliances Energy Prediction (UCI)
* **Cenário:** Análise do consumo de eletrodomésticos residenciais sob variações de temperatura e umidade.
* **Destaques:** Filtragem de consumo acima de 70% do pico e cruzamento com a temperatura média da residência ($T_1$).

### 🏭 Dataset 2 — Steel Industry Energy Consumption (UCI)
* **Cenário:** Identificação de picos de demanda energética em uma indústria siderúrgica e diagnóstico de ineficiência operacional.
* **Destaques:** Mapeamento de consumo $\ge 75\%$ do máximo ($153,14\text{ kWh}$), correlação com a categoria `Maximum_Load` (62 registros) e estabelecimento de limiar para Fator de Potência Adiantado ($\le 60\%$) com base na assimetria da distribuição.

### Dataset 3 — Power Consumption of Tetouan City (UCI)
* **Cenário:** Planejamento de distribuição de energia entre 3 zonas urbanas da cidade de Tétouan (Marrocos).
* **Destaques:** Identificação da Zona 1 como maior pico de consumo ($51.571,50\text{ kW}$), aplicação do limiar de 70% (2.388 registros / 30,37%) e análise do impacto ambiental ao filtrar temperaturas acima da média ($18,79^\circ\text{C}$), resultando em 1.597 registros.

### Dataset 4 — Solar Power Generation Data (Kaggle)
* **Cenário:** Monitoramento de geração em usina fotovoltaica e frequência de produção por inversor.
* **Destaques:** Mapeamento da potência CA máxima, filtro de alta geração (> 70% do pico — 1.185 registros / 8,61%) e contagem da distribuição de carga através do método `value_counts()` na chave do inversor (`SOURCE_KEY`).

### Dataset 5 — Wind & Solar Energy Production (Kaggle)
* **Cenário:** Comparação da distribuição de picos entre fontes renováveis eólica e solar.
* **Destaques:** Normalização relativa das fontes respeitando suas escalas máximas individuais (70% do pico solar vs. 70% do pico eólico) e justificativa técnica da inadequação do uso de limiares numéricos absolutos para fontes distintas.

### Dataset 6 — Individual Household Electric Power Consumption (UCI)
* **Cenário:** Monitoramento de alta demanda elétrica residencial e sobrecarga de corrente.
* **Destaques:** Limpeza de registros ausentes (`NaN`), cálculo do limiar de 75% da Potência Ativa Média e aplicação de condição simultânea com a Corrente Média ($4,6376\text{ A}$), comprovando intersecção total ($A \cap B = A$) dada a intensidade da demanda.

---

## Estrutura do Repositório

```text
├── datasets/
│   ├── energydata_complete_sample.csv
│   ├── steel_industry_energy_consumption_sample.csv
│   ├── power_consumption_of_tetouan_city_sample.csv
│   ├── solar_power_generation_sample.csv
│   ├── wind_solar_energy_sample.csv
│   └── household_power_consumption_sample.csv
├── analise_dados.ipynb    # Notebook principal contendo os exercícios
└── README.md              # Documentação do repositório
```

---

## Como Executar

- Faça o download dos datasets e do python notebook.
- Abra o .ipynb no Google Colab.
- Suba os datasets no notebook aberto do Colab.
- Execute todas as células.
