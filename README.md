<div align="center">

# Portfolio Ux

</div>

![Screenshot_1](https://github.com/user-attachments/assets/0350e649-9f2b-4775-b06b-5fe36c073317)

## 🎯 Visão Geral

O **Portfolio Moderno** é uma aplicação web moderna desenvolvida em Vue.js 3 que apresenta um portfólio profissional com design futurista e interativo. A aplicação utiliza tecnologias modernas como TypeScript, Tailwind CSS, e várias bibliotecas de animação para criar uma experiência visual impressionante.

### Características Principais

- **Design Futurista**: Interface com gradientes, efeitos neon e animações fluidas
- **Responsivo**: Adaptável a todos os dispositivos
- **Performance Otimizada**: Carregamento rápido e animações suaves
- **Acessibilidade**: Respeita preferências de movimento reduzido
- **SEO Friendly**: Estrutura semântica e meta tags adequadas

---

## 🛠 Tecnologias Utilizadas

### Core Technologies
- **Vue.js 3.5.17** - Framework JavaScript progressivo
- **TypeScript 5.8.0** - Superset JavaScript com tipagem estática
- **Vite 7.0.0** - Build tool e dev server rápido

### Styling & UI
- **Tailwind CSS 3.4.17** - Framework CSS utilitário
- **PostCSS 8.5.6** - Processador CSS
- **Autoprefixer 10.4.21** - Prefixos CSS automáticos

### Animation & Motion
- **@vueuse/motion 3.0.3** - Biblioteca de animações para Vue
- **motion-v 1.4.0** - Animações baseadas em Vue
- **framer-motion 12.23.0** - Biblioteca de animações
- **tailwindcss-animate 1.0.7** - Animações para Tailwind

### Icons & UI Components
- **Lucide Vue Next 0.525.0** - Ícones modernos
- **@heroicons/vue 2.2.0** - Ícones Heroicons
- **@headlessui/vue 1.7.23** - Componentes UI acessíveis
- **@tanstack/vue-table 8.21.3** - Componente de tabela

### Utilities
- **@vueuse/core 13.5.0** - Utilitários Vue
- **class-variance-authority 0.7.1** - Sistema de variantes de classes
- **clsx 2.1.1** - Utilitário para classes condicionais
- **tailwind-merge 3.3.1** - Merge de classes Tailwind

### Fonts
- **@fontsource/inter 5.2.6** - Fonte Inter
- **@fontsource/poppins 5.2.6** - Fonte Poppins
- **@fortawesome/fontawesome-free 6.7.2** - FontAwesome

### Development Tools
- **ESLint 9.29.0** - Linter JavaScript
- **Vue TSC 2.2.10** - Type checking para Vue
- **Vite Plugin Vue DevTools 7.7.7** - DevTools para Vue

---

## 📁 Estrutura do Projeto

```
portfolio-moderno/
├── public/                    # Arquivos estáticos
│   ├── about_hero.png        # Imagem da seção about
│   ├── banner_star_mb.png    # Banner mobile
│   ├── bg-down.png           # Background inferior
│   ├── bg-down2.png          # Background inferior 2
│   ├── bg-r.png              # Background direito
│   ├── hero.png              # Imagem hero
│   ├── left-bg.png           # Background esquerdo
│   ├── logo.svg              # Logo da aplicação
│   ├── right-bg.png          # Background direito
│   └── time.png              # Imagem de tempo
├── src/
│   ├── assets/
│   │   ├── favicon.ico       # Favicon
│   │   └── main.css          # Estilos globais
│   ├── components/
│   │   ├── ui/               # Componentes UI reutilizáveis
│   │   │   ├── blur-reveal/  # Componente de revelação com blur
│   │   │   ├── button/       # Componente de botão
│   │   │   └── neon-border/  # Componente de borda neon
│   │   ├── icons/            # Ícones customizados
│   │   ├── AboutSection.vue  # Seção sobre
│   │   ├── FooterSection.vue # Seção rodapé
│   │   ├── PortfolioHero.vue # Seção hero principal
│   │   ├── ProjectsSection.vue # Seção projetos
│   │   └── ScrollToTop.vue   # Botão scroll to top
│   ├── lib/
│   │   └── utils.ts          # Utilitários
│   ├── App.vue               # Componente raiz
│   ├── main.ts               # Ponto de entrada
│   └── vue-shim.d.ts         # Tipos Vue
├── components.json           # Configuração de componentes
├── env.d.ts                  # Tipos de ambiente
├── eslint.config.ts          # Configuração ESLint
├── index.html                # HTML principal
├── package.json              # Dependências e scripts
├── postcss.config.js         # Configuração PostCSS
├── tailwind.config.js        # Configuração Tailwind
├── tsconfig.json             # Configuração TypeScript
├── tsconfig.app.json         # Configuração TS para app
├── tsconfig.node.json        # Configuração TS para node
└── vite.config.ts            # Configuração Vite
```

---

## ⚙️ Configuração e Instalação

### Pré-requisitos
- Node.js 18+ 
- npm ou yarn

### Instalação

1. **Clone o repositório**
```bash
git clone https://github.com/juanfsouza/WebpageUx.git
cd portfolio-moderno
```

2. **Instale as dependências**
```bash
npm install
```

3. **Execute em modo desenvolvimento**
```bash
npm run dev
```

4. **Acesse a aplicação**
```
http://localhost:5173
```

---

## 🏗 Arquitetura da Aplicação

### Estrutura de Componentes

A aplicação segue uma arquitetura baseada em componentes Vue 3 com Composition API:

```
App.vue (Root)
├── PortfolioHero.vue (Hero Section)
├── AboutSection.vue (About Section)
├── ProjectsSection.vue (Projects Section)
├── FooterSection.vue (Footer Section)
└── ScrollToTop.vue (Scroll to Top Button)
```

### Sistema de Componentes UI

```
src/components/ui/
├── blur-reveal/
│   ├── BlurReveal.vue        # Animação de revelação com blur
│   └── index.ts              # Exportações
├── button/
│   ├── Button.vue            # Componente de botão
│   └── index.ts              # Exportações
└── neon-border/
    ├── NeonBorder.vue        # Borda com efeito neon
    └── index.ts              # Exportações
```

### Configuração de Build

- **Vite**: Build tool rápido com HMR
- **TypeScript**: Tipagem estática
- **Tailwind CSS**: Sistema de design utilitário
- **PostCSS**: Processamento CSS avançado

---

### Plataformas de Deploy

#### Vercel
```bash
npm install -g vercel
vercel --prod
```

#### Netlify
```bash
npm install -g netlify-cli
netlify deploy --prod
```

#### GitHub Pages
```bash
npm run build
git add dist
git commit -m "Build for production"
git subtree push --prefix dist origin gh-pages
```

### Configurações de Ambiente

#### Variáveis de Ambiente
```env
VITE_APP_TITLE=Portfolio Moderno
VITE_APP_DESCRIPTION=Portfolio profissional moderno
```

#### Configuração de Base URL
```javascript
// vite.config.ts
export default defineConfig({
  base: process.env.NODE_ENV === 'production' ? '/portfolio-moderno/' : '/',
  // ...
})
```

---

## 🔧 Configurações

### TypeScript
- **tsconfig.json**: Configuração geral
- **tsconfig.app.json**: Configuração para aplicação
- **tsconfig.node.json**: Configuração para Node.js

### ESLint
- **eslint.config.ts**: Regras de linting
- Suporte a Vue 3 e TypeScript
- Auto-fix habilitado

### Tailwind CSS
- **tailwind.config.js**: Configuração do framework
- Cores customizadas
- Animações personalizadas
- Fontes configuradas

### Vite
- **vite.config.ts**: Configuração do build tool
- Aliases configurados
- Plugins habilitados

---
