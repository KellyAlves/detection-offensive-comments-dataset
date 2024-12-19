# detection-offensive-comments-dataset
# Este repositório contém o dataset gerado a partir de comentários extraídos da rede social Youtube.

A coleta dos dados foi realizada por meio da API YouTube Data, com o objetivo de construir um conjunto representativo de comentários em língua portuguesa, oriundos de vídeos do YouTube Brasil. Foram selecionados cinco vídeos de diferentes temas, escolhidos pela sua grande repercussão e pelo fato de serem amplamente conhecidos e polêmicos. Justamente por serem vídeos de alta visibilidade, eles atraem um grande volume de comentários, incluindo um número expressivo de comentários negativos e ofensivos, o que enriquece a análise. De cada vídeo, foram extraídos 1000 comentários, totalizando 5000 mil comentários. Para garantir a qualidade e a relevância dos dados textuais, uma série de etapas de pré-processamento foram executadas, visando reduzir o ruído e preservar a estrutura linguística dos comentários:

Remoção de caracteres especiais: eliminando emojis, links e símbolos para focar no conteúdo textual.
Filtragem de onomatopeias: expressões como ‘kkkk’, ‘haha’, e ‘ksks’ foram removidas.
Exclusão de nomes próprios: com o intuito de evitar vieses que poderiam afetar o modelo.
Filtragem de idioma: apenas os comentários em português brasileiro foram mantidos.
Eliminação de texto não inteligível: exemplos como ‘hdjk’ foram descartados.
Conversão para minúsculas: padronizando o texto para melhorar a consistência dos dados.

Os critérios de rotulação incluem:
Linguagem inapropriada
Discurso de ódio
Ameaças
Assédio ou bullying
Conteúdo discriminatório
Desrespeito
Incitação à violência
Intenções maliciosas
Expressão excessivamente negativa

Os comentários foram rotulados manualmente, com base em uma série de critérios que representam comportamentos ofensivos e inadequados. A cada comentário, foi atribuída uma classe binária, onde 1 indica comentário ofensivo e 0 indica comentário não ofensivo.

Após o pré-processamento, o conjunto de dados passou a ser composto por 4139 documentos, dos quais 2683 (cerca de 64,82%) foram classificados como não ofensivos e 1456 (aproximadamente 35,18%) como ofensivos. Esse desbalanceamento é um aspecto relevante para a modelagem, pois demanda técnicas de ajuste para evitar viés em favor da classe majoritária (não ofensivo). A análise exploratória indicou um total de 48495 palavras no conjunto, com uma média de 12 palavras por documento.

