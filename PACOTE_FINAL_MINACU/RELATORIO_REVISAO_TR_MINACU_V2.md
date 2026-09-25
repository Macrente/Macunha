# Relatório de Revisão do Termo de Referência — Plataforma de Inteligência Contábil e Gestão Fiscal — Minaçu/GO (V2)

> Este relatório é a versão V1 (`RELATORIO_REVISAO_TR_MINACU.md`) acrescida exclusivamente das seções 12 e 13, abaixo, que registram a microcorreção pontual aplicada ao TR já revisado e a auditoria de referências internas. Nenhum conteúdo das seções 1 a 11 (metodologia, estrutura, POC, quantitativos, matriz comparativa) foi alterado — o escopo, a POC e os quantitativos do TR V2 são idênticos aos da V1.

## 1. Arquivos entregues

1. `/home/user/Macunha/TR_Inteligencia_Contabil_Minacu_REVISADO_V2.docx`
2. `/home/user/Macunha/TR_Inteligencia_Contabil_Minacu_REVISADO_V2.pdf`
3. `/home/user/Macunha/RELATORIO_REVISAO_TR_MINACU_V2.md` (este relatório)

Nenhum arquivo pré-existente em `/home/user/Macunha` foi sobrescrito (a V1 do TR, o ETP V2 e os relatórios anteriores permanecem intocados).

## 2. Metodologia

O TR original (`1765dfd8-TR_Inteligencia_Contabil.docx`, elaborado originalmente para "Cidade Ocidental/GO") foi lido integralmente via `pandoc -t markdown`, comparado bloco a bloco com o ETP V2 (documento controlador) e reescrito por completo. Diante de uma incompatibilidade identificada entre `pandoc --reference-doc` e o estilo de tabela deste TR específico (as tabelas perdiam a estrutura de colunas na renderização), optei por reconstruir o `word/document.xml` programaticamente, reaproveitando os estilos de parágrafo e de tabela (`Ttulo1/2/3`, corpo de texto, `TabeladeGradeClara`) já existentes e comprovadamente funcionais no arquivo original — preservando 100% a identidade visual (fontes Arial, margens, tamanhos, cabeçalhos numerados, bordas de tabela) sem inventar marca d'água, brasão ou paginação especial (o original não possui nenhum desses elementos). O `.docx` final foi validado estruturalmente (`validate.py` — **todas as verificações passaram**) e revisado visualmente página a página (27 páginas, renderizadas via LibreOffice + `pdftoppm`).

## 3. Busca textual de confirmação (documento final)

| Termo buscado | Ocorrências |
|---|---|
| "inteligência artificial" | **0** |
| "token" | **0** |
| "IA" (sigla isolada) | **0** |
| "validador" / "validação e diagnóstico" | **0** |
| "franquia" | **0** |
| "Cidade Ocidental" (município do TR antigo) | **0** |
| "Minaçu" | 3 (objeto, fundamentação, cabeçalho de fundamentação) |

O módulo de **Validação e Diagnóstico Fiscal** (antigo item 5.3) foi **totalmente eliminado**, assim como o módulo de **Inteligência Artificial Setorial** (antigo item 5.5), a franquia de 30 milhões de tokens, o painel de consumo de IA, a POC-04 (validação) e a POC-07 (IA), e todas as menções a IA em fundamentação, descrição da solução, obrigações contratante/contratada, riscos, pagamento e sanções.

## 4. Estrutura funcional final do TR

- **1.** Definição do objeto (objeto, natureza/regime, unidade/quantidade, modalidade/critério de julgamento)
- **2.** Fundamentação e justificativa (sem IA/validador; alinhada ao diagnóstico do ETP V2 — governança, integração e inteligência da informação)
- **3.** Descrição da solução como um todo (componentes: plataforma web, aplicativo móvel, base de dados/integrações, camada analítica, gestão de conformidade, segurança/continuidade — DCA/RREO/RGF/MSC citados exclusivamente como fontes de dados)
- **4.** Requisitos gerais da contratação
- **5.** Requisitos da plataforma:
  - 5.1 Requisitos gerais (fornecimento, controle de acesso, parametrização, transparência de origem, recursos padrão dos painéis)
  - 5.2 Painéis analíticos executivos (receita, despesa, despesas críticas, caixa/patrimônio, relações institucionais, indicadores legais, apresentação)
  - 5.3 Entregas, obrigações e conformidade — com **5.3.2 CAUC** e **5.3.3 Processos do TCM-GO** como subseções (consolidando os núcleos 3 e 4 do escopo funcional do ETP)
  - 5.4 Aplicativo móvel (única solução SaaS com a web)
  - 5.5 Integrações, importação e rastreabilidade
  - 5.6 Segurança, privacidade e continuidade (requisito transversal, não módulo comercial)
