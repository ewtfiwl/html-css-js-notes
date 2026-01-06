# 🏗️ CSS Grid – Template Rows e Organização de Layout

Este projeto faz parte do estudo de **CSS Grid**, com foco na criação de layouts mais organizados, previsíveis e fáceis de manter.

O objetivo principal foi entender não apenas as propriedades do Grid, mas **como a estrutura do HTML influencia diretamente a simplicidade do CSS**.

---

## 📚 Conteúdos estudados

### `grid-template-rows`

Define explicitamente a altura das linhas do grid.

- `auto`: a linha se ajusta ao conteúdo
- Valores fixos como `300px`: a linha terá altura fixa
- É possível combinar múltiplos valores:

```css
grid-template-rows: auto 300px auto;
```

Nesse exemplo, a linha do meio tem tamanho fixo, enquanto as outras se adaptam ao conteúdo.

---

### `grid-auto-rows`

Define o tamanho padrão das **linhas criadas automaticamente**, ou seja, linhas que não foram declaradas em `grid-template-rows`.

Exemplo:

```css
grid-template-rows: 300px auto auto;
grid-auto-rows: 200px;
```

- A primeira linha tem 300px
- A segunda e terceira são automáticas
- Todas as linhas seguintes terão 200px

---

### `repeat()`

Função utilizada para evitar repetição excessiva de valores no Grid.

Exemplo:

```css
grid-template-columns: repeat(2, 1fr);
```

É equivalente a:

```css
grid-template-columns: 1fr 1fr;
```

Pode ser utilizada tanto em colunas quanto em linhas:

```css
grid-template-rows: repeat(4, 200px);
```

---

## ⚠️ Problema identificado

Inicialmente, o layout foi construído posicionando cada elemento diretamente no Grid principal, controlando manualmente linhas e colunas.

Isso resultou em:

- Uso excessivo de `grid-row` e `grid-column`
- Dependência de múltiplas linhas do grid
- Layout mais frágil e difícil de manter

Esse tipo de abordagem tende a escalar mal quando o conteúdo muda ou cresce.

---

## ✅ Solução aplicada: reorganização do HTML

Ao invés de complexar o CSS, a solução foi **reorganizar a estrutura do HTML** para refletir melhor o layout visual.

### Estrutura anterior

- Todos os elementos posicionados diretamente no Grid principal

### Estrutura atual

- Grid principal com apenas **duas colunas**
- Uma coluna dedicada à imagem
- Uma coluna contendo todas as informações do produto
- Criação de um container `.info` para agrupar conteúdo relacionado

Essa abordagem permite que o Grid trabalhe a favor da estrutura, e não contra ela.

---

## 🧩 Estrutura final do layout

- Grid principal define apenas as colunas
- `.info` se torna um grid interno para organizar texto e botão
- Menos posicionamento manual
- Código mais limpo e semântico

---

## 🏁 Resultado

Com a nova estrutura:

- O CSS ficou mais simples
- O layout ficou mais previsível
- O código ficou mais fácil de manter
- A estrutura HTML passou a representar melhor o design

---

## 🧠 Aprendizado principal

Antes de aumentar a complexidade do CSS Grid, vale revisar a estrutura do HTML.

👉 **Um bom layout começa com uma boa organização de elementos.**

CSS Grid é mais poderoso quando a estrutura trabalha junto com ele.

---
