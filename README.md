# Case Técnico - Data Science em Crédito

## 📌 Contexto do Desafio
Este projeto simula um cenário real de concessão de crédito em um dos maiores bancos do país, que busca reduzir seus índices de inadimplência.  
O desafio consiste em desenvolver uma solução preditiva capaz de estimar, em tempo real, a probabilidade de inadimplência de contratos de crédito solicitados por clientes pessoa física.

Além do modelo, também é esperado propor **políticas de crédito** que indiquem como as previsões podem ser utilizadas para apoiar decisões de negócio, como aprovar, rejeitar ou ajustar condições de contratos.

---

## 🎯 Objetivos
1. Construir um **modelo preditivo** para estimar a probabilidade de inadimplência de contratos de crédito.  
2. Definir e justificar uma **variável target** apropriada (FPD, EVER30MOB03, OVER60MOB06, ou outra).  
3. Elaborar uma **política de crédito** baseada nas previsões, descrevendo como o banco pode utilizar os resultados do modelo.  

---

## 🗂️ Bases de Dados
As seguintes bases foram disponibilizadas para o desenvolvimento da solução:

- **base_cadastral.parquet** → Dados cadastrais dos clientes (sexo, estado civil, renda, ocupação etc.).  
- **base_submissao.parquet** → Conjunto de contratos recentes em análise, para os quais o modelo deve gerar previsões.  
- **historico_emprestimos.parquet** → Histórico de contratos anteriores por cliente, incluindo valores, status e características.  
- **historico_parcelas.parquet** → Histórico de pagamentos de cada contrato (valores previstos, pagos e datas).  
- **dicionario_dados.csv** → Dicionário com descrição completa das variáveis.

As tabelas se relacionam principalmente pelas chaves:
- `id_cliente`  
- `id_contrato`  

---

## 📦 Entregáveis
A solução completa inclui:

1. **Arquivo de submissão**:  
   - `submissao_case.csv` contendo:  
     - `id_cliente`  
     - `probabilidade_inadimplencia`  

2. **Código-fonte reprodutível**:  
   - Notebooks ou scripts organizados para permitir reprodução do fluxo do início ao fim.  
   - `requirements.txt` com as dependências.  
   - Versão da linguagem e bibliotecas principais.  

3. **Documentação da abordagem**:  
   - Definição da variável target e justificativa.  
   - Política de crédito proposta.  
   - Principais decisões metodológicas.  

---

## ✅ Critérios de Avaliação
A solução é avaliada de acordo com:

- Definição clara e justificada da **variável target**.  
- Qualidade da **política de crédito** proposta.  
- Uso eficiente das informações de clientes, contratos e pagamentos.  
- Clareza, organização e **reprodutibilidade do código**.  
- Viabilidade da solução em **cenário de produção** (tempo real).  

---

## 🛠️ Tecnologias Utilizadas
- Python 3.x  
- Bibliotecas de manipulação e análise de dados: **pandas, numpy**  
- Visualização: **matplotlib, seaborn**  
- Modelagem: **scikit-learn, cuML (GPU)**  
- Validação e métricas: **ROC AUC, cross-validation**  

---

## 🚀 Estrutura do Repositório
```

├── notebooks/              # Jupyter notebooks de exploração e modelagem
├── src/                    # Scripts Python organizados por módulos
├── data/                   # Diretório para armazenar dados (não versionados)
├── requirements.txt        # Dependências do projeto
├── README.md               # Documentação do projeto
└── submissao\_case.csv      # Arquivo de submissão final

```

---

## 🔍 Observações
- Este projeto é **apenas um estudo de caso** com fins educacionais e de demonstração de aplicação prática de Data Science.   
- Todo o código foi estruturado para ser **reprodutível** e de fácil entendimento.  