- **6.** Níveis de serviço (disponibilidade 99,5%, suporte por severidade, atualizações regulatórias)
- **7.** Quantidade, prazo e quadro de itens (licença única, 20 usuários, 36 meses, implantação, reajuste)
- **8.** Prova de Conceito — POC (reestruturada, ver seção 5 abaixo)
- **9.** Gestão e fiscalização (glosas, pagamento sem franquia de IA)
- **10-12.** Obrigações da contratada/contratante; proteção de dados/LGPD (sem menção a treinamento de IA/prompts)
- **13.** Estimativa do valor e regras de precificação (sem componente de IA; pendência de pesquisa de preços expressamente registrada)
- **14.** Matriz de riscos (sem riscos exclusivos de IA/validação; adaptados: implantação, suporte, indisponibilidade de CAUC/TCM-GO, reversibilidade, segurança)
- **15-17.** Sanções; garantia/subcontratação/propriedade dos dados; adequação orçamentária

## 5. Prova de Conceito (POC) — cenários finais

| Código final | Conteúdo | Origem |
|---|---|---|
| POC-01 | Acesso e permissões | Mantido (antigo POC-01, sem menção a IA) |
| POC-02 | Painéis analíticos, resultados e controles | Mantido (antigo POC-02) |
| POC-03 | Importação e reimportação controlada | Mantido (antigo POC-03) |
| POC-04 | Entregas, obrigações **e CAUC** | **Novo/fundido**: substitui o antigo POC-04 (validação fiscal — removido) e incorpora a demonstração do CAUC que antes não tinha teste próprio |
| POC-05 | Processos do TCM-GO | Renumerado (era POC-06) |
| POC-06 | Aplicativo móvel | Renumerado (era POC-08), sem item de uso de IA |

**Removidos:** antigo POC-04 (Validação e diagnóstico fiscal) e antigo POC-07 (Inteligência artificial).

Foi incluído o item **8.1.6**, permitindo que testes dependentes de fonte externa (CAUC e TCM-GO) sejam demonstrados com dados controlados/simulados representativos quando o acesso em tempo real não estiver disponível, evitando prova impossível ou dependente de disponibilidade de terceiros. Os testes essenciais para julgamento passaram a ser POC-01 a POC-04 (4 testes, antes 5); complementares POC-05 e POC-06 (antes 3).

## 6. Quantitativos finais e verificação de coerência com o ETP V2

| Item | TR revisado | ETP V2 | Situação |
|---|---|---|---|
| Licença corporativa | 1 (uma) | 1 (uma) | Compatível |
| Usuários simultâneos | 20 (vinte) | 20 (vinte) | Compatível |
| Aplicativo móvel integrado | 1 (um) | 1 (um) | Compatível |
| Vigência inicial | 36 meses (3 anos) | 3 anos | Compatível |

Não foi identificada divergência quantitativa entre o TR e o ETP V2. O preço unitário do usuário simultâneo adicional permanece como `[INFORMAÇÃO A PREENCHER]`, a ser definido pela pesquisa de preços (não inventado).

## 7. Campos marcados como [INFORMAÇÃO A PREENCHER]

- Item 7.1.2 — preço unitário do usuário simultâneo adicional
- Item 13.1 — processo de pesquisa de preços
- Item 17 — dotação orçamentária, fonte de recursos e programa/ação

Nenhum valor, secretaria requisitante, processo administrativo, servidor responsável ou dado não comprovado foi inventado.

## 8. Matriz comparativa ETP V2 × TR revisado

