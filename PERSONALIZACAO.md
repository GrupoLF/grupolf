# 🔧 Guia de Personalização - Grupo LF

Este documento fornece instruções detalhadas sobre como fazer alterações comuns no site do Grupo LF.

---

## 📝 Como Alterar Textos

### Título Principal (Hero)
**Arquivo:** `index.html`  
**Localização:** Linha ~48-50

```html
<h1 class="hero-title">
    Segurança privada profissional para <span class="highlight">empresas</span> e <span class="highlight">condomínios</span>.
</h1>
```

### Telefones de Contato
**Arquivo:** `index.html`  
**Localizações:** Várias (buscar por `3222-3800` e `98118-2729`)

Para alterar todos os telefones de uma vez, use buscar e substituir:
- Buscar: `3222-3800`
- Substituir por: `NOVO-NUMERO`

### Endereço
**Arquivo:** `index.html`  
**Localização:** Seção Footer (linha ~370+)

```html
<li>📍 Rua do Sossego, 1348<br>Santo Amaro, Recife/PE</li>
```

---

## 🎨 Como Alterar Cores

### Método 1: Alterar Variáveis CSS (Recomendado)
**Arquivo:** `css/style.css`  
**Localização:** Início do arquivo (linhas 13-24)

```css
:root {
    --color-primary: #00e676;        /* Verde neon - CTAs */
    --color-secondary: #1e4a8a;      /* Azul médio */
    --color-dark: #0d1b2a;           /* Azul escuro */
    --color-gold: #ffd700;           /* Dourado */
    /* ... outras cores ... */
}
```

**Exemplo:** Para mudar o verde dos botões para laranja:
```css
--color-primary: #ff6b35;
```

### Cores Pré-definidas Sugeridas

**Paleta Azul Profissional:**
```css
--color-primary: #2196F3;
--color-secondary: #1565C0;
--color-dark: #0D47A1;
```

**Paleta Verde Corporativo:**
```css
--color-primary: #4CAF50;
--color-secondary: #388E3C;
--color-dark: #1B5E20;
```

**Paleta Laranja Energia:**
```css
--color-primary: #FF9800;
--color-secondary: #F57C00;
--color-dark: #E65100;
```

---

## 📱 Como Alterar o WhatsApp

### Número do WhatsApp
**Arquivo:** `index.html`  
**Buscar por:** `5581981182729`  
**Substituir por:** `55XX9XXXXXXXX` (código do país + DDD + número)

**Importante:** Manter o formato sem espaços, parênteses ou hífens.

### Mensagem Pré-definida (opcional)
Para adicionar uma mensagem automática ao clicar no WhatsApp:

```html
<!-- DE: -->
<a href="https://wa.me/5581981182729">

<!-- PARA: -->
<a href="https://wa.me/5581981182729?text=Olá! Gostaria de solicitar um orçamento.">
```

---

## 🖼️ Como Adicionar Imagens Reais

### Substituir Ilustrações SVG por Fotos

**1. Hero Section (Imagem Principal)**

**Localização:** `index.html` linha ~70

```html
<!-- REMOVER: -->
<div class="hero-illustration">
    <svg viewBox="0 0 400 400">...</svg>
</div>

<!-- ADICIONAR: -->
<div class="hero-illustration">
    <img src="images/hero-security.jpg" alt="Equipe Grupo LF">
</div>
```

**Não esqueça de:**
1. Criar pasta `images/`
2. Adicionar a imagem otimizada
3. Adicionar CSS para a imagem:

```css
.hero-illustration img {
    width: 100%;
    max-width: 400px;
    border-radius: 16px;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
}
```

---

## 📄 Como Adicionar Novos Serviços

**Arquivo:** `index.html`  
**Localização:** Seção "Nossos Serviços" (linha ~180+)

**Template de novo card:**

