# Site_Matheus_engenharia

Site pessoal de **Matheus Vinícius Martins dos Santos** — currículo vivo, blog e loja de tecnologia ("Clareance"), publicado no GitHub Pages em **https://mattttheus.github.io/Site_Matheus_engenharia/**.

Esta é a **versão estática** do ecossistema — gerada a partir do projeto original em PHP + MySQL (pasta `Projeto Matheus/` fora deste repositório), que roda em WAMP ou qualquer hospedagem com PHP. Como o GitHub Pages só serve arquivos estáticos, o conteúdo do blog e da loja aqui é fixo (renderizado uma vez a partir do banco de dados), sem admin via phpMyAdmin.

> **Nota sobre os caminhos:** como este é um repositório de projeto (não `Mattttheus.github.io`), o GitHub Pages publica em um subcaminho, não na raiz do domínio. Todos os links internos (`href`/`src`) já foram ajustados com o prefixo `/Site_Matheus_engenharia/`. Se um dia você renomear o repositório, precisa regenerar o export com o novo prefixo (ou nenhum, se virar `Mattttheus.github.io`).

## Estrutura

```text
index.html         → site institucional / currículo
blog/index.html     → posts do blog
loja/index.html      → catálogo + seção de clearance
assets/css/style.css → design system
assets/js/main.js    → menu mobile + formulário de contato (mailto)
.nojekyll             → evita que o GitHub Pages tente processar como Jekyll
```

## Como publicar

```bash
git remote add origin https://github.com/Mattttheus/Site_Matheus_engenharia.git
git push -u origin main
```

Depois, em Settings → Pages do repositório, confirme que a fonte é a branch `main` (pasta raiz `/`). Em alguns minutos o site fica no ar em **https://mattttheus.github.io/Site_Matheus_engenharia/**.

## Atualizando o conteúdo

Este repositório **não é a fonte de verdade** — é um retrato estático. Para atualizar:
1. Edite o conteúdo no projeto original (`Projeto Matheus/index.php`, `blog/index.php`, `loja/index.php`, ou direto nas tabelas `posts`/`produtos` do MySQL).
2. Rode o projeto localmente (WAMP) e gere novamente os `.html` a partir do resultado renderizado.
3. Reaplique o prefixo `/Site_Matheus_engenharia/` nos links internos (`index.html`, `blog/index.html`, `loja/index.html`, `assets/css/style.css`, `assets/js/main.js`).
4. Copie os arquivos atualizados para cá e publique de novo (`git add . && git commit && git push`).

Se no futuro quiser conteúdo realmente dinâmico no ar (sem repetir esse passo manual), a alternativa é hospedar o projeto PHP+MySQL original em um provedor que rode PHP (hospedagem compartilhada, Railway, Render etc.) em vez do GitHub Pages.
