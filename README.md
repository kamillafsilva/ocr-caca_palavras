# Solucinando Caça-Palavras com OCR

<p align="center">
  <img width="300" height="300" src="https://github.com/kamillafsilva/test-ocr/assets/43034083/8250beb1-0d0e-401d-8f43-4362208fff6e">
</p>

## Overview
Neste projeto pus em prática os conteúdos aprendido no curso de [Reconhecimento de texto com OCR e OpenCV](https://cursos.alura.com.br/formacao-visao-computacional-opencv) para solucionar jogos de caça-palavras. O projeto foi desenvolvido em Python utilizando os pacotes `cv2` e `pytesseract` para tratar e extrair caracteres de caça-palavras gerados no site [Geniol](https://www.geniol.com.br/palavras/caca-palavras/criador/).

## Implementação
A primeira etapa da solução implementada consistiu em extrair todos os caracteres da imagem de entrada um a um. Para melhor detecção desses caracteres foram aplicadas diversas técnicas de pré-processamento de imagem disponíveis no pacote `cv2`. Após a detecção dos caracteres, o texto da imagem foi extraído usando o `pytesseract`. As coordenadas desses caracteres também foram extraídas e salvas para serem utilizadas posteriormente na marcação das palavras encontradas na imagem de entrada (pacote `imutils`).

Todo texto extraído foi salvo em forma de uma matriz com as mesmas dimensões do caça-palavras de entrada. Com isso, foi possível buscar as palavras da solução do jogo percorrendo essa matriz horizontalmente, verticalmente e nas diagonais. Os índices associados a cada palavra foram usados para marcar no caça-palavras os locais onde elas se encontravam, completando a solução do jogo.

## Utilização
O projeto foi desenvolvido na plataforma [Colab](https://colab.research.google.com/) do Google, devido a praticidade na instalação dos pacotes. O notebook do projeto pode ser baixado do repositório do Github e importado para o Colab para execução dos códigos.
