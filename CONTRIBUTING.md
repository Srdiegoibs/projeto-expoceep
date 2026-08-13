# Guia pedagógico de contribuição — projeto-expoceep

Bem-vindos, estudantes!
Este guia explica de forma simples como escolher uma tarefa, trabalhar nela e submeter o trabalho para revisão.

1) Como escolher uma issue (passo a passo)
- Olhe as labels: `dados`, `frontend`, `backend`, `docs`, e o nível `easy/medium/hard`.
- Comente na issue: "Vou trabalhar nesta task". Se for permitido, atribua-se.
- Escolha issues `easy` quando estiver começando.

2) Fluxo Git com explicações (simples)
- Sincronizar: `git checkout main && git pull origin main`  # traz a versão mais atual
- Criar branch: `git checkout -b feature/<tipo>-<descricao-curta>`  # isola seu trabalho
  - Ex.: `feature/dados-baixar-uci`
- Trabalhar localmente e fazer commits pequenos: 
  - `git add arquivo`  
  - `git commit -m "dados: adicionar script baixar (passo X)"`
- Subir branch: `git push -u origin HEAD`  # cria a branch remota
- Abrir Pull Request no GitHub apontando para `main` e linkando a issue (ex.: `Fixes #3`)

3) O que escrever no PR (modelo curto)
- Descrição do que foi feito (2–3 frases)
- Como testar localmente (comandos mínimos)
- Quais arquivos foram alterados
- Link para a issue relacionada

4) Checklist do PR (para estudantes)
- Código roda localmente conforme as instruções
- Não comitar dados sensíveis
- Mensagens de commit claras e pequenos passos
- Adicionar notas na documentação se necessário

5) Revisão e feedback (o que esperar)
- Revisores vão comentar pequenas mudanças; responda e faça correções em commits na mesma branch
- Quando aprovado, o instrutor fará o merge (ou você, se autorizado)

6) Como rodar o projeto localmente (exemplo)
```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python baixar.py
python limpar.py
python treinar.py
streamlit run app.py
```

7) Pedir ajuda
- Abra uma issue com label `help-wanted` e explique o que tentou e qual erro encontrou
- Em PRs, use comentários para pedir revisão específica

8) Avaliação (sugestão para o professor)
- Avaliar PRs por: completude do entregável, clareza da documentação e processo (commits/PR)
- Pontos extra por documentação clara e testes simples

Obrigado — este repositório é para aprender. Cometer erros é parte do processo; use PRs para pedir feedback.

