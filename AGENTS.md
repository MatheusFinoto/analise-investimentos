# Instruções do projeto

@C:\Users\Usuario\.codex\RTK.md

- Responder e escrever a documentação em português do Brasil.
- Prefixar comandos de shell com `rtk`; usar `rtk proxy` quando o comando não tiver um adaptador específico.
- A aplicação ainda não tem stack ou funcionalidades definidas. Escolher dependências conforme os requisitos concretos do trabalho.

## Uso do ECC

O projeto usa as skills do plugin nativo `ecc@ecc` no Codex. A instalação e os comandos de manutenção estão no README.md.

- Ler o `SKILL.md` da skill relevante antes de seguir seu fluxo.
- Aplicar `coding-standards` à implementação, `tdd-workflow` a funcionalidades e correções que precisem de testes, `security-review` a alterações de segurança e `verification-loop` à validação final, conforme o escopo da tarefa.
- Fazer verificações proporcionais à mudança e relatar os resultados e limitações reais.
- Manter uma única instalação nativa do ECC. Não executar o sincronizador legado `sync-ecc-to-codex.sh` junto com o plugin.
- Usar os controles do próprio Codex para revisar e confiar nos hooks; não alterar manualmente os registros de confiança.
- Não versionar credenciais, arquivos `.env` ou dados privados de investimentos.
