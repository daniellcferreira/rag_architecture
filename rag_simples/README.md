# RAG Simples

![Python](https://img.shields.io/badge/Python-Linguagem-3776AB?style=flat-square&logo=python&logoColor=white)
![Groq](https://img.shields.io/badge/Groq-LLM-4A90E2?style=flat-square&logo=groq)
![Sentence-Transformers](https://img.shields.io/badge/Sentence%20Transformers-Embeddings-FF6F61?style=flat-square)
![Wikipedia API](https://img.shields.io/badge/Wikipedia%20API-Retrieval-000000?style=flat-square)

## Descrição

Este notebook apresenta um **exemplo simples de arquitetura RAG (Retrieval-Augmented Generation)** usando Python.  
O fluxo consiste em: buscar conteúdo na Wikipedia, gerar embeddings com **Sentence-Transformers**, recuperar os trechos mais relevantes e gerar uma resposta usando um modelo LLM hospedado na **Groq**.

## Funcionalidades

- Buscar páginas da Wikipedia em português.  
- Dividir o conteúdo em parágrafos (chunks).  
- Gerar embeddings semânticos de cada parágrafo.  
- Calcular similaridade semântica entre a pergunta e os parágrafos.  
- Recuperar os 3 parágrafos mais relevantes.  
- Enviar o contexto + pergunta para o Groq LLM gerar a resposta.  
