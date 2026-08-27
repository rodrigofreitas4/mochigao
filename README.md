# Mochigão

Saí de Porto Alegre com uma mochila de 40 litros e voltei 113 dias depois, tendo passado por 32 países. Esse repositório é o site que guarda o que sobrou dessa viagem: 48 histórias contadas do jeito que aconteceram, 49 lugares avaliados com uma régua que eu inventei, um mapa pra percorrer a rota inteira e tudo que aprendi no caminho, pra quem quiser fazer o seu.

🔗 **[Ver o site](#)** _(troque pelo link depois de publicar — veja o passo a passo mais abaixo)_

![status](https://img.shields.io/badge/status-pronto-2A9D8F) ![tipo](https://img.shields.io/badge/tipo-site%20est%C3%A1tico-16213E)

---

## O que tem no site

- **Mapa** — a rota inteira, com o mochigão percorrendo o trajeto e "onde eu estava há X anos" pra qualquer data da viagem
- **Histórias** — os 48 capítulos, com fotos e vídeos de cada cidade, busca por palavra, e um pop-up com setinhas pra ir passando de uma história pra outra
- **Cidades & Notas** — ranking dos 49 lugares avaliados, com os critérios de nota, "o que achei" e sugestões de cada um
- **A Viagem** — como o roteiro foi montado, burocracia do Espaço Schengen, o passe de trem, controle de orçamento
- **Dicas** — pra quem quiser fazer o seu: como montar roteiro, Schengen, deslocamento, dinheiro, onde ficar, o que levar na mochila, apps de viagem
- **Sobre** — agradecimentos

## Tecnologia

Só HTML, CSS e JavaScript puro — sem framework, sem build, sem dependência de servidor. Um único arquivo `index.html` que lê a pasta `assets/` ao lado dele (o mapa interativo é outro arquivo HTML próprio, carregado por dentro do site).

## Estrutura de pastas

```
index.html
assets/
  fotos/      # fotos de cada história, comprimidas pra web
  videos/     # vídeos de cada história, comprimidas pra web
  img/        # mochigão, foto do hero, ilustrações de fundo, favicon
  mapa/       # o mapa interativo (arquivo HTML próprio)
```

**Importante:** o `index.html` só funciona com a pasta `assets` do lado dele. Se for mover ou copiar o site, mova a pasta `assets` junto.

## Como abrir localmente

Baixe os dois (o arquivo e a pasta) e dê duplo clique no `index.html`. Abre em qualquer navegador, sem instalar nada.

---

## Como publicar no GitHub Pages

Isso deixa o site com um link público (tipo `https://seu-usuario.github.io/mochigao`), grátis, direto do GitHub.

### 1. Crie o repositório

1. Entre em [github.com](https://github.com) e faça login (crie uma conta grátis se ainda não tiver).
2. No canto superior direito, clique no **+** e depois em **New repository**.
3. Dê um nome, por exemplo `mochigao`.
4. Deixe marcado como **Public**.
5. Não marque nenhuma das caixinhas de "Add a README" ou `.gitignore` — vamos subir os arquivos prontos.
6. Clique em **Create repository**.

### 2. Suba os arquivos

Na página do repositório recém-criado, vai ter um link **uploading an existing file**. Clique nele.

1. Arraste pra lá o `index.html`, o `README.md` (o que eu te mandei) e a pasta `assets` inteira.
   - Se o GitHub não aceitar arrastar a pasta `assets` de uma vez, arraste os arquivos de dentro dela mantendo a mesma estrutura (`assets/fotos/...`, `assets/videos/...`, `assets/img/...`, `assets/mapa/...`) — o GitHub recria as pastas sozinho a partir do caminho dos arquivos.
2. Espere o upload terminar (a pasta `assets` é grande, com fotos e vídeos — pode demorar alguns minutos dependendo da internet).
3. Escreva uma mensagem no campo "Commit changes", por exemplo `primeira versão do site`.
4. Clique em **Commit changes**.

### 3. Ative o GitHub Pages

1. No repositório, clique em **Settings** (aba no topo).
2. No menu da esquerda, clique em **Pages**.
3. Em **Build and deployment → Source**, escolha **Deploy from a branch**.
4. Em **Branch**, escolha `main` e a pasta `/ (root)`. Clique em **Save**.
5. Espere um ou dois minutos. Atualize a página — vai aparecer um link verde no topo, algo como:
   `https://seu-usuario.github.io/mochigao/`

Esse é o link do site no ar. Pode compartilhar, colocar no Instagram, no LinkedIn, onde quiser.

### 4. Fazendo o preview do link ficar bonito (LinkedIn, WhatsApp, etc.)

Quando você cola um link em redes sociais, elas mostram um preview (imagem + título + descrição) lendo umas tags chamadas Open Graph, que já estão configuradas no `index.html`. O único problema: essas tags precisam do link **completo** da imagem, e antes de publicar ninguém sabe qual vai ser esse link.

Depois de ativar o GitHub Pages e saber o seu link (passo 3), abra o `index.html` pelo GitHub (clique no arquivo → ícone de lápis pra editar), procure por essas duas linhas perto do topo:

```html
<meta property="og:image" content="assets/img/mochigao.png">
...
<meta name="twitter:image" content="assets/img/mochigao.png">
```

E troque o `content` das duas pelo link completo, por exemplo:

```html
<meta property="og:image" content="https://seu-usuario.github.io/mochigao/assets/img/mochigao.png">
```

Salve (**Commit changes**). Alguns minutos depois, o preview do link já sai bonito. Se o LinkedIn tiver guardado uma versão antiga em cache, teste colar o link no [Post Inspector do LinkedIn](https://www.linkedin.com/post-inspector/) pra forçar ele a reler.

### 5. Atualizando o site depois

Sempre que quiser trocar alguma coisa (uma foto, um texto), é só voltar no repositório, abrir o arquivo, clicar no lápis (**Edit**) pra editar direto pelo navegador, ou fazer upload de novo pra substituir um arquivo. O GitHub Pages atualiza o site sozinho, alguns minutos depois de cada mudança.

---

## Créditos

Fotos, vídeos e histórias: Rodrigo.
Personagem Mochigão: ilustração encomendada pelo Rodrigo.
Carimbos de passaporte no fundo do site: baseados nos carimbos reais da viagem, com números de identificação trocados por segurança.
