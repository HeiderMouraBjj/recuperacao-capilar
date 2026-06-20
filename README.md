# Minha Recuperação · Transplante Capilar

App pessoal para acompanhar a recuperação pós transplante capilar, com base nas orientações de alta e na receita do **Instituto Milhomem (Dr. Pablo Milhomem)**.

## O que ele faz
- **Hoje** — mostra em que dia da recuperação você está, qual é o próximo passo e o checklist do dia.
- **Jornada** — a linha do tempo completa, do dia da cirurgia ao acompanhamento. O que é feito fica marcado.
- **Medicamentos** — receita (Cefalexina, Dexametasona, Dipirona) e produtos da orientação, com barra de duração de cada tratamento.
- **Contato** — telefones e WhatsApp da equipe.

A contagem parte da **data da cirurgia** ("Dia 0"), que você ajusta no botão de engrenagem. O progresso fica salvo no próprio navegador (`localStorage`).

## Rodar no computador
É um único arquivo, sem build. Basta abrir o `index.html` no navegador (duplo clique). Pronto.

## Subir no GitHub
```bash
git init
git add .
git commit -m "Primeira versão do app de recuperação"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/SEU-REPO.git
git push -u origin main
```

## Publicar na Vercel
1. Entre em [vercel.com](https://vercel.com) e conecte sua conta do GitHub.
2. **Add New → Project** e selecione este repositório.
3. Em *Framework Preset*, escolha **Other** (é um site estático, não precisa de build).
4. Deixe *Build Command* e *Output Directory* em branco e clique em **Deploy**.

A Vercel serve o `index.html` direto e gera um link público. Cada `git push` novo atualiza o site automaticamente.

## Observação importante
Este app **organiza** as orientações que você recebeu — não substitui a equipe médica. Qualquer dor forte, sangramento, febre ou dúvida: fale com o Instituto Milhomem.
