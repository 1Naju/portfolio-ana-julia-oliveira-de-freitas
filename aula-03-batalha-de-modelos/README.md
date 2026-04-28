# ⚔️ Batalha de Modelos & Engenharia de Prompt (XML)

## 📝 Descrição do Projeto
Este projeto consiste na construção de um **Prompt Estruturado em XML** para geração de uma página HTML Single Page com CSS integrado, testado simultaneamente em 7 LLMs diferentes: ChatGPT, Gemini, DeepSeek, Qwen, Grok, Maritaca e Claude.

O objetivo foi avaliar a fidelidade de cada modelo às instruções do prompt XML, comparar o consumo de tokens e identificar qual ferramenta performa melhor para cada tipo de tarefa.

Desenvolvido como parte da disciplina de **Engenharia de Prompt e Aplicações em IA**, em trio com Ana Julia Oliveira de Freitas, Cauan Lima de Souza Silva e Victoria Lohany Almeida dos Santos.

## 🚀 Tecnologias Utilizadas
* **Linguagem do prompt:** XML estruturado
* **Saída esperada:** HTML5 + CSS3 (Single Page)
* **LLMs testados:** ChatGPT · Gemini · DeepSeek · Qwen · Grok · Maritaca · Claude

## 📊 Resultados e Aprendizados

| Critério | Melhor | Pior |
| :--- | :--- | :--- |
| Precisão ao prompt XML | Claude | Qwen |
| Precisão do HTML | Claude | Gemini |
| Criatividade | Claude | Maritaca |
| Tokens gerados | Maritaca (~950) | Claude (~5.200) |

* Claude superou as expectativas em precisão e criatividade, porém com maior consumo de tokens.
* Houve variação significativa de ~950 a ~5.200 tokens para o mesmo prompt entre os modelos.
* Para prototipagem rápida, modelos mais enxutos são mais eficientes; para código complexo, Claude se destacou.

## 🔧 Como foi executado
1. Construção do prompt XML com tema, paleta de cores e obrigatoriedades técnicas.
2. Envio do mesmo prompt para os 7 LLMs via celular.
3. Avaliação por fidelidade ao XML, não por estética.
4. Preenchimento do quadro comparativo e redação da reflexão crítica.

---
[Voltar ao início](https://github.com/1Naju/Portif-lio)
