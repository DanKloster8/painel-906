# Painel CTC 906 — Admin e Leitor

## Dois modos (mesma URL, sufixo diferente)

- **Administrador:** `https://SEU-SITE.vercel.app/?admin`
  Mostra: carregar/trocar planilha e "Gerar versão do leitor".
- **Leitor:** `https://SEU-SITE.vercel.app/`
  Mostra só os resultados. Sem upload, sem botões de base.

> Importante: por ser site estático, isto **organiza** o acesso (cada um abre o link certo),
> mas não é uma trava de segurança. Não compartilhe o link `?admin` com quem não deve administrar.

## Como ATUALIZAR a base que o leitor vê (3 passos)

1. Abra o site com `?admin`, clique em **📂 Trocar base** e selecione a planilha nova.
2. Clique em **💾 Gerar versão do leitor** — o navegador baixa um arquivo **`dados.js`**.
3. Suba esse **`dados.js`** no mesmo repositório do GitHub (junto do `index.html`) e faça commit.
   O Vercel republica sozinho. O leitor passa a ver a base nova ao abrir o site.

(Se ainda não existir `dados.js` publicado, o leitor vê "Aguardando publicação".
O modo admin funciona normalmente mesmo sem `dados.js`.)

## Arquivos do repositório
- `index.html`  → o painel (sempre necessário)
- `dados.js`    → a base publicada para o leitor (gerada pelo botão; opcional até a 1ª publicação)
