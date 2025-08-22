#O Art Seeker é um sistema de busca semântica inteligente que permite encontrar obras de arte a partir de descrições em linguagem natural.

##  Objetivo do Projeto

O Art Seeker é uma Inteligência Artificial projetada para realizar buscas semânticas em obras de arte.
Em vez de depender apenas de palavras exatas, o sistema entende descrições em linguagem natural (ex.: “pinturas renascentistas com anjos e temas religiosos”) e retorna obras que melhor correspondem ao contexto.
O objetivo não é apenas localizar títulos específicos, mas permitir exploração inteligente de acervos artísticos, reconhecendo estilos, períodos históricos, artistas e características descritivas.

## Lógica e Algoritmos

  - O projeto combina técnicas modernas de Processamento de Linguagem Natural (PLN) com busca vetorial:
      .Pré-processamento dos dados: leitura do JSON contendo as obras; Criação de uma descrição unificada para cada obra (título, artista, data, estilo).

  - Geração de Embeddings: uso do modelo intfloat/multilingual-e5-large para transformar textos em vetores numéricos;Normalização dos vetores para permitir cálculos de similaridade por cosseno.

  - Indexação FAISS: os embeddings são armazenados em um índice FAISS para buscas rápidas e escaláveis
  
  - Re-ranking com CrossEncoder: após a busca inicial, os resultados são refinados com cross-encoder/ms-marco-MiniLM-L-6-v2, que faz uma análise mais detalhada da relação entre a consulta e cada obra candidata.

## Como Executar
Clique no botão "Open in Colab" no topo deste notebook.
No ambiente do Colab, execute todas as células em ordem (Ambiente de execução -> Executar tudo).
O resultado final, com a tabela de probabilidades e o gráfico, será exibido ao final da execução.
