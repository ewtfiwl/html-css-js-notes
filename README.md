![HTML](https://img.shields.io/badge/HTML-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

# 📘 HTML / CSS / JS — Notes & Studies

Repositório criado para organizar meus estudos de **Front-End.**  
 Aqui vou guardar exemplos, exercícios, testes, anotações importantes e tudo que for aprendendo no caminho.  
 Criei este repositório para organizar meus estudos de **front-end**, experimentar novas ideias e documentar minha evolução como **desenvolvedor**.

---

## 📑 Índice

- [📘 Sobre o Repositório](#-sobre-o-repositório)
- [📂 Estrutura de Pastas](#-estrutura-de-pastas)
- [📚 Anotações Importantes](#-anotações-importantes)
- [🔧 Comandos Git Essenciais](#-comandos-git-essenciais)
- [🚀 Fluxo de Trabalho com Git](#-fluxo-de-trabalho-com-git)
- [✨ Boas Práticas de Commit](#-boas-práticas-de-commit)
- [👣 Próximos Passos](#-próximos-passos)
- [📞 Contato](#-contato)

---

## 📘 Sobre o Repositório

Este repositório existe para acompanhar minha evolução como **desenvolvedor Front-End**.

Aqui eu documento:

- Minhas anotações de estudo
- Códigos de treino
- Exercícios das aulas
- Pequenos projetos pessoais
- Testes com **HTML**, **CSS** e **JavaScript**

---

## 📂 Estrutura de Pastas

- [Background e Colors](/BackGround%20e%20Colors/)
- [Box Model](/Box%20Model/)
- [Cinema](/Cinema/)
- [Estilos do Browser](/Estilos%20do%20%20Browser/)
- [web](/web/)
- [README](/README.md/)

> Essa estrutura vai crescer conforme eu evoluir nos estudos.

---

## 📚 Anotações Importantes

### 🔸 Fundamentos de HTML

- Tags essenciais

  - **Tag `<div>`:**
    ```html
    <div></div>
    ```
    _Usada como um contêiner genérico para agrupar elementos e estruturar a página. Muito utilizada na construção de layouts._

- Atributos

  - **O que são? Informações extras usadas dentro das tags para configurar comportamento, identificação e estilo.**
  - **Principais atributos essenciais:**
  - **id — identifica um elemento único:**
    ```html
    <div id="menu"></div>
    ```
  - **class — agrupa elementos para estilização:**
    ```html
    <p class="descricao"></p>
    ```
  - **src — caminho de imagens/scripts:**
    ```html
    <img src="foto.png" />
    ```
  - **href — usado em links:**
    ```html
    <a href="https://google.com">Google</a>
    ```
  - **alt — descrição de imagem (acessibilidade):**
    ```html
    <img src="foto.png" alt="Foto de perfil" />
    ```
  - **type — define o tipo de inputs:**
    ```html
    <input type="text" />
    ```
  - **title — mostra uma dica ao passar o mouse**
    ```html
    <button title="Enviar formulário">Enviar</button>
    ```

- HTML semântico
  > (Vou preencher mais tarde)
- Estrutura base (super importante!)

  - **Modelo inicial obrigatório de qualquer página HTML. Serve como ponto de partida para estruturar todo o documento.**

    ```html
    <!DOCTYPE html>
    <html lang="pt-br">
      <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Título da Página</title>
        <link rel="stylesheet" href="style.css" />
      </head>
      <body>
        <!-- Conteúdo aqui -->
      </body>
    </html>
    ```

    _Essa é a estrutura mínima de uma página HTML, usada em **todo projeto**_

### 🔸 Fundamentos de CSS

- Seletores

  - **Seletor universal `*`:**
    ```css
    * {
      box-shadow: inset 0 0 0 1px rgba(255, 0, 0, 0.5);
    }
    ```
    _Usado para visualizar todos os elementos, adicionando uma borda interna vermelha. Útil para depuração._

- 🎨 Estilos de Navegador (User Agent Stylesheet)  
  Cada navegador aplica estilos padrões no HTML.  
  Exemplos:
  - **`<a>`→ cor azul + sublinhado:**
  - **`<button>`→ borda, padding e background padrão:**
  - **`<h1>`→ tamanho de fonte grande:**
  - **`<p>`→ margem própria:**

_Esses estilos podem variar entre browsers, então é comum sobrescrever ou resetar esses padrões para garantir consistência._

- 🧬 Herança no CSS (inherit)  
  Algumas propriedades são herdadas automaticamente pelos elementos filhos:

  - **`color`**
  - **`font-family`**
  - **`line-height`**
    Já outras, não são herdadas, como:
  - **`background`**
  - **`border`**
  - **`width`/`height`**
    E alguns elementos ignoram parte da herança, como:
  - **`<a>`→ não herda a cor automaticamente**
  - **`<button>`→ praticamente nada é herdado (borda, fundo, cor vêm do navegador)**  
     -**Exemplo utilizado:**

    ```css
    body {
      color: seagreen;
    }

    a {
      color: inherit;
    }
    ```

_Assim, quando o `body` muda de cor, todos os elementos — inclusive os links — acompanham automaticamente, deixando o código mais limpo e fácil de manter._

- 🔘 Comportamento do `<button>`  
  O elemento `<button>` possui um estilo próprio do navegador e não herda:

  - **cor do texto**
  - **borda**
  - **background**

Se quisermos deixá-lo “cru” e estilizar 100% manualmente:

```css
button {
  color: inherit;
  background: none;
  border: none;
  padding: 0;
}
```

_Isso remove os estilos padrão e passa a usar a cor do elemento pai._

- Flexbox
- Grid
- Responsividade

  ### 🔸 Fundamentos de JavaScript

  - Variáveis
  - Funções
  - DOM
  - Arrays e Objetos

  > (Vou preencher conforme estudo.)

  ***

  ## 🔧 Comandos Git Essenciais

  ### 🔹 Inicializar o Git

  ```bash
  git init
  ```

  ### 🔹 Adicionar arquivos ao commit

  ```bash
  git add .
  ```

  ### 🔹 Criar um commit

  ```bash
  git commit -m "mensagem"
  ```

  ### 🔹 Enviar para o GitHub (primeira vez)

  ```bash
  git push -u origin main
  ```

  ### 🔹 Enviar atualizações

  ```bash
  git push
  ```

  ### 🔹Baixar atualizações

  ```bash
  git pull
  ```

  ### 🔹Ver status do que foi modificado

  ```bash
  git status
  ```

  ***

  ### 🚀 Fluxo de Trabalho com Git

  Alterar algo:

  ```bash
  git add .
  ```

  Registrar alteração:

  ```bash
  git commit -m "descrição"
  ```

  Enviar pro GitHub:

  ```bash
  git push
  ```

  Atualizar projeto local:

  ```bash
  git pull
  ```

  ***

  ### ✨ Boas Práticas de Commit

  ❌ Evite:

  ```bash
  git commit -m "aaa"
  git commit -m "teste"
  git commit -m "arrumei"
  ```

  ✔️ Prefira:

  ```bash
  git commit -m "Adiciona seção de HTML semântico"
  git commit -m "Corrige bug no menu responsivo"
  ```

  ***

  ### 👣 Próximos Passos

  - 🖌️ Criar **README** específico para cada projeto

  - ➕ Adicionar exercícios de **Flexbox**

  - ✍️ Estudar e anotar **Grid Layout**

  - 📖 Criar primeiros mini projetos com **JS**

  - 📸 Adicionar GIFs de demonstração dos **projetos**

  ***

  ### 📞 Contato

  📱 (11) 95682-5748

  📧 Enzo.lemos05@gmail.com

  🔗 https://www.linkedin.com/in/enzo-lemos-599530270/

  ***
