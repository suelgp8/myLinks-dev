# Documentação Detalhada do Projeto MyLinks Dev

## 📋 Visão Geral

O **MyLinks Dev** é um projeto web simples e moderno inspirado no Linktree, desenvolvido para centralizar links pessoais em um único lugar acessível. Ele permite aos usuários compartilhar múltiplos links de redes sociais, portfólio e outros recursos de forma organizada e visualmente atraente. O projeto foi criado como um exercício de prática em desenvolvimento web, utilizando tecnologias básicas como HTML5, CSS3 e JavaScript.

### 🎯 Objetivo do Projeto

- Centralizar links pessoais para facilitar o compartilhamento.
- Oferecer uma interface responsiva e moderna.
- Implementar alternância entre temas claro e escuro.
- Servir como material de estudo para conceitos de web development.

### 🌐 Acesso ao Projeto

O projeto está hospedado no GitHub Pages e pode ser acessado em: [https://suelgp8.github.io/myLinks-dev/](https://suelgp8.github.io/myLinks-dev/)

## 🏗️ Estrutura do Projeto

A estrutura de arquivos do projeto é simples e organizada:

```
mylinks/
├── index.html          # Arquivo principal HTML
├── style.css           # Estilos CSS (responsivos e com variáveis)
├── script.js           # Lógica JavaScript para alternância de tema
├── README.md           # Documentação básica (já existente)
└── assets/             # Pasta de recursos visuais
    ├── avatar.png      # Imagem de perfil (modo escuro)
    ├── avatar-light.png # Imagem de perfil (modo claro)
    ├── bg-mobile.jpg   # Fundo mobile (modo escuro)
    ├── bg-mobile-light.jpg # Fundo mobile (modo claro)
    ├── bg-desktop.jpg  # Fundo desktop (modo escuro)
    ├── bg-desktop-light.jpg # Fundo desktop (modo claro)
    ├── Cover.jpg       # Imagem de preview para README
    ├── MoonStars.svg   # Ícone para botão de alternância (escuro)
    └── Sun.svg         # Ícone para botão de alternância (claro)
```

## 📁 Descrição Detalhada dos Arquivos

### 1. `index.html`

Este é o arquivo principal que define a estrutura da página web.

**Estrutura HTML:**

- **DOCTYPE e Meta Tags:** Define o documento como HTML5, com charset UTF-8, viewport responsivo e título "My Links-Dev".
- **Links Externos:** Importa fontes do Google Fonts (Inter) e ícones do Ionicons.
- **Corpo da Página:**
  - **Container Principal:** Div com ID `container` que centraliza o conteúdo.
  - **Perfil:** Seção com imagem de avatar e nome de usuário (@suelgp8).
  - **Interruptor de Tema:** Botão para alternar entre modo claro e escuro.
  - **Lista de Links:** Lista não ordenada com links para portfólio, playlist no YouTube e servidor Discord.
  - **Links Sociais:** Ícones para GitHub, Instagram, YouTube e LinkedIn.
  - **Rodapé:** Créditos ao desenvolvedor com link para Instagram.
- **Scripts:** Carrega o Ionicons e o arquivo `script.js`.

**Funcionalidades Implementadas:**

- Links abrem em nova aba (`target="_blank"`).
- Uso de ícones vetoriais do Ionicons para redes sociais.

### 2. `style.css`

Arquivo de estilos que define a aparência visual, responsividade e animações.

**Principais Características:**

- **Reset CSS:** Remove margens e paddings padrão com `* { margin: 0; padding: 0; box-sizing: border-box; }`.
- **Variáveis CSS:** Usa `:root` para definir variáveis de cor e imagens de fundo, facilitando a alternância de tema.
  - Modo escuro: Cores brancas/translúcidas sobre fundo escuro.
  - Modo claro: Cores pretas/translúcidas sobre fundo claro.
- **Layout Responsivo:**
  - Fundo muda automaticamente entre mobile e desktop usando media queries (`@media (min-width: 700px)`).
  - Container centralizado com largura máxima de 588px.
- **Componentes Estilizados:**
  - **Perfil:** Imagem circular de 112px, texto centralizado.
  - **Interruptor:** Botão animado que desliza entre posições (lua/sol).
  - **Links:** Botões com efeito hover, blur de fundo para transparência.
  - **Links Sociais:** Ícones circulares com efeito hover.
- **Animações:** Transições suaves e keyframes para o botão de alternância (`slide-in` e `slide-back`).
- **Tipografia:** Fonte Inter em todos os elementos.

**Técnicas Avançadas:**

- `backdrop-filter: blur(4px)` para efeito de vidro fosco.
- Variáveis CSS para facilitar manutenção e alternância de tema.

### 3. `script.js`

Arquivo JavaScript responsável pela lógica de alternância de tema.

**Função Principal: `toggleMode()`**

- Alterna a classe `"light"` no elemento `<html>`.
- Muda dinamicamente a imagem do avatar entre `avatar.png` (escuro) e `avatar-light.png` (claro).
- Usa `document.documentElement.classList.toggle("light")` para alternar o tema global.
- Seleciona a imagem com `document.querySelector("#profile img")` e altera o atributo `src`.

**Comentários no Código:**

- Inclui lógica comentada para toggle manual (não utilizada).
- Código limpo e comentado para fins educacionais.

### 4. Pasta `assets/`

Contém todos os recursos visuais necessários:

- **Avatares:** Duas versões da foto de perfil para cada tema.
- **Fundos:** Quatro imagens de fundo (mobile/desktop x claro/escuro).
- **Ícones:** SVG para o botão de alternância (lua e sol).
- **Cover:** Imagem para preview no README.

## 🚀 Como Executar o Projeto

### Pré-requisitos

- Navegador web moderno (Chrome, Firefox, Edge, etc.).
- Conexão com internet (para carregar fontes e ícones externos).

### Passos para Execução

1. **Clone o Repositório:**

   ```bash
   git clone https://github.com/suelgp8/myLinks-dev.git
   ```

2. **Navegue até a Pasta:**

   ```bash
   cd myLinks-dev
   ```

3. **Abra no Navegador:**
   - Abra o arquivo `index.html` diretamente no navegador.
   - Ou use um servidor local (opcional, mas recomendado para desenvolvimento):

     ```bash
     # Usando Python
     python -m http.server 8000

     # Ou Node.js com http-server
     npx http-server
     ```

## 📱 Funcionalidades Implementadas

- **Alternância de Tema:** Botão que muda entre modo claro e escuro, alterando cores, fundos e avatares.
- **Responsividade:** Layout adaptável para desktop (≥700px) e mobile.
- **Links Personalizados:** Lista de links principais com hover effects.
- **Redes Sociais:** Ícones clicáveis para plataformas populares.
- **Interface Moderna:** Design clean com efeitos de blur e transições suaves.

## 🛠️ Tecnologias e Conceitos Utilizados

- **HTML5:** Estrutura semântica, meta tags, links externos.
- **CSS3:**
  - Variáveis CSS para temas.
  - Flexbox para layout.
  - Media queries para responsividade.
  - Animações e transições.
  - Filtros de fundo (backdrop-filter).
- **JavaScript:** Manipulação do DOM para alternância de tema.
- **Ionicons:** Biblioteca de ícones vetoriais.
- **Google Fonts:** Fonte Inter para tipografia consistente.

## 🔧 Personalização e Extensões Possíveis

Para adaptar este projeto aos seus estudos ou uso pessoal:

1. **Alterar Links:** Edite a lista `<ul>` em `index.html` com seus próprios links.
2. **Mudar Perfil:** Substitua as imagens em `assets/` e atualize o texto em `#profile p`.
3. **Adicionar Funcionalidades:**
   - Contador de cliques nos links.
   - Animações de entrada.
   - Formulário de contato.
4. **Melhorar Acessibilidade:** Adicione atributos ARIA e navegação por teclado.
5. **Otimização:** Comprimir imagens e minificar CSS/JS para produção.

## 📚 Lições Aprendidas e Conceitos de Estudo

Este projeto demonstra conceitos fundamentais de desenvolvimento web:

- **Estruturação HTML:** Organização semântica de conteúdo.
- **Estilização CSS:** Uso de variáveis, responsividade e efeitos visuais.
- **Interatividade JS:** Manipulação básica do DOM.
- **Design Responsivo:** Adaptação a diferentes tamanhos de tela.
- **Versionamento:** Uso de Git e GitHub para controle de versão.
- **Deploy:** Publicação em GitHub Pages.

## 👨‍💻 Autor

**France Welber** (suelgp8)

- GitHub: [https://github.com/suelgp8](https://github.com/suelgp8)
- LinkedIn: [https://www.linkedin.com/in/suelgp8](https://www.linkedin.com/in/suelgp8)
- Instagram: [https://www.instagram.com/suelgp8](https://www.instagram.com/suelgp8)

## 📝 Notas para Revisão

- **Pontos Fortes:** Código limpo, bem comentado, uso de boas práticas (variáveis CSS, estrutura organizada).
- **Áreas de Melhoria:** Poderia incluir mais comentários em HTML, usar classes CSS mais descritivas, adicionar testes automatizados.
- **Escalabilidade:** Fácil de expandir com mais seções ou funcionalidades.

Esta documentação serve como referência completa para entender, revisar e replicar o projeto em futuros estudos. Você pode usar este template para documentar outros projetos pessoais.
