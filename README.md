# MLOps Pipeline

**Autor:** Marcos Veronez

Projeto desenvolvido como parte dos estudos de MLOps, com foco na organização, modularização e execução de um pipeline de Machine Learning.

A proposta é estruturar as diferentes etapas do fluxo de aprendizado de máquina em módulos independentes, facilitando a manutenção, reutilização e evolução do código.

## 📁 Organização do projeto

```text
mlops-pipeline/
│
├── data/
│   └── raw/
│       └── points.csv
│
├── src/
│   ├── data.py
│   ├── train.py
│   ├── evaluate.py
│   └── predict.py
│
├── outputs/
│   └── metrics.json
│
├── generate_data.py
├── main.py
└── requirements.txt
```

### Componentes principais

| Arquivo / Diretório | Responsabilidade |
|---|---|
| `data/` | Armazenamento dos dados utilizados pelo pipeline. |
| `src/data.py` | Leitura, tratamento e preparação dos dados. |
| `src/train.py` | Implementação do treinamento do modelo. |
| `src/evaluate.py` | Avaliação do desempenho do modelo. |
| `src/predict.py` | Geração de previsões a partir do modelo treinado. |
| `outputs/` | Armazenamento dos resultados gerados. |
| `generate_data.py` | Criação da base de dados utilizada no projeto. |
| `main.py` | Orquestração e execução do pipeline. |
| `requirements.txt` | Relação das dependências necessárias. |

## ⚙️ Instalação e configuração

Clone o repositório e acesse o diretório do projeto.

Instale as dependências necessárias:

```bash
pip install -r requirements.txt
```

## ▶️ Execução

O pipeline deve ser executado seguindo a sequência abaixo.

**1. Preparação dos dados**

Gere a base de dados de entrada:

```bash
python generate_data.py
```

O arquivo `points.csv` será criado em `data/raw/`.

**2. Implementação dos módulos**

Implemente as funcionalidades de processamento, treinamento, avaliação e predição nos respectivos arquivos do diretório `src/`, conforme as especificações do exercício.

**3. Execução do pipeline**

Inicie o fluxo completo através do arquivo principal:

```bash
python main.py
```

Os resultados da execução serão disponibilizados no diretório `outputs/`, incluindo as métricas de avaliação em formato JSON.

## 🔗 Publicação no GitHub

Para disponibilizar o projeto, inicialize o repositório Git e configure o endereço remoto.

**Opção A — HTTPS**

```bash
git init
git add .
git commit -m "Initial project structure"
git branch -M main
git remote add origin https://github.com/marcosavdl/mlops-pipeline.git
git push -u origin main
```

**Opção B — SSH**

```bash
git init
git add .
git commit -m "Initial project structure"
git branch -M main
git remote add origin git@github.com:marcosavdl/mlops-pipeline.git
git push -u origin main
```

Substitua `marcosavdl` pelo nome da sua conta no GitHub.

> **Importante:** mantenha o repositório com visibilidade pública (*Public*), pois a correção automatizada do exercício depende do acesso público ao código.

---

## 🎯 Objetivo de aprendizagem

Este projeto busca consolidar conceitos fundamentais de MLOps, especialmente:

- Modularização de aplicações de Machine Learning.
- Separação de responsabilidades entre componentes.
- Organização de estruturas de projetos Python.
- Automatização da execução de pipelines.
- Registro e armazenamento de métricas de avaliação.
- Versionamento e publicação de código utilizando Git e GitHub.