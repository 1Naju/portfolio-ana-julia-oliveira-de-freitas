# 🔄 Vibe Coding — Engenharia Reversa com IA

## 📝 Descrição do Projeto

Este projeto explora o conceito de **engenharia reversa assistida por IA**: reconstruir um webapp funcional a partir da observação de sua interface externa, sem visualizar o código-fonte original. Toda a construção foi feita via **Google AI Studio**, configurando o Gemini como desenvolvedor Full-Stack por meio de System Instructions.

Desenvolvido como parte da disciplina de **Engenharia de Prompt e Aplicações em IA**, o projeto transfere o esforço da escrita sintática para a descrição lógica e funcional.

🔗 **Acesse o projeto:** [AI Studio](https://ai.studio/apps/34baefa2-9529-433b-916b-8254692283bc)

---

## 🛠️ Tecnologias Utilizadas

* **Plataforma:** Google AI Studio
* **Modelo:** Gemini
* **Metodologia:** System Instructions + engenharia reversa visual
* **Saída:** HTML + CSS + JavaScript (Single Page)

---

## 🧩 Desafio Técnico

O principal desafio foi **descrever comportamentos visuais e interativos em linguagem natural** com precisão suficiente para que a IA gerasse código funcional sem ver o original.

### Dificuldades encontradas e como foram superadas

| Desafio | Descrição | Solução |
| :--- | :--- | :--- |
| **Ambiguidade visual** | Elementos da UI eram difíceis de descrever sem termos técnicos de CSS | Uso de analogias e referências visuais nas System Instructions |
| **Comportamento dinâmico** | Interações e estados da interface não eram óbvios só pela observação | Mapeamento cuidadoso de cada estado antes de descrever à IA |
| **Erros de geração** | A IA gerou código funcional mas com bugs visuais | Ciclo de validação → diagnóstico → ajuste iterativo do prompt |
| **Fidelidade ao original** | Reproduzir layout sem ver o CSS original | Descrição detalhada de proporções, cores e hierarquia visual |

### System Instructions utilizadas

As instruções configuraram o Gemini para atuar como desenvolvedor Full-Stack com as seguintes diretrizes:
- Gerar código em HTML + CSS + JavaScript em arquivo único (Single Page)
- Priorizar fidelidade visual ao webapp de referência
- Comentar o código gerado para facilitar revisão humana
- Validar acessibilidade e responsividade básica

---

## 🔧 Como foi executado

1. Acesso e exploração do webapp de referência para mapear componentes e lógicas
2. Configuração das System Instructions no Google AI Studio
3. Geração do código e validação no ambiente de teste
4. Ajuste iterativo até o comportamento corresponder à referência

---

## 📊 Resultados e Aprendizados

* Com a IA escrevendo código, o desenvolvedor precisa saber **descrever o problema** e **validar o que foi gerado**
* **Leitura crítica de código:** a IA erra, e quem não entende o que foi gerado coloca problemas em produção
* **Clareza na comunicação:** quanto melhor se descreve o que se quer, melhor a IA entrega
* A engenharia reversa vira plágio quando o objetivo deixa de ser aprender e passa a ser lucrar com o trabalho alheio sem dar crédito

---

## 📎 Arquivos do Projeto

| Arquivo | Descrição |
| :--- | :--- |
| [analise-critica.md](./analise-critica.md) | Reflexão sobre Vibe Coding e originalidade na era da IA |

---

[Voltar ao início](https://github.com/1Naju/portfolio-ana-julia-oliveira-de-freitas)
