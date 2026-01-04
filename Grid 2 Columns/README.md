## 📐 CSS Grid — Colunas, Itens e Alinhamento

Continuação do estudo de **CSS Grid Layout**, agora focando em **grid-column**, **span**, alinhamento de itens e a diferença entre **conteúdo** vs **caixa**.

## 🧱 Estrutura Base do Grid

O layout utiliza duas colunas iguais:

```css
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 20px;
}
```

Isso cria duas colunas flexíveis, que servem de base para controlar onde cada elemento aparece.

## 📐 Controle de Colunas com `grid-column`

Para fazer um elemento ocupar mais de uma coluna, usamos:

```css
grid-column: 1 / 3;
```

📌 Nesse caso:

- O Grid tem 2 **colunas**

- As linhas do Grid são numeradas

- `1 / 3 `significa:

  - Começa na coluna 1

  - Vai até antes da linha 3

  - Ou seja: ocupa as duas colunas

## Exemplos do projeto

```css
.foto {
  grid-column: 1 / 3;
}

.descricao {
  grid-column: 1 / 3;
}

.comprar {
  grid-column: 1 / 3;
}
```

👉 Isso faz imagem, descrição e botão ocuparem a largura total do Grid.

## 🔁 Usando `-1` para ir até o final

Quando não sabemos quantas colunas existem, ou elas são dinâmicas, usamos:

```css
grid-column: 1 / -1;
```

📌 O `-1` sempre representa a última linha do Grid (final das colunas),
independentemente da quantidade de colunas.

✔ Mais seguro  
✔ Mais flexível  
✔ Muito usado em layouts reais

## 📏 Expandindo Colunas com span

O `span` serve para expandir a partir da posição inicial.

Exemplo:

```css
grid-column: span 2;
```

Ou

```css
grid-column: span 3;
grid-column: span 4;
```

_📌 O comportamento sempre depende da quantidade de colunas disponíveis._

## ▶️ Começar de uma coluna específica + span

Também é possível combinar:

```css
grid-column: 2 / span 3;
```

Significa:

- Começa na coluna 2

- Ocupa 3 colunas

👉 Muito útil em grids maiores e layouts complexos.

## 📦 Alinhamento de Itens (`align-items` e `justify-items`)

Agora entramos no alinhamento dos itens, não do conteúdo do Grid.

Importante:

> Alinhamento de itens ≠ alinhamento do conteúdo

O alinhamento é sempre baseado no maior item do Grid.

Exemplo:

```css
.grid {
  align-items: center;
}
```

- Itens menores tentam se alinhar ao centro do item maior

- O tamanho do maior elemento define o eixo

## 🧩 Atalho com `place-items`

O `place-items` é um atalho para:

- `align-items`

- `justify-items`

Exemplo:

```css
place-items: center;
```

Equivale a:

```css
align-items: center;
justify-items: center;
```

Com dois valores:

```css
place-items: end center;
```

- Vertical → `end`

- Horizontal → `center`

📌 Alinha os itens respeitando o tamanho real de cada um.

## 🎯 Alinhando Itens Individualmente (`place-self`)

Para alinhar um item específico, usamos:

```css
place-self: start end;
```

Ou separadamente:

```css
align-self: start;
justify-self: end;
```

👉 Muito útil para botões, preços ou elementos pontuais.

## 📦 Caixa vs Conteúdo (**conceito MUITO importante**)

Alguns elementos (como títulos) ocupam 100% da largura da coluna.

Exemplo:

```css
.titulo {
  grid-column: 2;
}
```

📌 Isso move a caixa, mas não o texto.

Para alinhar o texto:

```css
.titulo {
  grid-column: 2;
  text-align: right;
}
```

Extra 👽

- Também é possível usar `text-align: end`, para a mesma função do `text-align: right`, mas ainda é experimental

- Portanto prefira: `text-align: right`, para maior compatibilidade com todos os navegadores

## 🧠 Alinhar a Caixa ≠ Alinhar o Texto

Resumo importante:
| O que você quer mover | Propriedade |
| --------------------- | --------------------------- |
| Caixa do elemento | `grid-column`, `place-self` |
| Texto dentro da caixa | `text-align` |

Exemplo completo:

```css
.comprar {
  align-self: start;
  text-align: center;
}
```

- Caixa vai para o topo

- Texto fica centralizado

## 🧠 Conceitos-Chave Aprendidos

- `grid-column` controla onde o item vive no Grid

- `span` expande a partir da posição inicial

- `-1` sempre representa o final do Grid

- `align-items` e `justify-items` alinham itens

- `place-items` é apenas um atalho

- `place-self` serve para itens individuais

- Caixa e conteúdo **não são a mesma coisa**

---
