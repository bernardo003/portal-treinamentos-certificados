# CertiForm — visão integrada do projeto

**Projeto acadêmico | Modelo 2 — Educação Corporativa e RH**  
**Grupo:** Bernardo, Samir, Rafael, Lucas e Leonardo  
**Versão:** 1.0 | **Data:** 18/11/2026

> O cenário é uma simulação acadêmica. Não representa implantação oficial de hospital ou instituição. Todos os registros da demonstração devem ser fictícios.

## 1. Resumo executivo

O CertiForm é um portal web que organiza o ciclo de uma capacitação: inscrição, acesso ao curso, acompanhamento de atividades, avaliação, decisão de aprovação, geração de certificado e validação por código. A proposta reduz tarefas repetidas em planilhas e emissão individual de documentos, mantendo a regra de aprovação visível e o histórico consultável.

A primeira versão é um protótipo front-end que simula uma atividade, coleta o nome para o certificado, aplica nota mínima, bloqueia emissão quando falta atividade ou aprovação e prepara uma página de certificado para impressão como PDF. A validação por código funciona localmente no mesmo navegador e serve apenas para demonstrar o conceito; não é uma assinatura ou autenticação inviolável.

## 2. Problema, contexto e oportunidade

No cenário do trabalho, cursos internos são controlados por listas, planilhas e conferências manuais. A equipe precisa comparar inscrições, comprovação de conclusão e resultado de avaliação antes de emitir certificados. Esse caminho pode gerar retrabalho, divergências e demora. O contexto didático aponta uma espera potencial de 15 a 30 dias; a equipe não mediu esse prazo em uma instituição real.

A oportunidade é centralizar os passos e tornar explícito por que um certificado pode ou não ser emitido. A automação deve diminuir o tempo administrativo e erros de transcrição sem remover a conferência, as permissões e a rastreabilidade.

## 3. Objetivo geral e objetivos específicos

**Objetivo geral:** demonstrar um fluxo web simples e rastreável para inscrição em capacitações e emissão de certificado após conclusão e aprovação.

**Objetivos específicos:**

1. reunir os dados mínimos necessários para identificar participante e curso;
2. mostrar etapas concluídas e pendentes;
3. aplicar a nota mínima geral de 70%, permitindo a regra superior do curso quando configurada;
4. bloquear o certificado quando falta atividade obrigatória ou a nota não atinge o mínimo;
5. gerar uma página de certificado imprimível com nome, curso, carga horária, data e código;
6. permitir consulta de um código sem expor matrícula ou outros dados desnecessários;
7. comparar o processo manual proposto com o fluxo automatizado por tempo, erros e facilidade de uso;
8. manter a demonstração sem dados reais e sem integração institucional.

## 4. Usuários e partes interessadas

| Perfil | Necessidade | Acesso proposto |
|---|---|---|
| Participante/colaborador | Encontrar curso elegível, entender progresso e obter certificado | Catálogo, atividades, avaliação, histórico e certificado próprio |
| Gestor de setor | Acompanhar conclusão e pendências de sua equipe | Indicadores agregados e registros do setor autorizado |
| Administrador de treinamento | Cadastrar curso, público, carga horária, questões e nota mínima | Gestão de cursos e parâmetros |
| Auditor/revisor | Conferir consistência de eventos e mudanças | Registros de auditoria autorizados |
| Instituição/área de RH | Definir regras, retenção e integração futura | Participação na validação do processo e regras |
| Equipe do projeto | Construir, documentar e revisar a demonstração | Ambiente acadêmico com massa fictícia |

Os perfis administrativos e de gestor são descritos para a solução futura. O protótipo atual demonstra somente a jornada do participante e a consulta local do código.

## 5. Processo atual e pontos a otimizar

### Fluxo atual do cenário

1. gestor divulga o treinamento;
2. participante manifesta interesse por formulário, lista ou mensagem;
3. responsável consolida inscrições em planilha;
4. participante acessa o conteúdo em um canal separado;
5. presença e atividades são conferidas manualmente;
6. avaliação é corrigida ou consolidada em outra lista;
7. responsável compara presença, conclusão e nota;
8. dados são transcritos para o certificado;
9. certificado é gerado e enviado individualmente;
10. participante guarda o arquivo e terceiros não têm verificação simples.

### Pontos críticos

