# 🔄 Vibe Coding — ShadowLab

> Ferramenta para geração de CSS neumórfico com IA integrada, exportação de código e sistema de favoritos.

## 📝 Descrição do Projeto

O **ShadowLab** é uma aplicação web desenvolvida via **Vibe Coding** no Google AI Studio, usando engenharia reversa assistida por IA: reconstruir um webapp funcional a partir da observação de sua interface externa, sem visualizar o código-fonte original. Toda a construção foi feita configurando o Gemini como desenvolvedor Full-Stack por meio de System Instructions.

Desenvolvido como parte da disciplina de **Engenharia de Prompt e Aplicações em IA**, o projeto transfere o esforço da escrita sintática para a descrição lógica e funcional.

🔗 **Acesse o projeto no AI Studio:** [ShadowLab](https://ai.studio/apps/34baefa2-9529-433b-916b-8254692283bc)
🔗 **Repositório do projeto:** [github.com/1Naju/ShadowLab](https://github.com/1Naju/ShadowLab)

---

## 🛠️ Tecnologias e Bibliotecas Utilizadas

| Tecnologia | Função |
| :--- | :--- |
| **TypeScript** | Linguagem principal (94.8% do projeto) |
| **React** | Biblioteca de UI com hooks (useState, useEffect) |
| **Gemini API** | IA integrada para geração de CSS neumórfico |
| **Firebase Auth** | Autenticação de usuários |
| **Firebase Firestore** | Armazenamento do sistema de favoritos |
| **Vite** | Build tool e servidor de desenvolvimento |
| **Lucide React** | Biblioteca de ícones (ex: ícone Lightbulb) |
| **CSS Variables** | Theming dinâmico baseado na cor escolhida |

---

## 🧩 Parâmetros de Geração do CSS Neumórfico

O ShadowLab controla os seguintes parâmetros em tempo real para gerar o CSS:

| Parâmetro | Tipo | Valor Padrão | Função |
| :--- | :--- | :--- | :--- |
| `color` | hex | `#e0e0e0` | Cor base do elemento |
| `size` | number | `150px` | Tamanho do elemento |
| `radius` | number | `50px` | Border radius |
| `distance` | number | `20px` | Distância das sombras |
| `intensity` | float | `0.15` | Intensidade claro/escuro das sombras |
| `blur` | number | `60px` | Desfoque das sombras |
| `shape` | enum | `flat` | Formato: flat, pressed, concave, convex |
| `lightSource` | enum | `top-left` | Direção da fonte de luz (8 posições) |

### Lógica de geração do box-shadow

```css
/* Gerado dinamicamente pelo ShadowLab */
box-shadow: {offsetX}px {offsetY}px {blur}px {darkColor},
           -{offsetX}px -{offsetY}px {blur}px {lightColor};
```

A cor escura e a cor clara são calculadas a partir da cor base usando a função `colorLuminance`, que ajusta o brilho em `±intensity`:

```typescript
const darkColor  = colorLuminance(state.color, -state.intensity);
const lightColor = colorLuminance(state.color,  state.intensity);
```

---

## 🧠 Desafio Técnico e Processo de Vibe Coding

O principal desafio foi **descrever em linguagem natural** a lógica matemática de sombras duplas e manipulação de cores para que a IA gerasse código TypeScript funcional.

### Dificuldades encontradas e como foram superadas

| Desafio | Descrição | Solução |
| :--- | :--- | :--- |
| **Cálculo de luminância** | A função `colorLuminance` manipula valores HEX — difícil de descrever sem código | Descrição do comportamento esperado ("escurecer 15% a cor base") em vez da implementação |
| **Direção da fonte de luz** | 8 posições diferentes gerando offsets X e Y distintos | Tabela de mapeamento descrita em linguagem natural no prompt |
| **Shapes (concave/convex)** | Gradientes lineares diferentes para cada forma | Descrição do efeito visual desejado em cada caso |
| **Integração Firebase** | Persistência de favoritos com autenticação | System Instructions incluindo exemplo de estrutura de dados |
| **CSS Variables dinâmicas** | Theming em tempo real via `document.documentElement` | Prompt especificando quais variáveis CSS deveriam ser atualizadas |

### System Instructions utilizadas

```
Você é um desenvolvedor Full-Stack especialista em CSS neumórfico e React/TypeScript.
Crie uma ferramenta web chamada ShadowLab que:
- Permita ajustar cor, tamanho, raio, distância, intensidade e desfoque de sombras neumórficas
- Suporte 4 formatos: flat, pressed, concave e convex
- Tenha 8 posições de fonte de luz clicáveis no preview
- Exporte o CSS gerado com um botão de copiar
- Integre Firebase Auth e Firestore para salvar favoritos
- Use TypeScript + React + Vite
```

---

## 🔧 Como executar localmente

**Pré-requisitos:** Node.js

```bash
# Clone o repositório
git clone https://github.com/1Naju/ShadowLab.git
cd ShadowLab

# Instale as dependências
npm install

# Configure a chave da API
# Crie um arquivo .env.local e adicione:
GEMINI_API_KEY=sua_chave_aqui

# Execute o app
npm run dev
```

---

## 📊 Resultados e Aprendizados

* Com a IA escrevendo código, o desenvolvedor precisa saber **descrever o problema** e **validar o que foi gerado**
* **Leitura crítica de código:** a IA gerou a lógica de `colorLuminance` corretamente, mas com edge cases não previstos no prompt — exigindo revisão humana
* **Clareza na comunicação:** descrever o comportamento visual em vez da implementação técnica produziu resultados mais precisos
* A engenharia reversa vira plágio quando o objetivo deixa de ser aprender e passa a ser lucrar com o trabalho alheio sem dar crédito

---

## 📎 Arquivos do Projeto

| Arquivo | Descrição |
| :--- | :--- |
| [analise-critica.md](./analise-critica.md) | Reflexão sobre Vibe Coding e originalidade na era da IA |
| [src/App.tsx](https://github.com/1Naju/ShadowLab/blob/main/src/App.tsx) | Componente principal com lógica de geração CSS |
| [src/components/](https://github.com/1Naju/ShadowLab/tree/main/src/components) | Componentes React do projeto |

---

[Voltar ao início](https://github.com/1Naju/portfolio-ana-julia-oliveira-de-freitas)
