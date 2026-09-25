# Dataset: Credit Card Fraud Detection (ULB)

**Fonte:** Machine Learning Group, Université Libre de Bruxelles (ULB), em colaboração com a Worldline.
**Disponível em:** https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud

O arquivo `creditcard.csv` (cerca de 150 MB) **não está versionado neste repositório**, porque ultrapassa o limite de 100 MB por arquivo do GitHub. O notebook o baixa automaticamente via `kagglehub`. Para baixar manualmente, use o link acima (é preciso ter conta no Kaggle).

## Conteúdo

- **284.807 transações** com cartão de crédito de portadores europeus, ocorridas em **dois dias de setembro de 2013**.
- **492 fraudes** (cerca de 0,172% do total): o conjunto é fortemente desbalanceado.
- **31 colunas numéricas:**

| Coluna | Descrição |
|---|---|
| `Time` | Segundos decorridos desde a primeira transação do conjunto |
| `V1` … `V28` | Componentes principais (PCA) de atributos originais não divulgados, por confidencialidade |
| `Amount` | Valor da transação |
| `Class` | Variável-alvo: 1 = fraude, 0 = legítima |

## Anonimização e limitações

- Os atributos originais (dados do portador, do estabelecimento etc.) foram transformados por PCA pelos autores do dataset antes da publicação. O conjunto não contém dados pessoais identificáveis.
- A transformação impede interpretar semanticamente `V1`–`V28` e restringe a engenharia de atributos a `Time` e `Amount`.
- O horário real de início da coleta não é informado. Por isso, a hora derivada de `Time` é **relativa** ao início da coleta.
- O período de dois dias não permite avaliar sazonalidade de longo prazo nem a mudança de padrões de fraude ao longo do tempo (*concept drift*).

## Referência

Dal Pozzolo, A.; Caelen, O.; Johnson, R. A.; Bontempi, G. *Calibrating Probability with Undersampling for Unbalanced Classification*. IEEE Symposium Series on Computational Intelligence (SSCI), 2015.
