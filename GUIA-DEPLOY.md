# 🚀 Guia de Deploy - Grupo LF

Este documento contém instruções passo a passo para publicar o site do Grupo LF online.

---

## 📋 Pré-requisitos

Antes de começar, tenha em mãos:
- ✅ Todos os arquivos do projeto
- ✅ Acesso à ferramenta de deploy OU conta em serviço de hospedagem
- ✅ Domínio (opcional, mas recomendado)

---

## 🎯 Opção 1: Deploy via Aba Publish (RECOMENDADO)

### Passo a Passo

1. **Clique na aba "Publish"**
   - Localize a aba Publish no topo desta interface
   - Clique para abrir o painel de publicação

2. **Revise os arquivos**
   - Confirme que todos os 7 arquivos estão listados:
     - index.html
     - css/style.css
     - js/script.js
     - README.md
     - PERSONALIZACAO.md
     - RESUMO-EXECUTIVO.md
     - guia-estilo.html

3. **Clique em "Publicar"**
   - Aguarde o processo de deploy (30-90 segundos)
   - Não feche a janela durante o processo

4. **Copie a URL**
   - Após a conclusão, copie a URL fornecida
   - Exemplo: `https://seu-projeto.seu-dominio.com`

5. **Teste o site**
   - Acesse a URL em diferentes dispositivos
   - Verifique se todos os links funcionam
   - Teste o botão WhatsApp e telefone

### ✅ Vantagens
- ⚡ Deploy em menos de 1 minuto
- 🔄 Atualizações automáticas
- 🌐 URL pública imediatamente
- 📊 SSL/HTTPS automático
- 💰 Geralmente gratuito

---

## 🌐 Opção 2: Netlify (Gratuito e Fácil)

### Passo a Passo

1. **Acesse o Netlify**
   - Vá para: https://www.netlify.com/
   - Crie uma conta gratuita (ou faça login)

2. **Novo Site**
   - Clique em "Add new site" → "Deploy manually"
   - OU arraste a pasta do projeto para a área indicada

3. **Faça Upload**
   - Selecione TODOS os arquivos do projeto
   - Mantenha a estrutura de pastas
   - Aguarde o upload completar

4. **Configurações (Opcional)**
   - Altere o nome do site: Site settings → Change site name
   - Exemplo: `grupolf-seguranca.netlify.app`

5. **Domínio Customizado (Opcional)**
   - Site settings → Domain management
   - Add custom domain
   - Siga as instruções DNS

### ✅ Vantagens
- 🆓 Plano gratuito robusto
- ⚡ CDN global (carregamento rápido)
- 🔒 HTTPS automático
- 🔄 Deploy contínuo (se usar Git)
- 📊 Analytics básico

### 📌 Resultado
URL final: `https://grupolf-seguranca.netlify.app`

---

## 🔷 Opção 3: Vercel (Alternativa ao Netlify)

### Passo a Passo

1. **Acesse o Vercel**
   - Vá para: https://vercel.com/
   - Crie uma conta (GitHub, GitLab ou email)

2. **Novo Projeto**
   - Clique em "Add New..." → "Project"
   - Escolha "Import from Git" OU "Deploy from template"

3. **Upload Manual**
   - Se não usar Git, arraste a pasta do projeto
   - Configure o nome do projeto
   - Clique em "Deploy"

4. **Aguarde o Deploy**
   - Processo leva 30-60 segundos
   - Vercel compila e otimiza automaticamente

5. **Acesse o Site**
   - URL será algo como: `grupolf.vercel.app`
   - Pode adicionar domínio customizado

### ✅ Vantagens
- 🆓 Gratuito para sites estáticos
- ⚡ Performance excelente
- 🔒 HTTPS automático
- 🌍 Edge Network global
- 📈 Analytics integrado

---

## 📁 Opção 4: GitHub Pages (Para Desenvolvedores)

### Passo a Passo

1. **Crie um Repositório**
   - Vá para: https://github.com/
   - Clique em "New repository"
   - Nome: `grupolf-site` (ou similar)

