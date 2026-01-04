![HTML](https://img.shields.io/badge/HTML-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![VSCode](https://img.shields.io/badge/VSCode-007ACC?style=for-the-badge&logo=visual-studio-code&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)
![Windows](https://img.shields.io/badge/Windows-0078D4?style=for-the-badge&logo=windows&logoColor=white)

# 📘 HTML / CSS / JS — Notes & Studies

Repositório criado para organizar meus estudos de **Front-End**.

Aqui guardo exemplos, exercícios, testes, anotações importantes e pequenos projetos, documentando minha evolução como desenvolvedor.

---

## 📑 Índice

- [📘 Sobre o Repositório](#-sobre-o-repositório)
- [📂 Estrutura de Pastas](#-estrutura-de-pastas)
- [🚗 Projetos](#-projetos)
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
- [Grid](/Grid/)
- [Posicionamento](/Posicionamento/)
- [Top, Right, Bottom, Left](/Top%2C%20Right%2C%20Bottom%2C%20Left/)
- [img](/img/)
- [web](/web/)
- [README Principal](/README.md/)

> Cada pasta de estudo possui seu próprio README com anotações específicas da aula.

---

## 🚗 Projetos

### Carros e Bicicletas

Mini-projeto para praticar **HTML e CSS**, focando em Box Model, cards, links estilizados e organização visual.

- Pasta: [Box Model/Carros e Bicicletas](./Box%20Model/Carros%20e%20Bicicletas/)
- [README do projeto](./Box%20Model/Carros%20e%20Bicletas/README.md)

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
  - **Exemplo utilizado:**

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
  - **Se quisermos deixá-lo “cru” e estilizar 100% manualmente:**

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

  - **Inicializar o git**

    ```c#
    git init
    ```

  - **Adicionar arquivos ao commit**

    ```c#
    git add .
    ```

  - **Criar um commit**

    ```c#
    git commit -m "mensagem"
    ```

  - **Enviar para o GitHub (primeira vez)**

    ```c#
    git push -u origin main
    ```

  - **Enviar atualizações**

    ```c#
    git push
    ```

  - **Baixar atualizações**

    ```c#
    git pull
    ```

  - **Ver status do que foi modificado**

    ```c#
    git status
    ```

  ***

  ## 🚀 Fluxo de Trabalho com Git

  - **Alterar algo:**

    ```c#
    git add .
    ```

  - **Registrar alteração:**

    ```c#
    git commit -m "descrição"
    ```

  - **Enviar pro GitHub:**

    ```c#
    git push
    ```

  - **Atualizar projeto local:**

    ```c#
    git pull
    ```

  ***

  ### ✨ Boas Práticas de Commit

  - ❌ Evite:

    ```c#
    git commit -m "aaa"
    git commit -m "teste"
    git commit -m "arrumei"
    ```

  - ✔️ Prefira:

    ```c#
    git commit -m "Adiciona seção de HTML semântico"
    git commit -m "Corrige bug no menu responsivo"
    ```

---

### 👣 Próximos Passos

- 🖌️ Criar **README** específico para cada projeto

- ➕ Adicionar exercícios de **Flexbox**

- ✍️ Estudar e anotar **Grid Layout**

- 📖 Criar primeiros mini projetos com **JS**

- 📸 Adicionar GIFs de demonstração dos **projetos**

---

### 📞 Contato

📱 (11) 95682-5748

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/enzo-lemos-599530270/)
[![Gmail](https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:enzo.lemos05@gmail.com)

---
