# EngMan Copilot

## 1. Nome do projeto e integrantes

**Assistente:** EngMan Copilot

**Integrantes:**
- Larissa Fernandes - RM574592 - 1CCPS
- Guilherme Cavalcante da Costa - RM575153 - 1CCPS
- Pedro Henrique Hernandes - RM575010 - 1CCPS
- Nicolas Assunção - RM575154 - 1CCPS

## 2. Problema abordado

A Motiva opera mais de 5 mil km de rodovias e depende das câmeras de CFTV para monitorar a via e despachar socorro com agilidade. Essas câmeras ficam expostas a barro, fuligem, teia de aranha e vibração do poste, e por isso estão sempre sujas. Como não existe nenhuma tecnologia automática que avise quais precisam ser limpas, hoje quem percebe a falha é o operador do CCO, olhando a imagem. Com o plano de manutenção por calendário, é necessário limpar todas, até mesmo as que estão em bom estado, o que gera desperdício de tempo e de manutenção.

Além disso, a manutenção é reativa (só age depois que quebrou), visto que poucas pessoas acessam o histórico de falhas do FSM para antecipar problemas. O EngMan Copilot busca reduzir essa lacuna: o assistente consulta o histórico de falhas de uma câmera PTZ, indica a causa provável (como hipótese a validar em campo) e recomenda o tipo de manutenção.

**Evidências do briefing:**
- A Motiva opera mais de 5 mil km de rodovias.
- As câmeras de CFTV ficam expostas a barro, fuligem, teia de aranha e vibração do poste.
- Hoje quem percebe a falha é o operador do CCO, olhando a imagem. A detecção é reativa.
- O plano de manutenção é majoritariamente estático, por calendário.
- O histórico de falhas do FSM existe, mas é pouco explorado.

## 3. Recorte e persona

- **Recorte escolhido:** A, Diagnóstico e Confiabilidade
- **Persona principal:** engenheiro de manutenção
- **Ativo coberto:** CFTV (câmeras PTZ)

**Justificativa:**

O recorte A foi escolhido porque se baseia no histórico de falhas de cada equipamento, o que permite identificar a causa provável de um problema. Com isso, é possível economizar tempo de manutenção: em vez de limpar todas as câmeras por calendário, limpam-se apenas as que realmente precisam. Além disso, observando os padrões e as probabilidades de falha, é possível antecipar problemas e agir antes que aconteçam, e não só depois que quebrou. Por fim, o recorte A tem menor risco de consequência imediata na via, já que toda resposta do assistente é uma hipótese a validar em campo antes de qualquer ação.

A persona escolhida foi o engenheiro de manutenção, pois é ele quem fica no escritório, com computador, analisando por que os equipamentos falham e decidindo onde investir. Essa análise combina com o recorte A, já que ele usa o histórico de falhas para escolher entre manutenção corretiva, preventiva, inspeção ou CBM (manutenção baseada em condição). Por isso, o assistente fala de forma técnica, com histórico e números. O risco principal dessa persona é tomar uma decisão de investimento sem base estatística, e o assistente reduz esse risco mostrando o histórico, as premissas e o nível de confiança em cada resposta.

## 4. Escopo do assistente

**O que o assistente faz:**
- Explica conceitos de manutenção e confiabilidade das câmeras PTZ.
- Consulta e resume o histórico de falhas de uma câmera pelo TAG (o código que identifica cada equipamento).
- Indica a causa provável de uma falha, deixando claro que é hipótese a validar em campo.
- Recomenda o tipo de manutenção (corretiva, preventiva, inspeção ou CBM) e a prioridade.
- Escreve o texto de uma ordem de serviço e o resumo de um atendimento.
- Quando não encontra o dado, avisa e encaminha para o responsável.

**O que o assistente recusa:**
- Emitir laudo técnico ou parecer de engenharia com validade legal.
- Liberar, bloquear ou mexer fisicamente em equipamento.
- Dar orientação de segurança elétrica no lugar do procedimento oficial (NR-10 / NR-35).
- Responder sobre assuntos que não são de manutenção (receitas, política, esportes).
- Inventar TAG, modelo, norma, métrica ou histórico que não esteja na base de conhecimento.
- Tratar dados pessoais de terceiros (placas, imagens de pessoas, dados de empregados).
- Responder sobre outros equipamentos além das câmeras (painéis, totens, sensores).


## 5. Estrutura de Arquivos da Sprint 01

- [`/prompts/system_prompts.md`](./prompts/system_prompts.md): **System Prompt (Artefato 1)** completo e estruturado com as diretrizes de persona, escopo, regras anti-alucinação, instruções Chain-of-Thought (CoT), formato de saída com Nível de Confiança, exemplos Few-Shot e comentários pedagógicos.
- `/evals/sprint1_eval_set.json`: Conjunto de casos de teste para validação de comportamento e respostas do assistente.
- `/tools/tools_spec.json`: Especificação de schemas e integração com a base do FSM.
- `/data/knowledge_base/`: Base de conhecimento e inventário de ativos.
