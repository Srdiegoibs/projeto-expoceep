# Contributing — projeto-expoceep

Obrigado por contribuir! Este guia explica como pegar uma issue, trabalhar nela e abrir um PR seguindo um fluxo simples.

1) Escolher uma issue
- Olhe as labels (dados, frontend, backend, docs) e `easy/medium/hard`.
- Comente na issue "Quero essa" e espere confirmação do instrutor (ou atribua a si mesmo se permitido).

2) Fluxo Git (passo-a-passo)
- Atualizar main: `git checkout main && git pull origin main`
- Criar branch: `git checkout -b feature/<tipo>-<breve-descricao>`
  - Ex.: `feature/dados-baixar-uci` ou `feature/frontend-streamlit-form`
- Faça commits pequenos e atômicos: `git add . && git commit -m "Dados: adicionar script baixar"`
- Suba a branch: `git push -u origin HEAD`
- Abra um Pull Request no GitHub apontando para `main` e vinculando a issue (ex.: `Fixes #3`).

3) Checklist do PR
- O código roda localmente e não inclui dados sensíveis
- Atualizou/ adicionou documentação mínima (README ou docs/)
- Testes (se existirem) passam
- Marcar reviewers e aguardar aprovação

4) Mesclagem
- Após aprovação, o responsável (instrutor ou mantenedor) fará o merge. Use "Squash and merge" para histórico limpo, se combinado.

Como rodar localmente (exemplo mínimo)
```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python baixar.py
python limpar.py
python treinar.py
streamlit run app.py
```

Comunicação
- Use Issues e PRs para discutir alterações
- Para dúvidas rápidas, abrir issue com label `help-wanted`

Obrigado — mantenha commits pequenos e mensagens claras.

