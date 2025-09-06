# RAG Workflow com Avaliação de Respostas e Roteamento Inteligente

![Python](https://img.shields.io/badge/Python-Linguagem-3776AB?style=flat-square&logo=python)
![LangChain](https://img.shields.io/badge/LangChain-RAG-3DDC84?style=flat-square&logo=langchain)
![NVIDIA](https://img.shields.io/badge/NVIDIA-Embeddings-76B900?style=flat-square&logo=nvidia)
![Tavily](https://img.shields.io/badge/Tavily-WebSearch-FF6600?style=flat-square)

## Descrição

Este projeto implementa um workflow de **Retrieval-Augmented Generation (RAG)** usando um grafo de estados (`StateGraph`) com roteamento inteligente de consultas. O sistema consegue decidir se uma pergunta deve ser respondida a partir de uma base vetorial ou realizada uma busca na web. Além disso, avalia a relevância dos documentos e verifica se a resposta do modelo está baseada nos fatos e responde corretamente à pergunta.

## Funcionalidades

- Recuperação de documentos relevantes de uma base vetorial (vectorstore)
- Geração de respostas usando RAG (modelos LLM NVIDIA)
- Avaliação de relevância dos documentos recuperados
- Detecção de alucinações e validação de respostas
- Roteamento de consultas entre vectorstore e web search (Tavily)
- Execução do workflow com streaming de eventos
- Visualização do grafo de estados usando Mermaid
