# Aula 01 - HTML5 - Estrutura Básica de uma página
> Vamos começar com uma demonstração prática da estrutura básica do HTML5 e explicar cada elemento essencial. 
>
> O HTML5 é a linguagem de marcação mais recente usada para criar páginas web. Ele fornece uma estrutura clara e semântica, o que facilita a organização e a interpretação do conteúdo tanto para desenvolvedores quanto para navegadores e mecanismos de busca.
---

## :one: **Estrutura mínima de uma Página HTML5**

Aqui está um exemplo **mínimo** de uma página `HTML5`:

:spider_web: **Código** : 
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de Estrutura HTML5</title>
    <meta name="description" content="Uma página de exemplo para demonstrar a estrutura básica do HTML5.">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    
</body>
</html>
```

---

### :bookmark: **Explicação dos Elementos**

Agora, vamos detalhar cada parte da estrutura acima:

#### 1. `<!DOCTYPE html>`
- Declara que o documento está escrito em HTML5.
- É obrigatório e deve ser a primeira linha do arquivo.

#### 2. `<html lang="pt-BR">`
- Define o início do documento HTML.
- O atributo `lang` especifica o idioma da página (neste caso, português do Brasil).

#### 3. `<head>`
- Contém metadados sobre a página, como o título, descrição, conjunto de caracteres e links para arquivos externos (CSS, por exemplo).
- Elementos importantes no `<head>`:
  - `<meta charset="UTF-8">`: Define o conjunto de caracteres usado na página.
  - `<meta name="viewport" ...>`: Garante que a página seja responsiva em dispositivos móveis.
  - `<title>`: Define o título exibido na aba do navegador.
  - `<link>`: Conecta folhas de estilo CSS externas.

#### 4. `<body>`
- Contém todo o conteúdo visível da página, como texto, imagens, links, etc.


## :two: **Estrutura Básica de uma Página HTML5**

Aqui está um exemplo **simples** de uma página `HTML5`, este exemplo inclui um o uso de algumas tags utilizadas no corpo da página e que possuem valor semântico. 

:spider_web: **Código** : 
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de Estrutura HTML5</title>
    <meta name="description" content="Uma página de exemplo para demonstrar a estrutura básica do HTML5.">
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Elemento HEADER --> 
    <header>
        <h1>Título Principal do Site</h1>
        <nav>
            <ul>
                <li><a href="#section1">Seção 1</a></li>
                <li><a href="#section2">Seção 2</a></li>
                <li><a href="#footer">Rodapé</a></li>
            </ul>
        </nav>
    </header>

    <!-- Ememento MAIN - Área principal da página -->
    <main>
        <section id="section1">
            <h2>Seção 1: Introdução</h2>
            <p>Esta é a primeira seção da página. Aqui você pode adicionar informações introdutórias.</p>
        </section>

        <section id="section2">
            <h2>Seção 2: Conteúdo Detalhado</h2>
            <article>
                <h3>Artigo 1</h3>
                <p>Este é um artigo dentro da Seção 2. Cada artigo deve ser independente e autoexplicativo.</p>
            </article>
            <article>
                <h3>Artigo 2</h3>
                <p>Outro artigo dentro da mesma seção. Use tags de cabeçalho para organizar o conteúdo.</p>
            </article>
        </section>
    </main>

    <!-- Elemento FOOTER - Roda-pé da página --> 
    <footer id="footer">
        <p>&copy; 2025 - Todos os direitos reservados.</p>
    </footer>
</body>
</html>
```

---

### :bookmark: **Explicação dos Elementos**

Agora, vamos detalhar cada parte da estrutura acima:

1. **Elemento `<header>`**
    - Representa o cabeçalho da página ou de uma seção.
    - Geralmente contém o título principal (`<h1>`) e a navegação (`<nav>`).

1. **Elemento `<nav>`**
    - Usado para agrupar links de navegação.
    - No exemplo, há uma lista não ordenada (`<ul>`) com links para diferentes partes da página.

1. **Elemento `<main>`**
    - Define o conteúdo principal da página.
    - Deve ser único e conter as informações mais relevantes.

1. **Elemento `<section>`**
    - Representa uma seção genérica de conteúdo.
    - No exemplo, temos duas seções (`Seção 1` e `Seção 2`), cada uma com seu próprio título (`<h2>`).

1. **Elemento `<article>`**
    - Usado para conteúdos independentes, como posts de blog, notícias ou artigos.
    - No exemplo, cada artigo tem seu próprio título (`<h3>`).

1. **Elemento `<footer>`**
    - Representa o rodapé da página ou de uma seção.
    - Geralmente contém informações de direitos autorais, links adicionais ou contato.

1. **Elementos `<h1>` a `<h6>`**
    - São títulos hierárquicos, onde `<h1>` é o mais importante e `<h6>` o menos importante.
    - No exemplo, `<h1>` é o título principal da página, enquanto `<h2>` e `<h3>` são usados para organizar subseções.

1. **Elemento `<p>`**
    - Define parágrafos de texto.
    - No exemplo, cada seção e artigo contém parágrafos para explicar o conteúdo.

---

### :loudspeaker: **Organização de uma Página Web**

A estrutura típica de uma página `web` segue este fluxo:

1. **Cabeçalho (`<header>`):**
   - Pode conter o logotipo, título principal e menu de navegação.
   - É a primeira área que os visitantes veem.

2. **Conteúdo Principal (`<main>`):**
   - Geralmente esta área é dividido em seções (`<section>`) e artigos (`<article>`).
   - Organizado de forma lógica e hierárquica usando títulos (`<h1>` a `<h6>`).

3. **Rodapé (`<footer>`):**
   - Fica no final da página.
   - Contém informações adicionais, como links úteis, direitos autorais ou redes sociais.

---

## :three: Referências

- [HTML Tutorial](https://www.w3schools.com/html/default.asp)