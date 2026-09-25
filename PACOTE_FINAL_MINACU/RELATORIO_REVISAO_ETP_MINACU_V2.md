# Relatório de Revisão do ETP — Plataforma de Inteligência Contábil e Gestão Fiscal (Minaçu/GO) — V2 (Microcorreções)

Este relatório complementa `RELATORIO_REVISAO_ETP_MINACU.md` (V1). Ele documenta uma rodada de **microcorreções pontuais** aplicadas sobre o ETP já finalizado (`ETP_Inteligencia_Contabil_Minacu_REVISADO.docx`), sem alteração de estrutura, layout ou escopo. Nada do conteúdo do relatório V1 foi invalidado; o V2 apenas corrige e revalida pontos específicos, incluindo uma menção residual a "inteligência artificial" que havia passado despercebida na V1.

## Microcorreções aplicadas na V2

1. **Item 5 (Estimativa das quantidades)** — a frase que narrava o processo de edição ("Os quantitativos abaixo preservam os já definidos no ETP original desta contratação, excluídos os itens relativos a módulos de inteligência artificial, os quais não subsistem no escopo revisado.") foi substituída por:
   > "Os quantitativos foram dimensionados considerando a necessidade de disponibilização de uma plataforma municipal integrada, o número estimado de usuários simultâneos e os componentes necessários ao atendimento do objeto."
   A tabela de quantitativos e todos os números (1 licença corporativa, 20 usuários simultâneos, 3 anos de vigência, 1 aplicativo móvel) foram **preservados sem alteração**.

2. **CAUC (item 3.4 e demais ocorrências)** — a expansão da sigla foi trocada de "CAUC — Cadastro Único de Convênios" para **"CAUC — Sistema de Informações sobre Requisitos Fiscais"**. A sigla em si e as funcionalidades descritas para o módulo/painel de CAUC não foram alteradas.

3. **Item 9 (Contratações correlatas e interdependentes)** — o texto que afirmava a existência de um contrato municipal específico já em uso foi substituído por redação tecnicamente neutra (ver seção "Redação final do item 9" abaixo), sem inventar número de contrato, fornecedor ou data.

4. **Estimativa do valor — pendência impeditiva** — foi inserida, na seção 6 do ETP (Estimativa preliminar do valor da contratação), a frase explícita:
   > "O ETP permanece em condição de minuta até a incorporação da estimativa do valor da contratação, acompanhada da memória de cálculo e dos documentos de suporte."
   Isso reforça — sem alterar o texto já existente sobre a pendência de pesquisa de preços — que o documento não deve ser tratado como definitivamente apto à aprovação enquanto o valor não for incorporado.

5. **Limpeza de linguagem de revisão** — buscadas e reescritas todas as ocorrências de expressões que narravam o histórico de edição do documento:
   - "escopo revisado" (item 6, na frase sobre pesquisa de preços) → "objeto ora definido";
   - "escopo revisado" (item 13, posicionamento conclusivo) → removido, mantendo apenas "escopo consolidado em painéis analíticos executivos...";
   - "escopo ora revisado" (item 13, recomendação final) → "objeto ora definido";
   - "ETP original", "revisado à luz", "módulos excluídos", "não subsistem no escopo" → eliminados junto com a correção do item 5 (eram todos parte da mesma frase).
   A fundamentação legítima de economicidade, proporcionalidade dos requisitos e definição das funcionalidades necessárias (itens 5, 8 e 13) foi **mantida integralmente** — apenas a linguagem de "antes/depois" foi removida.

6. **Confirmação de ausência de IA/token/Cidade Ocidental** — nova varredura completa do texto pós-correção (ver seção dedicada abaixo), que identificou e eliminou a menção residual a "inteligência artificial" existente no item 5 (item 1 desta lista).

## Busca por "IA" / "inteligência artificial" / "token" / "Cidade Ocidental"

**Antes da correção (texto herdado da V1):** a varredura da V1 havia concluído "nenhuma ocorrência restante" de IA/token/Cidade Ocidental, mas essa conclusão estava **incompleta** — a frase do item 5 ainda continha "módulos de inteligência artificial", que não havia sido capturada na varredura anterior.

**Depois da correção (V2), busca em `word/document.xml` do docx final:**

| Termo | Resultado |
|---|---|
| "inteligência artificial" | 0 ocorrências |
| "IA" (como sigla isolada, delimitada por fronteira de palavra, case-insensitive) | 0 ocorrências |
| "token" | 0 ocorrências |
| "Cidade Ocidental" | 0 ocorrências |

Confirmado por `grep` sobre o XML já processado (`merge_runs.py` aplicado, 0 runs fragmentados a mesclar — o texto já estava contíguo). Todas as buscas retornaram vazio (exit code 1 do grep = nenhum match).

## Busca por "ETP original", "escopo revisado" e demais expressões de revisão (item 5 da tarefa)

**Antes da correção:**

