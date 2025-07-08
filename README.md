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

## 🧩 Componentes

### 1. App.vue (Componente Raiz)

**Localização**: `src/App.vue`

**Responsabilidades**:
- Estrutura principal da aplicação
- Composição dos componentes principais
- Configuração de layout global

**Características**:
- Layout responsivo
- Overflow hidden para evitar scroll horizontal
- Altura mínima de 100vh

### 2. PortfolioHero.vue

**Localização**: `src/components/PortfolioHero.vue`

**Responsabilidades**:
- Seção hero principal
- Navegação
- Apresentação do profissional
- Efeitos visuais de fundo

**Características**:
- Background com gradientes animados
- Linhas geométricas animadas
- Elementos flutuantes
- Navegação responsiva
- Botões de ação
- Links para redes sociais

**Efeitos Visuais**:
- Linhas horizontais, verticais e diagonais animadas
- Pulsos de energia
- Grid animado
- Elementos flutuantes com gradientes

### 3. AboutSection.vue

**Localização**: `src/components/AboutSection.vue`

**Responsabilidades**:
- Apresentação sobre o profissional
- Estatísticas de experiência
- Cards de serviços
- Seção de habilidades

**Características**:
- Círculo de experiência com efeito 3D
- Cards de serviços interativos
- Estatísticas animadas
- Background com elementos flutuantes

**Dados Exibidos**:
- 10+ anos de experiência
- 241 projetos completados
- 150+ clientes satisfeitos
- 25+ prêmios conquistados

### 4. ProjectsSection.vue

**Localização**: `src/components/ProjectsSection.vue`

**Responsabilidades**:
- Exibição de projetos
- Habilidades técnicas
- Experiência profissional
- Educação

**Características**:
- Grid de projetos responsivo
- Cards de projeto interativos
- Barras de progresso animadas
- Timeline de experiência
- Seção de educação

**Habilidades Exibidas**:
- **Design**: UI/UX, Figma, Adobe XD, Sketch
- **Desenvolvimento**: JavaScript, React, Vue.js, Node.js

### 5. FooterSection.vue

**Localização**: `src/components/FooterSection.vue`

**Responsabilidades**:
- Informações de contato
- Links rápidos
- Newsletter
- Redes sociais

**Características**:
- Layout em grid responsivo
- Formulário de newsletter
- Links de navegação
- Informações de contato
- Efeitos de hover

### 6. ScrollToTop.vue

**Localização**: `src/components/ScrollToTop.vue`

**Responsabilidades**:
- Botão de scroll para o topo
- Indicador de progresso
- Animação de água

**Características**:
- Aparece após 20% do scroll
- Animação de água baseada no progresso
- Efeito de hover
- Scroll suave

### 7. Componentes UI

#### BlurReveal.vue
**Localização**: `src/components/ui/blur-reveal/BlurReveal.vue`

**Propósito**: Animação de revelação com efeito blur

**Props**:
- `duration`: Duração da animação (default: 1s)
- `delay`: Delay entre elementos (default: 0.2s)
- `blur`: Intensidade do blur (default: 20px)
- `yOffset`: Offset vertical (default: 20px)

#### Button.vue
**Localização**: `src/components/ui/button/Button.vue`

**Propósito**: Componente de botão reutilizável

**Props**:
- `variant`: Variante do botão
- `size`: Tamanho do botão
- `as`: Elemento HTML (default: button)

#### NeonBorder.vue
**Localização**: `src/components/ui/neon-border/NeonBorder.vue`

**Propósito**: Borda com efeito neon animado

