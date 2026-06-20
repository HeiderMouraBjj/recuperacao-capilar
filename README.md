# Minha Recuperação · Transplante Capilar

App pessoal (PWA) para acompanhar a recuperação pós transplante capilar, com base nas orientações de alta e na receita do **Instituto Milhomem (Dr. Pablo Milhomem)**.

## O que ele faz
- **Hoje** — em que dia da recuperação você está, o próximo passo e o checklist do dia. Dá pra navegar para **dias anteriores** (setas) e marcar/corrigir o que esqueceu.
  - Doses com **horário** (marca a hora atual e dá pra editar) e botão **"Não fiz"** em cada item.
  - **Próxima dose** calculada automaticamente nos remédios com intervalo (ex.: Cefalexina 12/12h).
- **Jornada** — a linha do tempo completa, da cirurgia ao acompanhamento.
- **Medicamentos** — receita e produtos, com a duração de cada tratamento.
- **Diário** — duas abas: **Marcações** (o que foi feito em cada dia, com horários) e **Fotos** (registro da evolução, salvo no aparelho).
- **Contato** — telefones e WhatsApp da equipe.
- **Ajustes** (ícone de engrenagem): data da cirurgia, **lembretes** (notificações), e **backup/restaurar** os dados.

A contagem parte da **data da cirurgia** ("Dia 0"). As marcações ficam no navegador (`localStorage`) e as fotos no aparelho (`IndexedDB`).

## Backup
Em **Ajustes → Backup**, baixe uma cópia das suas marcações e horários (arquivo `.json`) e guarde num lugar seguro. Para recuperar, use **Restaurar** e selecione o arquivo. As fotos não entram no `.json` (ficam no próprio aparelho).

## Lembretes
Em **Ajustes → Lembretes**, ative as notificações e defina horários. Eles tocam de forma confiável **com o app aberto**; no iPhone, notificações em segundo plano são limitadas — por isso o app também mostra a próxima dose em cada remédio.

## Arquivos do projeto (raiz do repositório)
```
index.html              o app inteiro
manifest.webmanifest    identidade do PWA
sw.js                   service worker (instalação + offline + aviso de nova versão)
icon-192.png · icon-512.png · icon-maskable-512.png · apple-touch-icon.png
README.md
```

## Publicar na Vercel
Site estático: *Framework Preset* = **Other**, *Build Command* e *Output Directory* em branco. Cada `git push` atualiza o site. Quando publicar uma nova versão, o app mostra um aviso **"Nova versão disponível → Atualizar"**.

## Instalar no celular (pelo link HTTPS da Vercel)
- **Android (Chrome):** menu ⋮ → **Instalar app**.
- **iPhone (Safari):** **Compartilhar** → **Adicionar à Tela de Início**.

## Observação
Este app **organiza** as orientações que você recebeu — não substitui a equipe médica. Qualquer dor forte, sangramento, febre ou dúvida: fale com o Instituto Milhomem.
