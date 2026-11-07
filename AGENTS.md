# Instruções do projeto

@C:\Users\Usuario\.codex\RTK.md

- Responder e escrever a documentação em português do Brasil.
- Prefixar comandos de shell com `rtk`; usar `rtk proxy` quando o comando não tiver um adaptador específico.
- Stack confirmada: React + Vite no frontend, Node.js + TypeScript no backend e PostgreSQL no banco. Autenticação é a primeira funcionalidade.
- A interface deve priorizar a apresentação clara e bonita dos valores e funcionar nos dispositivos definidos no briefing.
- Consultar `docs/DEFINICAO-DO-PROJETO.md` e `docs/ARQUITETURA.md` antes de implementar. Distinguir decisões confirmadas de propostas; campos pendentes não são aprovações.
- Escolher as dependências restantes conforme os requisitos concretos, sem substituir a stack confirmada.

## Documentação contínua

- Atualizar a documentação no mesmo trabalho que altera requisitos, comportamento, contratos de API, banco, configuração ou deploy.
- Registrar escolhas técnicas relevantes e seus motivos. Manter o README como entrada para instalação, execução, testes e documentos vigentes.
- Documentar variáveis com exemplos fictícios e manter migrações e instruções operacionais junto da implementação.
- Relatar separadamente o que foi documentado, implementado e verificado. Não afirmar que uma aplicação está pronta para deploy sem as verificações do ambiente correspondente.

## Uso do ECC

O projeto usa as skills do plugin nativo `ecc@ecc` no Codex. A instalação e os comandos de manutenção estão no README.md.

- Ler o `SKILL.md` da skill relevante antes de seguir seu fluxo.
- Aplicar `coding-standards` à implementação, `tdd-workflow` a funcionalidades e correções que precisem de testes, `security-review` a alterações de segurança e `verification-loop` à validação final, conforme o escopo da tarefa.
- Fazer verificações proporcionais à mudança e relatar os resultados e limitações reais.
- Manter uma única instalação nativa do ECC. Não executar o sincronizador legado `sync-ecc-to-codex.sh` junto com o plugin.
- Usar os controles do próprio Codex para revisar e confiar nos hooks; não alterar manualmente os registros de confiança.
- Não versionar credenciais, arquivos `.env` ou dados privados de investimentos.
