# Roadmap pedagógico: projeto-expoceep

Objetivo pedagógico
- Aprender o ciclo completo de um projeto de IA: coleta/limpeza de dados, modelagem simples e apresentação de resultados.
- Prática colaborativa com GitHub: issues pequenas, PRs, revisão e entrega em equipe.

Resultados de aprendizagem esperados
- Executar pipeline de dados reproduzível
- Treinar e avaliar um modelo simples (interpretável)
- Criar interface básica para demonstração
- Comunicar resultados e limitações com responsabilidade (LGPD)

Visão do MVP (para a feira)
1. Pipeline: baixar dataset público → limpar → exportar 8 features + alvo
2. Treinamento: script que salva `modelo.joblib` e gera métricas simples
3. Interface: Streamlit mínimo com formulário e explicação das principais variáveis
4. Documentação curta com instruções de execução e aviso de privacidade

Organização da turma
- Labels sugeridas: dados, frontend, backend, docs, mvp, easy, medium, hard, help-wanted
- Times (flexíveis): Dados & Modelo | Interface | Infra | Documentação

Issues didáticas (cada issue deve ensinar algo)
- dados/01-baixar-dataset [dados, easy]
  - Aprendizado: acessar fontes e salvar dados localmente
  - Entregável: `dados/raw.csv` (gerado pelo script)

- dados/02-limpar-dados [dados, easy]
  - Aprendizado: limpeza, seleção de colunas e anonimização
  - Entregável: `dados/processed.csv` com 8 features + `evadiu`

- dados/03-treinar-modelo [dados, medium]
  - Aprendizado: pipeline de treino, salvar modelo, métricas básicas
  - Entregável: `dados/modelo.joblib` + relatório simples (README ou notebook)

- front/01-streamlit-form [frontend, easy, mvp]
  - Aprendizado: integrar modelo à interface e explicar saída para usuário
  - Entregável: `app.py` que roda com `streamlit run app.py`

- infra/01-docker-app [backend, medium]
  - Aprendizado: empacotar app para reproducibilidade
  - Entregável: `Dockerfile` com instruções de uso

- docs/01-readme-expand [docs, easy]
  - Aprendizado: escrever instruções claras e concisas
  - Entregável: README com como rodar e aviso LGPD

Sprints sugeridos (curtos e orientados)
- Sprint 1 (1 semana): baixar + limpar + README básico
- Sprint 2 (1 semana): treinar modelo + app mínimo
- Sprint 3 (1 semana): melhorias, testes e preparação de demo

Orientações para o professor (mentoria e avaliação)
- Reserve check-ins curtos (15–30 min) por sprint para tirar dúvidas
- Peça pequenos PRs por tarefa (1–3 arquivos) para facilitar revisão
- Critérios de avaliação: completude do entregável, clareza da documentação e qualidade do processo (commits/PRs)

Avisos de privacidade (LGPD)
- Nunca commitar CSVs com dados pessoais
- Usar apenas datasets públicos ou simulados para desenvolvimento

Referências
- Veja CONTRIBUTING.md para fluxo Git e execução local

