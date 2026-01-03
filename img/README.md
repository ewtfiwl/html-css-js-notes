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

## 🧠 Boas Práticas

- Nunca esticar imagens rasterizadas além do tamanho original

- Preferir SVG para ícones e logos

- Controlar tamanho via CSS, não alterando o arquivo original

- Usar imagens otimizadas para web

---

## 🚀 Conclusão

Entender os formatos de imagem evita:

- Perda de qualidade

- Layout quebrado

- Problemas de performance

---
