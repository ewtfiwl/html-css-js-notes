### 📐 CSS Grid — Introdução e Fundamentos

Anotações iniciais sobre **CSS Grid Layout**, utilizando um exemplo de comércio eletrônico para entender comportamento de colunas, espaçamento e organização de elementos.

Este conteúdo cobre apenas os fundamentos iniciais aprendidos até o momento.

---

## 🧱 Estrutura do Projeto

O layout é composto por:

- Um título (`<h1>`)

- Um container principal (`.grid`)

- Vários cards de produto (`.item`)

  - Cada card contém:

  - Nome do produto

  - Preço

  - Descrição

  - Botão de compra

---

## 🧩 Estrutura HTML

```html
<div class="grid">
  <div class="item">
    <h2>Camiseta Polo</h2>
    <p class="preco">R$ 39</p>
    <p>Descrição do produto</p>
    <a class="comprar" href="/">Comprar</a>
  </div>
</div>
```

📌 Observação:  
É totalmente normal utilizar uma `div` dentro de outra `div`.  
Antes de aprender elementos semânticos como `section`, `article`, etc., o uso de `div` é comum e correto.

---

## 📦 Container Grid

O layout principal é controlado pela classe `.grid`:

```css
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
}
```

Por que usar ``fr` em vez de porcentagem?

❌ Evitar:

```css
grid-template-columns: 50% 50%;
```

Ou:

```css
grid-template-columns: 45% 45%;
```

❌ Problemas do uso de porcentagem:

- O `gap` não entra corretamente no cálculo

- As colunas podem ficar com larguras diferentes

- O layout quebra ao redimensionar a tela

- Espaçamentos laterais e verticais ficam inconsistentes

✅ Uso correto com `fr`:

- `fr` significa fração do espaço disponível

- O `Grid` calcula automaticamente o espaço restante

- O `gap` é respeitado corretamente

- O layout se adapta sem quebrar

📌 Importante:
Usar valores como `2fr` `1fr` não resolve o problema nesse caso, pois o comportamento continua inconsistente quando há gap.

---

## 🧱 Grid dentro dos Cards (`.item`)

Cada card também utiliza Grid:

```css
.item {
  display: grid;
}
```

Vantagens de usar Grid dentro do `.item`:

- Os elementos internos se organizam automaticamente

- Nada “entra em cima” de outro elemento

- Alterações respeitam o layout existente

- Evita ajustes manuais constantes de `padding`, `margin` e `border`

📌 Sem Grid no `.item`:

- Botão pode invadir outros elementos

- Mudanças exigem reajustes manuais

- Layout quebra facilmente ao alterar tamanhos

📌 Com Grid no `.item`:

- O layout se adapta sozinho

- Basta alterar uma vez

- Todos os elementos respeitam os limites automaticamente

---

## 🧠 Conceitos Importantes Aprendidos

- Grid resolve problemas de layout que seriam difíceis com outras abordagens

- `fr` é preferível a `%` em layouts com colunas e espaçamento

- Grid pode ser usado:

  - No container principal

  - Dentro dos componentes

- Divs podem ser aninhadas sem problema algum

- Grid facilita manutenção e evolução do layout

---

## 🚀 Próximos Passos

Este README cobre **apenas a introdução ao Grid**.

Conteúdos que ainda serão estudados e adicionados futuramente:

- `grid-template-rows`

- `grid-area`

- `auto-fit` e `auto-fill`

- `minmax()`

- Alinhamento (`align` / `justify`)

- Layouts responsivos com Grid

- Comparação entre Grid e Flexbox

---

## 🧰 Ferramentas Visuais e Guias de CSS Grid

Durante o estudo de **CSS Grid Layout**, foram utilizados guias visuais que mostram o comportamento do Grid de forma prática e interativa.

Esses materiais ajudam a entender melhor:

- Distribuição de colunas e linhas

- Uso de `fr`, `auto`, `minmax()`

- `grid-template-areas`

- Espaçamentos (`gap`)

- Alinhamento de itens e containers

## 📘 Guias Utilizados

- Guia CSS Grid Layout — Origamid
  https://www.origamid.com/projetos/grid/

_Guia visual e interativo que demonstra, na prática, como cada propriedade do Grid afeta o layout._

- Guia Completo de CSS Grid Layout — Origamid
  https://www.origamid.com/projetos/css-grid-layout-guia-completo/

_Material de referência completo para consulta durante o desenvolvimento e estudo de Grid._

📌 Observação:
No momento, apenas os guias da Origamid estão sendo utilizados como apoio direto nas aulas e nos exercícios práticos.

---

_📌 Este projeto serve como base para evoluir o estudo de CSS Grid conforme novos conceitos forem aprendidos._

---
