# 📂 Codex — Coleção de Prompts

Esta pasta contém uma coleção sequencial de prompts utilizados para construir, iterar e converter um site portfólio de moda de alta qualidade. Os prompts foram organizados em ordem lógica de execução — do zero ao deploy em WordPress.

---

## 📋 Índice de Prompts

| # | Arquivo | Descrição Resumida |
|---|---------|-------------------|
| 1 | `fashion-portfolio-website.md` | Criação completa do site portfólio de moda |
| 2 | `fix-layout-dimensions.md` | Correção de dimensões e layout full-screen |
| 3 | `mobile-responsive-update.md` | Responsividade completa para mobile e tablet |
| 4 | `assets-folder-setup.md` | Configuração e gerenciamento da pasta de assets |
| 5 | `hero-text-behind-subject.md` | Efeito de texto atrás do sujeito na hero section |
| 6 | `hero-image-and-typography-update.md` | Ajustes de imagem e tipografia do hero |
| 7 | `hero-typography-scaling.md` | Escala e posicionamento tipográfico do hero |
| 8 | `wordpress-theme-conversion.md` | Conversão do site para tema WordPress |

---

## 📖 Descrição Detalhada de Cada Prompt

### 1. `fashion-portfolio-website.md`

**Objetivo:** Criar do zero um site portfólio completo para um designer de moda, baseado em uma imagem de referência.

**O que faz:**
- Gera um site single-page com HTML5, CSS3 e JavaScript puro (sem frameworks)
- Implementa layout editorial de alta qualidade com seções alternadas claro/escuro
- Inclui 8 seções: Header, Hero, About, Skills, Portfolio, Quote Artístico, Depoimentos e Footer
- Utiliza paleta de cores específica (charcoal `#111111`, cinza claro `#F2F2F2`, rosa empoeirado `#D9A5A5`)
- Aplica tipografia editorial (Bebas Neue/Oswald para títulos, Inter/Poppins para corpo)
- Adiciona animações: scroll suave, fade-in por seção, efeito glitch, texto circular rotativo
- Cria carrossel de imagens com navegação via JavaScript
- Design totalmente responsivo para desktop, tablet e mobile

**Quando usar:** Este é o prompt inicial que gera toda a base do projeto. Use-o como ponto de partida para criar o site completo.

**Pré-requisitos:** Uma imagem de referência do design desejado deve ser fornecida junto ao prompt.

---

### 2. `fix-layout-dimensions.md`

**Objetivo:** Corrigir problemas de dimensões do layout para que o site ocupe corretamente a tela inteira em monitores desktop.

**O que faz:**
- Remove wrappers que limitam a largura do site
- Faz backgrounds de seções ocuparem 100% da largura da tela
- Define container de conteúdo entre 1400px–1600px de largura máxima
- Garante que o hero ocupe 100vh em desktop
- Ajusta espaçamento para resoluções de 1440px, 1600px e 1920px
- Mantém responsividade para tablet e mobile

**Quando usar:** Após gerar o site com o prompt 1, caso o layout fique confinado em um container estreito ou não preencha a tela corretamente.

**Regra importante:** Este prompt **não altera** design, cores, tipografia, estrutura ou conteúdo — apenas corrige dimensões.

---

### 3. `mobile-responsive-update.md`

**Objetivo:** Tornar o site completamente responsivo para dispositivos mobile e tablet, mantendo o design desktop inalterado.

**O que faz:**
- Implementa media queries CSS para telas de 320px a 1024px
- Converte o menu de navegação desktop em **menu hamburger** (tela cheia ou slide-in)
- Empilha conteúdo do hero verticalmente em mobile, reduzindo tamanhos de título
- Converte layouts de duas colunas em coluna única para telas pequenas
- Ajusta grids de imagens para 1 ou 2 colunas em mobile
- Garante que o carrossel funcione com **swipe horizontal** em toque
- Ajusta tipografia para melhor legibilidade em telas pequenas
- Corrige paddings e margins para evitar texto colado nas bordas
- Otimiza carregamento de imagens para dispositivos móveis

**Quando usar:** Após corrigir as dimensões do layout (prompt 2), use este prompt para garantir que o site funcione perfeitamente em smartphones e tablets.

**Regra importante:** **Não modifica** o design desktop — apenas adiciona melhorias responsivas para mobile e tablet.

---

### 4. `assets-folder-setup.md`

**Objetivo:** Estabelecer uma pasta `/assets` como repositório central para todos os recursos estáticos do projeto.

**O que faz:**
- Define a pasta `/assets` para armazenar imagens, ícones, ilustrações, fontes e gráficos
- Instrui o agente a monitorar mudanças na pasta de assets
- Atualiza automaticamente caminhos em HTML, CSS e JS quando assets são adicionados ou movidos
- Notifica sobre assets não utilizados ou com links quebrados
- Mantém a estrutura do projeto organizada

**Quando usar:** Após ter o site base criado, use este prompt para organizar os recursos estáticos. Depois, sempre que adicionar ou mover assets, informe ao agente com "Adicionei novos assets" ou "Atualizei assets".

**Fluxo de trabalho:** Diga "Adicionei novos assets" → o agente escaneia a pasta → verifica integração → confirma mudanças.

---

### 5. `hero-text-behind-subject.md`

