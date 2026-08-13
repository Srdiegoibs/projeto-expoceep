# Roadmap: projeto-expoceep

Objetivo: fornecer um repositório limpo e didático para a turma construir um sistema simples de previsão de evasão, dividindo o trabalho em issues pequenas e claras. MVP deve estar pronto para apresentação (EXPOCEEP).

Datas-chave
- Kickoff & divisão de issues: imediato
- MVP funcional (modelo + UI minimal): até a data de entrega da feira

MVP (mínimo realmente necessário)
1. Pipeline de dados: baixar UCI → limpar → gerar 8 features + alvo
2. Modelo simples: treinar e salvar (ex.: regressão logística / sklearn)
3. Interface mínima: Streamlit com formulário + botão "Prever" mostrando risco e fatores principais
4. Instruções para reproduzir localmente + pequeno README

Estrutura de times e labels sugeridos
- labels: dados, frontend, backend, docs, mvp, easy, medium, hard, help-wanted
- times: Dados & Modelo (dados), Interface (frontend), Backend/Infra (backend), Documentação (docs)

Lista de issues pequenas (sugestões prontas para criar)
- dados/01-baixar-dataset [dados, easy]
  - Tarefa: implementar `baixar.py` que baixa o dataset UCI e salva em `dados/raw.csv`.
  - Critério de aceite: `dados/raw.csv` criado localmente após rodar script.

- dados/02-limpar-dados [dados, easy]
  - Tarefa: `limpar.py` transforma raw -> `dados/processed.csv` com as 8 colunas + `evadiu`.
  - Critério: script idempotente e sem dados pessoais.

- dados/03-treinar-modelo [dados, medium]
  - Tarefa: `treinar.py` treina um modelo simples e grava `modelo.joblib` em `dados/`.
  - Critério: script gera arquivo e relatório com métricas (acurácia/AUC).

- front/01-streamlit-form [frontend, easy, mvp]
  - Tarefa: `app.py` com formulário, chamada local ao modelo e exibição de risco + fatores.
  - Critério: roda com `streamlit run app.py` e retorna previsão.

- infra/01-docker-app [backend, medium]
  - Tarefa: Dockerfile para rodar a app Streamlit (opcional para MVP).
  - Critério: imagem builda e roda localmente.

- docs/01-readme-expand [docs, easy]
  - Tarefa: completar README com como rodar, dependências e LGPD (não subir dados reais).

- docs/02-licenca [docs, easy]
  - Tarefa: adicionar LICENSE (MIT) e `CODE_OF_CONDUCT.md` simples.

Aceitação geral de issues
- Pequenos commits atômicos
- Instruções claras no PR
- Não commitar dados sensíveis

Board e sprints
- Sprint 1 (7 dias): baixar + limpar + README básico
- Sprint 2 (7 dias): treinar modelo + app minimal
- Sprint 3 (7 dias): refinamento e preparação de demo

Observações LGPD
- Nunca comitar CSVs com dados reais
- Usar datasets anonimizados/ públicos apenas

Referências
- Instruções de execução local (ver CONTRIBUTING.md)

