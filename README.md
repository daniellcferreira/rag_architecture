# RAG ARCHITECTURE

![Python](https://img.shields.io/badge/Python-Linguagem-3776AB?style=flat-square&logo=python)
![Groq](https://img.shields.io/badge/Groq-LLM-5C2D91?style=flat-square&logo=groq)
![LangChain](https://img.shields.io/badge/LangChain-RAG-3DDC84?style=flat-square&logo=langchain)
![NVIDIA](https://img.shields.io/badge/NVIDIA-Embeddings-76B900?style=flat-square&logo=nvidia)
![Tavily](https://img.shields.io/badge/Tavily-WebSearch-FF6600?style=flat-square)
![Wikipedia](https://img.shields.io/badge/Wikipedia-API-000000?style=flat-square&logo=wikipedia)
![SentenceTransformers](https://img.shields.io/badge/SentenceTransformers-Embeddings-FF6F61?style=flat-square&logo=transformers)
![NumPy](https://img.shields.io/badge/NumPy-Array-F7DF1E?style=flat-square&logo=numpy)
![Requests](https://img.shields.io/badge/Requests-HTTP-FF6F61?style=flat-square&logo=python)
![Textwrap](https://img.shields.io/badge/Textwrap-Formatting-4B8BBE?style=flat-square&logo=python)

## Descrição
Este projeto demonstra duas implementações de **RAG (Retrieval-Augmented Generation)** utilizando Python e modelos LLM da **Groq Cloud**, integrando conteúdos da Wikipedia para responder perguntas de forma precisa e contextualizada.  

O RAG permite que o modelo utilize textos externos como referência, evitando respostas inventadas e aumentando a confiabilidade das respostas geradas.  

O projeto está dividido em duas abordagens: uma mais simples e outra avançada, com workflows complexos em grafo.

---

## Funcionalidades

### RAG Simples
- Recupera textos de páginas da Wikipedia usando a API oficial.
- Divide os textos em parágrafos para criar "chunks" de contexto.
- Gera embeddings semânticos de cada parágrafo com SentenceTransformers.
- Gera embeddings semânticos da pergunta do usuário.
- Calcula similaridade entre a pergunta e os parágrafos da Wikipedia.
- Seleciona os parágrafos mais relevantes com base na similaridade.
- Formata os textos para exibição legível.
- Cria contexto concatenado para envio ao modelo LLM.
- Envia prompt ao modelo Groq instruindo-o a responder baseado no contexto.
- Retorna respostas precisas ou informa caso a resposta não esteja disponível.
- Permite testar rapidamente o RAG sem configuração complexa.
- Excelente para prototipagem e aprendizado sobre RAG.
- Suporta múltiplas perguntas sequenciais com reuso do modelo de embeddings.
- Permite análise da relevância dos parágrafos pelo score de similaridade.
- Pode ser usado como base para outros projetos de NLP contextualizados.

### RAG Avançada
- Implementa workflow em grafo usando `StateGraph` e `GraphState`.
- Permite múltiplos nós de processamento: busca web, recuperação, avaliação e geração.
- Define nós condicionais com regras de transição de estados.
- Avalia a utilidade dos documentos recuperados antes de gerar respostas.
- Adiciona lógica de retry para perguntas que não possuem respostas úteis.
- Suporta múltiplos caminhos de execução dependendo do fluxo.
- Gera respostas baseadas em contexto de documentos e resultados de avaliação.
- Permite integração com fontes externas além da Wikipedia.
- Possibilita controlar a estratégia de resposta de forma mais refinada.
- Ideal para casos de uso empresarial e aplicações complexas de RAG.
- Permite monitoramento de cada etapa do fluxo de perguntas e respostas.
- Suporta limites máximos de tentativas e decisões automáticas de fallback.
- Facilita depuração e análise do desempenho do modelo em cada nó.
- Pode ser estendido para workflows híbridos combinando múltiplos LLMs.
- Garante maior robustez e confiabilidade na geração de respostas.
- Ideal para aplicações que exigem resposta contextual sofisticada.
- Possui visualização gráfica do workflow usando Mermaid.
- Integração nativa com embeddings e modelos LLM da Groq.
- Permite comparar diferentes estratégias de recuperação e geração.
