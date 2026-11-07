# Análise de investimentos

Projeto em preparação para análise de investimentos. A aplicação, a stack e as dependências do produto ainda serão definidas.

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

1. Descreva o objetivo da aplicação e peça um plano antes da implementação.
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
