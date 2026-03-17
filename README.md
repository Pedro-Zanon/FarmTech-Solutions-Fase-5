# FarmTech Solutions — Fase 5: Machine Learning

Projeto desenvolvido para a **FarmTech Solutions**, empresa de IA prestando serviços para uma fazenda de 200 hectares. O objetivo é analisar dados de condições climáticas e de solo para prever o rendimento de safra utilizando Machine Learning, além de avaliar o custo de hospedagem na nuvem AWS.

---

## Entregas

### Entrega 1 — Machine Learning
📓 [Notebook Jupyter](./notebook/PEDROZANONCASTROSANTANA_rm567350_pbl_fase4.ipynb)  
🎥 Vídeo ML: *(adicionar link do YouTube)*

O notebook contém o pipeline completo de Machine Learning:
- Análise Exploratória dos dados (EDA)
- Clusterização com K-Means para identificar tendências e outliers
- Treinamento e comparação de 5 modelos preditivos de regressão
- Avaliação com métricas RMSE, MAE e R²
- Exportação dos modelos treinados

### Entrega 2 — Computação em Nuvem (AWS)
📸 [Prints São Paulo](./aws/prints_sao_paulo/)  
📸 [Prints Virgínia](./aws/prints_virginia/)  
🎥 Vídeo AWS: *(adicionar link do YouTube)*

---

## Comparação de Custos AWS

Estimativa On-Demand para uma máquina Linux com **2 CPUs, 1 GiB RAM, até 5 Gbps de rede e 50 GB de armazenamento**, usada para hospedar a API com o modelo de Machine Learning.

| Região | Instância | Custo mensal (On-Demand) |
|--------|-----------|--------------------------|
| São Paulo — `sa-east-1` | *(preencher instância)* | *(preencher valor)* |
| Virgínia do Norte — `us-east-1` | *(preencher instância)* | *(preencher valor)* |

> 📸 Prints detalhados das cotações disponíveis em [`aws/prints_sao_paulo/`](./aws/prints_sao_paulo/) e [`aws/prints_virginia/`](./aws/prints_virginia/)

### Justificativa Técnica

Apesar de São Paulo apresentar custo mais elevado, ela é a escolha mais adequada por dois motivos:

**LGPD — Lei Geral de Proteção de Dados:** os dados coletados pelos sensores da fazenda são dados brasileiros. A legislação pode restringir o armazenamento e processamento desses dados fora do território nacional, tornando o uso da região `sa-east-1` mais seguro do ponto de vista legal.

**Latência:** os sensores estão localizados no Brasil. Hospedar a API em São Paulo reduz significativamente o tempo de resposta em comparação com Virgínia do Norte, que fica a aproximadamente 7.000 km de distância. Menor latência significa respostas mais rápidas e maior confiabilidade no envio dos dados dos sensores.

---

## Como Executar

```bash
# Instalar dependências
pip install -r requirements.txt

# Abrir o notebook
jupyter notebook notebook/PEDROZANONCASTROSANTANA_rm567350_pbl_fase4.ipynb
```

---

## Estrutura do Repositório

```
fase5-ml/
├── data/
│   └── crop_yield.csv          # Dataset com dados das plantações
├── notebook/
│   └── PEDROZANONCASTROSANTANA_rm567350_pbl_fase4.ipynb
│   └── models/                     # Modelos treinados exportados (.pkl)
├── assets/                     # Imagens usadas no README
├── aws/
│   ├── prints_sao_paulo/       # Screenshots da cotação São Paulo
│   └── prints_virginia/        # Screenshots da cotação Virgínia
├── .env.example                # Modelo de variáveis de ambiente
├── .gitignore
├── requirements.txt
└── README.md
```

---

**Aluno:** Pedro Zanoncastro Santana — RM 567350
