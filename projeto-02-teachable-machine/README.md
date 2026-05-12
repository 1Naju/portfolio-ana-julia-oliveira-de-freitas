# 🧠 Viés em IA — Teachable Machine

## 📝 Descrição do Projeto
Este projeto explora como a seleção restrita e enviesada de dados de treinamento corrompe a lógica de um algoritmo de classificação visual. Utilizando o **Teachable Machine (Google)**, o modelo foi treinado deliberadamente com estereótipos para demonstrar, na prática, como o viés nos dados gera classificações injustas e seus impactos sociais.

Desenvolvido como parte da disciplina de **Engenharia de Prompt e Aplicações em IA**, o projeto é composto por dois momentos: o experimento técnico com o Teachable Machine e uma análise ética escrita sobre os impactos do modelo enviesado.

## 🚀 Tecnologias Utilizadas
* **Plataforma:** Teachable Machine — Google
* **Tipo de modelo:** Classificação de imagem
* **Dispositivo de coleta:** Câmera/celular

## 📊 Resultados e Aprendizados
* Quando selecionamos os dados de forma restrita, corrompemos a lógica do algoritmo porque o modelo aprende apenas os padrões presentes no conjunto de treinamento, sem qualquer capacidade de generalização.
* Decisões algorítmicas enviesadas podem barrar promoções, restringir acessos e perpetuar desigualdades estruturais, legitimando preconceitos sob o manto de objetividade técnica.
* É recomendada a implementação de um protocolo de revisão humana antes de qualquer treinamento ou atualização do modelo.

## 🔧 Como foi executado
1. Definição das duas classes: "mãos femininas" e "mãos masculinas".
2. Captura de 20 imagens para cada classe utilizando critérios estereotipados.
3. Teste de inferência com uma imagem que não se encaixava nos padrões treinados.
4. Registro do erro (print) e redação da análise ética.

---
[Voltar ao início](https://github.com/1Naju/Portif-lio)
