# Detection Offensive Comments Dataset

Este repositório contém o **dataset gerado a partir de comentários extraídos da rede social YouTube**.

## Descrição do Dataset

A coleta dos dados foi realizada por meio da **API YouTube Data**, com o objetivo de construir um conjunto representativo de comentários em língua portuguesa, oriundos de vídeos do YouTube Brasil. Foram selecionados **cinco vídeos de diferentes temas**, escolhidos pela sua grande repercussão e pelo fato de serem amplamente conhecidos e polêmicos.

### Características da Coleta

- **Número total de comentários**: 5000  
  - **1000 comentários por vídeo**
- **Critérios de seleção**: Vídeos de alta visibilidade que atraem um grande volume de comentários, incluindo um número expressivo de comentários negativos e ofensivos.

## Pré-processamento dos Dados

Para garantir a qualidade e relevância dos dados textuais, foram aplicadas as seguintes etapas de pré-processamento:

1. **Remoção de caracteres especiais**:  
   Emojis, links e símbolos foram removidos para focar no conteúdo textual.

2. **Filtragem de onomatopeias**:  
   Expressões como `kkkk`, `haha` e `ksks` foram removidas.

3. **Exclusão de nomes próprios**:  
   Evita vieses que poderiam afetar o modelo.

4. **Filtragem de idioma**:  
   Apenas comentários em português brasileiro foram mantidos.

5. **Eliminação de texto não inteligível**:  
   Exemplos como `hdjk` foram descartados.

6. **Conversão para minúsculas**:  
   Padronização para melhorar a consistência dos dados.

## Critérios de Rotulação

Os comentários foram rotulados manualmente com base nos seguintes critérios:

- Linguagem inapropriada  
- Discurso de ódio  
- Ameaças  
- Assédio ou bullying  
- Conteúdo discriminatório  
- Desrespeito  
- Incitação à violência  
- Intenções maliciosas  
- Expressão excessivamente negativa  

### Classes

- **1**: Comentário ofensivo  
- **0**: Comentário não ofensivo  

## Estatísticas do Dataset

Após o pré-processamento, o dataset ficou composto da seguinte forma:

- **Total de documentos**: 4139  
  - **Comentários não ofensivos**: 2683 (64,82%)  
  - **Comentários ofensivos**: 1456 (35,18%)  

### Observações

- O desbalanceamento entre as classes demanda técnicas de ajuste para evitar viés em favor da classe majoritária (não ofensivo).  
- **Total de palavras**: 48495  
- **Média de palavras por documento**: 12  

