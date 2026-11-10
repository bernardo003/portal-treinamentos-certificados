# Análise e validação de requisitos

## Portal de treinamentos e certificados | Modelo 2

Versão 1.0 | 10 de novembro de 2026


> Projeto A3 de Garantia da Qualidade de Software — UNIFACS


## Resumo e contexto

Esta entrega define os requisitos iniciais do portal de treinamentos e certificados proposto para o Hospital Inácia Pinto dos Santos (Hospital da Mulher), em Feira de Santana. O escopo segue o Modelo 2 do cronograma: Educação Corporativa e RH. A função principal será permitir que um colaborador conclua um curso, seja aprovado em uma avaliação e receba um certificado PDF verificável.

A análise transforma a narrativa do enunciado em requisitos identificáveis e critérios observáveis. A integração com RH é simulada; todos os dados do protótipo serão fictícios. O documento registra decisões ainda pendentes como perguntas, sem tratá-las como regras aprovadas.



## 1. Problema e objetivo

No cenário didático, listas em papel e planilhas dificultam comprovar a participação em capacitações e podem atrasar a emissão de certificados por 15 a 30 dias. A equipe propõe organizar inscrição, progresso, avaliação, histórico e emissão de certificados em um portal responsivo.

Objetivo: demonstrar um fluxo rastreável que, após a conclusão das atividades e aprovação do colaborador, gere um certificado PDF em até cinco segundos e permita confirmar sua autenticidade por um código exclusivo, com exposição mínima de dados pessoais. A meta institucional de eliminar a espera administrativa e alcançar conformidade até o fim do trimestre é uma meta de negócio; não substitui os critérios verificáveis do software.



## 2. Escopo da solução

Incluído no escopo funcional proposto: acesso por matrícula e senha; catálogo de cursos; elegibilidade por setor ou função; acompanhamento de progresso; avaliação objetiva; configuração administrativa de cursos e nota mínima; emissão e consulta de certificado; histórico preservado após arquivamento; relatórios por setor; e avisos de vencimento, sujeitos à definição do prazo.

Fora do escopo desta entrega: integração real com RH, autenticação institucional, armazenamento de dados reais, assinatura institucional juridicamente válida, operação hospitalar em produção e construção de todo o sistema. A entrega de 04/11/2026 pede análise e validação de requisitos. Esboço de telas e fluxo e o plano detalhado de testes pertencem à etapa seguinte do cronograma.



## 3. Requisitos funcionais

RF-01 — A aplicação deve permitir que o colaborador acesse sua área usando matrícula e senha fictícias no protótipo.

RF-02 — O colaborador deve consultar o catálogo e identificar cursos disponíveis, obrigatórios e destinados ao seu setor ou função.

RF-03 — O colaborador deve iniciar um curso elegível e consultar as atividades concluídas e o progresso registrado.

RF-04 — O sistema deve apresentar avaliação objetiva e registrar respostas, nota, resultado e data da tentativa.

RF-05 — Um administrador deve cadastrar e atualizar curso, carga horária, conteúdo, período de oferta, questões e nota mínima; deve também suspender inscrições e arquivar cursos sem apagar o histórico.

RF-06 — O sistema deve aplicar nota mínima geral de 70% e permitir configurar limite superior por curso, conforme regra de negócio descrita no enunciado.

RF-07 — O sistema deve aprovar a emissão somente quando todas as atividades obrigatórias estiverem concluídas e a nota atingir a mínima aplicável.

RF-08 — Após aprovação, o sistema deve gerar um PDF com nome, identificação apropriada, curso, carga horária, data de conclusão e código exclusivo de verificação.

RF-09 — A consulta de autenticidade pelo código deve informar se o certificado é válido sem revelar dados pessoais além do necessário. A informação exata exibida depende de validação.

RF-10 — O histórico de cursos, resultados e certificados deve continuar disponível após o arquivamento do curso.

RF-11 — Gestores autorizados devem consultar a situação dos treinamentos de seus setores e relatórios de inscrições, aprovações, reprovações, conclusões e pendências.

