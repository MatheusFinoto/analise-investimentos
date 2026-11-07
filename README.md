# Análise de investimentos

Plataforma de análise de investimentos em definição, com autenticação como primeira funcionalidade e foco na apresentação visual dos valores.

| Parte | Tecnologia confirmada |
| --- | --- |
| Frontend | React + Vite |
| Backend | Node.js + TypeScript |
| Banco de dados | PostgreSQL |

## Definição e arquitetura

Comece pelo [documento de definição do projeto](docs/DEFINICAO-DO-PROJETO.md). A seção **Respostas essenciais** reúne o que falta decidir para a primeira entrega; as demais seções detalham autenticação, investimentos, visual e operação. Você pode escrever `DELEGAR` nas escolhas para as quais deseja uma proposta técnica.

A [arquitetura inicial](docs/ARQUITETURA.md) descreve a organização sugerida, os limites entre frontend e API, os cuidados com valores financeiros e a preparação para deploy. As propostas estão identificadas e serão ajustadas conforme as respostas.

Neste momento, o repositório contém a documentação de planejamento. Os comandos de execução, testes, migrações e publicação serão documentados junto com a implementação correspondente.

## ECC no Codex

O [ECC](https://github.com/affaan-m/ECC) foi instalado como plugin nativo do Codex, na versão **2.2.3**. A instalação pertence ao usuário no `CODEX_HOME` ativo e pode ser usada pelos projetos desse usuário.

Node.js, Git e Codex CLI já estão disponíveis. Não há dependências da aplicação para instalar nesta pasta.

Comandos de instalação e consulta, usando o RTK configurado no ambiente:

```powershell
rtk proxy codex plugin marketplace add affaan-m/ECC --json
rtk proxy codex plugin add ecc@ecc --json
rtk proxy codex plugin list --json
```

## Como começar

Reinicie o Codex para carregar o plugin. As skills estarão disponíveis no próximo turno após o reinício.

1. Preencha as respostas essenciais do [briefing](docs/DEFINICAO-DO-PROJETO.md).
2. Use `$tdd-workflow` ao desenvolver funcionalidades com testes.
3. Use `$verification-loop` para verificar as alterações antes de concluir.

Os hooks têm uma decisão de confiança separada da instalação. No Codex CLI, abra `/hooks`, revise a definição do ECC e conceda confiança pela interface se desejar habilitá-la. Não edite os registros de confiança manualmente.

## Verificar e atualizar

A consulta de plugins confirma o registro; o verificador abaixo confere os arquivos referenciados pelo plugin. Use a **raiz de cache retornada por `plugin add --json`**. O `source.path` de `plugin list` aponta para o marketplace, não para a instalação ativa.

Na instalação atual:

```powershell
rtk proxy node 'C:\Users\Usuario\.codex\plugins\cache\ecc\ecc\2.2.3\scripts\codex\check-plugin-cache.js' --plugin-dir 'C:\Users\Usuario\.codex\plugins\cache\ecc\ecc\2.2.3'
```

Para atualizar:

```powershell
rtk proxy codex plugin marketplace upgrade ecc --json
rtk proxy codex plugin add ecc@ecc --json
rtk proxy codex plugin list --json
```

Repita a verificação com a nova raiz de cache retornada por `plugin add --json`, reinicie o Codex e revise novamente os hooks se a definição mudar.

Mantenha apenas a instalação nativa: não execute o sync legado nem instale outra cópia do ECC sobre ela. A instalação atual não exige `npm install` neste projeto.

Referência: [notas oficiais do plugin ECC para Codex](https://github.com/affaan-m/ECC/blob/main/.codex-plugin/README.md).
