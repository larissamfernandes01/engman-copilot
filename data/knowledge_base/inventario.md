# INVENTÁRIO DA BASE DE CONHECIMENTO (RAG) — ENGMAN COPILOT

**Projeto:** EngMan Copilot — Diagnóstico e Confiabilidade (Recorte A)  
**Domínio:** Concessionária Motiva Rodovias — Engenharia de Manutenção  
**Versão:** 1.0 (Sprint 01)  

---

### 1. Documentos da Base de Conhecimento

| ID Documento | Título do Documento | Categoria | Ativo Relacionado | Resumo do Conteúdo |
|---|---|---|---|---|
| **POP-CFTV-001** | Procedimento de Manutenção Preventiva em Câmeras PTZ | Procedimento | CFTV | Passo a passo para limpeza de lentes, verificação do dome e reaperto estrutural. |
| **POP-PMV-002** | Diagnóstico de Falhas em Painéis de Mensagem Variável | Procedimento | PMV | Guia de teste de matriz de LEDs, placas controladoras e fontes chaveadas. |
| **POP-CBX-001** | Manutenção Corretiva e Calibração de Callbox | Procedimento | Callbox | Instruções para reparo de rádio bidirecional, bateria solar e botão de pânico. |
| **POP-SAT-002** | Calibração de Sensores do Sistema Analisador de Tráfego | Procedimento | SAT | Procedimento de ajuste óptico e calibração de laços indutivos na pista. |
| **PMP-ITS-2026** | Plano de Manutenção Preventiva Geral de ITS | Plano | Todos os Ativos | Tabela de periodicidades (mensal, trimestral, anual) e checklists de campo. |
| **MAN-PTZ-V4** | Manual do Fabricante — Câmera PTZ HD Outdoor | Manual | CFTV | Especificações elétricas, limites de temperatura e consumo do illuminador IR. |
| **NR-10-MOTIVA** | Diretrizes de Segurança Elétrica em Instalações de Campo | Segurança | Todos os Ativos | Protocolos de desenergização, bloqueio/etiquetagem (LOTO) e uso de EPIs. |
| **NR-35-MOTIVA** | Diretrizes de Trabalho em Altura para Postes e Pórticos | Segurança | CFTV / PMV / SAT | Regras obrigatorias para ancoragem, cinto duplo e uso de plataforma elevatória. |
| **HIS-FSM-2025** | Histórico de Ocorrências e Falhas Registradas no FSM | Histórico | Todos os Ativos | Base histórica de falhas reincidentes, tempos médios de reparo (MTTR) e MTBF. |

---

### 2. Regras de Acesso e Atualização
* **Formato dos Arquivos:** Ficheiros indexados em formato Markdown (`.md`) e JSON para ingestão na Vector Store do assistente.
* **Periodicidade de Atualização:** Mensal ou sempre que houver revisão de norma técnica pela Engenharia de Manutenção.