RF-12 — O sistema deve notificar o colaborador sobre vencimento próximo de treinamento; antecedência, canais e frequência precisam ser definidos.

RF-13 — A aplicação deve manter registros de auditoria das operações relevantes, associados a usuário, data, horário e ação, respeitando o perfil de acesso.

RF-14 — O protótipo deve simular o cadastro de RH e usar somente contas, cursos e resultados fictícios.



## 4. Requisitos não funcionais

RNF-01 — Responsividade: as páginas principais devem se adaptar a computador e dispositivo móvel. As larguras e combinações de navegadores a validar ainda precisam ser definidas.

RNF-02 — Acessibilidade: operações principais devem poder ser realizadas por teclado. O nível, as tecnologias assistivas e os critérios de conformidade ainda precisam ser acordados.

RNF-03 — Desempenho: sob uma carga de referência de até 500 acessos simultâneos, páginas principais devem carregar em até três segundos. O perfil de carga e as condições de medição precisam ser definidos.

RNF-04 — Geração: o certificado deve ser disponibilizado em até cinco segundos após o sistema confirmar aprovação e conclusão, sob condições de medição acordadas.

RNF-05 — Disponibilidade: a meta didática é 99,5% ao mês, excluída manutenção programada. Janela de medição, monitoramento e comunicação de indisponibilidade precisam ser definidos.

RNF-06 — Segurança e privacidade: perfis de acesso, proteção dos dados, trilha de auditoria e consulta de autenticidade com exposição mínima de dados devem ser considerados desde o desenho. Não usar dados pessoais reais no protótipo.

RNF-07 — Manutenibilidade: administradores devem poder atualizar conteúdos e parâmetros do curso sem perder resultados, certificados ou histórico já registrados.

RNF-08 — Portabilidade: o fluxo principal deve funcionar em navegadores atuais e em telas móveis. A lista de versões suportadas deve ser acordada antes da validação final.



## 5. Regras de negócio

RN-01 — Um certificado só pode ser emitido após a conclusão de todas as atividades obrigatórias e aprovação na avaliação.

RN-02 — A nota mínima padrão é 70%; um curso pode exigir percentual superior quando configurado.

RN-03 — Cada certificado deve possuir código exclusivo que permita verificar sua autenticidade.

RN-04 — Arquivar um curso não apaga o histórico de participação, resultado ou certificado.

RN-05 — O colaborador só acessa cursos compatíveis com seu público-alvo e gestores só consultam os setores autorizados.

RN-06 — O protótipo usa exclusivamente dados fictícios e não se integra a sistemas reais do hospital.



## 6. Atributos de qualidade prioritários

Funcionalidade — O fluxo completo deve cumprir as regras de conclusão, aprovação e emissão. Isso é essencial para que o certificado represente um treinamento concluído.

Usabilidade e acessibilidade — Colaboradores precisam localizar treinamentos e entender claramente progresso, resultado e próximo passo; o fluxo principal precisa operar por teclado.

Eficiência de desempenho — Os limites de três segundos para páginas e cinco segundos para emissão dão referências mensuráveis, condicionadas a um perfil de carga definido.

Confiabilidade — Resultado, data, certificado e histórico precisam permanecer consistentes; arquivamento não pode remover registros já emitidos.

Segurança — Acesso por perfil, trilha de auditoria e validação pública com dados mínimos reduzem exposição indevida e ajudam a rastrear alterações.

Manutenibilidade — Atualizar conteúdo e nota mínima sem perder histórico facilita a gestão contínua dos cursos.

Portabilidade — Compatibilidade com navegadores atuais e uso em dispositivos móveis atendem ao contexto web e mobile do enunciado.



## 7. Critérios de aceitação iniciais

CA-01 (RF-03, RF-07): dado um colaborador com todas as atividades concluídas e nota igual ou superior à mínima do curso, ao finalizar a avaliação, o sistema registra aprovação e habilita a emissão. Se faltar uma atividade ou a nota ficar abaixo do limite, a emissão permanece bloqueada.