- dados repetidos em formulários, planilhas e documentos;
- ausência de uma visão única do estado de cada participante;
- risco de emitir antes da conclusão ou registrar resultado incorreto;
- tempo gasto copiando nomes, cursos, datas e cargas horárias;
- histórico difícil de localizar após encerrar uma turma;
- verificação de autenticidade dependente de contato manual;
- acesso a dados sem uma regra explícita por perfil.

### Fluxo proposto

Divulgação e catálogo → inscrição → curso e progresso → conclusão das atividades → avaliação objetiva → regra de aprovação → certificado em PDF com código → verificação mínima por código → histórico e relatório autorizado.

A jornada detalhada e os casos de falha estão em [Entrega 2 — Planejamento de testes](entrega-02-planejamento-testes.md).

## 6. Canvas de otimização do processo — 12 vertentes

1. **Objetivo geral:** reduzir a fragmentação e demonstrar emissão consistente após conclusão e aprovação.
2. **Processo de referência:** inscrição, realização do curso, registro de progresso, avaliação, conferência e emissão.
3. **Pontos a otimizar:** redigitação, espera pela conferência, erros de consolidação, falta de status e busca manual de comprovantes.
4. **Público e envolvidos:** participantes, gestores, administradores de treinamento, RH e equipe de revisão.
5. **Modelo futuro:** formulário único ligado ao curso, registro de progresso, regra de aprovação e geração automática.
6. **Simulação e viabilidade:** front-end local, curso/questões fictícias, geração via impressão para PDF e lista local de códigos demonstrativos.
7. **Dados e análise:** registrar tempo de cada etapa, número de correções, emissão bloqueada corretamente e percepção de clareza; comparar cenários equivalentes.
8. **Ferramentas e tecnologia:** HTML, CSS e JavaScript sem dependências para o protótipo; servidor e banco ficam para uma fase posterior.
9. **Impactos da mudança:** menos cópia manual e maior visibilidade do status; será necessário treinar usuários, definir responsáveis e manter regras atualizadas.
10. **Contribuições esperadas:** rastreabilidade didática, resposta rápida para o participante, histórico organizado e verificação simples por código.
11. **Desafios e riscos:** dados expostos, regra de nota ambígua, código copiável, falha de armazenamento local, acessibilidade incompleta e expectativa de integração real.
12. **Trabalhos relacionados e referências:** geradores a partir de formulários, certificados de LMS e criação em lote de designs ajudam a comparar a solução, mas não são equivalentes ao portal integrado proposto.

## 7. Análise de alternativas e concorrentes

| Referência | Pontos fortes observados na proposta do produto | Limites para o problema do CertiForm | Aprendizado para a solução |
|---|---|---|---|
| Form Publisher para Google Forms | Gera documentos a partir de respostas submetidas em formulário e pode produzir PDF | A geração do documento, por si só, não cobre o ciclo de curso, progresso, avaliação e regra de aprovação descrito neste projeto | Automatizar o documento depois de validar dados e resultado |
| Moodle Custom Certificate | Emite certificados PDF ligados a cursos e oferece código de verificação | Depende de um ambiente LMS e configuração do curso; pode ser mais amplo do que um fluxo simples de emissão | Vincular certificado a um curso e permitir conferir autenticidade |
| Canva Bulk Create | Gera variações de um design com dados em linhas/colunas | Criação em lote de peças não substitui inscrição, acompanhamento e aprovação | Manter o certificado visualmente consistente e preencher campos padronizados |