**Props**:
- `color1`: Primeira cor do gradiente (default: #ec4899)
- `color2`: Segunda cor do gradiente (default: #ef4444)
- `animationType`: Tipo de animação (none/half/full)
- `duration`: Duração da animação (default: 4s)

---

## 🎨 Estilos e Design System

### Sistema de Cores

```css
/* Cores Primárias */
--pink-500: #ec4899
--red-500: #ef4444
--purple-600: #9333ea

/* Gradientes */
.gradient-primary: linear-gradient(135deg, #ec4899 0%, #ef4444 100%)
.gradient-text: linear-gradient(135deg, #ec4899 0%, #ef4444 100%)

/* Cores de Fundo */
--background: #0f0f0f (dark mode)
--card: rgba(255, 255, 255, 0.1)
```

### Tipografia

```css
/* Fontes */
font-family: 'Inter', ui-sans-serif, system-ui, sans-serif
font-family: 'Poppins', ui-sans-serif, system-ui, sans-serif

/* Tamanhos */
text-xs: 0.75rem
text-sm: 0.875rem
text-base: 1rem
text-lg: 1.125rem
text-xl: 1.25rem
text-2xl: 1.5rem
text-3xl: 1.875rem
text-4xl: 2.25rem
text-5xl: 3rem
text-6xl: 3.75rem
text-7xl: 4.5rem
```

### Efeitos Visuais

#### Glass Effect
```css
.glass {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
}
```

#### Neon Border
```css
.neon-border {
  filter: blur(1px) drop-shadow(0 0 12px #ec4899);
}
```

#### Gradient Background
```css
.gradient-bg {
  background: linear-gradient(135deg, #ec4899 0%, #ef4444 100%);
}
```

---

## ✨ Animações e Efeitos

### Animações CSS

#### Float Animation
```css
@keyframes float {
  0%, 100% { transform: translateY(0px); }
  50% { transform: translateY(-20px); }
}
```

#### Pulse Glow
```css
@keyframes pulse-glow {
  0%, 100% { box-shadow: 0 0 20px rgba(236, 72, 153, 0.5); }
  50% { box-shadow: 0 0 40px rgba(236, 72, 153, 0.8); }
}
```

#### Neon Border Animation
```css
@keyframes neon-border {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
```

### Animações JavaScript

#### Scroll Reveal
- Detecta quando elementos entram na viewport
- Aplica animações baseadas na posição
- Suporte a diferentes tipos de animação

#### Motion Plugin
- Integração com @vueuse/motion
- Animações baseadas em scroll
- Transições suaves

### Efeitos de Hover

#### Hover Lift
```css
.hover-lift:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
}
```

#### Scale Effect
```css
.group-hover:scale-110 {
  transform: scale(1.1);
}
```

---

## 📱 Responsividade

### Breakpoints

```css
/* Mobile First */
sm: 640px   /* Small devices */
md: 768px   /* Medium devices */
lg: 1024px  /* Large devices */
xl: 1280px  /* Extra large devices */
2xl: 1536px /* 2X large devices */
```

### Estratégias Responsivas

#### Grid System
```css
/* Mobile */
grid-cols-1

/* Tablet */
md:grid-cols-2

/* Desktop */
lg:grid-cols-3
```

#### Typography Scaling
```css
/* Mobile */
text-2xl md:text-4xl lg:text-5xl

/* Responsive spacing */
px-6 md:px-8 lg:px-12
```

#### Navigation
- Menu hambúrguer em mobile
- Navegação horizontal em desktop
- Dropdown menus responsivos

---

## ⚡ Performance

### Otimizações Implementadas

#### Lazy Loading
- Componentes carregados sob demanda
- Imagens otimizadas
- Animações baseadas em viewport

#### CSS Optimization
- Tailwind CSS purged
- Critical CSS inlined
- Unused styles removed

#### JavaScript Optimization
- Tree shaking
- Code splitting
- Bundle optimization

### Métricas de Performance

#### Core Web Vitals
- **LCP (Largest Contentful Paint)**: < 2.5s
- **FID (First Input Delay)**: < 100ms
- **CLS (Cumulative Layout Shift)**: < 0.1

#### Bundle Size
- JavaScript: ~200KB (gzipped)
- CSS: ~50KB (gzipped)
- Images: ~500KB (optimized)

---

## 📜 Scripts Disponíveis

### Desenvolvimento
```bash
npm run dev          # Inicia servidor de desenvolvimento
npm run lint         # Executa ESLint
npm run type-check   # Verifica tipos TypeScript
```

### Produção
```bash
npm run build        # Build para produção
npm run preview      # Preview do build
npm run build-only   # Build sem type-check
```

### Qualidade de Código
```bash
npm run lint         # Lint e auto-fix
```

---

## 🚀 Deploy

### Build para Produção

1. **Execute o build**
```bash
npm run build
```

2. **Arquivos gerados**
```
dist/
├── index.html
├── assets/
│   ├── css/
│   ├── js/
│   └── images/
```

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
