# Análise Exploratória do Prêmio de Seguro Rural (2006–2025)

Este projeto investiga a evolução do **Programa de Subvenção ao Prêmio do Seguro Rural (PSR)** no Brasil (2006–2025), com foco em:

- Retenção de segurados  
- Localidades com mais assegurados  
- Localidades em crescimento e em queda  
- Valores pagos em seguro (prêmio, subvenção, valor segurado)  
- Eventos preponderantes causadores dos sinistros  
- Análise comparativa por seguradora  

## 🎯 Objetivo

Projeto de **portfólio em Data Science**, guiado pela metodologia **CRISP-DM**, utilizando **pandas** e **geopandas**.

## 📂 Estrutura inicial

```
Seguro Rural/
├─ data/
│  ├─ raw/        # Dados originais (2006–2025)
│  ├─ interim/    # Limpezas parciais
│  └─ processed/  # Dados prontos para análise
├─ notebooks/     # Notebooks CRISP-DM (01 a 06)
├─ src/           # Funções utilitárias (data, viz, etc.)
├─ reports/       # Figuras e saídas
├─ docs/          # Documentação e dicionário de dados
```

## ⚙️ Instalação

```bash
pip install -r requirements.txt
```

## 🧭 Metodologia

O projeto segue as etapas da **CRISP-DM**:

1. **Business Understanding**  
2. **Data Understanding**  
3. **Data Preparation**  
4. **Modeling** (opcional)  
5. **Evaluation**  
6. **Deployment / Reporting**  

## 📜 Licença

[MIT](LICENSE)
