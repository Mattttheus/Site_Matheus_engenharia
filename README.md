# mattttheus.github.io

Site pessoal de **Matheus Vinícius Martins dos Santos** — currículo vivo, blog e loja de tecnologia ("Clareance"), publicado no GitHub Pages.

Esta é a **versão estática** do ecossistema — gerada a partir do projeto original em PHP + MySQL (pasta `Projeto Matheus/` fora deste repositório), que roda em WAMP ou qualquer hospedagem com PHP. Como o GitHub Pages só serve arquivos estáticos, o conteúdo do blog e da loja aqui é fixo (renderizado uma vez a partir do banco de dados), sem admin via phpMyAdmin.

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

1. Crie o repositório **`Mattttheus.github.io`** na sua conta do GitHub (o nome precisa ser exatamente esse, sem `git init` prévio nele).
2. Neste diretório:
   ```bash
   git init
   git add .
   git commit -m "Site pessoal — institucional, blog e loja"
   git branch -M main
   git remote add origin https://github.com/Mattttheus/Mattttheus.github.io.git
   git push -u origin main
   ```
3. Em alguns minutos o site fica no ar em **https://mattttheus.github.io/**. Se não aparecer, confira em Settings → Pages do repositório se a branch `main` está selecionada como fonte.

## Atualizando o conteúdo

Este repositório **não é a fonte de verdade** — é um retrato estático. Para atualizar:
1. Edite o conteúdo no projeto original (`Projeto Matheus/index.php`, `blog/index.php`, `loja/index.php`, ou direto nas tabelas `posts`/`produtos` do MySQL).
2. Rode o projeto localmente (WAMP) e gere novamente os `.html` a partir do resultado renderizado.
3. Copie os arquivos atualizados para cá e publique de novo (`git add . && git commit && git push`).

Se no futuro quiser conteúdo realmente dinâmico no ar (sem repetir esse passo manual), a alternativa é hospedar o projeto PHP+MySQL original em um provedor que rode PHP (hospedagem compartilhada, Railway, Render etc.) em vez do GitHub Pages.
