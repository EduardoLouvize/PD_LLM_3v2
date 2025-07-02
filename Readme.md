# 📊 Extração e Análise de Entidades Nomeadas em Notícias da Folha UOL

**Este projeto foi desenvolvido como parte da disciplina _IA Generativa para Linguagem (Large Language Model)_ do Instituto Infnet, sob orientação do professor Fernando Guimarães Ferreira.**

Este projeto utiliza modelos de Processamento de Linguagem Natural (PLN) para extrair e analisar **organizações mencionadas nas notícias da seção "Mercado" da Folha UOL no primeiro trimestre de 2015**. Ele emprega um modelo de NER (Reconhecimento de Entidades Nomeadas) em português e gera visualizações como nuvem de palavras e gráficos de barras com os resultados.

---

## 🧠 Tecnologias e Bibliotecas Utilizadas

- Python 3
- [Transformers](https://huggingface.co/docs/transformers/)
- `kagglehub`
- `wordcloud`
- `matplotlib`
- `seaborn`
- `nltk`
- `pandas`
- `re`

---

## 📦 Instalação

Execute o seguinte comando para instalar as dependências:

```bash
pip install transformers[torch] kagglehub wordcloud matplotlib seaborn nltk
```

---

## 📥 Download do Dataset

O notebook realiza o download automático do dataset hospedado no Kaggle:

- **Fonte:** [Kaggle - Folha UOL News Dataset](https://www.kaggle.com/datasets/marlesson/news-of-the-site-folhauol)
- **Arquivo:** `articles.csv`

> ℹ️ **Nota:** É necessário autenticar com o `kagglehub` para acessar o dataset.

---

## ⚙️ Execução do Projeto

1. Filtra as notícias da seção **"Mercado"** publicadas entre **01/01/2015 e 31/03/2015**.
2. Utiliza o modelo **`monilouise/ner_pt_br`** do Hugging Face para extrair entidades nomeadas do tipo **Organização**.
3. Realiza pré-processamento nos dados:
   - Remove caracteres especiais no início das palavras
   - Descarta palavras com menos de dois caracteres
   - Remove *stopwords* da língua portuguesa
4. Gera visualizações:
   - ✅ Nuvem de Palavras
   - ✅ Gráfico de Barras com as 20 organizações mais frequentes

---

## 📈 Visualizações Geradas

- **Nuvem de Palavras**: representação visual das organizações mais citadas.
- **Gráfico de Barras**: exibe o Top 20 das organizações por número de ocorrências.

---

## 🧹 Pré-processamento

As entidades extraídas passam por uma etapa de limpeza que inclui:

- Remoção de ruídos (caracteres especiais, palavras curtas)
- Filtro de *stopwords*
- Padronização textual (ex: lowercase, remoção de espaços)

---

## 📊 Resultados

Os resultados destacam as **organizações mais frequentemente mencionadas** em notícias da editoria de economia da Folha UOL no 1º trimestre de 2015. Isso pode ser útil para:

- Análise de mídia
- Estudos sobre cobertura jornalística
- Identificação de tendências de mercado

---

## 📌 Observações

- Para utilizar o modelo da Hugging Face, recomenda-se gerar um token de autenticação em [huggingface.co/settings/tokens](https://huggingface.co/settings/tokens).
- Caso esteja utilizando o Google Colab, mensagens podem sugerir melhorias de desempenho ao utilizar processamento em batch com datasets.

---