2. **Faça Upload dos Arquivos**
   - Via interface web: "Add file" → "Upload files"
   - OU via Git:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin https://github.com/SEU-USUARIO/grupolf-site.git
   git push -u origin main
   ```

3. **Ative GitHub Pages**
   - Settings → Pages
   - Source: Deploy from a branch
   - Branch: main / (root)
   - Save

4. **Aguarde o Deploy**
   - Pode levar 2-5 minutos
   - Verifique o status na aba Actions

5. **Acesse o Site**
   - URL: `https://seu-usuario.github.io/grupolf-site/`

### ✅ Vantagens
- 🆓 Totalmente gratuito
- 🔄 Versionamento completo
- 👥 Colaboração fácil
- 📚 Documentação integrada

---

## 🏢 Opção 5: Hospedagem Tradicional (cPanel/FTP)

### Passo a Passo

1. **Acesse o cPanel**
   - Login na sua hospedagem
   - Abra o Gerenciador de Arquivos

2. **Navegue até public_html**
   - Ou diretório público do seu domínio
   - Exemplo: `public_html/grupolf/`

3. **Faça Upload**
   - Clique em "Upload"
   - Selecione todos os arquivos
   - OU use FTP (FileZilla):
     - Host: ftp.seudominio.com.br
     - Usuário: seu-usuario
     - Senha: sua-senha
     - Porta: 21

4. **Mantenha a Estrutura**
   ```
   public_html/
   ├── index.html
   ├── css/
   │   └── style.css
   ├── js/
   │   └── script.js
   └── (outros arquivos)
   ```

5. **Teste o Site**
   - Acesse: `https://seudominio.com.br`
   - Verifique se tudo funciona

### ✅ Vantagens
- 🎛️ Controle total
- 📧 Email profissional incluído
- 💾 Mais espaço de armazenamento
- 🔧 Acesso a banco de dados (MySQL)

---

## 🔐 Opção 6: WordPress (Não Recomendado para este Projeto)

**⚠️ AVISO:** Este é um site estático (HTML/CSS/JS), não precisa de WordPress.

Mas se ainda assim quiser usar WordPress:

1. Instale tema em branco (Blank Theme)
2. Crie uma página customizada
3. Cole o código HTML no editor de blocos (HTML personalizado)
4. Adicione CSS no Customizer
5. Adicione JavaScript no footer

**Desvantagens:**
- ❌ Muito mais lento
- ❌ Precisa de manutenção constante
- ❌ Vulnerabilidades de segurança
- ❌ Complexidade desnecessária

---

## 📊 Checklist Pós-Deploy

Após publicar o site, verifique:

### Funcionalidades
- [ ] Página carrega corretamente
- [ ] CSS está aplicado (cores, fontes, layout)
- [ ] JavaScript funciona (animações, menu mobile)
- [ ] Links internos funcionam (navegação suave)
- [ ] Botão WhatsApp abre corretamente
- [ ] Link de telefone funciona no mobile
- [ ] Links de Instagram abrem

### Responsividade
- [ ] Desktop (1920x1080)
- [ ] Laptop (1366x768)
- [ ] Tablet (768x1024)
- [ ] Mobile (375x667)
- [ ] Mobile pequeno (320x568)

### Performance
- [ ] Página carrega em menos de 3 segundos
- [ ] Fontes carregam corretamente
- [ ] Sem erros no console do navegador
- [ ] Imagens (SVG) aparecem

### SEO Básico
- [ ] Título da página está correto
- [ ] Meta description presente
- [ ] Favicon (opcional)
- [ ] Open Graph tags (opcional)

---

## 🔧 Troubleshooting (Solução de Problemas)

### Problema 1: CSS não carrega
**Sintomas:** Página sem estilo, tudo desorganizado  
**Solução:**
- Verifique se `css/style.css` está no lugar correto
- Verifique o caminho no HTML: `<link rel="stylesheet" href="css/style.css">`
- Limpe o cache do navegador (Ctrl + Shift + R)