**Objetivo:** Posicionar o texto "DESIGNER" grande atrás da imagem do sujeito na hero section, criando um efeito de profundidade visual.

**O que faz:**
- Centraliza a imagem do sujeito (modelo) horizontalmente na página
- Posiciona o texto headline grande atrás da imagem usando CSS `position` e `z-index`
- Cria efeito de camadas: texto no fundo, sujeito na frente
- Mantém o texto grande e visualmente impactante
- Preserva comportamento responsivo

**Quando usar:** Após o site estar funcional, para refinar o layout do hero section e criar o efeito visual de sobreposição entre texto e imagem.

**Regra importante:** Altera **apenas** a hero section. Nenhuma outra parte do site é modificada.

---

### 6. `hero-image-and-typography-update.md`

**Objetivo:** Refinar a hero section com ajustes na imagem do sujeito e na composição tipográfica.

**O que faz:**
- Remove o efeito monocromático/escala de cinza da imagem do sujeito (mostra em cores originais)
- Aumenta ligeiramente o tamanho da imagem do sujeito mantendo-a centralizada
- Mantém apenas "DESIGNER" como texto de fundo (remove outras palavras de fundo)
- Aumenta significativamente o tamanho do texto "DESIGNER"
- Adiciona texto "FASHION" menor, posicionado no canto superior-esquerdo do "DESIGNER"
- Mantém o layering correto: texto atrás, sujeito na frente

**Quando usar:** Após aplicar o prompt 4 (texto atrás do sujeito), para refinar as proporções e composição visual do hero.

**Regra importante:** Altera **apenas** elementos da hero section.

---

### 7. `hero-typography-scaling.md`

**Objetivo:** Ajustar o tamanho e posicionamento final da tipografia do hero para corresponder melhor ao design de referência.

**O que faz:**
- Aumenta o tamanho do texto "DESIGNER" para ficar mais dominante e visualmente impactante
- Faz o texto se estender mais amplamente pela hero section
- Ajusta a posição do texto "FASHION" para alinhar corretamente com o novo tamanho do "DESIGNER"
- Garante que a tipografia escale corretamente em desktop, tablet e mobile
- Mantém o sujeito centralizado e na frente do texto

**Quando usar:** É o último ajuste fino da tipografia do hero, após os prompts 4 e 5. Use quando o texto ainda não está grande o suficiente ou precisa de melhor posicionamento.

**Regra importante:** Ajusta **apenas** tamanho e posicionamento tipográfico do "DESIGNER" e "FASHION".

---

### 8. `wordpress-theme-conversion.md`

**Objetivo:** Converter todo o site HTML/CSS/JS estático em um tema WordPress funcional e completo.

**O que faz:**
- Transforma a estrutura estática em arquivos de tema WordPress
- Cria toda a estrutura de pastas padrão do WordPress:
  ```
  /theme-name
      style.css
      functions.php
      index.php, header.php, footer.php
      front-page.php, page.php, single.php, archive.php
      sidebar.php, screenshot.png
      /assets (css, js, images)
      /template-parts (hero.php, sections.php)
  ```
- Enqueue de estilos e scripts via `functions.php`
- Converte seções reutilizáveis em template parts
- Cria menus de navegação dinâmicos via WordPress
- Habilita: imagens destacadas, logo customizado, widgets, blocos Gutenberg
- Converte áreas de conteúdo em WordPress loops

**Quando usar:** Quando o site estiver finalizado e aprovado visualmente, use este prompt para convertê-lo em um tema WordPress pronto para instalação.

**Regra importante:** O design visual **não é alterado** — apenas a estrutura do código é refatorada para a arquitetura WordPress.

---

## 🔄 Ordem de Execução Recomendada

```
1. fashion-portfolio-website.md        → Gerar o site completo
2. fix-layout-dimensions.md            → Corrigir dimensões do layout
3. mobile-responsive-update.md         → Responsividade mobile e tablet
4. assets-folder-setup.md              → Organizar pasta de assets
5. hero-text-behind-subject.md         → Efeito texto atrás do sujeito
6. hero-image-and-typography-update.md  → Refinar imagem e tipografia
7. hero-typography-scaling.md           → Ajuste fino da escala tipográfica
8. wordpress-theme-conversion.md        → Converter para tema WordPress
```

> **Nota:** Os prompts 5, 6 e 7 são iterações progressivas sobre a hero section. Cada um refina o resultado do anterior. Os prompts foram projetados para serem usados sequencialmente, mas podem ser adaptados individualmente conforme a necessidade.

---

## ⚙️ Stack Tecnológica

| Tecnologia | Uso |
|-----------|-----|
| HTML5 | Estrutura semântica |
| CSS3 | Estilização (Flexbox + Grid) |
| JavaScript (Vanilla) | Interatividade e animações |
| WordPress | Conversão final para CMS |

---

## 📌 Regras Gerais

1. **Sem frameworks CSS/JS** — Todo o código é escrito do zero
2. **Design fiel à referência** — Sempre forneça a imagem de referência junto ao prompt 1
3. **Modificações cirúrgicas** — Prompts 2–6 alteram apenas o que está descrito, sem efeitos colaterais
4. **Responsivo** — Todos os prompts mantêm compatibilidade com desktop, tablet e mobile
5. **Código limpo** — Estrutura semântica e bem comentada
