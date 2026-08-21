# 🚀 Portfolio — Guia de Personalização e Deploy

## 📁 Estrutura do projeto

```
portfolio/
├── index.html       ← Todo o portfólio (HTML + CSS + JS)
├── vite.config.js   ← Configuração do Vite
├── package.json     ← Dependências
├── vercel.json      ← Configuração do deploy
└── README.md        ← Este arquivo
```

---

## ✏️ Como personalizar

### 1. Seus dados pessoais
Edite a seção `<title>` e as variáveis CSS no `index.html`:
```css
:root {
  --accent:  #c8f135;   /* ← Mude a cor de destaque principal */
  --accent2: #ff6b35;   /* ← Mude a cor de destaque secundária */
  --bg:      #0a0a0a;   /* ← Cor de fundo */
  --text:    #f0ede8;   /* ← Cor do texto */
}
```

### 2. Textos e conteúdo
Busque por `[Seu Nome]` no arquivo e substitua pelo seu nome real.
Edite também:
- **Hero**: título principal e descrição
- **Sobre**: bio, habilidades, foto
- **Projetos**: nome, descrição, tags, links
- **Experiência**: empresas, cargos, datas
- **Contato**: e-mail, links das redes sociais

### 3. Sua foto
No bloco `#about`, troque a URL da imagem:
```html
<img src="SUA_FOTO_AQUI.jpg" alt="Foto de perfil" />
```
Coloque sua foto na pasta raiz do projeto ou use uma URL pública.

### 4. Links dos projetos
Em cada `.project-card`, edite os `href="#"` com os links reais:
```html
<a href="https://seusite.com" class="project-link">↗ Live Demo</a>
<a href="https://github.com/..." class="project-link">⌥ GitHub</a>
```

### 5. Redes sociais
Edite os `href="#"` na seção `.socials`:
```html
<a href="https://linkedin.com/in/seuusuario" class="social-link">LinkedIn</a>
<a href="https://github.com/seuusuario" class="social-link">GitHub</a>
```

### 6. Contador de estatísticas
No Hero, edite os valores `data-count`:
```html
<div class="stat-num" data-count="42">  ← projetos entregues
<div class="stat-num" data-count="5">   ← anos de experiência
<div class="stat-num" data-count="18">  ← clientes satisfeitos
```

### 7. Formulário de contato
O formulário está simulado. Para conectar com um serviço real, use:
- **Formspree**: https://formspree.io (gratuito, sem backend)
- **EmailJS**: https://emailjs.com (gratuito, sem backend)
- **Netlify Forms** / **Vercel Functions** (se quiser backend próprio)

Exemplo com Formspree — substitua a função `submitForm()`:
```html
<form action="https://formspree.io/f/SEU_ID" method="POST">
  ...
</form>
```

---

## 🌐 Deploy no Vercel

### Opção 1 — Via GitHub (recomendado)
1. Crie um repositório no GitHub e faça push do projeto:
```bash
git init
git add .
git commit -m "primeiro commit"
git remote add origin https://github.com/seuusuario/portfolio.git
git push -u origin main
```

2. Acesse https://vercel.com e clique em **"Add New Project"**
3. Importe o repositório do GitHub
4. Clique em **Deploy** — pronto! 🎉

A partir daí, qualquer `git push` atualiza o site automaticamente.

### Opção 2 — Via Vercel CLI
```bash
npm install -g vercel
vercel login
vercel
```

### Opção 3 — Drag & Drop
Acesse https://vercel.com/new, faça login e arraste a pasta do projeto.

---

## 🎨 Customizações avançadas

### Trocar fontes
Edite o link do Google Fonts e as variáveis CSS:
```css
--font-head: 'Syne', sans-serif;
--font-body: 'DM Mono', monospace;
--font-serif: 'Instrument Serif', serif;
```

### Adicionar projetos
Copie um bloco `.project-card` e edite o conteúdo. Use as classes:
- `.featured` — ocupa 7 colunas (maior)
- `.small` — ocupa 5 colunas
- `.wide` — ocupa todas as 12 colunas

### Adicionar experiências
Copie um bloco `.exp-item` na seção `#experience`.

### Mudar tema para claro
Substitua no `:root`:
```css
--bg:      #f5f5f0;
--surface: #eeede8;
--border:  #ddd;
--text:    #0a0a0a;
--muted:   #666;
```

---

## 📱 Responsividade
O portfólio é totalmente responsivo:
- **Desktop**: layout completo com grid e cursor customizado
- **Tablet (< 900px)**: coluna única, menu hamburguer
- **Mobile (< 600px)**: cursor desabilitado, estatísticas ocultas

---

Feito com ☕ — Boa sorte no seu portfólio!
