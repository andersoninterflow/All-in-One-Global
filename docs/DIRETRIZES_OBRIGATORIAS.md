# Diretrizes Obrigatórias — All-in-One + Valley

**Status:** Regra mandatória do projeto  
**Vigência:** 22 de julho de 2026  
**Aplicação:** Todas as IAs, pessoas desenvolvedoras, revisores, pipelines e agentes de automação que atuem no ecossistema.

## 1. Regra de controle de pendências

1. Toda atividade sem evidência objetiva de conclusão permanece marcada como pendente.
2. Declarações, previsões, planos, builds locais ou resultados parciais não equivalem a conclusão.
3. Uma pendência só pode ser encerrada mediante evidência verificável, como:
   - código integrado no repositório correto;
   - testes aprovados;
   - workflow de CI/CD concluído com sucesso;
   - ambiente publicado e acessível;
   - validação funcional registrada;
   - documento ou artefato final anexado;
   - aceite expresso do responsável.
4. Itens não confirmados devem ser transferidos para a próxima atividade para verificação e, quando necessário, correção posterior.
5. É proibido remover, ocultar ou marcar como concluída uma pendência sem registrar a evidência correspondente.

## 2. Fonte de verdade

- O arquivo `docs/PENDENCIAS_PROJETO.md` é a lista operacional oficial de pendências.
- Documentos de roadmap, planos de execução, issues e pull requests devem apontar para essa lista ou manter rastreabilidade equivalente.
- Em caso de divergência, prevalece o estado sustentado por evidências técnicas mais recentes.

## 3. Front-end e experiência do usuário

- Tolerância zero para botões mortos, rotas sem ação, formulários incompletos ou dados mockados apresentados como integração real.
- Toda interface deve utilizar português do Brasil, preservando termos estrangeiros apenas quando forem consolidados no uso brasileiro.
- Os módulos devem estar conectados ao API Hub e exibir estados reais de carregamento, sucesso, vazio, indisponibilidade e erro.
- A arquitetura visual deve respeitar os templates Stitch e as diretrizes oficiais das marcas All-in-One e Valley.
- Logomarcas oficiais não podem ter linhas, cores, formas, proporções ou estrutura alteradas sem autorização expressa. Quando determinado, apenas o fundo externo pode ser removido, mantendo transparência real.

## 4. Segurança, dados e integrações

- Segredos não podem ser gravados no repositório. Devem ser injetados por gerenciador de segredos ou variáveis protegidas.
- Integrações com GCP, Kubernetes, RabbitMQ, Telegram, Apigee, bancos de dados e serviços externos devem possuir observabilidade, tratamento de falhas e documentação operacional.
- Fluxos financeiros, identidade, KYC, biometria, saúde e dados pessoais devem atender aos requisitos de segurança, auditoria e LGPD aplicáveis.

## 5. Critério de conclusão

Um item somente pode receber `[x]` quando contiver, no próprio item ou em referência vinculada:

- data da validação;
- responsável ou agente executor;
- evidência verificável;
- ambiente ou versão afetada;
- resultado dos testes relevantes.

Sem esses elementos, o item permanece `[ ]` ou recebe o estado `EM VERIFICAÇÃO`.

## 6. Regra para agentes de IA

Antes de iniciar qualquer nova atividade, o agente deve:

1. consultar `docs/PENDENCIAS_PROJETO.md`;
2. verificar quais itens possuem evidência de conclusão;
3. executar primeiro os bloqueadores de maior prioridade;
4. atualizar o documento ao final;
5. manter pendente tudo que não tenha sido confirmado;
6. registrar riscos, dependências e próximos passos sem presumir sucesso.
