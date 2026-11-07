# Definição do projeto — plataforma de análise de investimentos

**Atualizado em:** 06/11/2026  
**Status:** briefing para preenchimento; implementação ainda não iniciada.  
**Responsável pelo produto:** [PREENCHER]  
**Nome da plataforma:** [PREENCHER]

## Como preencher

Comece pela seção **1. Respostas essenciais**. Os detalhes das demais seções podem ser complementados durante o desenvolvimento. Respostas curtas e exemplos reais do uso esperado são suficientes.

- Substitua `[PREENCHER]` pelas suas respostas.
- Use `DELEGAR` quando quiser que eu proponha uma solução com justificativa e custo estimado, quando aplicável.
- Use `A DEFINIR` quando ainda precisar pensar. Um campo em branco não aprova uma sugestão.
- As opções e os exemplos ajudam a responder; não representam funcionalidades já escolhidas.
- Informe nomes de serviços e disponibilidade de contas, sem inserir senhas, tokens, chaves ou dados financeiros pessoais.

### O que já está confirmado

| Tema | Decisão do usuário |
| --- | --- |
| Produto | Plataforma de análise de investimentos. |
| Frontend | React + Vite. |
| Backend | Node.js + TypeScript. |
| Banco de dados | PostgreSQL. |
| Primeira funcionalidade | Autenticação. Os fluxos e métodos de entrada ainda serão definidos. |
| Experiência visual | Interface bonita, com apresentação de valores como prioridade. |
| Engenharia | Arquitetura organizada e preparação para deploy desde o início. |
| Documentação | Manter requisitos, decisões, funcionamento e operação documentados junto ao projeto. |
| Ferramentas de desenvolvimento | ECC instalado no Codex. |

TypeScript no frontend, framework do backend, ORM, bibliotecas visuais, estratégia de autenticação e hospedagem são escolhas em aberto. A [proposta de arquitetura](ARQUITETURA.md) apresenta uma base para discutir essas escolhas.

## 1. Respostas essenciais

Estas respostas orientam a primeira implementação. Se preferir, preencha somente esta tabela agora e use as outras seções para detalhar depois.

| ID | O que preciso saber | Sua resposta |
| --- | --- | --- |
| E01 | Quem usará a plataforma e qual problema ela deve resolver primeiro? Ex.: uso pessoal, investidores convidados, assessores ou clientes de um produto público. | [PREENCHER] |
| E02 | Os dados pertencem a cada pessoa ou a organizações/equipes? Haverá compartilhamento de carteiras ou acesso de um assessor aos dados de clientes? | [PREENCHER] |
| E03 | Qual é o limite da primeira entrega: autenticação e área logada vazia, autenticação com dashboard demonstrativo ou dashboard com dados reais? | [PREENCHER] |
| E04 | Como alguém obtém acesso: cadastro aberto, convite ou conta criada por administrador? | [PREENCHER] |
| E05 | Como será o login: e-mail e senha, Google/Microsoft, link por e-mail ou outro método? Já existe um serviço de autenticação contratado? | [PREENCHER] |
| E06 | Quais perfis de usuário existirão e o que cada um poderá fazer? Ex.: usuário e administrador, com permissões de leitura e edição distintas. | [PREENCHER] |
| E07 | Após entrar, quais são as três informações ou ações mais importantes que o usuário deve encontrar? | [PREENCHER] |
| E08 | De onde virão os dados da primeira apresentação: exemplos fictícios, cadastro manual, arquivo importado ou uma integração já disponível? | [PREENCHER] |
| E09 | Qual direção visual prefere? Informe tema claro/escuro, dispositivo principal e links de duas ou três interfaces de referência, se tiver. | [PREENCHER] |
| E10 | Onde pretende publicar? Informe orçamento mensal aproximado, domínio e serviços já disponíveis, ou escreva DELEGAR. | [PREENCHER] |
| E11 | Quais mercados, tipos de investimento e moedas devem ser atendidos primeiro? Ex.: Brasil, ações e fundos, em reais. | [PREENCHER] |
| E12 | O que você precisa conseguir demonstrar para considerar essa primeira versão pronta? Há uma data desejada e uma prioridade que pode ficar para depois? | [PREENCHER] |

## 2. Escopo da primeira versão

Use `MVP`, `DEPOIS`, `FORA` ou `DELEGAR` na coluna Fase. MVP significa a menor versão útil para a primeira entrega.

