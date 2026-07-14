# Calendário LLUCENA Infraestrutura

Calendário de reuniões e lembretes publicado via GitHub Pages, com o padrão visual da LLUCENA (azul #2D4976 / vermelho #EE3537).

## Estrutura

```
calendario-llucena/
├── index.html      → página do calendário (visual + formulário de eventos)
├── events.json     → onde os eventos ficam salvos
└── assets/         → logotipos LLUCENA
```

## Como publicar (uma vez só)

1. Crie um repositório no GitHub (ex.: `calendario`). Pode ser público ou privado*.
2. Envie todos os arquivos desta pasta para o repositório (arraste na página **Add file → Upload files**).
3. Vá em **Settings → Pages → Branch: main → / (root) → Save**.
4. Em ~1 minuto o calendário estará em `https://SEU-USUARIO.github.io/calendario/`.

*Em repositório privado, o GitHub Pages exige plano pago; em repo público a página funciona no plano gratuito.

## Como adicionar eventos pela própria página

A página grava os eventos direto no `events.json` do repositório usando a API do GitHub. Para isso, uma única vez:

1. No GitHub: **Settings (do seu perfil) → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. Em **Repository access**, selecione apenas o repositório do calendário.
3. Em **Permissions → Contents**, escolha **Read and write**. Gere o token e copie.
4. Na página do calendário, clique em **⚙ Configurar**, confira o repositório (é detectado automaticamente) e cole o token. Ele fica salvo apenas no seu navegador.

Depois disso, use **+ Novo evento** (ou clique em qualquer dia) para adicionar reuniões e lembretes. A lixeira na lista lateral exclui.

Quem abrir a página sem token consegue **ver** o calendário normalmente; o token só é necessário para adicionar/excluir.
