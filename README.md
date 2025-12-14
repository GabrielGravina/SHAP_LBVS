# SHAP_LBVS

Projeto de análise XAI (Explainable AI) aplicado a Ligand-Based Virtual Screening usando SHAP values para interpretabilidade de modelos de machine learning.

## Requisitos

- Conda ou Mamba
- Python 3.8

## Instalação

1. Clone o repositório:
```bash
git clone https://github.com/GabrielGravina/SHAP_LBVS.git
cd SHAP_LBVS
```

2. Crie o ambiente conda com todas as dependências:
```bash
conda env create -f environment.yml
```

3. Ative o ambiente:
```bash
conda activate chem_native
```

## Uso

Execute o notebook principal:
```bash
jupyter notebook SOS1_AllAlgo.ipynb
```

Ou use VS Code com a extensão Jupyter para abrir e executar o notebook diretamente.

## Estrutura do Projeto

```
.
├── SOS1_AllAlgo.ipynb    # Notebook principal com todas as análises
├── dataset/              # Dados de entrada
│   └── all_structures.csv
├── images/               # Gráficos e visualizações gerados
├── environment.yml       # Dependências do ambiente conda
└── README.md            # Este arquivo
```

## Modelos Implementados

O projeto compara três algoritmos de machine learning:

- Random Forest Regressor
- Decision Tree Regressor
- LightGBM Regressor

Para cada modelo são realizadas:
- Otimização de hiperparâmetros
- Avaliação de performance (R², RMSE, MAE)
- Análise SHAP para interpretabilidade
- Visualizações de importância de features

## Dataset

O dataset contém estruturas moleculares com:
- ChEMBL ID
- SMILES (estrutura molecular)
- Valores de pChEMBL (atividade biológica)

Descritores moleculares são calculados automaticamente usando RDKit.

## Resultados

Os resultados incluem:
- Métricas de performance comparativas
- SHAP beeswarm plots
- SHAP bar plots
- Heatmaps de correlação de features
- Gráficos de resíduos
- Análise de normalidade

Todas as visualizações são salvas na pasta `images/`.
