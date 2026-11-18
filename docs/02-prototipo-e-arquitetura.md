# Protótipo e arquitetura — CertiForm

**Versão 1.0 | 18/11/2026**

## Propósito

Demonstrar o fluxo principal de certificação com uma página estática, sem instalação ou serviço externo. O arquivo [index.html](../prototype/index.html) reúne interface, estilos e lógica de demonstração.

## Fluxo

1. A pessoa informa um nome fictício, escolhe a capacitação e confirma as atividades concluídas.
2. O protótipo apresenta quatro questões de múltipla escolha.
3. A nota é calculada em percentual. A regra padrão de demonstração é 70%; a opção de 80% simula um curso com exigência superior.
4. Se faltar atividade, o certificado fica bloqueado. Se a nota não atingir o mínimo, o resultado informa reprovação e também bloqueia a emissão.
5. Com conclusão e nota suficientes, o protótipo gera um código demonstrativo e mostra o certificado.
6. O usuário pode imprimir ou salvar a página como PDF pelo navegador.
7. A área de validação aceita o código no mesmo navegador e mostra apenas validade, curso e data.

## Telas e elementos

| Área | Conteúdo | Comportamento esperado |
|---|---|---|
| Catálogo/formulário | Curso de exemplo, carga horária, nome e conclusão de atividades | Campos com rótulo; avançar para avaliação |
| Avaliação | Quatro questões com alternativas | Calcular nota sem mostrar resposta correta antes do envio |
| Resultado | Aprovado/reprovado e próximo passo | Explicar bloqueio sem apagar respostas |
| Certificado | Nome, atividade, carga horária, data e código | Imprimir/salvar PDF; ocultar controles na impressão |
| Verificação | Campo de código e resultado | Validar código local e não mostrar nome ou matrícula |

## Dados da demonstração

- Nome do participante: informado na sessão; usar um nome fictício.
- Curso padrão fictício: “Segurança do paciente e boas práticas assistenciais” (4 horas); segunda opção demonstrativa: “Comunicação e trabalho em equipe” (2 horas).
- Carga horária: 4 horas.
- Conclusão: data escolhida no formulário.
- Nota mínima: 70% ou 80% no modo de demonstração.
- Código: identificador aleatório demonstrativo.

O navegador mantém no armazenamento local apenas código, curso, data e situação para a consulta da própria demonstração. O nome é usado para compor o certificado na sessão e não é retornado pela tela de validação. Limpar os dados do navegador remove as chaves locais.

## Decisões de implementação

- HTML semântico e rótulos associados aos controles;
- CSS responsivo para telas estreitas;
- JavaScript sem biblioteca externa;
- conteúdo inserido pelo usuário exibido como texto, não interpretado como marcação HTML;
- emissão por janela de impressão do navegador, que permite “Salvar como PDF”;
- código e validação são locais, não criptográficos e não compartilhados com terceiros.

## Limitações técnicas

- Sem backend, API, banco, login, envio de e-mail ou sincronização entre dispositivos.
- O armazenamento local pode ser editado ou apagado pelo usuário; não serve para verificar um certificado oficial.
- O certificado não inclui assinatura institucional.
- A configuração de curso é fixa na demonstração; o seletor de nota é apenas um modo didático.
- Não foram medidos desempenho sob concorrência, disponibilidade mensal ou segurança de produção.
- Acessibilidade foi considerada no markup, mas ainda precisa de inspeção formal com teclado e tecnologias assistivas.


## Referências do conteúdo demonstrativo

As perguntas introdutórias sobre identificação segura e higiene das mãos são baseadas nas orientações oficiais da [Anvisa sobre identificação do paciente](https://www.gov.br/anvisa/pt-br/assuntos/servicosdesaude/seguranca-do-paciente/avaliacao-nacional-das-praticas-de-seguranca-do-paciente/DILISEORIENTAESDEPREENCHIMENTOAVALIACODASPRATICASDESEGDOPACIENTE2025_versofinal010425.pdf) e no [protocolo de higiene das mãos](https://www.gov.br/anvisa/pt-br/centraisdeconteudo/publicacoes/servicosdesaude/publicacoes/protocolo-de-higiene-das-maos). O conteúdo é educativo e genérico; a capacitação real deve seguir protocolos e orientação profissional da instituição. A demonstração não substitui treinamento oficial.
