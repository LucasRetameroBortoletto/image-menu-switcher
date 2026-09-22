# Image Menu Switcher

Página simples em HTML, CSS e JavaScript puro que exibe uma imagem de fundo em tela cheia e um menu flutuante para trocar entre diferentes wallpapers com um clique.

## Demonstração

A página abre com um wallpaper padrão e um menu de navegação (com efeito de vidro fosco) fixado na parte inferior da tela. Ao clicar em uma das opções do menu, o item correspondente é destacado e a imagem de fundo é trocada instantaneamente.

## Estrutura do projeto

```
image-menu-switcher-main/
├── index.html          # Estrutura, estilos e lógica da página
├── README.md
└── assets/
    ├── wallpaper1.jpg
    ├── wallpaper2.png
    └── wallpaper3.jpg
```

## Como usar

Basta abrir o arquivo `index.html` em qualquer navegador — não há dependências externas nem necessidade de servidor.

```bash
# opcional: subir um servidor local
python3 -m http.server
```

Depois acesse `http://localhost:8000` (se usar o servidor local) ou abra o `index.html` diretamente.

## Funcionalidades

- **Troca de imagem de fundo**: três itens de menu (IMG1, IMG2, IMG3) alternam o `src` da imagem exibida em tela cheia.
- **Indicador de item ativo**: o item selecionado recebe a classe `active`, destacando-o visualmente; o item selecionado inicialmente é o IMG1.
- **Texto alternativo dinâmico**: o atributo `alt` da imagem é atualizado a cada troca, descrevendo a cena para acessibilidade.
- **Menu com efeito de vidro (glassmorphism)**: fundo semitransparente com `backdrop-filter: blur()` e contorno destacado ao passar o mouse.
- **Totalmente responsivo em largura**: a imagem ocupa 100% da largura e altura da viewport.

## Personalização

Para adicionar ou trocar wallpapers:

1. Coloque a nova imagem na pasta `assets/`.
2. Adicione um novo `<li>` no menu (`<nav><ul>`) em `index.html`.
3. Crie um novo `addEventListener('click', ...)` no `<script>`, seguindo o padrão dos já existentes, apontando para o novo arquivo e ajustando as classes `active`.

## Tecnologias

- HTML5
- CSS3 (Flexbox, `backdrop-filter`, transições)
- JavaScript (DOM puro, sem frameworks)

## Licença

Defina a licença de sua preferência (ex.: MIT) caso pretenda distribuir este projeto.
