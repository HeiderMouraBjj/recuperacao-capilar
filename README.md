# Minha Recuperação · Transplante Capilar

App pessoal (PWA) para acompanhar a recuperação pós transplante capilar, com base nas orientações de alta e na receita do **Instituto Milhomem (Dr. Pablo Milhomem)**.

## O que ele faz
- **Hoje** — em que dia da recuperação você está, o próximo passo e o checklist do dia. Doses com horário (marca a hora atual e dá pra editar) e botão **"Não fiz"** em cada item.
- **Jornada** — a linha do tempo completa, da cirurgia ao acompanhamento.
- **Medicamentos** — receita e produtos, com a duração de cada tratamento.
- **Histórico** — o que foi marcado em cada dia, com os horários de cada dose.
- **Contato** — telefones e WhatsApp da equipe.

A contagem parte da **data da cirurgia** ("Dia 0"), ajustável no ícone de engrenagem. O progresso fica salvo no navegador (`localStorage`).

## Arquivos do projeto
```
index.html              o app inteiro
manifest.webmanifest    identidade do PWA (nome, cores, ícones)
sw.js                   service worker (instalação + offline)
icon-192.png            ícone
icon-512.png            ícone
icon-maskable-512.png   ícone adaptativo (Android)
apple-touch-icon.png    ícone (iOS)
README.md               este arquivo
```
Todos devem ficar na **mesma pasta**, na raiz do repositório.

## Publicar na Vercel
Como já é um site estático, em *Framework Preset* use **Other** e deixe *Build Command* e *Output Directory* em branco. Cada `git push` atualiza o site automaticamente.

## Instalar no celular (a partir do link da Vercel — precisa ser HTTPS)

**Android (Chrome)**
1. Abra o link da Vercel no Chrome.
2. Toque no menu **⋮** → **Instalar app** (ou "Adicionar à tela inicial").
3. Confirme. O ícone vai para a tela inicial e abre em tela cheia.

**iPhone (Safari)**
1. Abra o link da Vercel no **Safari** (precisa ser o Safari).
2. Toque no botão **Compartilhar** (quadrado com seta para cima).
3. **Adicionar à Tela de Início** → **Adicionar**.

> Importante: a instalação como app só funciona pelo link da Vercel (HTTPS). Abrir o `index.html` direto do arquivo no celular não habilita o PWA.

## Observação
Este app **organiza** as orientações que você recebeu — não substitui a equipe médica. Qualquer dor forte, sangramento, febre ou dúvida: fale com o Instituto Milhomem.