As referências servem como comparação funcional, não como avaliação completa de custo, segurança ou adequação institucional. Páginas oficiais consultadas: [Form Publisher — geração de documentos](https://support.form-publisher.com/hc/en-us/articles/4412622922258-Overview-of-generating-documents-for-Google-Forms), [Moodle — Custom certificate](https://docs.moodle.org/502/en/Custom_certificate_module) e [Canva — Bulk Create](https://www.canva.com/help/bulk-create/).

## 8. Proposta de valor e diferenciais

- fluxo de emissão condicionado a conclusão e nota, em vez de emissão automática após um formulário isolado;
- justificativa clara quando o certificado está bloqueado;
- código de verificação sem mostrar matrícula na consulta;
- desenho de uma jornada completa, do catálogo à validação;
- dados fictícios e protótipo leve, adequado a demonstração acadêmica;
- possibilidade futura de integração, mediante autorização, segurança e definição de dados necessários.

## 9. Escopo e fora de escopo

**Incluído nesta demonstração:** dados de participante fictício, curso de exemplo, atividades, avaliação objetiva, aprovação/reprovação, bloqueio de emissão, certificado imprimível e validação local por código.

**Fora do protótipo:** autenticação real, integração com RH/LMS, armazenamento em servidor, assinatura digital, notificações, relatórios reais de setor, escalabilidade de 500 acessos, disponibilidade de 99,5% e uso em hospital ou instituição em produção. As metas de desempenho e disponibilidade são requisitos a validar em ambiente próprio, não resultados já comprovados.

## 10. Indicadores para avaliar a proposta

- tempo entre aprovação e certificado disponível;
- tempo total da conferência no fluxo manual e no protótipo;
- erros de transcrição detectados por cenário;
- percentual de tentativas bloqueadas corretamente por pendência ou reprovação;
- sucesso de consulta de código válido e rejeição de código desconhecido;
- conclusão do fluxo por teclado e em tela móvel;
- percepção de clareza do participante em uma avaliação simples;
- defeitos encontrados e corrigidos antes da demonstração.

A coleta deve descrever número de participantes, cenário, instrumento, data e versão. Nenhuma métrica será afirmada sem registro.

## 11. Riscos e respostas

| Risco | Resposta de projeto |
|---|---|
| Certificado emitido indevidamente | Regra explícita de conclusão e nota, com cenários de bloqueio |
| Código tratado como prova forte de autenticidade | Informar que o código local é demonstrativo; solução real precisaria de serviço seguro e assinatura/verificação adequada |
| Exposição de dado pessoal | Verificação pública retorna apenas estado, curso e data se aprovado pelos envolvidos; nunca exibir matrícula |
| Regra de nota ou tentativas mal interpretada | Registrar premissas e validar com orientador/usuários antes de congelar |
| Usuário não perceber o motivo do bloqueio | Mensagem direta, indicação de atividade pendente e progresso |
| Falha ou limpeza do armazenamento local | Avisar que a demonstração depende do mesmo navegador; não prometer persistência real |
| Grupo atribuir resultado sem teste | Distinguir claramente planejamento, protótipo e evidência observada |
| Falha de acesso por teclado ou em tela pequena | Revisar etiquetas, foco, mensagens e layout; registrar limitações não corrigidas |

## 12. Questões pendentes de validação

- Há limite de tentativas da avaliação? O enunciado tem referências divergentes; nenhuma regra foi inventada.
- Como arredondar nota, tratar questão anulada e definir atividades obrigatórias?
- O curso pode definir nota acima de 70%? Quem configura?
- Quais campos podem aparecer no PDF e na consulta pública?
- Como cancelar ou reemitir certificado?
- Qual validade e política de aviso para cada treinamento?
- Quais papéis podem alterar cursos, resultados e certificados?
- Qual prazo de retenção para resultados, logs e documentos?
- Quais tecnologias assistivas, navegadores e condições de carga serão adotados na validação?

## 13. Roteiro de evolução

1. revisar requisitos e decisões pendentes com o orientador;
2. apresentar o fluxo e o protótipo aos colegas;
3. coletar evidências reais de inspeção e execução dos casos planejados;
4. corrigir problemas de usabilidade e de regra encontrados;
5. preparar ambiente com backend fictício somente se a disciplina exigir persistência compartilhada;
6. medir desempenho apenas em ambiente controlado e documentar perfil/carga;
7. fechar o relatório e o pitch com resultados observados, limites e próximos passos.

## Referências do problema e da solução

- Form Publisher, “Overview of generating documents with Form Publisher for Google Forms”: https://support.form-publisher.com/hc/en-us/articles/4412622922258-Overview-of-generating-documents-for-Google-Forms
- MoodleDocs, “Custom certificate module”: https://docs.moodle.org/502/en/Custom_certificate_module
- Canva Help Center, “Bulk Create”: https://www.canva.com/help/bulk-create/
- Requisitos e regras do cenário acadêmico: [Análise e validação de requisitos](entrega-01-analise-requisitos.md).
- Estratégia e casos planejados: [Planejamento dos testes](entrega-02-planejamento-testes.md).
