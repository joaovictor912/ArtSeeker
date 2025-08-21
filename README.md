#O Art Seeker é um sistema de busca semântica inteligente que permite encontrar obras de arte a partir de descrições em linguagem natural.
Utilizando embeddings de linguagem e similaridade de cossenos, o modelo entende o significado do texto da consulta e retorna as obras mais relevantes de acordo com seu conteúdo descritivo.

#A base de dados utilizada é a API pública do Art Institute of Chicago, contendo milhares de obras catalogadas.

#Tecnologias utilizadas:
Python 
Sentence Transformers (modelo paraphrase-multilingual-mpnet-base-v2) para geração de embeddings
FAISS (Facebook AI Similarity Search) para indexação vetorial e busca eficiente
Requests para coleta de dados da API
Cache local para otimizar requisições e reduzir latência

#Como funciona
Coleta dos dados: informações sobre obras de arte são obtidas via API do Art Institute of Chicago.
Geração dos embeddings: os textos descritivos das obras são convertidos em vetores numéricos usando Sentence Transformers.
Indexação no FAISS: os embeddings são armazenados em um índice vetorial otimizado para busca por similaridade.
Consulta semântica: o usuário digita uma descrição em linguagem natural (ex.: “pintura impressionista com paisagem noturna”).
Busca por similaridade de cossenos: o sistema compara o embedding da consulta com os embeddings das obras e retorna as mais relevantes.
