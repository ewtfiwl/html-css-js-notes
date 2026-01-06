# 📍 CSS Position — Fluxo, Fixed, Relative e Absolute

Estudo da propriedade **`position`**, entendendo como ela altera o **fluxo normal do layout** e quando deve (ou não) ser utilizada.

---

## 🧠 O que é o fluxo normal?

Por padrão, os elementos HTML seguem o **fluxo normal**:

- Um elemento fica abaixo do outro
- O layout cresce de cima para baixo
- Nada fica “flutuando” ou sobreposto

Quando precisamos de algo que **não siga esse fluxo** (ex: botão de cookies, etiquetas, avisos), usamos **`position`**.

---

## 📌 Tipos de Position Estudados

- `static` (padrão)
- `fixed`
- `relative`
- `absolute`

---

## 📍 Position: fixed

O `position: fixed` remove o elemento do fluxo normal e fixa sua posição em relação à **tela (viewport)**.    

Usado quando um elemento deve **permanecer visível na tela**, mesmo com scroll.   

Exemplo clássico:

- Botão de cookies
- Botão flutuante
- Barra fixa

```css
.cookie {
  position: fixed;
}
```

📌 Ao usar apenas `position: fixed` o elemento **sai do fluxo** e pode desaparecer da tela.

Por isso, precisamos definir **onde ele deve ficar**:

```css
.cookie {
  position: fixed;
  top: 0px;
  left: 0px;
}
```

## 📐 Propriedades de posicionamento

Essas propriedades só funcionam se o `position` for **diferente de** `static`:

- `top`

- `right`

- `bottom`

- `left`

## 📏 Esticando o elemento

```css
.cookie {
  position: fixed;
  top: 20px;
  left: 20px;
  right: 20px;
}
```

📌 Utilizando `left` e `right`, o elemento ocupa toda a largura disponível.

⚠️ É possível usar `top` e `bottom` juntos, o que define a altura do elemento.    

Porém, na prática, geralmente escolhe-se `top` OU `bottom` para evitar comportamentos inesperados.    


## 📦 Position: relative

O `relative` não move o elemento sozinho.

Ele só passa a funcionar quando usamos:

```css
.elemento {
position: relative;
top: 20px;
```

📌 O elemento:

- Continua ocupando seu espaço original

- Se move **em relação a ele mesmo**

- Continua ocupando seu espaço original no fluxo

- O deslocamento é apenas visual


Valores comuns:

- `20px`

- `-20px`

- `50px`

- `-320px`

👉 Muito usado para **pequenos ajustes visuais**.

## 📌 Position: absolute

O `absolute` **remove completamente o elemento do fluxo**.

Exemplo básico:

```css
 .elemento {
  position: absolute;
  top: 0px;
}
```

📌 Sem referência, ele se posiciona em relação **à tela inteira**.

## 🎯 Tornando o posicionamento relativo ao container

Para resolver isso:

```css
.container {
  position: relative;
}
```

```css
.elemento {
  position: absolute;
  top: 0px;
}
```

_📌 Agora o elemento se posiciona em relação ao container, não à tela._

## 🧩 Uso prático: Etiqueta “Saiba Mais”

Esse tipo de layout seria difícil no fluxo normal, exigindo:

- margens negativas

- hacks visuais

Com `position`, fica simples e limpo.

## 🧪 Código Final do Projeto

### HTML

```html
<div>
  <span>Saiba Mais</span>
  <h1>Primeiro Conteúdo</h1>
</div>

<div>
  <span>Saiba Mais</span>
  <h1>Segundo Conteúdo</h1>
</div>
```

### CSS

```css
body {
  height: 1200px;
}

div {
  border: 2px solid #ddd;
  margin-top: 40px;
  padding: 20px 20px 40px 20px;
  position: relative;
}

span {
  background: #e7e7e7;
  border: 2px solid #ccc;
  padding: 10px;
  position: absolute;
  top: 0px;
}
```

📌 O `span` fica posicionado no topo de cada `div`, respeitando o container correto.

---

## ⚠️ Boas Práticas Importantes

- ❌ Não usar `position` para estruturar layouts

- ❌ Não usar para menus ou grids inteiros

- ✅ Usar para:

  - etiquetas

  - avisos

  - elementos flutuantes

  - sobreposições específicas

👉 Layout principal → Grid e Flexbox
👉 Ajustes pontuais → Position

## 🧠 Conceitos-Chave Aprendidos

- `position` altera o fluxo do layout

- `fixed` prende o elemento à tela

- `relative` move em relação a si mesmo

- `absolute` se relaciona ao pai com `position`

- `top/right/bottom/left` só funcionam com `position`

- Position deve ser usado com **moderação**

---

_📌 Este conteúdo reforça que Grid, Flexbox e Position resolvem problemas diferentes e devem ser usados juntos, cada um no seu papel._

---
