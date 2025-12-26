---
layout: post
title: "Como Centralizar uma DIV no CSS"
date: 2025-12-26 12:00:00 -0300
categories: [css, frontend, tutorial]
tags: [css, html, web-design, layout]
---

Centralizar elementos na página é uma das tarefas mais comuns no desenvolvimento
web. Neste guia, vou mostrar as principais técnicas para centralizar uma `div`
usando CSS, desde métodos clássicos até soluções modernas.

## 1. Centralização Horizontal com Margin Auto

A forma mais simples de centralizar uma div horizontalmente é usando `margin: auto`.
Este método funciona quando a div tem uma largura definida.

```css
.container {
  width: 300px;
  margin: 0 auto;
}
```

**Quando usar:** Perfeito para centralizar containers de conteúdo, como artigos
ou cards.

## 2. Flexbox: A Solução Moderna

O Flexbox é uma das maneiras mais versáteis de centralizar elementos, tanto
horizontal quanto verticalmente.

```css
.pai {
  display: flex;
  justify-content: center; /* centraliza horizontalmente */
  align-items: center; /* centraliza verticalmente */
  height: 100vh; /* altura da tela */
}
```

**Vantagens:**

- Funciona com elementos de qualquer tamanho
- Centraliza em ambas as direções facilmente
- Responsivo por padrão

## 3. CSS Grid: Controle Total

O Grid oferece uma sintaxe ainda mais limpa para centralização.

```css
.pai {
  display: grid;
  place-items: center; /* centraliza em ambos os eixos */
  height: 100vh;
}
```

**Quando usar:** Ideal para layouts complexos ou quando você já está usando
Grid no projeto.

## 4. Position Absolute: Método Clássico

Uma técnica tradicional que ainda é útil em certos contextos.

```css
.pai {
  position: relative;
}

.filho {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

**Atenção:** O elemento pai precisa ter `position: relative` ou `position: absolute`.

## 5. Text-Align para Elementos Inline

Para centralizar elementos inline ou inline-block dentro de um container.

```css
.pai {
  text-align: center;
}

.filho {
  display: inline-block;
}
```

## Qual Método Escolher?

- **Flexbox:** Use quando precisar de centralização e flexibilidade
- **Grid:** Ideal para layouts bidimensionais complexos
- **Margin auto:** Perfeito para centralização horizontal simples
- **Position absolute:** Quando precisar sobrepor elementos
- **Text-align:** Para conteúdo inline dentro de containers

## Conclusão

Existem várias formas de centralizar uma div no CSS, e a melhor escolha depende
do seu contexto específico. Para a maioria dos casos modernos, **Flexbox**
oferece o melhor equilíbrio entre simplicidade e funcionalidade. Experimente
os diferentes métodos e escolha o que melhor se adapta ao seu projeto!
