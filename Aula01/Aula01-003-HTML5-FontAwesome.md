# Aula 01 - HTML5 - Fonte Awsone
>
> Para incluir o suporte à versão gratuita e do **Font Awesome**, precisamos adicionar o link para o arquivo CSS do Font Awesome via CDN (Content Delivery Network). 
>
> O Font Awesome é uma **biblioteca de ícones vetoriais** que pode ser usada para melhorar a aparência visual da página, adicionando ícones modernos e personalizáveis.
>
---

## :one: **Página HTML5 com Bootstrap e Font Awesome**

:memo: **Código** :
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exemplo de Estrutura HTML5 com Bootstrap e Font Awesome</title>
    <meta name="description" content="Uma página de exemplo para demonstrar a estrutura básica do HTML5 com Bootstrap e Font Awesome.">

    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">

    <!-- Font Awesome CSS -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css" rel="stylesheet">

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
        .icon {
            margin-right: 8px;
        }
    </style>
</head>
<body>

    <!-- Cabeçalho -->
    <header class="container">
        <div class="d-flex justify-content-between align-items-center">
            <h1 class="text-primary"><i class="fas fa-home icon"></i>Título Principal do Site</h1>
            <nav>
                <ul class="nav">
                    <li class="nav-item"><a href="#section1" class="nav-link"><i class="fas fa-info-circle icon"></i>Seção 1</a></li>
                    <li class="nav-item"><a href="#section2" class="nav-link"><i class="fas fa-book icon"></i>Seção 2</a></li>
                    <li class="nav-item"><a href="#footer" class="nav-link"><i class="fas fa-arrow-down icon"></i>Rodapé</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Conteúdo principal -->
    <main class="container">
        <section id="section1" class="mb-5">
            <h2 class="text-success"><i class="fas fa-lightbulb icon"></i>Seção 1: Introdução</h2>
            <p class="lead">Esta é a primeira seção da página. Aqui você pode adicionar informações introdutórias.</p>
        </section>

        <section id="section2" class="mb-5">
            <h2 class="text-info"><i class="fas fa-file-alt icon"></i>Seção 2: Conteúdo Detalhado</h2>

            <article class="card mb-3">
                <div class="card-body">
                    <h3 class="card-title text-warning"><i class="fas fa-pencil-alt icon"></i>Artigo 1</h3>
                    <p class="card-text">Este é um artigo dentro da Seção 2. Cada artigo deve ser independente e autoexplicativo.</p>
                </div>
            </article>

            <article class="card">
                <div class="card-body">
                    <h3 class="card-title text-danger"><i class="fas fa-pen icon"></i>Artigo 2</h3>
                    <p class="card-text">Outro artigo dentro da mesma seção. Use tags de cabeçalho para organizar o conteúdo.</p>
                </div>
            </article>
        </section>
    </main>

    <!-- Rodapé -->
    <footer id="footer" class="container text-center">
        <p class="text-muted"><i class="far fa-copyright icon"></i> 2023 - Todos os direitos reservados.</p>
    </footer>

    <!-- Bootstrap JS e dependências -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

---

## :two: **Explicação das Alterações**

### :bookmark: **Inclusão do Font Awesome**
No `<head>`, foi adicionado o link para o arquivo CSS do Font Awesome:

```html
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.2/css/all.min.css" rel="stylesheet">
```

Isso permite usar os ícones do Font Awesome na página.

### :bookmark: **Adição de Ícones**

Os ícones foram adicionados usando a classe `fas` (ícones sólidos) ou `far` (ícones regulares) seguida pelo nome do ícone. 

**Exemplos**:
  - `<i class="fas fa-home"></i>`: Adiciona um ícone de casa.
  - `<i class="fas fa-info-circle"></i>`: Adiciona um ícone de informação circular.
  - `<i class="fas fa-book"></i>`: Adiciona um ícone de livro.

### :bookmark:  **Classe Personalizada `.icon`**

- Foi criada uma classe `.icon` no CSS para adicionar margem à direita dos ícones, garantindo que haja espaço entre o ícone e o texto ao lado:
  ```css
  .icon {
      margin-right: 8px;
  }
  ```


### :bookmark: **Como Funciona**

1. **Cabeçalho (`<header>`):**
   - O título principal agora inclui um ícone de casa (**`fa-home`**).
   - Os links de navegação também têm ícones, como **`fa-info-circle`** e **`fa-book`**.

2. **Seções (`<section>`):**
   - Cada título de seção tem um ícone relacionado ao conteúdo:
     - **`fa-lightbulb`** para "Introdução".
     - **`fa-file-alt`** para "Conteúdo Detalhado".

3. **Artigos (`<article>`):**
   - Os títulos dos artigos incluem ícones como **`fa-pencil-alt`** e **`fa-pen`** para representar escrita ou edição.

4. **Rodapé (`<footer>`):**
   - O rodapé usa o ícone **`far fa-copyright`** para representar o símbolo de direitos autorais.

---

### :bookmark: **Resultados Visuais**

Com a integração do **Font Awesome**, a página agora possui ícones modernos e estilizados que complementam o design. Isso melhora a experiência do usuário, tornando a interface mais intuitiva e visualmente atraente.

---

## :loudspeaker: **Como Usar o Font Awesome**

1. **Escolha um Ícone**:

   - Acesse o site oficial do Font Awesome ([fontawesome.com](https://fontawesome.com)) e pesquise o ícone desejado.
   - Copie o código HTML fornecido (ex.: **`<i class="fas fa-home"></i>`**).

2. **Personalize o Ícone**:
   - Altere o tamanho usando classes como **`fa-lg`**, **`fa-2x`**, **`fa-3x`**, etc.
   - Altere a cor usando CSS ou classes do Bootstrap, como **`text-primary`**.

3. **Combine com Outros Elementos**:
   - Use ícones em botões, links, títulos ou qualquer outro elemento para destacar informações importantes.