| Funcionalidade | Fase | Comportamento esperado / observações |
| --- | --- | --- |
| Autenticação | MVP — confirmado | Detalhar os fluxos na seção 3. |
| Cadastro ou convite de usuários | [PREENCHER] | Relacionar com E04. |
| Recuperação de acesso e confirmação de e-mail | [PREENCHER] | Depende do método de login. |
| Perfil do usuário e administração de acessos | [PREENCHER] | [PREENCHER] |
| Dashboard de indicadores | [PREENCHER] | Quais indicadores e se serão demonstrativos ou reais. |
| Consulta e comparação de ativos | [PREENCHER] | [PREENCHER] |
| Cadastro de carteiras e movimentações | [PREENCHER] | [PREENCHER] |
| Importação de arquivos / integração externa | [PREENCHER] | [PREENCHER] |
| Relatórios e exportação | [PREENCHER] | [PREENCHER] |
| Cobrança, planos ou assinatura | [PREENCHER] | [PREENCHER] |

**Outras funcionalidades desejadas:** [PREENCHER]  
**O que explicitamente fica fora da primeira versão:** [PREENCHER]

## 3. Autenticação, usuários e privacidade

E04–E06 definem a base. Aqui entram os detalhes necessários para desenhar as telas, os dados e os testes.

| Tema | Definição a preencher |
| --- | --- |
| Dados do cadastro | Quais informações são necessárias além do identificador de login? Há justificativa para cada dado? [PREENCHER] |
| Confirmação de e-mail | É necessária antes do primeiro acesso? Quem enviará os e-mails? [PREENCHER] |
| Recuperação de acesso | Qual fluxo espera quando o usuário perde a senha ou o acesso ao provedor? [PREENCHER] |
| Dois fatores | Necessário no MVP, somente para administradores ou em etapa futura? [PREENCHER] |
| Permanecer conectado | Por quanto tempo? Haverá prazo de inatividade e uma opção de lembrar o acesso? [PREENCHER] |
| Dispositivos e logout | Pode haver várias sessões? O usuário precisa encerrar todas ou consultar dispositivos conectados? [PREENCHER] |
| Administração | Quem convida, bloqueia, reativa ou remove usuários? Como será criado o primeiro administrador? [PREENCHER] |
| Conta e dados | O usuário poderá exportar ou excluir os dados? Há prazo de retenção ou restrição de país/região conhecida? [PREENCHER] |

Detalhe as permissões com um exemplo por perfil:

