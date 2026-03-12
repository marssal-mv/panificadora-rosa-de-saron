# Plano de Análise e Melhorias: Projeto Padaria

🤖 **Applying knowledge of `@[orchestrator]`, `@[seo-specialist]`, `@[qa-automation-engineer]`, and `@[backend-specialist]`...**

Este documento detalha o plano de avaliação do seu projeto estático atual (HTML, CSS, JS) e propõe um roteiro progressivo de evolução focado em SEO, acessibilidade e qualidade.

---

## 🎯 Objetivo e Alinhamento

Com base nas suas respostas, o escopo do projeto foi definido:

1. **Objetivo Principal:** Cartão de visita digital focado em **SEO Local** para que os clientes encontrem facilmente a **localização e o WhatsApp**.
2. **Cardápio:** Será um arquivo **PDF estático** (sem necessidade de painel administrativo).
3. **Hospedagem:** Foco em opções **gratuitas e rápidas para sites estáticos** (recomendações no plano de execução).

Dada essa abordagem, o foco total será em **Performance (Core Web Vitals)** e **SEO (Search Engine Optimization)** para que a padaria domine as buscas locais, com uma camada de **Testes Automatizados (QA)** para garantir que nenhum link ou PDF quebre. O **Backend** será dispensado nesta etapa, focando na excelência do front-end.

---

## 🔍 Análise e Ideias de Melhoria (Por Área)

### 📈 1. SEO & GEO (`@[seo-specialist]`)
O site atual é um HTML básico perfeito para carregar rápido, mas invisível para os buscadores se não for otimizado.
*   **Ideias de Melhoria:**
    *   **LocalBusiness Schema:** Adicionar dados estruturados JSON-LD na página. Essencial para o Google Maps e para o painel de informações da pesquisa do Google exibir horário de funcionamento, localização e telefone.
    *   **Meta Tags & Open Graph:** Inserir tag `<meta name="description">` persuasiva e tags `<meta property="og:...">` para que ao compartilhar o link no WhatsApp apareça uma prévia bonita com a logo.
    *   **Acessibilidade (A11y) & Core Web Vitals:** Garantir contraste adequado nos botões e verificar o `alt` de todas as imagens para melhorar a pontuação do Lighthouse (fator de ranqueamento).

### 🛡️ 2. Qualidade (QA) (`@[qa-automation-engineer]`)
Não há validação automatizada verificando se seu site continua funcionando se algo no código mudar.
*   **Ideias de Melhoria:**
    *   **Verificação de Links (Smoke Test):** Garantir via script que os links do WhatsApp, Localização e (futuramente) do PDF do Cardápio não estejam quebrados (retornando erro 404).
    *   **Auditoria de Performance:** Validar o peso do PDF do cardápio para não frustrar o usuário no 3G.

### 🚀 3. Hospedagem (`@[devops-engineer]`)
Para um site estático focado em velocidade e custo zero:
*   **Recomendações (Gratuitas e com Certificado HTTPS nativo):**
    *   **Vercel** ou **Netlify:** As opções mais fáceis. Você arrasta a pasta ou conecta o GitHub, e eles deixam online em segundos, com servidores super rápidos.
    *   **GitHub Pages:** Ótimo se você já for colocar o código no GitHub.
    *   *Nossa indicação inicial será a **Vercel** pela simplicidade e velocidade.*

---

## 🗺️ Passos de Execução Propostos (Roadmap)

1.  **Fase 1: Quick Wins (Foco em SEO)**
    *   Ajustar a hierarquia de tags (`<main>`, `<header>`).
    *   Adicionar metatags descritivas, Open Graph (WhatsApp) e *Schema Markup* de Negócio Local no `index.html`.
    *   Melhorar atributos de acessibilidade (A11y).
2.  **Fase 2: Preparação do Cardápio**
    *   Ajustar o botão "Ver cardápio" para apontar para o futuro PDF (`target="_blank"`), talvez adicionando um atributo `download`.
3.  **Fase 3: Deployment (Publicação)**
    *   Subir o projeto no GitHub (se ainda não estiver).
    *   Configurar a hospedagem gratuita na Vercel ou Netlify.

---

**[✅] Plan created: `docs/PLAN-analise-padaria.md`**

**Próximos passos:**
Responda às 3 perguntas do Socratic Gate para seguirmos com o refinamento ou chame o comando `/create` ou me dê luz verde para iniciarmos a **Fase 1**!
