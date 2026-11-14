# Replicação de PDS: Filtros Passa-Baixas Baseados em Grafos (GLPF) para Imagens

Este repositório contém o código, os materiais e o relatório técnico do projeto desenvolvido para a disciplina de Processamento Digital de Sinais (PDS), focado na replicação e análise do artigo de Sonti et al. (2022)[cite: 1, 2].

---

## 📋 Sobre o Projeto

O trabalho estuda a remoção de ruídos em imagens digitais (especificamente ruído Gaussiano e ruído Sal e Pimenta) aplicando conceitos de Processamento de Sinais em Grafos (GSP)[cite: 1, 2]. O pipeline implementado abrange:
* Carregamento e normalização das imagens clássicas de referência (`Cameraman` e `Butterfly`)[cite: 2, 3, 5].
* Adição controlada de ruído Gaussiano (com variância de 0,01) e ruído Sal e Pimenta (com densidade de 5%)[cite: 2, 3].
* Construção de grafo a partir da imagem ruidosa por meio de um núcleo de afinidade bilateral e cálculo do Laplaciano combinatório $L = D - W$[cite: 2].
* Aplicação do filtro passa-baixas baseado em grafos (GLPF) no domínio do sinal de grafo e reconstrução da imagem[cite: 2].
* Implementação do filtro de Mediana para fins de comparação empírica de desempenho[cite: 2, 3].
* Avaliação quantitativa de desempenho utilizando as métricas **MSE, RMSE, PSNR e SSIM**[cite: 1, 3].

---

## 🛠️ Tecnologias e Ambiente

O projeto foi implementado em linguagem Python no ambiente do Google Colab[cite: 3, 5], utilizando as seguintes bibliotecas:
* `NumPy`[cite: 3, 5]
* `SciPy`[cite: 3, 5]
* `scikit-image`[cite: 3, 5]
* `OpenCV` (`cv2`)[cite: 3, 5]
* `Matplotlib`[cite: 3, 5]
* `Pandas`[cite: 5]

---

## 🤖 Uso de Inteligência Artificial (IA) no Desenvolvimento

Durante o desenvolvimento deste projeto, ferramentas de Inteligência Artificial foram empregadas de forma colaborativa para otimizar o fluxo de trabalho técnico e acadêmico:
* **Compreensão da Metodologia:** Utilizou-se IA para analisar o artigo original, auxiliando na compreensão de como os autores modelaram o problema de filtragem não linear por meio de grafos e Sinais em Grafos (GSP)[cite: 1, 2].
* **Depuração de Código:** A IA foi utilizada para identificar, diagnosticar e corrigir erros e exceções encontrados durante a execução do código no Google Colab (como tratamento de matrizes esparsas e tipos de dados)[cite: 4, 5].
* **Validação da Replicação:** O auxílio da IA foi empregado para verificar o grau de adequação entre a replicação executada e a especificação metodológica descrita no estudo original[cite: 3, 4].
* **Elaboração da Apresentação:** A estruturação dos tópicos e a síntese visual dos resultados para a criação dos slides de apresentação do projeto contaram com suporte de IA.
* **Escrita Científica:** A IA colaborou na adaptação, refinamento e formatação do texto técnico para o padrão LaTeX utilizado no Overleaf para a redação do relatório final[cite: 1].

---

## 📊 Principais Resultados

* O filtro de Mediana obteve melhor desempenho numérico em cenários de ruído impulsivo puro (`salt & pepper`) na imagem `Cameraman` (alcançando PSNR de 21,2792 contra 17,3791 do GLPF)[cite: 3].
* O GLPF destacou-se expressivamente na preservação de estruturas complexas na imagem `Butterfly` sob ruído Gaussiano, registrando um SSIM de 0,8544 frente a 0,6986 da Mediana[cite: 3].