| Expressão | Ocorrências encontradas |
|---|---|
| "ETP original" | 1 (item 5) |
| "escopo revisado" | 3 (item 5 — "não subsistem no escopo revisado"; item 6 — "pesquisa de preços concluída para o escopo revisado"; item 13 — "com o escopo revisado consolidado...") |
| "escopo ora revisado" | 1 (item 13, recomendação final) |
| "revisado à luz" | 0 |
| "módulos excluídos" | 0 (não constava como string literal, mas a ideia estava embutida na frase do item 5, já corrigida) |
| "não subsistem" | 1 (item 5, mesma frase) |
| "redução de escopo" | 0 (não constava como string literal no texto final da V1; a V1 usava linguagem de "justificativa da redução de escopo" apenas no seu próprio relatório, não no ETP) |

**Depois da correção (V2):** todas as expressões acima retornam **0 ocorrências** no `document.xml` final. A fundamentação de economicidade e proporcionalidade dos requisitos permanece no texto (itens 5, 8 e 13), apenas sem a linguagem narrativa de "antes/depois".

## Redação final do item 9 — Contratações correlatas e interdependentes

> "A solução pressupõe interação com o SIAFIC e demais sistemas de gestão pública utilizados pelo Município, bem como a disponibilidade de acesso à internet, dependendo, para sua plena implantação, da disponibilização pela Administração dos dados, arquivos e interfaces necessários à integração. A solução não substituirá o SIAFIC, cuja operação e competências permanecem preservadas. Eventual contrato correlato já existente no âmbito municipal deverá ser identificado e formalmente registrado nos autos do processo administrativo, se aplicável."

Nenhum número de contrato, fornecedor ou data foi inventado.

## Nomenclatura final do CAUC

**"CAUC — Sistema de Informações sobre Requisitos Fiscais"** (item 3.4 e nas demais menções ao painel/módulo de CAUC no corpo do ETP). A sigla "CAUC" e as funcionalidades descritas para esse painel (situação de adimplência, pendências, grupos de conformidade, histórico de consultas, data da última consulta, indicação de indisponibilidade/defasagem da fonte) permanecem inalteradas.

## Pendência impeditiva — estimativa do valor da contratação

Confirma-se explicitamente que a ausência de estimativa de valor **continua tratada como pendência impeditiva** da aprovação final do ETP. A frase inserida no corpo do documento (item 6, Estimativa preliminar do valor da contratação) é:

> "O ETP permanece em condição de minuta até a incorporação da estimativa do valor da contratação, acompanhada da memória de cálculo e dos documentos de suporte."

Essa frase foi acrescentada ao parágrafo já existente que registrava a ausência de pesquisa de preços concluída como pendência a ser suprida pela Administração antes do prosseguimento da fase externa da licitação. Nenhuma pesquisa de preços foi realizada e nenhum valor foi inventado nesta rodada de microcorreções, conforme instruído.

## Validação técnica e revisão visual

- `scripts/merge_runs.py` executado sobre o docx desempacotado: 0 runs a mesclar (texto já contíguo nos trechos editados).
- Edições aplicadas diretamente em `word/document.xml`, sem reformatação da estrutura XML.
- `scripts/office/validate.py ETP_V2_OUT.docx --original ETP_V2.docx`: **"All validations PASSED!"** (227 parágrafos antes e depois — nenhuma alteração estrutural).
- Conversão para PDF via `soffice.py --headless --convert-to pdf` e renderização com `pdftoppm -jpeg -r 100`: documento manteve **12 páginas**.
- Revisão visual das páginas afetadas pelas mudanças:
  - **Página 5** (item 3.4, CAUC): título "3.4. CAUC -- Sistema de Informações sobre Requisitos Fiscais" renderizado corretamente, sem corte de texto ou quebra ruim.
  - **Página 7** (item 5, quantitativos): novo parágrafo introdutório renderizado por completo, tabela de quantitativos íntegra e sem alteração de números.
  - **Página 9** (itens 8 e 9): item 9 com a nova redação completa, sem corte de texto nem quebra de página no meio do parágrafo.

## Entregas desta rodada (V1 preservados, não sobrescritos)

Salvos em `/home/user/Macunha`:

1. `ETP_Inteligencia_Contabil_Minacu_REVISADO_V2.docx`
2. `ETP_Inteligencia_Contabil_Minacu_REVISADO_V2.pdf` (12 páginas, revisado visualmente nas páginas afetadas)
3. `RELATORIO_REVISAO_ETP_MINACU_V2.md` (este relatório)

Os arquivos V1 (`ETP_Inteligencia_Contabil_Minacu_REVISADO.docx`, `.pdf` e `RELATORIO_REVISAO_ETP_MINACU.md`) permanecem inalterados em `/home/user/Macunha`.

O TR (`1765dfd8-TR_Inteligencia_Contabil.docx`) **não foi tocado** nesta tarefa, conforme instruído — sua revisão está prevista para etapa posterior, já mapeada na tabela da seção 9 do relatório V1.
