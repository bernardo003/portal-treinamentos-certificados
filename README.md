# CertiForm — Portal de treinamentos e certificados

Projeto acadêmico do grupo Bernardo, Samir, Rafael, Lucas e Leonardo, iniciado para a disciplina de Garantia da Qualidade de Software (UNIFACS). O produto reúne inscrição em capacitações, acompanhamento da conclusão, avaliação objetiva e geração de certificados verificáveis.

O cenário de referência é educação corporativa e RH. Qualquer menção ao Hospital Inácia Pinto dos Santos (Hospital da Mulher) é apenas um cenário didático: o repositório não contém integração institucional nem dados reais.

## O projeto em um só lugar

- [Visão integrada e Canvas](docs/01-visao-integrada.md): problema, processo, usuários, concorrentes, objetivos, impactos, riscos, referências e recorte do protótipo.
- [Protótipo e arquitetura](docs/02-prototipo-e-arquitetura.md): telas, regras, fluxo e funcionamento da demonstração.
- [Plano de validação](docs/03-plano-de-validacao.md): critérios, roteiro de inspeção, evidências a coletar e limites conhecidos.
- [Rascunho do relatório final UC HUB](docs/04-relatorio-final-uc-hub.md): respostas organizadas conforme o modelo, sem inventar resultados ainda não medidos.
- [Roteiro de pitch](docs/05-pitch-3-minutos.md): sequência e fala para apresentação curta.
- [Protótipo web](prototype/index.html): demonstração local do fluxo de inscrição, avaliação, certificado e consulta por código.
- [Entrega 1 — Requisitos](docs/entrega-01-analise-requisitos.md).
- [Entrega 2 — Planejamento de testes](docs/entrega-02-planejamento-testes.md).

## Executar o protótipo

Abra `prototype/index.html` em um navegador atual. Não precisa instalar dependências nem criar conta. Use apenas dados fictícios. Na emissão, escolha imprimir/salvar como PDF no diálogo do navegador. A verificação de código funciona no mesmo navegador, usando armazenamento local.

## Limites da demonstração

Este é um protótipo acadêmico de front-end, sem servidor, autenticação institucional, integração real com RH, armazenamento seguro, assinatura digital ou certificado oficial. O código de validação demonstra o fluxo, mas não é uma prova criptográfica. Não use dados pessoais reais. A emissão do PDF depende do recurso de impressão do navegador.

## Equipe

Bernardo · Samir · Rafael · Lucas · Leonardo

As responsabilidades individuais serão definidas pelo grupo. O proponente da proposta do Way Hub aparece como responsável pelo envio; isso não atribui papéis aos demais integrantes.

## Situação das evidências

Requisitos e casos de teste estão especificados. A construção do protótipo está disponível no repositório; medições, execução formal dos casos, capturas de evidência e aprovação de usuários devem ser registradas pelo grupo antes de afirmar resultados.
## Abrir o protótipo pela web

O site ainda precisa ser habilitado no GitHub Pages. No repositório, abra **Settings → Pages**. Em **Build and deployment**, escolha **Deploy from a branch**, selecione **main** e a pasta **/(root)** e clique em **Save**. Depois da publicação, o endereço esperado é https://bernardo003.github.io/portal-treinamentos-certificados/. Como o repositório é público, o site também ficará público. A página inicial redireciona para o protótipo em `prototype/index.html`.

A configuração de Pages é feita nas configurações do repositório; o código já está preparado para essa publicação. Consulte também a [orientação oficial do GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).
