# Plano de validação do protótipo — CertiForm

**Versão 1.0 | 18/11/2026**  
**Grupo:** Bernardo, Samir, Rafael, Lucas e Leonardo

## O que verificar

A avaliação deve usar dados fictícios e registrar versão, dispositivo/navegador, passos, resultado esperado, resultado observado e evidência. Os casos detalhados continuam em [Entrega 2 — Planejamento de testes](entrega-02-planejamento-testes.md); este roteiro concentra a demonstração do protótipo.

## Roteiro de inspeção manual

| Cenário | Ação | Resultado esperado | Evidência a salvar |
|---|---|---|---|
| Jornada aprovada | Concluir atividades e responder corretamente o suficiente | Aprovação, código e certificado disponíveis | Capturas sem dados reais; data e navegador |
| Atividade pendente | Deixar uma atividade desmarcada e tentar avançar/emitir | Mensagem de pendência; nenhum certificado | Captura da mensagem |
| Nota abaixo do mínimo | Concluir atividades e acertar menos que o mínimo | Reprovação e emissão bloqueada | Captura da nota e do bloqueio |
| Limite superior | Selecionar regra de 80% e obter uma nota entre 70% e 79% | Reprovação conforme configuração simulada | Captura da regra e resultado |
| Código válido | Consultar o código emitido na mesma sessão/navegador | Status válido, curso e data; sem nome/matrícula | Captura do resultado mínimo |
| Código inválido | Consultar um código que não existe | Mensagem “não localizado”; sem dados de terceiros | Captura do estado inválido |
| Layout móvel | Usar janela estreita e percorrer os controles | Texto e botões utilizáveis sem rolagem horizontal | Capturas da tela estreita |
| Teclado | Percorrer campos e ações sem mouse | Foco visível e ordem de navegação compreensível | Registro de barreiras, se houver |
| PDF | Imprimir ou salvar certificado | Apenas o certificado é impresso; conteúdo e código legíveis | PDF demonstrativo fictício |

## Critérios de aceitação do protótipo

- Certificado disponível somente com atividades concluídas e nota mínima atingida.
- O resultado de reprovação informa que nenhum certificado foi criado.
- O PDF imprimível contém nome informado, curso, carga horária, data e código.
- Validação local reconhece um código emitido e rejeita um valor desconhecido.
- Tela de consulta não mostra nome nem matrícula.
- As limitações da validação local aparecem claramente para quem usar a demonstração.

## Como registrar defeitos

Para cada problema: ID, data, versão, cenário, passos para reproduzir, esperado, observado, severidade, navegador/dispositivo, captura e responsável pela triagem. Depois da correção, repetir o cenário e anotar resultado. Não classificar como “aprovado” antes de executar.

## Resultados

**Execução formal:** ainda não registrada neste documento.  
**Medições:** ainda não realizadas.  
**Defeitos:** registrar somente após inspeção real.  
**Aprovação de usuários:** não realizada.

Não afirmar que os cenários passaram sem a evidência correspondente. As metas de 3 segundos, 5 segundos e 99,5% descritas nos requisitos dependem de ambiente controlado e não podem ser demonstradas pela página local.