| Aspecto | ETP V2 | TR revisado | Situação |
|---|---|---|---|
| Objeto | Plataforma SaaS de inteligência contábil e gestão fiscal, web + app, painéis, entregas/obrigações, CAUC, TCM-GO, integração/rastreabilidade | Idem, redigido no mesmo escopo | COMPATÍVEL |
| Módulos | 5 núcleos funcionais + app + segurança transversal | Idem (5.2 a 5.6) | COMPATÍVEL |
| Usuários | 20 simultâneos | 20 simultâneos | COMPATÍVEL |
| Vigência | 3 anos | 36 meses | COMPATÍVEL |
| Aplicativo | Integrado, mesma base/perfis | Integrado, mesma base/perfis | COMPATÍVEL |
| SaaS/nuvem | Sim | Sim | COMPATÍVEL |
| Painéis | Receita, despesa, despesas críticas, caixa/patrimônio, relações institucionais, indicadores legais, apresentação | Idênticos grupos | COMPATÍVEL |
| Obrigações | Agenda, prazos, responsáveis, status, alertas, evidências | Idêntico (5.3.1) | COMPATÍVEL |
| CAUC | Situação de adimplência, pendências, grupos, histórico, data de consulta, sem tempo real falso | Idêntico (5.3.2) | COMPATÍVEL |
| TCM-GO | Número, órgão, exercício, fase, prazos, diligências, decisões, alertas | Idêntico (5.3.3) | COMPATÍVEL |
| Integrações | Balancetes, arquivos, API quando oficial/estável | Idêntico (5.5) | COMPATÍVEL |
| Rastreabilidade | Vínculo dado-lote-origem | Idêntico (5.5.3) | COMPATÍVEL |
| Segurança | Requisito transversal, não módulo comercial | Idêntico (5.6) | COMPATÍVEL |
| SLA | 99,5% de disponibilidade | 99,5% (item 6.1 e 5.6.6) | COMPATÍVEL |
| Suporte | Severidades, prazos | Mantido (item 6.2) | COMPATÍVEL |
| Implantação | Fases (mobilização a operação assistida) | Prazo de 10 dias corridos + fases (item 7.3) — nível de detalhe do TR é maior que o ETP, mas não conflitante | COMPATÍVEL |
| Reversibilidade | Exportação estruturada, apoio de saída | Mantida (5.6.7, item 16) | COMPATÍVEL |
| Lote único | Justificado por integração/interoperabilidade, sem menção a IA/validador | Idêntico (item 1.3 e implícito na descrição da solução) | COMPATÍVEL |
| POC | Não detalhada no ETP (delegada ao TR) | Detalhada, sem IA/validação, com fallback para dados simulados em CAUC/TCM-GO | COMPATÍVEL |
| Valor estimado | Ausente — pendência expressa | Ausente — pendência expressa (item 13.1) | COMPATÍVEL (mesma pendência administrativa) |

**Resultado: zero divergências materiais** entre o ETP V2 e o TR revisado. A única pendência comum aos dois documentos é a **pesquisa de preços**, que ambos registram explicitamente como condição para prosseguimento da fase externa da licitação — não é uma divergência entre os documentos, mas uma pendência administrativa compartilhada e assumida por ambos.

## 9. Revisão visual do PDF (27 páginas)

Todas as 27 páginas foram renderizadas (LibreOffice → PDF → `pdftoppm`) e inspecionadas individualmente. Verificado:

- Nenhum título órfão ao final de página.
- Todas as 7 tabelas (componentes da solução; grupos de painéis; severidade de suporte; quantitativo; quadro geral da POC; componentes de preço; matriz de riscos) renderizam com colunas corretamente alinhadas e bordas visíveis, sem colapso de layout.
- Tabelas longas (severidade, matriz de riscos) quebram de forma limpa entre páginas, sem cortar células ao meio de forma ilegível.
- Numeração hierárquica (1., 1.1, 1.1.1...) consistente do início ao fim, sem saltos após a remoção dos módulos de validação e IA.
- Nenhuma referência residual a "TR antigo", "escopo anterior", "módulo removido" ou expressão equivalente no corpo do texto — o histórico de edição consta apenas neste relatório.

Único ponto cosmético menor (não estrutural): em tabelas com 4-5 colunas (severidade, quadro POC, matriz de riscos), os cabeçalhos mais curtos ("Impacto", "Probabilidade") quebram em duas linhas por serem colunas estreitas; o conteúdo permanece integralmente legível.

## 10. Pendências que dependem da pesquisa de preços

- Valor estimado da contratação (mensal, anual, global) — não apresentado, conforme item 13.1.
- Preço unitário do usuário simultâneo adicional — `[INFORMAÇÃO A PREENCHER]`.
- O TR **não** foi declarado pronto para a fase externa; o documento registra expressamente que a estimativa de valor é pendência a ser suprida antes da publicação do edital, no mesmo sentido do ETP V2.

## 11. Confirmações finais (herdadas da V1)

