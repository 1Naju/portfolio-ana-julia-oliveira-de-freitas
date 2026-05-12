# 🎮 Jogo dos 5 Prompts — Refinamento Iterativo

## 📝 Descrição do Projeto

Este projeto consiste em um desafio de refinamento iterativo de prompts com limite de apenas 5 tentativas para atingir um resultado específico definido pelo professor. O objetivo é desenvolver a capacidade de avaliar criticamente a resposta de uma IA e melhorar o prompt seguinte com base no erro identificado, sem desperdiçar iterações.

Desenvolvido como parte da disciplina de **Engenharia de Prompt e Aplicações em IA**, a atividade foi realizada em trio e explorou dois tipos de saída: **texto** (e-mail formal de um pirata para um rei) e **imagem** (astronauta estilo barroco tocando violoncelo em Marte).

---

## 🛠️ Tecnologias Utilizadas

* **Ferramentas de IA:** ChatGPT (geração de texto e imagem)
* **Dispositivo:** Celular
* **Metodologia:** Prompt iterativo com avaliação crítica a cada rodada

---

## 🔁 Como a Iteração Melhorou a Precisão

O refinamento iterativo demonstrou que pequenas mudanças no prompt geram grandes diferenças no resultado. A cada tentativa, o trio identificava o erro principal da resposta anterior e ajustava apenas o elemento mais crítico — evitando reescrever o prompt inteiro e perdendo o que já estava funcionando.

### Padrão de Evolução Observado

| Iteração | Problema Identificado | Ajuste Aplicado | Impacto |
| :--- | :--- | :--- | :--- |
| Prompt 1 | Resposta genérica, sem personalidade | Adicionado contexto de personagem (pirata) | Tom mudou completamente |
| Prompt 2 | Linguagem informal demais | Especificado "e-mail formal" e "destinatário rei" | Estrutura melhorou |
| Prompt 3 | Faltava vocabulário da época | Adicionado "linguagem do século XVII" | Autenticidade aumentou |
| Prompt 4 | Extensão inadequada | Especificado número de parágrafos | Resultado mais preciso |
| Prompt 5 | Ajuste fino de detalhes | Refinamento de tom e assinatura | Resultado final aprovado |

### Principais Aprendizados Técnicos

* **Especificidade progressiva:** começar amplo e afunilar a cada iteração é mais eficiente do que tentar acertar tudo no primeiro prompt.
* **Diagnóstico antes do reenvio:** identificar *qual* elemento está errado antes de reescrever o prompt evita perder o que já estava funcionando.
* **Contexto cumulativo:** adicionar camadas de contexto (personagem + destinatário + época + formato) aumenta exponencialmente a precisão da IA.
* **Limite como disciplina:** o teto de 5 tentativas força o pensamento estratégico ao invés de tentativa e erro aleatório.

---

## 🧠 Técnicas de Prompt Engineering Aplicadas

### Few-Shot Prompting

O **Few-Shot Prompting** foi aplicado ao fornecer exemplos do estilo esperado diretamente no prompt. Em vez de apenas descrever o resultado desejado, o trio incluiu fragmentos de referência que demonstravam o tom, vocabulário e estrutura corretos — reduzindo a ambiguidade e guiando o modelo com exemplos concretos.

**Exemplo aplicado:**
```
"Escreva um e-mail formal no estilo do século XVII, como neste exemplo:
'Vossa Majestade, humildemente me apresento...'
O remetente é um pirata e o destinatário é um rei."
```

### Chain of Thought (CoT)

O **Chain of Thought** foi aplicado ao solicitar que a IA explicitasse seu raciocínio antes de gerar o resultado. Isso permitiu identificar onde o modelo estava "pensando errado" e corrigir a lógica no prompt seguinte.

**Exemplo aplicado:**
```
"Antes de escrever o e-mail, liste os elementos formais
que um pirata do século XVII usaria para se dirigir a um rei.
Depois, use esses elementos na redação."
```

### Impacto das Técnicas

| Técnica | Prompt sem a técnica | Prompt com a técnica | Melhoria |
| :--- | :--- | :--- | :--- |
| **Few-Shot** | Resultado genérico, tom incorreto | Tom histórico e formal desde a 1ª frase | Alta |
| **Chain of Thought** | IA ignorava restrições de época | IA listou e aplicou restrições corretamente | Alta |

---

## 🔧 Como foi executado

1. O professor forneceu o "alvo" (texto ou imagem a ser gerado).
2. O trio avaliou criticamente cada resposta antes de enviar o próximo prompt.
3. Cada prompt enviado foi registrado junto com a resposta recebida.
4. Ao final das 5 tentativas, o resultado foi apresentado para discussão coletiva.

---

## 📊 Resultados

* Uma única palavra ou detalhe de contexto pode mudar completamente a interpretação da IA.
* Avaliar antes de reenviar é tão importante quanto redigir o prompt.
* Limite de tentativas força o pensamento estratégico ao invés de tentativa e erro aleatório.

---

[Voltar ao início](https://github.com/1Naju/portfolio-ana-julia-oliveira-de-freitas)