CA-02 (RF-06): em curso com limite padrão, nota de 70% aprova e nota abaixo de 70% reprova. Em curso configurado com limite superior, o resultado respeita esse limite.

CA-03 (RF-08, RNF-04): após aprovação, o sistema gera um PDF em até cinco segundos contendo nome, identificação apropriada, curso, carga horária, data de conclusão e código exclusivo.

CA-04 (RF-09): ao informar um código válido, a consulta identifica o certificado como válido; para código inexistente, informa que não foi localizado. A resposta não exibe matrícula ou outros dados pessoais, salvo decisão expressa dos interessados.

CA-05 (RF-05, RF-10, RN-04): após arquivar um curso, novos acessos seguem o estado definido para o curso e registros anteriores de participação, nota e certificado continuam consultáveis por perfil autorizado.

CA-06 (RF-11, RN-05): um gestor consulta dados do setor autorizado; tentativa de consultar setor não autorizado não retorna dados desse setor.

CA-07 (RNF-01, RNF-02): o colaborador consegue percorrer catálogo, curso, avaliação e certificado em viewport móvel acordado e completar o fluxo sem mouse.

CA-08 (RNF-03, RNF-04, RNF-05): sob ambiente, janela e perfil de carga aprovados pelos interessados, medição demonstra os limites de tempo e disponibilidade definidos. O perfil e o período de observação ainda são pendências de validação.



## 8. Ambiguidades e perguntas para validação

Tentativas: as avaliações terão tentativas ilimitadas ou limite de três? O limite será global ou configurável por curso? Haverá intervalo ou reinício de progresso entre tentativas?

Aprovação: a nota mínima acima de 70% será configurável por curso? Como tratar arredondamento da nota e questões anuladas? Quais atividades contam como obrigatórias?

Certificado: qual modalidade de assinatura ou validação institucional será usada? A matrícula deve aparecer no PDF ou pode ser substituída por identificador reduzido? O que exatamente a página pública de verificação deve exibir?

Código: qual formato e tamanho são aceitos? A consulta será pública sem autenticação? Como tratar certificado cancelado, corrigido ou reemitido?

Validade e avisos: quais cursos vencem? Qual antecedência, canal, frequência e destinatário dos avisos? O que acontece quando o colaborador muda de setor?

Perfis: quais ações cabem a colaborador, gestor, administrador e auditor? Quem pode alterar resultado, curso ou certificado e qual justificativa deve ficar registrada?

Integração: quais campos viriam do RH no cenário real? Para a atividade, quais dados fictícios bastam para demonstrar elegibilidade por setor e função?

Qualidade: quais navegadores e tecnologias assistivas serão considerados atuais? Como serão definidos perfil de 500 acessos, início/fim da medição de desempenho e disponibilidade, janela mensal e manutenções excluídas?

Retenção e privacidade: por quanto tempo manter cursos, resultados, logs e certificados? Quem aprova a política de retenção e a exposição mínima na verificação?



## 9. Definição da funcionalidade principal

Fluxo de ponta a ponta: (1) colaborador acessa o portal com conta fictícia; (2) consulta e inicia curso disponível para seu perfil; (3) conclui as atividades; (4) responde à avaliação objetiva; (5) sistema compara a nota com a regra aplicável; (6) em caso de aprovação, gera certificado PDF com código exclusivo; (7) usuário ou terceiro consulta o código e recebe apenas a informação mínima necessária para confirmar autenticidade.

Cenário de falha essencial: atividade pendente ou nota inferior à mínima impede emissão, apresenta o motivo e preserva o resultado para consulta autorizada. O protótipo da etapa futura deverá permitir demonstrar os dois caminhos com dados fictícios.



## 10. Encaminhamento

Antes de congelar os requisitos, validar as decisões listadas na seção 8 com os interessados ou registrar explicitamente as premissas adotadas para o trabalho. Na etapa seguinte, decompor a funcionalidade em fluxo e telas, preparar plano e casos de teste e ligar cada critério de aceitação ao requisito correspondente.



