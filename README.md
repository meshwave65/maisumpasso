info.sevenrock.com.br · Referência: 2026-09-28 14:08 (America/Sao_Paulo, UTC−03:00)

# Mais um Passo — ponto de entrada operacional

Ecossistema de reflexão, fé e transformação baseado em experiências de diálogo mediadas por inteligência artificial. Este README é o **índice de tarefas e o ponto de entrada dos agentes**: leia-o por inteiro antes de editar qualquer arquivo.

> **Atenção:** abrir o repositório ou ler este arquivo não inicia um agente sozinho. Quando um agente for acionado para trabalhar neste projeto, estas instruções dizem como ele deve identificar e assumir a próxima tarefa autorizada.

## Como assumir uma tarefa

1. Ler este README integralmente e respeitar a solicitação mais recente do usuário.
2. Consultar a tabela **Registro de tarefas** abaixo. Se a solicitação for apenas “continue”, assumir a primeira tarefa **READY** e sem responsável ativo. Não tomar tarefas **BLOCKED**, **HANDED OFF** ou **DONE**.
3. Abrir o TODO indicado na tabela e ler o escopo, os limites, as fases, as pendências e a próxima ação. O README é o índice; o TODO é o roteiro detalhado do lote.
4. Conferir `git status --short --branch`, branch e remoto antes de editar. Não descartar, sobrescrever ou incluir trabalho de outro agente.
5. Marcar a tarefa como **IN_PROGRESS** no TODO e neste registro antes de iniciar alterações. Ao terminar, validar o conteúdo, atualizar ambos e registrar os commits.
6. Se não houver tarefa READY, ou se a próxima ação exigir permissão, arquivo-fonte ou decisão que esteja faltando, explicar o bloqueio e pedir apenas o que é necessário. Não inventar trabalho nem contornar permissões.

### Hierarquia de referência

1. Regras de sistema, segurança e autorização, além da solicitação atual do usuário.
2. Este `README.md`: prioridades, responsável, estado e local do próximo passo.
3. O TODO ativo: limites e checklist específicos da tarefa.
4. `skills/conversas-para-fichas/SKILL.md`: método de leitura, segmentação, anonimização, edição e publicação.
5. Fichas existentes: referência de formato e estilo, não licença para copiar conteúdo nem para alterar fichas atribuídas a outra pessoa.

## Registro de tarefas

**Atualizar esta tabela sempre que o estado, responsável, bloqueio ou próxima ação mudar.** Um agente que chega sem contexto deve conseguir escolher a próxima tarefa usando somente esta tabela e, depois, abrir o TODO correspondente.

| Prioridade | Estado | Tarefa | TODO / responsável | Próxima ação autorizada |
|---|---|---|---|---|
| P0 | **BLOCKED — escrita GitHub** | Novo lote temático da conversa compartilhada “Perspectiva Espiritual de Xangô” | `TODO-novas-fichas-chatgpt.md`; novo lote, IDs planejados 017–018 | Restabelecer permissão de escrita restrita ao repositório. O TODO está num commit local (`edaf73b`), ainda não confirmado em `origin/main`. Depois de restaurar acesso, sincronizar o remoto, verificar o commit e criar as fichas/notas uma por vez. |
| P1 | **HANDED OFF — não editar** | Continuidade das fichas 001–016 | Responsabilidade de outro agente | Não modificar, renumerar, mover nem reformatar. Retomar somente quando o usuário atribuir explicitamente essa tarefa. |
| P2 | **BLOCKED — publicação pendente** | Este ponto de entrada e suas diretrizes de agente | Este README, `AGENTS.md` e `skills/conversas-para-fichas/` | As mudanças foram preparadas no clone local; validar o remoto e publicar cada arquivo em commit separado somente quando a escrita estiver autorizada. |

### Significado dos estados

- **READY:** pode ser assumida por um agente autorizado; não há bloqueio conhecido.
- **IN_PROGRESS:** alguém já está trabalhando; não duplicar. Coordenar antes de assumir.
- **BLOCKED:** falta acesso, decisão ou fonte. Não tentar contornar.
- **HANDED OFF:** reservado/transferido a outro agente; não tocar sem nova atribuição.
- **DONE:** concluído e, quando publicação foi solicitada, verificado no remoto.

## Procedimento operacional deste projeto

### Fichas e transcrições

- Trabalhar em lotes temáticos independentes. Não fundir espiritualidade, vida pessoal, educação/família, tecnologia, edição literária, imagens ou marketing apenas por estarem na mesma conversa.
- Aguardar a renderização total da fonte compartilhada; expandir blocos recolhidos e confirmar a extração integral antes de dividir o material.
- Guardar pergunta e resposta completas, em ordem. Corrigir apenas o que o usuário autorizou; não resumir, amputar nem inventar respostas ausentes.
- Manter instruções de estilo e observações editoriais em arquivo próprio, não como relato pessoal.
- Aplicar linguagem espiritual somente às respostas de interações explicitamente espirituais. Marcar como não aplicável nos temas não espirituais.
- Anonimizar terceiros segundo os papéis aprovados pelo usuário. Não publicar tabela de correspondência, anexos privados, caminhos locais, tokens ou outros identificadores.
- Tratar anexos que não estejam integralmente disponíveis como pendência; usar marcador neutro em vez de inferir seu conteúdo.

### TODOs, conflitos e propriedade

- Criar um TODO distinto por lote; não substituir o TODO ativo de outro agente.
- Registrar em cada TODO: fonte, tema, IDs, etapas de Fragmentação/Edição IA/Espiritualização, perguntas sem resposta, anexos pendentes, próxima ação e commits.
- Para novo lote, conferir o maior ID existente e evitar duplicação. Não alterar os arquivos 001–016 enquanto estiverem HANDED OFF.
- Se dois agentes puderem trabalhar no mesmo repositório, respeitar o estado do TODO e o `git status`; não assumir que arquivos locais são compartilhados.

### Commits e prova de persistência

- Fazer **um commit por novo documento ou ficha**, imediatamente após validá-lo; não agrupar fichas diferentes em um commit.
- Antes de cada alteração, sincronizar por fast-forward e confirmar que o arquivo preparado é o único incluído no commit.
- Após `git push`, verificar que o hash está em `origin/main` e anotá-lo no TODO. Só então marcar o documento como publicado.
- Um arquivo no clone, na sandbox ou em um commit local **não está salvo no GitHub**. Nunca dizer “publicado” sem confirmar o remoto.
- Em `401/403`, parar o push, preservar o commit local e registrar **BLOCKED**. Solicitar a permissão mínima, limitada a `meshwave65/maisumpasso` e `Contents: Read and write`; não usar outra conta, token ou escopo mais amplo como atalho.

## Estrutura do repositório

- `prompts/`: modelos de diálogo.
- `interacoes/fichas/`: fichas de interação revisadas e anonimizadas.
- `docs/`: diretrizes editoriais e privacidade.
- `ebook/apendices/`: materiais destinados aos apêndices do e-book.
- `skills/conversas-para-fichas/`: procedimento reutilizável e modelos de ficha/TODO/notas editoriais.
- `TODO-*.md`: roteiro detalhado de cada lote; a tarefa ativa deve estar listada acima.

As fichas são experiências de reflexão e não substituem acompanhamento profissional, liderança religiosa, comunidade de fé ou a consciência do leitor.
