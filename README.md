# Análise de Dataset de Voos

Análise exploratória de um dataset sintético de voos, com tratamento de dados, criação de variáveis derivadas e análise de correlação entre atrasos.

**Curso:** IA Industrial - SENAI EAD

## Dataset

- **Arquivo:** `Dataset_sint_tico_de_voos.csv`
- **Registros:** 100 voos
- **Colunas originais:** fl_date, op_unique_carrier, tail_num, origin, dest, crs_dep_time, dep_delay, arr_delay, distance

## Etapas da Análise

1. **Carregamento e inspeção** dos dados (shape, head, tail, info)
2. **Tratamento de valores ausentes**: preenchimento de `dep_delay` e `arr_delay` (10% de nulos cada) com a mediana
3. **Limpeza de colunas categóricas**: remoção de espaços em branco
4. **Conversão de tipos**: `fl_date` convertida para datetime
5. **Criação de variáveis derivadas**:
   - `Atraso_superior_15min`: indica se o atraso na chegada foi maior que 15 minutos
   - `Mes` e `Dia_da_Semana`: extraídos da data do voo
   - `Atraso_absoluto`: valor absoluto do atraso na chegada
6. **Visualizações**:
   - Histograma e boxplot da distribuição de atrasos na chegada
   - Gráfico de barras com os aeroportos de origem com maior média de atraso na partida
   - Mapa de calor de correlação entre variáveis numéricas

## Principais Resultados

**Aeroportos com maior atraso médio na partida:**
| Aeroporto | Atraso médio (min) |
|---|---|
| BSB | 19.2 |
| GIG | 17.1 |
| GRU | 16.3 |
| LAX | 12.6 |

**Correlação entre variáveis:**
- `arr_delay` e `Atraso_superior_15min` apresentam forte correlação (0.80)
- `Atraso_absoluto` tem correlação moderada com `Atraso_superior_15min` (0.45)
- `distance`, `Mes` e `Dia_da_Semana` mostram correlação fraca com os atrasos

## Ferramentas Utilizadas

- Python (Pandas, NumPy, Seaborn, Matplotlib)
- Jupyter Notebook (VS Code)


## Contexto Acadêmico

Atividade desenvolvida como parte do curso **IA Industrial - SENAI EAD**.