### Problema 2: JavaScript não funciona
**Sintomas:** Menu não abre, animações não funcionam  
**Solução:**
- Verifique se `js/script.js` está no lugar correto
- Abra o Console (F12) e procure por erros
- Verifique o caminho no HTML: `<script src="js/script.js"></script>`

### Problema 3: Fontes não carregam
**Sintomas:** Texto em Arial ou Times New Roman  
**Solução:**
- Verifique se há conexão com internet
- Confirme o link no `<head>`: Google Fonts
- Tente outro navegador

### Problema 4: WhatsApp não abre
**Sintomas:** Link não funciona no mobile  
**Solução:**
- Verifique o número: deve estar como `5581981182729`
- Formato correto: `https://wa.me/5581981182729`
- Sem espaços, parênteses ou hífens

### Problema 5: Site não aparece no Google
**Sintomas:** Busca pelo nome não encontra o site  
**Solução:**
- Aguarde 2-7 dias (indexação leva tempo)
- Adicione ao Google Search Console
- Crie sitemap.xml
- Envie sitemap para o Google

---

## 📈 Próximos Passos Após Deploy

### Imediato (Hoje)
1. ✅ Testar site em todos os dispositivos
2. ✅ Compartilhar URL com stakeholders
3. ✅ Verificar analytics (se configurado)

### Primeira Semana
1. 📊 Configurar Google Analytics
2. 🔍 Adicionar ao Google Search Console
3. 📱 Testar com usuários reais
4. 📝 Coletar feedback

### Primeiro Mês
1. 📈 Analisar métricas de acesso
2. 🎯 Otimizar conversões
3. 📸 Adicionar fotos reais
4. 💬 Implementar formulário de contato

### Três Meses
1. 📝 Criar blog
2. 👥 Adicionar depoimentos
3. 📊 A/B testing de CTAs
4. 🚀 Campanhas de marketing digital

---

## 💡 Dicas Importantes

### ✅ Boas Práticas
- Sempre teste antes de compartilhar
- Mantenha backup dos arquivos
- Atualize conteúdo regularmente
- Monitore analytics semanalmente
- Responda leads rapidamente

### ⚠️ Evite
- Modificar arquivos em produção sem testar
- Esquecer de renovar domínio/hospedagem
- Ignorar atualizações de segurança
- Deixar site sem monitoramento

---

## 📞 Suporte

### Dúvidas Técnicas
- Revise a documentação (README.md)
- Consulte o guia de personalização
- Verifique o console do navegador

### Problemas com Hospedagem
- Entre em contato com suporte da hospedagem
- Fornece URL e descrição do problema
- Screenshots ajudam muito

### Alterações no Site
- Consulte PERSONALIZACAO.md
- Teste em ambiente local primeiro
- Faça backup antes de modificar

---

## 🎉 Parabéns!

Se chegou até aqui, o site do **Grupo LF** está online e pronto para gerar resultados! 🛡️

**Lembre-se:** Um site não é um projeto finalizado, é um projeto em evolução. Continue melhorando e atualizando para melhores resultados.

---

## 📊 URLs Úteis

### Ferramentas de Teste
- **PageSpeed Insights:** https://pagespeed.web.dev/
- **Mobile-Friendly Test:** https://search.google.com/test/mobile-friendly
- **W3C Validator:** https://validator.w3.org/

### Analytics e SEO
- **Google Analytics:** https://analytics.google.com/
- **Google Search Console:** https://search.google.com/search-console/
- **Google Tag Manager:** https://tagmanager.google.com/

### Hospedagem Gratuita
- **Netlify:** https://www.netlify.com/
- **Vercel:** https://vercel.com/
- **GitHub Pages:** https://pages.github.com/
- **Render:** https://render.com/

---

*Última atualização: 10 de Março de 2025*  
*Versão: 1.0.0*  
*Status: Pronto para Deploy ✅*