- Linguagem de histórico de edição ("TR antigo", "versão anterior", "conforme revisão" etc.) **não aparece** no corpo do TR — confirmado por leitura integral e por busca textual.
- O ETP V2 (`ETP_Inteligencia_Contabil_Minacu_REVISADO_V2.docx`) **não foi alterado**.
- Nenhum arquivo pré-existente em `/home/user/Macunha` foi sobrescrito.
- Nenhum valor, secretaria, processo administrativo, fornecedor, contrato existente ou nome de servidor foi inventado.

---

## 12. Microcorreção aplicada nesta V2

**Item corrigido:** 5.1.1.3.

- **Antes:** "A interface deverá ser responsiva e adaptar-se a desktop, notebook e tablet, sem prejuízo do aplicativo móvel previsto na seção **5.6**."
- **Depois:** "A interface deverá ser responsiva e adaptar-se a desktop, notebook e tablet, sem prejuízo do aplicativo móvel previsto na seção **5.4**."

**Motivo:** após a renumeração aplicada na revisão anterior, a seção 5.4 passou a ser "Aplicativo móvel" e a seção 5.6 passou a ser "Segurança, privacidade e continuidade". A referência cruzada do item 5.1.1.3 ficou desatualizada, apontando para o conteúdo errado (segurança, em vez de aplicativo móvel). Esta foi a **única** alteração de conteúdo aplicada nesta versão — nenhum outro texto, quantitativo, escopo, POC ou estrutura foi modificado.

**Validação técnica:** o `.docx` corrigido foi validado estruturalmente com `scripts/office/validate.py --original` (536 parágrafos antes e depois, nenhuma divergência estrutural, todas as verificações aprovadas), reconvertido para PDF via LibreOffice e renderizado com `pdftoppm`. A página 5 do PDF (onde consta o item 5.1.1.3) foi inspecionada visualmente: o texto corrigido aparece de forma limpa, sem quebra de linha ruim, sem órfãos e sem impacto em parágrafos vizinhos (5.1.1.2 e 5.1.1.4 permanecem inalterados).

## 13. Auditoria de referências internas ("seção" / "item" / "subitem" / "itens" / "subitens")

Foi feita varredura completa do texto extraído do documento (`pandoc -t plain`) e confirmação cruzada diretamente no `word/document.xml`, em busca de toda ocorrência de "seção", "item", "itens", "subitem" ou "subitens" seguida de referência numérica. Foram localizadas **8 ocorrências**, listadas abaixo com o resultado da checagem contra a numeração atual do documento:

| # | Localização (item que contém a referência) | Referência encontrada | Aponta para | Situação |
|---|---|---|---|---|
| 1 | 1.2 (Natureza do objeto) | "subitens 7.2 e 7.4" | 7.2 = Vigência; 7.4 = Reajuste, revisão e alterações contratuais | **Correta** |
| 2 | 5.1.1.3 | "seção 5.6" | Antes da correção, apontava para "Segurança, privacidade e continuidade" (errado); deveria apontar para "Aplicativo móvel" | **Corrigida** (→ seção 5.4; ver seção 12 deste relatório) |
| 3 | 5.2.1.3 | "subitem 5.2.1.1" | 5.2.1.1 = "O módulo deverá contemplar, no mínimo, os grupos de painéis..." (mesmo item pai, 5.2.1) | **Correta** |
| 4 | 8.1.4 | "seção 5" | Seção 5 = "Requisitos da plataforma" (bloco completo de requisitos funcionais/técnicos referenciado pela matriz de conformidade da POC) | **Correta** |
| 5 | 8.1.4 (nota de rodapé/critério) | "item 8.1.6" | 8.1.6 = "Testes que dependam de fonte externa que possa estar indisponível..." | **Correta** |
| 6 | 8.5.4 | "item 8.1.6" | Mesmo item 8.1.6 acima (fallback para fonte externa indisponível) | **Correta** |
| 7 | 8.5.5 | "item 8.5.4" | 8.5.4 = "Falha pontual de ambiente, conectividade, projeção..." (parágrafo imediatamente anterior) | **Correta** |
| 8 | 10 (Obrigações da contratada) | "subitem 7.3" | 7.3 = "Implantação" (prazo de implantação, configuração, importação inicial e capacitação) | **Correta** |

**Resultado consolidado:** 8 referências internas encontradas; **7 já estavam corretas** e não foram alteradas; **1 estava incorreta** (item 5.1.1.3 → "seção 5.6") e foi corrigida para "seção 5.4", conforme instrução obrigatória desta revisão. Nenhuma outra referência cruzada foi tocada.
