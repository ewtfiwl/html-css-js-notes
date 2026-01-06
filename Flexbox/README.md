# 📦 Flexbox — Fundamentos, Comportamento e Comparação com Grid

Introdução ao **Flexbox**, entendendo seu propósito, funcionamento, principais propriedades e como ele se diferencia do **CSS Grid**.

---

## 🕰️ Contexto Histórico

Antes do Flexbox, layouts eram feitos com:

- `float`
- `clear`
- hacks e gambiarras

❌ Layouts quebravam facilmente  
❌ Difíceis de manter

O **Flexbox** surgiu para resolver **alinhamento e distribuição de elementos em uma dimensão (linha ou coluna)**.

Depois veio o **Grid**, mais poderoso para layouts bidimensionais, mas **um não substitui o outro** — eles se complementam.

---

## 📐 Estrutura Base do Flexbox

HTML base utilizado:

```html
<div class="flex">
  <h2>O Senhor dos Anéis</h2>
  <h2>Interestelar</h2>
  <h2>O Hobbit</h2>
  <h2>Titanic</h2>
</div>
```

Ao aplicar:

```css
.flex {
  display: flex;
}
```

📌 Todos os elementos filhos ficam **lado a lado automaticamente**.

---

## 🎨 Estilização dos Itens

```css
h2 {
  background: #e7e7e7;
  border: 1px solid #d7d7d7;
  padding: 20px;
  margin: 0px;
}
```

📌 Assim como no Grid, o maior elemento influencia os outros.

---

## 🔄 Quebra de Linha — `flex-wrap`

Quando o conteúdo não cabe mais no container:

```css
.flex {
  flex-wrap: wrap;
}
```

✔ Permite que os itens quebrem para a próxima linha  
✔ Evita que o layout estoure

---

## ↔️ Alinhamento Horizontal — `justify-content`

```css
.flex {
  justify-content: center;
}
```

📌 Funciona **somente se houver espaço sobrando** no container.

---

## ↕️ Alinhamento Vertical — `align-items`

Por padrão, não há espaço vertical.

Para que funcione:

```css
.flex {
  height: 100vh;
  align-items: center;
}
```

📌 `100vh` = 100% de Viewport Height/Altura da Viewport (tela).

---

## 🌱 Distribuição de Espaço — `flex-grow`

```css
h2 {
  flex-grow: 1;
}
```

- Distribui o espaço sobrando

- O maior conteúdo ainda influencia os outros

---

## 📏 Controle de Base — `flex-basis`

```css
h2 {
  flex-basis: 0;
}
```

📌 Ignora o tamanho do conteúdo  
📌 Todos os itens passam a ter o mesmo tamanho

Valores comuns:

- `auto` (padrão)

- `0` (muito usado)

---

## 📉 Encolhimento — `flex-shrink`

```css
h2 {
  flex-shrink: 1;
}
```

- Define se o item pode encolher

- `0` → não encolhe

- `1` → comportamento padrão

---

## ⚡ Atalho — `flex`

```css
h2 {
  flex: 1;
}
```

Equivale a:

```css
flex-grow: 1;
flex-shrink: 1;
flex-basis: 0%;
```

📌 Muito utilizado na prática.

---

## ⚠️ Flex × Justify-Content

Se os itens usam `flex: 1`:

- ❌ Não sobra espaço

- ❌ `justify-content` não funciona

👉 Para justificar conteúdo, não defina **flex-grow**.

---

## 🆚 Flexbox vs Grid

### Flexbox

- Não possui conceito de colunas

- Encaixa os itens automaticamente

- Ideal para **componentes e layouts lineares**

### Grid

- Trabalha com linhas **e** colunas

- Ideal para **layouts estruturais**

- Exige definição de colunas

---

## 🔁 Simulando Flex com Grid

```css
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, auto));
  gap: 20px;
}
```

📌 Significado:

- `auto-fit` → encaixa o máximo possível

- `minmax(150px, auto)` → mínimo fixo, máximo flexível

✔ Layout responsivo  
✔ Não precisa definir número de colunas

---

## 🧪 Código Final — Flex e Grid

### HTML

```html
<div class="flex">
  <h2>O Senhor dos Anéis</h2>
  <h2>Interestelar</h2>
  <h2>O Hobbit</h2>
  <h2>Titanic</h2>
</div>

<div class="grid">
  <h2>O Senhor dos Anéis</h2>
  <h2>Interestelar</h2>
  <h2>O Hobbit</h2>
  <h2>Titanic</h2>
</div>
```

### CSS

```css
.flex {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  justify-content: center;
}

.grid {
  margin-top: 60px;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, auto));
  gap: 20px;
}

body {
  margin: 0px;
}

h2 {
  background: #e7e7e7;
  border: 1px solid #d7d7d7;
  padding: 20px;
  margin: 0px;
}
```

> Os dois funcionam da mesma forma neste código em específico, mas a principal diferença entre eles é que o grid trabalha com **colunas**.

---

## 🧠 Conceitos-Chave Aprendidos

- Flexbox organiza elementos **em uma dimensão**

- O maior item **influencia** os outros

- `flex-wrap` evita quebra de layout

- `flex-basis: 0` ignora tamanho do conteúdo

- `flex: 1` é o atalho mais usado

- Flex e Grid não **competem**, se complementam

- Grid pode simular Flex com `auto-fit` + `minmax`

---