| Perfil | Pode consultar | Pode criar/alterar/excluir | Dados aos quais tem acesso |
| --- | --- | --- | --- |
| [PREENCHER] | [PREENCHER] | [PREENCHER] | Próprios, de uma equipe ou de toda a plataforma? |
| [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |

A proposta técnica prevê proteção das sessões, validação no servidor, autorização por recurso e controles contra tentativas abusivas de login. A solução concreta depende das respostas; veja [Autenticação na arquitetura](ARQUITETURA.md).

## 4. Investimentos, dados e regras de cálculo

Esta seção pode ficar para a próxima etapa quando a primeira entrega for somente autenticação. Ela deve estar definida antes de exibir resultados financeiros reais.

| Tema | Sua resposta |
| --- | --- |
| Tipo de uso | Consultar ativos, acompanhar uma carteira, simular cenários, comparar alternativas ou outra finalidade? [PREENCHER] |
| Carteiras | Uma ou várias por usuário? Existem carteiras compartilhadas, contas de corretoras ou agrupamentos? [PREENCHER] |
| Movimentações | Quais eventos precisam ser registrados: compras, vendas, aportes, retiradas, rendimentos, taxas ou outros? [PREENCHER] |
| Fontes de dados | Quais APIs, arquivos ou instituições? Já há acesso contratado e condições de uso/redistribuição conhecidas? [PREENCHER] |
| Atualização | Em tempo real, com atraso conhecido, diária ou manual? O que fazer quando uma fonte estiver indisponível? [PREENCHER] |
| Moedas e conversão | Haverá várias moedas? Qual fonte, horário e regra de câmbio deverão ser usados? [PREENCHER] |
| Datas | Quais períodos importam? Diferenciar data de operação, liquidação e horário de atualização, quando aplicável. [PREENCHER] |
| Correções | Como tratar importação duplicada, movimentação corrigida e histórico incompleto? [PREENCHER] |

Para cada indicador, descreva o significado e pelo menos um exemplo de resultado esperado. Nomes como patrimônio, retorno, lucro, proventos e rentabilidade podem representar cálculos diferentes.

| Indicador desejado | Definição / período | Inclui aportes, retiradas, taxas, impostos ou proventos? | Exemplo: entradas → resultado esperado |
| --- | --- | --- | --- |
| [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |
| [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |
| [PREENCHER] | [PREENCHER] | [PREENCHER] | [PREENCHER] |

**Comparações ou referências desejadas:** [PREENCHER]  
**Quantidade aproximada de ativos, movimentações e anos de histórico:** [PREENCHER]

## 5. Direção visual e apresentação dos valores

### Preferências a preencher

| Tema | Sua resposta |
| --- | --- |
| Identidade | Nome, logotipo, cores existentes e características desejadas: sóbria, editorial, tecnológica, outra. [PREENCHER] |
| Referências | Links de duas ou três interfaces e o que você gosta em cada uma. [PREENCHER] |
| Tema | Claro, escuro, ambos ou DELEGAR. [PREENCHER] |
| Uso principal | Desktop, celular ou apresentação em tela grande? Qual tem prioridade? [PREENCHER] |
| Densidade | Poucos indicadores em destaque ou muitos dados simultaneamente? [PREENCHER] |
| Hierarquia | Quais números, gráficos e comparações merecem maior destaque? Relacionar com E07. [PREENCHER] |
| Idioma e formato | Idioma, moeda, separadores numéricos, fuso de exibição e necessidades de internacionalização. [PREENCHER] |
| Privacidade na tela | Deve existir um controle para ocultar valores? Haverá modo de demonstração com dados fictícios? [PREENCHER] |

### Proposta visual inicial — a validar

- Composição com boa hierarquia, espaço entre blocos, tipografia legível e indicadores principais em destaque.
- Componentes consistentes para cards, tabelas, filtros, gráficos, formulários e mensagens de erro.
- Números alinhados e estáveis visualmente; moeda, unidade, período e variação identificados.
- Ganhos e perdas identificados por sinal ou texto, além da cor; foco visível e navegação por teclado. A referência proposta é [WCAG 2.2 AA](https://www.w3.org/WAI/WCAG22/quickref/).
- Gráficos acompanhados de rótulos e uma alternativa textual ou tabular para os dados relevantes.
- Estados próprios para carregamento, carteira vazia, erro, dados desatualizados e ausência de informação.
- Dados demonstrativos identificados; informações externas acompanhadas de fonte e horário de atualização.

Exemplos apenas de apresentação, usando o formato brasileiro como hipótese:

| Situação | Exemplo de apresentação | Regra a definir |
| --- | --- | --- |
| Valor monetário | R$ 125.430,87 | Moeda e casas de exibição. |
| Variação percentual | +3,42% no mês | Período, fórmula e base de comparação. |
| Resultado negativo | −R$ 320,15 | Usar sinal/texto e cor acessível. |
| Dado ausente | — / Indisponível | Nunca tratar ausência como zero. |
| Valor oculto | •••••• | A preferência deve valer também para os gráficos pertinentes. |

As casas exibidas na interface não determinam a precisão armazenada ou usada nos cálculos.

## 6. Deploy e operação

O desenho deve permitir publicar frontend, API e banco de forma reproduzível. Marque `DELEGAR` nas decisões de infraestrutura que quiser que eu proponha.

| Tema | Sua resposta |
| --- | --- |
| Hospedagem e orçamento | Detalhar E10: teto mensal, serviços existentes e se o limite inclui banco, e-mail e monitoramento. [PREENCHER] |
| Domínio e e-mail | Já possui domínio? Qual remetente deseja para confirmação de acesso e recuperação? [PREENCHER] |
| Ambientes | Precisa de desenvolvimento local, homologação e produção? Haverá ambiente público de demonstração? [PREENCHER] |
| Região | Existe preferência ou restrição de região para aplicação, banco e backups? [PREENCHER] |
| Volume | Quantos usuários cadastrados e simultâneos espera no início e nos próximos meses? [PREENCHER] |
| Disponibilidade | Quanto tempo de indisponibilidade seria tolerável? [PREENCHER] |
| Recuperação | Quanto dado pode ser perdido em um incidente e em quanto tempo precisa recuperar? Se não souber, DELEGAR. [PREENCHER] |
| Responsáveis | Quem terá acesso administrativo e receberá avisos de falhas? [PREENCHER] |
| Publicação | Deploy automático após validação ou execução manual? Há restrições de acesso ao repositório? [PREENCHER] |

As contas e credenciais serão configuradas pelos mecanismos privados dos serviços escolhidos, fora deste documento.

## 7. Preferências técnicas que podem ser delegadas

Preencha apenas se já tiver uma preferência. A stack confirmada será mantida em qualquer proposta.

| Escolha | Preferência ou DELEGAR |
| --- | --- |
| TypeScript também no frontend | [PREENCHER] |
| Framework HTTP do backend e acesso ao PostgreSQL / ORM | [PREENCHER] |
| Autenticação própria ou serviço externo | Relacionar com E05. [PREENCHER] |
| Biblioteca de componentes, estilos e gráficos | [PREENCHER] |
| Gerenciador de pacotes, testes e automação de CI | [PREENCHER] |

A proposta inicial usa monorepo e backend modular, com contratos de API documentados, migrações de banco e configurações por ambiente. São propostas, ainda sem código implementado; consulte [ARQUITETURA.md](ARQUITETURA.md).

## 8. Critérios de aceite propostos

As caixas representam verificações futuras. Os fluxos opcionais só entram no aceite se forem incluídos no escopo acima.

- [ ] Os fluxos de entrada escolhidos funcionam de ponta a ponta e têm mensagens de erro compreensíveis.
- [ ] Páginas protegidas e endpoints privados exigem autenticação; a API aplica as permissões de cada perfil.
- [ ] Testes comprovam o isolamento entre proprietários ou organizações distintos, se existirem.
- [ ] Expiração, renovação quando aplicável e logout seguem as regras de sessão; sessões revogadas deixam de autorizar chamadas.
- [ ] Recuperação e confirmação de acesso, quando previstas, cobrem códigos ou links inválidos, expirados e reutilizados.
- [ ] Telas permanecem legíveis e utilizáveis em 360, 768 e 1440 px; formulários funcionam por teclado.
- [ ] Indicadores reais conferem com exemplos de cálculo aprovados, incluindo precisão e arredondamento; dado ausente difere de zero.
- [ ] Dados demonstrativos, fontes externas e horários de atualização ficam identificados conforme o cenário.
- [ ] Build, tipos, lint e testes aplicáveis passam na integração contínua.
- [ ] Outra pessoa consegue preparar o ambiente e executar as migrações seguindo a documentação, sem receber segredos pelo repositório.
- [ ] O ambiente publicado passa por verificação de saúde e dos fluxos críticos. Antes da produção, backup/restauração e recuperação de publicação estão documentados e verificados.

## 9. Documentação que acompanhará o desenvolvimento

| Documento / artefato | Quando atualizar |
| --- | --- |
| Este briefing | Quando o escopo ou uma regra de negócio for definido ou mudar. |
| [Arquitetura](ARQUITETURA.md) | Quando responsabilidades, integrações, segurança ou infraestrutura mudarem. |
| [README](../README.md) | Quando os passos para instalar, desenvolver, testar ou navegar no projeto mudarem. |
| Contrato de API | Junto com cada endpoint implementado, incluindo autenticação, entradas, erros e exemplos. |
| Migrações e modelo de dados | Junto com cada mudança persistente no banco. |
| Guia de deploy e operação | Ao implementar os ambientes, com configuração, publicação, verificação, backup e recuperação. |

Requisitos, decisões confirmadas e propostas devem permanecer distinguíveis. A documentação é atualizada no mesmo trabalho que altera o comportamento correspondente.

## 10. Como transformar as respostas em implementação

1. Consolidar as respostas essenciais e delimitar a primeira entrega.
2. Detalhar os fluxos de autenticação, as telas e os critérios de aceite correspondentes.
3. Atualizar a arquitetura com as escolhas técnicas justificadas e os ambientes definidos.
4. Implementar a estrutura, o banco e a autenticação com os testes pertinentes e a documentação de execução.
5. Verificar a experiência visual e a publicação no ambiente escolhido, registrando o que foi efetivamente testado.

**Observações adicionais / restrições que ainda não apareceram:** [PREENCHER]