```html
<div class="service-card fade-in">
    <div class="service-icon">
        <svg viewBox="0 0 64 64" fill="none">
            <!-- Seu ícone SVG aqui -->
        </svg>
    </div>
    <h3 class="service-title">Nome do Serviço</h3>
    <p class="service-description">Descrição do serviço aqui.</p>
</div>
```

**Onde encontrar ícones SVG:**
- [Heroicons](https://heroicons.com/)
- [Feather Icons](https://feathericons.com/)
- [Bootstrap Icons](https://icons.getbootstrap.com/)

---

## 🔗 Como Adicionar Links de Redes Sociais

### Instagram
**Arquivo:** `index.html`  
**Localização:** Footer (linha ~390+)

```html
<li>📷 <a href="https://www.instagram.com/grupolf.pe/" target="_blank">@grupolf.pe</a></li>
```

### Facebook (adicionar)

```html
<li>📘 <a href="https://www.facebook.com/seuusuario" target="_blank">Facebook</a></li>
```

### LinkedIn (adicionar)

```html
<li>💼 <a href="https://www.linkedin.com/company/seuusuario" target="_blank">LinkedIn</a></li>
```

---

## 🎯 Como Adicionar Google Analytics

**Arquivo:** `index.html`  
**Localização:** Dentro da tag `<head>`, antes de `</head>`

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-XXXXXXXXXX"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'G-XXXXXXXXXX');
</script>
```

**Substituir:** `G-XXXXXXXXXX` pelo seu ID do Google Analytics.

---

## 📝 Como Adicionar Formulário de Contato

### Opção 1: Formspree (Gratuito e Simples)

1. Acesse [formspree.io](https://formspree.io/)
2. Crie uma conta gratuita
3. Adicione este código no HTML:

```html
<section class="contact-form" id="orcamento">
    <div class="container">
        <h2 class="section-title">Solicite um Orçamento</h2>
        <form action="https://formspree.io/f/SEUS-ID" method="POST">
            <div class="form-group">
                <input type="text" name="nome" placeholder="Seu nome" required>
            </div>
            <div class="form-group">
                <input type="email" name="email" placeholder="Seu e-mail" required>
            </div>
            <div class="form-group">
                <input type="tel" name="telefone" placeholder="Seu telefone" required>
            </div>
            <div class="form-group">
                <textarea name="mensagem" placeholder="Mensagem" rows="5" required></textarea>
            </div>
            <button type="submit" class="btn btn-primary btn-large">Enviar Mensagem</button>
        </form>
    </div>
</section>
```

### Estilos para o formulário

Adicionar no `css/style.css`:

```css
.contact-form {
    padding: var(--spacing-3xl) 0;
    background: var(--color-light-gray);
}

.form-group {
    margin-bottom: var(--spacing-md);
}

.form-group input,
.form-group textarea {
    width: 100%;
    padding: 14px 18px;
    border: 2px solid #e0e0e0;
    border-radius: var(--radius-sm);
    font-family: var(--font-family);
    font-size: 15px;
    transition: border-color 0.3s ease;
}

.form-group input:focus,
.form-group textarea:focus {
    outline: none;
    border-color: var(--color-primary);
}

form {
    max-width: 600px;
    margin: 0 auto;
}
```

---

## 🚀 Como Otimizar Imagens

### Ferramentas Recomendadas

1. **TinyPNG** - https://tinypng.com/
   - Comprime PNG e JPG sem perda visível de qualidade
   - Reduz até 70% do tamanho

2. **Squoosh** - https://squoosh.app/
   - Conversor online para WebP
   - Compara qualidade em tempo real

3. **ImageOptim** (Mac) - https://imageoptim.com/
   - App desktop para otimização em lote

### Formatos Recomendados

- **Fotos:** JPG ou WebP (80-85% de qualidade)
- **Ícones/Logos:** SVG ou PNG transparente
- **Ilustrações:** SVG (sempre que possível)

### Tamanhos Recomendados

- **Hero Image:** 1920x1080px (máx 200KB)
- **Serviços/Cards:** 800x600px (máx 100KB)
- **Thumbnails:** 400x300px (máx 50KB)

---

## 📊 Como Adicionar Google Search Console

1. Acesse [search.google.com/search-console](https://search.google.com/search-console/)
2. Adicione sua propriedade
3. Verifique com um destes métodos:

**Método 1: Tag HTML**
```html
<meta name="google-site-verification" content="SEU-CODIGO-AQUI" />
```
(Adicionar no `<head>` do `index.html`)

**Método 2: Arquivo HTML**
- Baixe o arquivo de verificação
- Faça upload na raiz do site

---

## 🔍 Como Melhorar SEO

### 1. Adicionar Meta Tags

**Arquivo:** `index.html`  
**Localização:** Dentro de `<head>`

```html
<!-- Meta Tags Essenciais -->
<meta name="description" content="Grupo LF - 15 anos oferecendo segurança privada de excelência em Pernambuco. Vigilância armada, controle de acesso e muito mais.">
<meta name="keywords" content="segurança privada, vigilância, Recife, Pernambuco, segurança armada, controle de acesso">
<meta name="author" content="Grupo LF">

<!-- Open Graph (Facebook) -->
<meta property="og:title" content="Grupo LF - Segurança Privada Profissional">
<meta property="og:description" content="15 anos elevando os padrões de segurança privada em Pernambuco">
<meta property="og:image" content="https://seusite.com.br/images/og-image.jpg">
<meta property="og:url" content="https://seusite.com.br">
<meta property="og:type" content="website">

<!-- Twitter Card -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Grupo LF - Segurança Privada">
<meta name="twitter:description" content="15 anos de experiência em segurança privada">
<meta name="twitter:image" content="https://seusite.com.br/images/twitter-card.jpg">
```

### 2. Criar sitemap.xml

**Criar arquivo:** `sitemap.xml` na raiz

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
  <url>
    <loc>https://seusite.com.br/</loc>
    <lastmod>2025-03-10</lastmod>
    <changefreq>monthly</changefreq>
    <priority>1.0</priority>
  </url>
</urlset>
```

### 3. Criar robots.txt

**Criar arquivo:** `robots.txt` na raiz

```
User-agent: *
Allow: /

Sitemap: https://seusite.com.br/sitemap.xml
```

---

## 💡 Dicas de Manutenção

### ✅ Checklist Semanal
- [ ] Verificar se todos os links estão funcionando
- [ ] Testar formulário de contato (se houver)
- [ ] Verificar WhatsApp e telefones
- [ ] Checar compatibilidade mobile

### ✅ Checklist Mensal
- [ ] Atualizar conteúdo e informações
- [ ] Verificar performance no PageSpeed Insights
- [ ] Revisar analytics e ajustar estratégias
- [ ] Fazer backup dos arquivos

### ✅ Checklist Semestral
- [ ] Revisar design e propor melhorias
- [ ] Adicionar depoimentos novos
- [ ] Atualizar fotos e cases de sucesso
- [ ] Avaliar necessidade de novas funcionalidades

---

## 🆘 Solução de Problemas Comuns

### Problema: Menu não abre no mobile
**Solução:** Verificar se o arquivo `js/script.js` está carregando corretamente.

### Problema: Animações não funcionam
**Solução:** Verificar se o navegador suporta Intersection Observer. Testar em navegador atualizado.

### Problema: WhatsApp não abre
**Solução:** Verificar se o número está no formato correto: `5581981182729` (sem espaços ou caracteres especiais).

### Problema: Site não responsivo
**Solução:** Verificar se a tag viewport está presente no `<head>`:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

---

## 📞 Suporte Técnico

Para dúvidas sobre personalização, entre em contato através dos canais oficiais do Grupo LF.

---

*Documento atualizado em: 10 de Março de 2025*