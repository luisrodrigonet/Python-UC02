# Aula 01 - HTML5 - Adicionando suporte a bootstrap
>
> Para atualizar  a página `básica` e integrar a versão mais recente do **Bootstrap**, precisamos incluir o `CSS` e o `JavaScript` do `Bootstrap` via CDN (Content Delivery Network). 
> O `Bootstrap` é uma biblioteca de `design` responsivo que facilita a criação de layouts modernos e adaptáveis para dispositivos móveis, `tablets` e `desktops`.
---

## :one: **Página HTML5 com Bootstrap**

:spider_web: **Código** :
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de Estrutura HTML5 com Bootstrap</title>
    <meta name="description" content="Uma página de exemplo para demonstrar a estrutura básica do HTML5 com Bootstrap.">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">

    <!-- Estilos personalizados (opcional) -->
    <style>
        body {
            padding: 20px;
        }
        header {
            margin-bottom: 20px;
        }
        footer {
            margin-top: 40px;
            padding-top: 20px;
            background-color: #f8f9fa;
        }
    </style>
</head>
<body>

    <!-- Cabeçalho -->
    <header class="container">
        <div class="d-flex justify-content-between align-items-center">
            <h1 class="text-primary">Título Principal do Site</h1>
            <nav>
                <ul class="nav">
                    <li class="nav-item"><a href="#section1" class="nav-link">Seção 1</a></li>
                    <li class="nav-item"><a href="#section2" class="nav-link">Seção 2</a></li>
                    <li class="nav-item"><a href="#footer" class="nav-link">Rodapé</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Conteúdo principal -->
    <main class="container">
        <section id="section1" class="mb-5">
            <h2 class="text-success">Seção 1: Introdução</h2>
            <p class="lead">Esta é a primeira seção da página. Aqui você pode adicionar informações introdutórias.</p>
        </section>

        <section id="section2" class="mb-5">
            <h2 class="text-info">Seção 2: Conteúdo Detalhado</h2>

            <article class="card mb-3">
                <div class="card-body">
                    <h3 class="card-title text-warning">Artigo 1</h3>
                    <p class="card-text">Este é um artigo dentro da Seção 2. Cada artigo deve ser independente e autoexplicativo.</p>
                </div>
            </article>

            <article class="card">
                <div class="card-body">
                    <h3 class="card-title text-danger">Artigo 2</h3>
                    <p class="card-text">Outro artigo dentro da mesma seção. Use tags de cabeçalho para organizar o conteúdo.</p>
                </div>
            </article>
        </section>
    </main>

    <!-- Rodapé -->
    <footer id="footer" class="container text-center">
        <p class="text-muted">&copy; 2023 - Todos os direitos reservados.</p>
    </footer>

    <!-- Bootstrap JS e dependências -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

---

### :bookmark: **Explicação das Alterações**

#### **Inclusão do Bootstrap via CDN**:

No `<head>`, foi adicionado o `link` para o arquivo CSS do Bootstrap:
 ```html
 <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">
 ```

No final do `<body>`, foi incluído o `script` do Bootstrap, que contém o JavaScript necessário para funcionalidades interativas (como menus dropdown, modais, etc.):
 ```html
 <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
 ```
 
### **Visão Geral**

- **Cabeçalho (`<header>`):**
  - O título principal (`<h1>`) e o menu de navegação são organizados usando flexbox (`d-flex`).
  - Os links de navegação são estilizados com as classes `nav` e `nav-link`.

- **Conteúdo Principal (`<main>`):**
  - As seções são separadas com margens (`mb-5`) para melhorar a legibilidade.
  - Os artigos são exibidos como cartões (`card`), com títulos e textos bem organizados.

- **Rodapé (`<footer>`):**
  - Centralizado com a classe `text-center`.
  - Usa a classe `text-muted` para aplicar uma cor mais suave ao texto.

####  **Classes do Bootstrap**:


| Elemento  | Explicação |
|-----------|------------|
| `<header class="container">` | **`container`**: Define uma área centralizada com margens automáticas. |
| `<div class="d-flex justify-content-between align-items-center">` | **`d-flex`, `justify-content-between`, `align-items-center`**: Usadas no cabeçalho para alinhar o título e o menu horizontalmente. |
| `<ul class="nav">` `<li class="nav-item"><a href="#section1" class="nav-link">Seção 1</a></li>` | **`nav`, `nav-item`, `nav-link`**: Criam um menu de navegação estilizado.|
| `<section id="section1" class="mb-5"> `| **`mb-5` (margin-bottom)**: Adiciona margem inferior às seções para melhorar o espaçamento. |
| `<article class="card">` | **`card`**: Estiliza os artigos como cartões, proporcionando um visual moderno. |
| `<p class="lead">` | **`lead`**:Destaca o texto inicial da seção. |
| `<h2 class="text-success">` |  **`text-*` classes**: Aplicam cores específicas ao texto (ex.: `text-primary`, `text-success`, etc.). |


#### **Elemento `<nav>`**

- **Finalidade**: Agrupa links de navegação.
- **Uso**: Usado para criar menus de navegação, como barras de navegação horizontais ou laterais.
- **Bootstrap Classes**:
  - `nav`, `nav-item`, `nav-link`: Estilizam os links de navegação.
- **Exemplo Prático**:
  ```html
  <nav>
      <ul class="nav">
          <li class="nav-item"><a href="#section1" class="nav-link">Seção 1</a></li>
          <li class="nav-item"><a href="#section2" class="nav-link">Seção 2</a></li>
      </ul>
  </nav>
  ```

#### **Classe (Bootstrap) `card`**
- **Finalidade**: Estiliza o conteúdo como um cartão visualmente destacado.
- **Uso**: Útil para exibir informações de forma organizada e esteticamente agradável.
- **Exemplo Prático**:
  ```html
  <article class="card">
      <div class="card-body">
          <h3 class="card-title">Artigo 1</h3>
          <p class="card-text">Este é um artigo dentro de um cartão.</p>
      </div>
  </article>
  ```


####  **Responsividade**:

O `Bootstrap` ajusta automaticamente o layout para diferentes tamanhos de tela, garantindo que a página seja visualizada corretamente em dispositivos móveis e desktops.

####  **Estilos Personalizados**:

Foram mantidos alguns estilos personalizados no `<style>` para complementar o design do `Bootstrap`.


## :two: Referências:

- [Get started with Bootstrap 5.3](https://getbootstrap.com/docs/5.3/getting-started/introduction/)
- [Bootstrap 5 Tutorial](https://www.w3schools.com/bootstrap5/index.php)
- [Get started with Bootstrap 4.0](https://getbootstrap.com/docs/4.0/getting-started/introduction/)
- [Bootstrap 4 Tutorial](https://www.w3schools.com/bootstrap4/default.asp)
