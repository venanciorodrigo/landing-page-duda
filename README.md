# Versão estática — Maria Eduarda Buss Jablonski (Psicóloga)

Esta pasta contém o site em **HTML + CSS puro**, sem build e sem JavaScript,
pronto para hospedagem no GitHub Pages.

```
static-site/
├── index.html      # página completa
├── styles.css      # todos os estilos
├── favicon.png
├── .nojekyll
└── assets/         # logos e fotos
```

## Como publicar no GitHub Pages

1. Crie um repositório no GitHub (ex.: `site-psicologa`).
2. Envie **o conteúdo desta pasta** para a raiz do repositório
   (o `index.html` precisa ficar na raiz):
   ```bash
   cd static-site
   git init
   git add .
   git commit -m "Site estático"
   git branch -M main
   git remote add origin https://github.com/SEU-USUARIO/SEU-REPO.git
   git push -u origin main
   ```
3. No GitHub, vá em **Settings → Pages**.
4. Em *Source*, escolha **Deploy from a branch**, branch `main` e pasta `/ (root)`.
5. Salve. Em ~1 minuto o site fica disponível em
   `https://SEU-USUARIO.github.io/SEU-REPO/`.

> O arquivo `.nojekyll` já está incluso para o GitHub não processar os arquivos.

## Domínio próprio (opcional)

Em **Settings → Pages → Custom domain**, informe o domínio e aponte o DNS
conforme as instruções exibidas pelo GitHub.

## Testar localmente

```bash
cd static-site
python3 -m http.server 8000
# abra http://localhost:8000
```

## Observações

- Todos os caminhos são **relativos**, então funciona em subpastas
  (`usuario.github.io/repo/`) sem ajustes.
- O menu mobile funciona sem JavaScript (CSS puro).
- As fontes Poiret One e Questrial são carregadas do Google Fonts.
