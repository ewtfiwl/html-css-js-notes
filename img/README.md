# 🖼️ Trabalhando com Imagens no HTML e CSS

Anotações da aula sobre uso de imagens na web, formatos, qualidade, resolução e boas práticas.

---

## 📌 Formatos de Imagem

### PNG

- Formato **rasterizado** (baseado em pixels)
- Perde qualidade ao aumentar o tamanho
- Ideal para:
  - Fotos
  - Imagens com muitos detalhes
- Suporta fundo transparente

📉 **Problema:** ao aumentar muito o tamanho, a imagem fica pixelada.

---

### SVG

- Formato **vetorial**
- Não perde qualidade ao redimensionar
- Ideal para:
  - Ícones
  - Logos
  - Ilustrações simples
- Pode ser estilizado com CSS
- Cor, tamanho e até animações podem ser controladas

📈 **Vantagem:** mantém qualidade em qualquer resolução.

---

## 🎨 Estilizando SVG com CSS

Quando o SVG está inline ou como background, é possível:

- Alterar cor
- Alterar tamanho
- Aplicar efeitos

Exemplo:

```css
.icon {
  width: 40px;
  height: 40px;
  fill: red;
}
```

---

## 📐 Redimensionando imagens sem perder qualidade

Uma boa prática é controlar o tamanho da imagem via CSS, e não alterar o arquivo original.

Exemplo:

```cs
 img {
  max-width: 100%;
  height: auto;
}
```

Isso permite que a imagem:

- Se adapte ao layout

- Não fique “esticada”

- Mantenha proporção correta

---

## 🧱 Padrão de Estilo para Imagens

É comum definir um estilo padrão para todas as imagens do projeto, evitando comportamentos estranhos no layout.

```css
img {
  max-width: 100%;
  display: block;
}
```

Por que usar isso como padrão?

- max-width: 100%

- Impede que a imagem ultrapasse o tamanho do elemento pai

- Mantém a proporção original da imagem

- Evita quebra de layout em telas menores

- display: block

- Remove espaços indesejados abaixo da imagem

- Facilita o controle de espaçamento com margin

- Evita o comportamento inline padrão das imagens

## 📐 Controle de Tamanho com Classe

Mesmo usando um padrão global, é comum controlar o tamanho de imagens específicas usando classes.

Exemplo:

```css
.foto {
  width: 150px;
}
```

_Esse método permite redimensionar a imagem sem alterar o arquivo original, mantendo o layout consistente._

---

## ⚠️ Diferença de Resolução e Deformação

Durante a aula, foi demonstrado o comportamento de imagens com resoluções diferentes:

- Imagem grande (ex: 1800×200)

- Imagem pequena (ex: 300×200)

Quando ambas recebem o mesmo tamanho via layout:

- A imagem menor pode aparentar perda de qualidade ou deformação

- A imagem maior se adapta melhor ao redimensionamento

Ao aplicar uma classe (.foto) com width apenas na imagem menor:

- O tamanho fica controlado

- A proporção é mantida

- A deformação visual é reduzida

## 🧠 Boas Práticas

- Nunca esticar imagens rasterizadas além do tamanho original

- Preferir SVG para ícones e logos

- Controlar tamanho via CSS, não alterando o arquivo original

- Usar imagens otimizadas para web

---

## 🚀 Conclusão

- Use um padrão global para imagens (img { max-width: 100%; display: block; })

- Controle tamanhos específicos com classes

- Evite esticar imagens pequenas além da sua resolução original

- Prefira imagens maiores ou SVG quando possível

Entender os formatos de imagem evita:

- Perda de qualidade

- Layout quebrado

- Problemas de performance

---
