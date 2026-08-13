# Roadmap de curso: Construindo o projeto (pedagógico)

Objetivo: orientar alunos passo a passo sobre o que aprender e fazer enquanto desenvolvem o projeto de previsão de evasão. Cada etapa tem objetivos de aprendizagem, tarefas práticas (issues) e entregáveis mínimos.

Como usar este roadmap
- Professores: usar como roteiro de aulas e checkpoints; ajustar prazos.
- Alunos: seguir módulos, pegar issues marcadas e abrir PRs curtos.

Pré-requisitos e configuração inicial (Módulo 0)
- Objetivos: criar conta GitHub, configurar Git local e Python, clonar repositório e rodar o projeto localmente.
- Tarefas/Issues:
  - setup/01-criar-conta-github [docs, easy]
    - Criar conta GitHub e ativar 2FA (se orientado)
  - setup/02-configurar-git [docs, easy]
    - Nome/email, SSH key ou token, testar `git push`.
  - setup/03-ambiente-python [docs, easy]
    - Criar venv, instalar `pip install -r requirements.txt`, rodar `python baixar.py` (se houver).
- Entregável: PR com screenshot de `git config --list` e comando `streamlit run app.py` rodando (ou instruções se não rodar).

Módulo 1 — Fundamentos de Git/GitHub e fluxo de trabalho
- Objetivos: entender branch, commit, PR, review e issue workflow.
- Exercícios:
  - git/01-abrir-issue-e-atualizar [docs, easy] — abrir uma issue explicando um problema simples
  - git/02-criar-branch-e-PR [docs, easy] — criar branch, fazer uma alteração pequena (README) e abrir PR
- Entregável: PR revisado e mergeado.

Módulo 2 — Exploração e ética de dados (LGPD)
- Objetivos: entender fontes de dados, exploração (EDA) e riscos de privacidade.
- Tarefas:
  - dados/01-explorar-raw [dados, easy] — carregar `dados/raw.csv`, checar tipos e missing
  - dados/02-anotar-limitacoes [docs, easy] — escrever breve nota sobre limitações e LGPD
- Entregável: notebook ou README com EDA básica (histogramas, missing, amostra de registros anonimizados).

Módulo 3 — Limpeza e engenharia de features
- Objetivos: transformar dados brutos nas 8 features do projeto, tratar missing e binarizar alvo.
- Tarefas:
  - dados/limpeza/01-mapping-variaveis [dados, medium]
  - dados/limpeza/02-validacao-idempotencia [dados, medium]
- Entregável: `dados/processed.csv` e script `limpar.py` com docstring explicando passos.

Módulo 4 — Modelagem e avaliação
- Objetivos: treinar modelo simples (regressão logística ou árvore), entender métricas e validação.
- Tarefas:
  - model/01-train-baseline [dados, medium] — treinar baseline e salvar `modelo.joblib`
  - model/02-avaliacao [dados, medium] — gerar relatório com acurácia, AUC, matriz de confusão
- Entregável: `modelo.joblib` e um relatório curto (README / notebook) explicando resultados.

Módulo 5 — Interpretabilidade e comunicação
- Objetivos: explicar por que um aluno tem risco (feature importance, coeficientes, SHAP simples).
- Tarefas:
  - interpret/01-feature-importance [dados, easy]
  - interpret/02-texto-para-usuario [docs, easy] — escrever frases curtas para explicar risco ao usuário
- Entregável: pequena seção na interface que mostra fatores que mais influenciaram a previsão.

Módulo 6 — Interface e demo (Streamlit)
- Objetivos: integrar modelo à interface e preparar demonstração.
- Tarefas:
  - front/01-form-basico [frontend, easy]
  - front/02-exibir-fatores [frontend, medium]
  - infra/01-docker-origami [backend, medium] — opcional: Dockerfile para rodar app
- Entregável: app que roda com `streamlit run app.py` e aceita inputs manuais.

Módulo 7 — Testes, documentação e reproducibilidade
- Objetivos: escrever instruções claras, testes básicos e garantir reprodutibilidade.
- Tarefas:
  - tests/01-smoke-tests [backend, easy] — script ou comando que roda pipeline mínimo
  - docs/01-runbook [docs, easy] — passo a passo para rodar localmente e preparar demo
- Entregável: comandos de smoke-test e runbook atualizado.

Módulo 8 — Preparação da apresentação e avaliação final
- Objetivos: consolidar resultados, preparar slides/roteiro e demo.
- Tarefas:
  - prep/01-script-demo [docs, easy]
  - prep/02-benchmark-e-mensagens [docs, easy] — slide com limitações e ética
- Entregável: apresentação de 5 minutos e demo funcional.

Método de execução em sala
- Dividir a turma em pares ou trios para cada issue.
- Check-ins curtos 2x por semana: 10–20 minutos por grupo.
- Cada sprint = 1 semana (ajustar conforme calendário).

Avaliação sugerida (rubrica simples)
- Completude do entregável (40%)
- Qualidade do código e commits (20%)
- Documentação e clareza (20%)
- Demonstração e comunicação (20%)

Recursos e materiais auxiliares
- Guia rápido de Git (links/trechos) — ver CONTRIBUTING.md
- Exemplos de notebooks de EDA e modelagem
- Materiais sobre LGPD e privacidade de dados

Notas finais
- Incentivar commits pequenos e PRs frequentes
- Proibir upload de dados reais no repositório
- Ajustar prazos conforme andamento da turma

