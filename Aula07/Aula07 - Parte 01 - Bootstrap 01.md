# Aula07 - Parte 01 - Bootstrap 01
> O [Bootstrap](https://getbootstrap.com/) é o framework front-end mais popular do mundo, oferecendo:  
> ✔ **Design responsivo** (adaptável a celulares, tablets e desktops)  
> ✔ **Componentes prontos** (botões, cards, navegação)  
> ✔ **Utilitários** (cores, espaçamento, flexbox)  
> 
> Nesta aula, focaremos em:  
> - **Ícones** (`Bootstrap Icons`)  
> - **Containers** (estrutura base)  
> - **Sistema de Grid** (responsividade)  
> - **Cores Contextuais** (feedback visual)  
> - **Cards** (exibição de conteúdo)  
> ---
> 

## :one: **Configuração Inicial**  

### **Estrutura HTML Básica**  
Antes de usar o Bootstrap, inclua no `<head>` e no `<body>` as seguintes linhas:  
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Aula Bootstrap</title>
  <!-- Bootstrap CSS -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
  <!-- Bootstrap Icons -->
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.0/font/bootstrap-icons.css">
</head>
<body>
  <!-- Conteúdo aqui -->
  
  <!-- Bootstrap JS (opcional para componentes interativos) -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

### **O que cada CDN faz?**  
| CDN | Função |  
|------|--------|  
| `bootstrap.min.css` | Estilos principais do Bootstrap |  
| `bootstrap-icons.css` | Biblioteca de ícones |  
| `bootstrap.bundle.min.js` | Funcionalidades JS (dropdowns, modais) |  

---

## :two: **Ícones (Bootstrap Icons)**  

### **Como Usar?**  
Adicione ícones com a classe `bi` + nome do ícone ([lista completa](https://icons.getbootstrap.com/)):  

```html
<i class="bi bi-emoji-smile"></i> Sorriso  
<i class="bi bi-check-circle-fill text-success"></i> Sucesso  
```

### **Exemplo Prático**  
```html
<button class="btn btn-primary">
  <i class="bi bi-download"></i> Baixar
</button>
```


---

## :three: **Containers**  

### **Tipos de Containers**  
| Classe | Comportamento |  
|--------|--------------|  
| `.container` | Largura fixa (responsiva por breakpoint) |  
| `.container-fluid` | Largura 100% da tela |  

### **Exemplo Detalhado**  

```html
<div class="container bg-light border p-4 my-4">
  <h2>Container Padrão</h2>
  <p>Centralizado com margens laterais automáticas.</p>
</div>

<div class="container-fluid bg-dark text-white p-4">
  <h2>Container Fluido</h2>
  <p>Ocupa toda a largura da tela.</p>
</div>
```
**Explicação das classes utilitárias:**  
- `bg-light`: Fundo claro  
- `border`: Borda sutil  
- `p-4`: Padding (espaçamento interno) grande  
- `my-4`: Margem no eixo Y (topo e base)  

---

## :four: **Sistema de Grid**  

### **Como Funciona?**  

- **`.row`**: Define uma linha.  
- **`.col-*`**: Define colunas (total de 12 por linha).  
- **Breakpoints**: `sm` (≥576px), `md` (≥768px), `lg` (≥992px).  

### **Exemplo Responsivo**  
```html
<!-- Container de linhas -->
<div class="container">
  <!-- Linha -->
  <div class="row">
    <!-- 1a Coluna -->
    <div class="col-md-4 bg-info p-3">Coluna 1 (4/12)</div>
    
    <!-- 2a Coluna -->
    <div class="col-md-4 bg-warning p-3">Coluna 2 (4/12)</div>
    
    <!-- 3a Coluna -->
    <div class="col-md-4 bg-danger p-3">Coluna 3 (4/12)</div>
  </div>
  <!-- Final 1a Linha -->
</div>
<!-- Final: Container de linhas -->
```
**Comportamento:**  
- Em telas **menores que 768px**, as colunas ficam empilhadas.  
- Em telas **maiores**, ficam lado a lado.  

---

## :five: **Cores Contextuais**  
### **6.1. Classes Principais**  
| Cor | Texto (`text-*`) | Fundo (`bg-*`) |  
|------|------------------|----------------|  
| Azul | `text-primary` | `bg-primary` |  
| Verde | `text-success` | `bg-success` |  
| Vermelho | `text-danger` | `bg-danger` |  

### **Exemplo Aplicado**  
```html
<div class="p-3 mb-2 bg-gradient">
  <p class="text-primary">Texto azul (primário)</p>
  <p class="bg-dark text-white">Fundo escuro com texto branco</p>
</div>
```

---

## :six: **Cards**  
### **Estrutura Básica**  
```html
<div class="card" style="width: 18rem;">
  <img src="https://via.placeholder.com/300" class="card-img-top" alt="...">
  <div class="card-body">
    <h5 class="card-title">Título do Card</h5>
    <p class="card-text">Descrição ou conteúdo resumido.</p>
    <a href="#" class="btn btn-primary">Ação</a>
  </div>
</div>
```

### **Card com Ícone e Cores**  
```html
<div class="card border-success mb-3">
  <div class="card-header bg-success text-white">
    <i class="bi bi-check-circle"></i> Status
  </div>
  <div class="card-body">
    <h5 class="card-title">Sucesso!</h5>
    <p class="card-text">Operação concluída sem erros.</p>
  </div>
</div>
```

---

## :computer:**Página Completa de Exemplo**  
```html
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exemplo Bootstrap</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.0/font/bootstrap-icons.css">
</head>
<body>
  <!-- Navbar -->
  <nav class="navbar navbar-expand-lg bg-primary navbar-dark">
    <div class="container">
      <a class="navbar-brand" href="#">
        <i class="bi bi-bootstrap"></i> Aula Bootstrap
      </a>
    </div>
  </nav>

  <!-- Container Principal -->
  <div class="container my-5">
    <h1 class="text-center mb-4"><i class="bi bi-code-slash"></i> Componentes Básicos</h1>
    
    <!-- Grid de Cards -->
    <div class="row g-4">
      <div class="col-md-4">
        <div class="card h-100">
          <div class="card-header bg-warning">
            <i class="bi bi-exclamation-triangle"></i> Alerta
          </div>
          <div class="card-body">
            <h5 class="card-title">Atenção</h5>
            <p class="card-text">Este é um card de aviso importante.</p>
            <a href="#" class="btn btn-warning">Saiba mais</a>
          </div>
        </div>
      </div>
      
      <div class="col-md-4">
        <div class="card h-100">
          <img src="https://via.placeholder.com/300x200" class="card-img-top" alt="...">
          <div class="card-body">
            <h5 class="card-title">Card com Imagem</h5>
            <p class="card-text">Exemplo de card com imagem no topo.</p>
          </div>
        </div>
      </div>
      
      <div class="col-md-4">
        <div class="card h-100 border-success">
          <div class="card-body">
            <h5 class="card-title text-success">
              <i class="bi bi-check2-circle"></i> Sucesso
            </h5>
            <p class="card-text">Operação concluída com êxito.</p>
            <button class="btn btn-outline-success">Voltar</button>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Rodapé -->
  <footer class="bg-dark text-white text-center p-4 mt-5">
    <p class="mb-0">Feito com <i class="bi bi-heart-fill text-danger"></i> e Bootstrap</p>
  </footer>

  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

---

## :loudspeaker: **Conclusão**  
Nesta aula, aprendemos:  
- **Ícones**: Como integrar e personalizar.  
- **Containers**: Diferença entre `container` e `container-fluid`.  
- **Grid**: Criar layouts responsivos.  
- **Cores**: Uso de classes utilitárias.  
- **Cards**: Estrutura e variações.  

**Próximos passos:**  
- Explorar [Navbars](https://getbootstrap.com/docs/5.3/components/navbar/).  
- Aprender sobre [Formulários](https://getbootstrap.com/docs/5.3/forms/overview/). 

