# 🧱 CSS Position — Parte 2: Profundidade, Ordem e z-index

Continuação do estudo sobre `position`, agora focando em **profundidade dos elementos, ordem de empilhamento** e no funcionamento do `z-index`.

---

## 🧠 Conceito de Profundidade (Stacking)

Além do eixo **horizontal (x) e vertical (y)**, os elementos HTML também possuem um **eixo de profundidade (z)**.

📌 Por padrão:

- Elementos que vêm **depois no HTML ficam por cima**

- O último elemento geralmente cobre os anteriores

Esse comportamento muda quando usamos `position` e `z-index`.

---

## 🧪 Exemplo Base

### HTML

```html
<h1>Elemento 1</h1>
<h1 class="index1">Elemento 2</h1>
<h1>Elemento 3</h1>
<h1 class="index2">Elemento 4</h1>
<h1>Elemento 5</h1>
```

### CSS

```css
h1 {
  margin: 0px;
  padding: 10px;
  background: lightblue;
}
```

---

## 📍 Position cria contexto para controle de empilhamento

Ao aplicar `position: relative` em um elemento:

```css
.index1 {
  position: relative;
  background: greenyellow;
  top: 30px;
}
```

📌 O elemento:

- Se desloca visualmente

- **Passa a ficar por cima dos outros**

- Ignora a regra padrão de empilhamento

Mesmo “passando por cima” de elementos seguintes no HTML, ele aparece acima.

---

## 🧱 Controlando profundidade com z-index

```css
.index1 {
  position: relative;
  top: 30px;
  z-index: -1;
}
```

📌 Resultado:

- O elemento passa a ficar **atrás de todos**

- Inclusive atrás de elementos anteriores e posteriores

Valores comuns:

- `z-index: -1` → fica atrás

- `z-index: 0` → padrão

- `z-index: 1+` → fica à frente

⚠️ Quanto **maior o valor**, mais à frente o elemento fica.

---

## 🆚 Dois elementos posicionados

```css
.index2 {
  position: absolute;
  background: lightcoral;
  top: 30px;
}
```

📌 Por padrão:

- Ele fica acima dos elementos estáticos

- Pode cobrir outros elementos posicionados

Se ajustarmos:

```css
.index2 {
  position: absolute;
  background: lightcoral;
  top: 60px;
}
```

O elemento `.index2` pode passar a ficar por cima de todos, inclusive de `.index1`.

---

## 🧬 Ordem do HTML influencia

Se mudarmos a ordem no HTML para:

```html
<h1>Elemento 1</h1>
<h1 class="index2">Elemento 4</h1>
<h1 class="index1">Elemento 2</h1>
<h1>Elemento 3</h1>
<h1>Elemento 5</h1>
```

📌 O elemento que vem **depois no HTML** tende a ficar por cima, mesmo que ambos tenham `position`.

---

## 🎯 Resolvendo com z-index

Voltando a ordem antiga do HTML:

```html
<h1>Elemento 1</h1>
<h1 class="index1">Elemento 2</h1>
<h1>Elemento 3</h1>
<h1 class="index2">Elemento 4</h1>
<h1>Elemento 5</h1>
```

E manipulando o `z-index` no CSS:

```css
.index1 {
  position: relative;
  z-index: 1;
}
```

```css
.index2 {
  position: absolute;
  z-index: 2;
}
```

📌 Obtemos exatamente o mesmo resultado, sem alterar a ordem do HTML.

- `.index2` fica acima de `.index1`

- A hierarquia agora é controlada explicitamente

---

## 🚨 O mito do z-index: 999999

É comum ver:

```css
.modal {
  z-index: 999999;
}
```

Para que o modal esteja sempre acima de todos os elementos.

📌 Funciona? Sim.

📌 É necessário? ❌ Não.

Boa prática:

- Organizar camadas:

  - Base → `1`

  - Conteúdo → `2`

  - Modal → `3`

  - Overlay → `4`

👉 Muito mais limpo, previsível e profissional.

---

## ⚠️ Regra IMPORTANTÍSSIMA do `z-index`

❗ `z-index` **só funciona em elementos posicionados**

❌ Isso NÃO funciona:

```css
.index3 {
  z-index: 99999;
}
```

✅ Isso funciona:

```css
.index3 {
  position: relative;
  z-index: 99999;
}
```

📌 O elemento precisa ter `position` diferente de `static`.

📌 Além disso, o `z-index` funciona dentro de **contextos de empilhamento (stacking context)**.
Elementos filhos não ultrapassam o `z-index` do pai.

---

## 🧠 Conceitos-Chave Aprendidos

- Existe um **eixo de profundidade (z)**

- `position` altera a ordem visual

- `z-index` controla quem fica por cima

- Maior valor → maior prioridade

- Ordem do HTML influencia

- `z-index` só funciona com position

- Valores gigantes não são necessários

- Organização > gambiarra

---

## ⚠️ Boas Práticas

- ❌ Não usar `z-index` sem necessidade

- ❌ Evitar valores absurdos

- ✅ Organizar camadas logicamente

- ✅ Usar apenas em elementos posicionados

- ✅ Ideal para modais, overlays, tooltips e avisos

---

📌 Grid → estrutura  
📌 Flexbox → alinhamento  
📌 Position → exceções  
📌 z-index → profundidade

_Cada ferramenta no seu lugar._

---
