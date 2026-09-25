# Relatório de Revisão do ETP — Plataforma de Inteligência Contábil e Gestão Fiscal (Minaçu/GO)

## 1. Modelo oficial de Minaçu utilizado

`1f86f205-ETP_e_Analise_de_Riscos_GED_Minacu_FINAL_FLUXO_CORRIGIDO_1.docx` — Estudo Técnico Preliminar oficial da Prefeitura de Minaçu (originalmente elaborado para a contratação de GED). Deste arquivo foram reaproveitados: cabeçalho com brasão e faixa institucional "PREFEITURA DE MINAÇU"; rodapé com faixa institucional (imagem "Papel Timbrado b.png") contendo endereço, telefone e e-mail da Prefeitura; fontes (Cambria/tema minorHAnsi), margens, tamanho de página (A4), estilo de tabela com grade, e o padrão visual de "caixas" de seção — título em barra cinza (D9D9D9) seguido do conteúdo, dentro de uma tabela de largura total, que é o padrão de diagramação de todo o documento original. Também foi reaproveitado o padrão de campo de assinatura final (linha, nome, cargo, ato de nomeação) e a convenção de placeholder `[PREENCHER — ...]` do próprio modelo, adaptada para `[INFORMAÇÃO A PREENCHER]` conforme instruído.

**Observação sobre marca d'água:** o modelo oficial de Minaçu **não possui marca d'água real** (imagem de fundo semitransparente atrás do texto). O que existe é uma imagem de cabeçalho (brasão + faixa "PREFEITURA DE MINAÇU") e uma imagem de rodapé (faixa com dados de contato), ambas opacas e fora da área de texto — não uma marca d'água sobreposta ao conteúdo. Isso foi preservado exatamente como está no modelo; nenhuma marca d'água foi inventada.

## 2. Quantidade final de páginas do docx revisado

**12 páginas** (verificado após conversão para PDF e renderização página a página).

## 3. Módulos que permaneceram

1. Painéis Analíticos Executivos (receita, despesa, despesas críticas, caixa/patrimônio, relações institucionais, indicadores legais, apresentação).
2. Entregas, Obrigações e Conformidade (agenda, prazos, responsáveis, status, alertas, notificações, evidências, protocolos, recibos).
3. CAUC (situação de adimplência, pendências, grupos de conformidade, histórico, data de consulta, indicação de indisponibilidade/defasagem da fonte).
4. Processos do TCM-GO (número, órgão, exercício, unidade, assunto, fase, situação, prazos, diligências, julgamentos/decisões, documentos, providências pendentes, alertas).
5. Integrações, Importação e Rastreabilidade (arquivos, balancetes, API quando houver interface oficial autorizada, origem, data de atualização, status, histórico).
6. Aplicativo móvel integrado (mesma base, usuários e perfis da plataforma web — não é sistema independente).

DCA, RREO, RGF e MSC foram mantidos, mas **apenas como fontes de dados legítimas** que alimentam os indicadores legais dos painéis analíticos (item 3.2/"Indicadores legais" do ETP revisado) — não há mais módulo autônomo de validação, cruzamento ou conferência desses demonstrativos.

## 4. Módulos removidos

- **Módulo de Validação e Diagnóstico Fiscal** (validação preventiva; cruzamentos DCA × RREO × RGF × MSC como módulo autônomo; validador; relatórios de inconsistências desse módulo; regras versionadas de validação).
- **Módulo de Inteligência Artificial Institucional/Setorial** (assistentes de IA por perfil/área; geração assistida de documentos; pesquisa contextualizada por IA; resumos/comparações por IA; base documental de IA; governança de IA; franquia de 30 milhões de tokens; painel de consumo de tokens; custos de IA; qualquer requisito de modelo de linguagem).
- **Módulo comercial autônomo "Administração, Segurança e Governança"** — dissolvido; seus requisitos técnicos aplicáveis foram redistribuídos como requisitos transversais (ver item 5).

## 5. Requisitos transversais de segurança preservados

Reorganizados no item 3.1 do ETP revisado ("Requisitos gerais e requisitos transversais de segurança, privacidade e continuidade"), explicitamente qualificados como **não constituindo módulo comercial autônomo**: autenticação segura; usuários individuais e intransferíveis; perfis e permissões configuráveis; controle de acesso pelo princípio do menor privilégio; segregação de acesso por perfil/órgão/unidade; logs e trilhas de auditoria; rastreabilidade; criptografia em trânsito e em repouso; backup; continuidade e disponibilidade (99,5% de referência); proteção de dados pessoais/LGPD; gestão de vulnerabilidades e notificação de incidentes; exportação estruturada dos dados; reversibilidade ao término do contrato; suporte técnico e manutenção corretiva/evolutiva.

## 6. Referências residuais encontradas e corrigidas

Foi feita varredura completa do texto final (via extração de texto do docx) em busca de: "Cidade Ocidental", "IA"/"inteligência artificial", "token", e menções aos módulos excluídos.

- **"Cidade Ocidental"**: aparecia repetidamente no ETP original (arquivo 1), inclusive nas seções 1, 2.1, 2.2 e 10. Todas as ocorrências foram substituídas por **"Minaçu"** (ou "Minaçu-GO", conforme o padrão do modelo oficial, inclusive no campo de assinatura final, que já trazia "Minaçu-GO" corretamente). Confirmado por busca no texto final: **nenhuma ocorrência restante**.
- **"IA" / "inteligência artificial" / "token"**: todas as menções foram removidas do corpo do ETP (sumário executivo, diagnóstico do problema — a antiga "quarta frente" de uso informal de IA foi eliminada —, requisitos da plataforma, quantitativos, estimativa de valor, descrição da solução, lote único, aplicativo móvel e indicadores de resultado). Confirmado por busca no texto final: **nenhuma ocorrência restante**.
- **Módulo de validação fiscal**: menções a "validação preventiva", "validador" e "cruzamento" como módulo foram removidas; DCA/RREO/RGF/MSC foram mantidos apenas como fontes de dados dos indicadores legais dos painéis (linguagem ajustada no item 2.2 e 3.2 do ETP).

## 7. Alterações textuais relevantes feitas

- Reestruturação completa do capítulo "Requisitos mínimos da plataforma" (antigo item 3), que passou a ter 7 subitens: 3.1 Requisitos gerais/transversais de segurança (absorveu o antigo 3.8 e o conteúdo de segurança do módulo comercial excluído); 3.2 Painéis analíticos executivos; 3.3 Entregas, obrigações e conformidade; 3.4 CAUC; 3.5 Processos do TCM-GO; 3.6 Integrações, importação e rastreabilidade; 3.7 Aplicativo móvel — eliminando os antigos itens 3.3 (validação) e 3.5 (IA setorial) do ETP original.
- Diagnóstico do problema (item 2) reduzido de quatro para três frentes, eliminando a "quarta frente" (uso informal de IA / governança institucional de IA).
- Justificativa da redução de escopo redigida com linguagem técnica de **adequação do objeto à necessidade identificada**, **economicidade**, **proporcionalidade dos requisitos** e **ampliação potencial da competitividade** — sem qualquer menção a "baratear a licitação".
- Levantamento de mercado (item 4) revisado para o novo objeto, mantendo os quatro cenários (modelo manual, desenvolvimento próprio, desenvolvimento sob encomenda, SaaS especializada), sem fornecedores ou preços inventados.
- Quantitativos (item 5) preservados exatamente como no ETP original — 1 licença corporativa, 20 usuários simultâneos, vigência de 3 anos, 1 aplicativo móvel integrado — com remoção apenas da linha "Capacidade de IA".
- Estimativa de valor (item 6): **não foi apresentado valor estimado**, pois os documentos-fonte não contêm pesquisa de preços concluída para o escopo revisado; isso foi registrado expressamente como pendência no corpo do ETP.
- Lote único (item 8) reescrito para fundamentar-se exclusivamente na integração entre painéis, obrigações, CAUC, processos do TCM-GO e no compartilhamento de autenticação/base entre web e aplicativo móvel — sem qualquer menção a IA ou ao antigo validador fiscal como fundamento.
- Indicadores de resultado (item 11) com as linhas relativas a IA (uso controlado de IA, supervisão humana sobre conteúdo de IA) e ao módulo de validação (identificação preventiva de inconsistências, cruzamentos automatizados) removidas; demais indicadores mantidos e um novo indicador de centralização de CAUC/TCM-GO incorporado.
- Campo de identificação do objeto e bloco de assinatura final adaptados com `[INFORMAÇÃO A PREENCHER]` para secretaria requisitante, setor, processo administrativo, data, nome do(a) signatário(a) e número do decreto — nenhum dado institucional foi inventado.

## 8. Pendências ainda dependentes da Administração

- **Secretaria requisitante, setor responsável, número do processo administrativo e data de elaboração** — não constavam nos documentos-fonte; marcados como `[INFORMAÇÃO A PREENCHER]`.
- **Nome do(a) Secretário(a)/autoridade signatária e número/data do decreto de nomeação** — idem, no campo de assinatura final.
- **Estimativa de valor da contratação** — não há pesquisa de preços concluída nos documentos-fonte para o escopo revisado; a Administração deve realizar pesquisa de preços formal antes de prosseguir para a fase externa da licitação.
- **Confirmação final da conclusão sobre lote único e sobre a alternativa SaaS** — ambas dependem dos resultados efetivos da pesquisa de mercado a ser realizada na fase preparatória, conforme já ressalvado no próprio texto do ETP.

## 9. Alterações necessárias no TR após a revisão do ETP

O Termo de Referência (`1765dfd8-TR_Inteligencia_Contabil.docx`) ainda contém integralmente os módulos excluídos do ETP. Ele **não foi alterado** neste trabalho (fora do escopo solicitado), mas deverá ser revisado nos seguintes pontos antes do prosseguimento da licitação:

| Seção/item do TR | O que deve ser alterado |
|---|---|
| 1.1 Objeto principal | Remover menções a "análise e diagnóstico fiscal, validação preventiva de demonstrativos" e a "inteligência artificial setorial e corporativa"; reescrever o objeto alinhado ao escopo reduzido do ETP (painéis, obrigações/conformidade, CAUC, processos TCM-GO, integrações/rastreabilidade). |
| 1.2 Natureza e regime de execução | Remover referência a "assistentes de IA em funcionamento" e a "franquia de processamento de inteligência artificial" como elemento do regime de execução. |
| 1.3 Unidade de contratação e quantidade | Remover "franquia de processamento de inteligência artificial" da lista de elementos padronizados/quantidade. |
| 2. Fundamentação e justificativa | Remover trechos que tratam da "quarta frente" de uso institucional de IA e do módulo de validação preventiva como justificativa; realinhar a fundamentação ao novo escopo (mantendo DCA/RREO/RGF/MSC apenas como fontes de indicadores). |
| 3. Descrição da solução como um todo (tabela de módulos) | Remover as linhas "Validador preventivo" e "IA corporativa e setorial"; ajustar a linha de segurança/continuidade para deixar claro que é requisito transversal, não módulo comercial. |
| 5.1.2 Controle de acesso | Remover a exigência específica de que "assistente de IA incorporado à plataforma" esteja integrado ao sistema de permissões (não há mais assistente de IA). |
| 5.3 Módulo de validação e diagnóstico fiscal (integralmente) | Excluir a seção inteira (5.3.1 a 5.3.4), incluindo tipos de verificação, resultado das verificações e versionamento de regras. Avaliar se algum requisito de transparência metodológica (origem/fórmula dos indicadores) deve ser reaproveitado dentro de 5.2 (painéis). |
| 5.4 Módulo de entregas, CAUC e processos | Renomear/reestruturar em linha com o ETP (Entregas e Obrigações; CAUC; Processos do TCM-GO como itens próprios, não necessariamente um único "módulo"). |
| 5.5 Módulo de inteligência artificial setorial (integralmente) | Excluir a seção inteira (5.5.1 a 5.5.3), incluindo assistentes por área, funcionalidades mínimas e capacidade de processamento/franquia de tokens (30.000.000 tokens mensais). |
| 5.6 Aplicativo móvel | Remover "assistentes de IA" da lista de funcionalidades do aplicativo; manter dashboard, receitas, despesas, caixa, indicadores, obrigações, CAUC, processos TCM-GO e alertas. |
| 5.8 Segurança, privacidade e continuidade | Remover referência a "treinamento de modelos de IA de terceiros" nas vedações de uso de dados; manter os demais requisitos como transversais. |
| 6. Níveis de serviço | Revisar se há SLA específico vinculado a IA/validação a ser removido (não identificado explicitamente no trecho revisado — checar seção completa). |
| 7.1 Quantitativo / 7.4 Reajuste e alterações | Remover referência a "franquia de processamento de IA" como item passível de acréscimo/termo aditivo. |
| 8. Prova de Conceito (POC) | Remover POC-04 (Validação e diagnóstico fiscal) e POC-07 (Inteligência artificial) da matriz de cenários de teste; renumerar os demais cenários; remover exigência de "permissões também à IA". |
| 9.2 Pagamento | Remover exigência de a nota fiscal discriminar "franquia de IA, consumo" — ajustar para os módulos remanescentes. |
| 10. Obrigações da contratada | Remover item que lista "processos, IA, segurança e suporte" — ajustar para o escopo remanescente. |
| 11. Obrigações da contratante | Remover item "assegurar que a IA seja utilizada como apoio, sem delegar a ela [decisões]" (não há mais IA). |
| 12. Proteção de dados, sigilo e governança documental | Remover referência a "históricos de IA" na lista de dados protegidos. |
| 13. Estimativa do valor e regras de precificação | Remover a linha "IA — Franquia mensal de 30.000.000 tokens..." da tabela de precificação; ajustar a memória de cálculo do preço para não incluir franquia de IA. |
| 14. Matriz de alocação de riscos | Remover as linhas de risco relacionadas a "IA gera texto sem [revisão]" e "Utilização de [conteúdo produzido] por IA sem revisão"; manter os demais riscos aplicáveis ao escopo remanescente (dados de origem, falha de importação, indisponibilidade de fonte externa como CAUC, atualização regulatória, desatualização dos dados apresentados). |

**Importante:** nenhuma dessas alterações foi aplicada ao arquivo do TR nesta tarefa — apenas o ETP foi revisado, conforme solicitado. A tabela acima deve orientar a próxima revisão do TR pela equipe responsável.

## 10. Resultado da revisão visual do PDF (página a página)

O PDF final (12 páginas) foi renderizado com `soffice`/`pdftoppm` e cada página foi lida e inspecionada visualmente. Resumo:

- **Página 1**: capa/identificação do objeto e item 1 (Sumário executivo). Cabeçalho (brasão + faixa "PREFEITURA DE MINAÇU") e rodapé institucional (endereço, telefone, e-mail) presentes e corretos. Sem quebras ruins.
- **Página 2**: item 2 (Identificação do problema), subitens 2.1 a 2.3 completos. Sem cortes.
- **Página 3**: subitem 2.4 finaliza a seção 2; título "3. Requisitos mínimos da plataforma" inicia ao final da página, mas **não fica órfão** — na primeira versão renderizada o título aparecia isolado no rodapé da página com a seguinte página quase toda em branco (problema de título órfão); **corrigido** unindo o título da seção e o primeiro parágrafo de conteúdo na mesma célula de tabela com `keepNext`, o que resultou em o título passar inteiro para a página seguinte junto do conteúdo, eliminando o órfão (a página 3 ficou apenas com o fim da seção 2, sem espaço desperdiçado relevante).
- **Página 4**: item 3.1 e 3.2 completos, incluindo a tabela de painéis analíticos — tabela renderizada sem cortes, cabeçalho da tabela (linha cinza) presente.
- **Página 5**: itens 3.3 a 3.7 completos, sem cortes.
- **Página 6**: item 4 (Levantamento de mercado) com tabela comparativa de 4 alternativas — tabela completa, sem corte de coluna ou linha.
- **Página 7**: item 5 (Quantitativos) com tabela — completa.
- **Página 8**: itens 6 (Estimativa de valor, com tabela) e 7 (Descrição da solução) — ambos completos na mesma página, sem cortes.
- **Página 9**: itens 8 (Lote único) e 9 (Contratações correlatas) — completos.
- **Página 10**: item 10 (Modelo de implantação) com tabela de fases — completa.
- **Página 11**: item 11 (Indicadores de resultado) — tabela grande; uma linha ("Assegurar atendimento e suporte aos usuários") é dividida entre as páginas 11 e 12 pela quebra natural de tabela do Word/LibreOffice (comportamento padrão de tabelas longas, não uma corrupção de conteúdo — o cabeçalho da tabela não se repete na página 12, o que é uma pequena imperfeição visual, mas o conteúdo permanece íntegro e legível).
- **Página 12**: final da tabela do item 11, itens 12 (Sustentabilidade) e 13 (Posicionamento conclusivo), e bloco de assinatura ("Minaçu-GO, em ____ de _______________ de 2026", linha de assinatura e placeholders `[INFORMAÇÃO A PREENCHER]`) — tudo presente e corretamente formatado, sem "Cidade Ocidental" nem qualquer referência a IA.

Marca d'água: como registrado no item 1 acima, **o modelo oficial não possui marca d'água real** — apenas cabeçalho e rodapé com imagens institucionais, que foram confirmados presentes em todas as 12 páginas.

Numeração de página: **o modelo oficial de Minaçu não contém campo de numeração de página** (nenhum campo `PAGE` foi localizado no cabeçalho ou rodapé do arquivo 3). Essa característica foi mantida tal como está no modelo — não foi adicionada numeração que não existia no padrão institucional original, para não descaracterizar o modelo oficial reaproveitado. Caso a Administração deseje numeração de página, é necessário decidir isso como alteração de padrão institucional, fora do escopo desta tarefa.

## Checklist de confirmação

| Item | Resposta |
|---|---|
| Nenhuma IA permaneceu como requisito | **SIM** |
| Nenhuma franquia de tokens permaneceu | **SIM** |
| Nenhum módulo de Validação e Diagnóstico Fiscal permaneceu | **SIM** |
| Segurança permanece apenas como requisito transversal (não como módulo comercial) | **SIM** |
| Aplicativo e sistema web permanecem integrados (não tratados como sistemas separados) | **SIM** |
| O ETP utiliza o padrão visual oficial de Minaçu (capa, cabeçalho, rodapé, marca-d'água, brasão do arquivo 3) | **PARCIAL — SIM para capa/cabeçalho/rodapé/brasão; NÃO há marca d'água real no modelo oficial (arquivo 3), portanto nenhuma foi adicionada, pois isso seria inventar um elemento inexistente no padrão institucional.** |
| Não há referência residual a "Cidade Ocidental" | **SIM** |

---

## Resumo final

Foram entregues em `/home/user/Macunha`:

- `ETP_Inteligencia_Contabil_Minacu_REVISADO.docx`
- `ETP_Inteligencia_Contabil_Minacu_REVISADO.pdf` (12 páginas, revisado visualmente página a página)
- `RELATORIO_REVISAO_ETP_MINACU.md` (este relatório)

O ETP foi reconstruído sobre o padrão visual real do modelo oficial de Minaçu (arquivo 3: cabeçalho com brasão, rodapé institucional, fontes, tabelas em caixa cinza para títulos de seção, bloco de assinatura), preenchido com o conteúdo técnico do ETP original (arquivo 1), reestruturado em torno de 5 pilares (painéis, entregas/obrigações/conformidade, CAUC, processos TCM-GO, integrações/rastreabilidade), com remoção completa e verificada de IA, tokens, módulo de validação fiscal autônomo e do módulo comercial de segurança/governança (convertido em requisitos transversais). Nenhum dado institucional (secretaria, processo, data, signatário) foi inventado — todos os campos ausentes nos documentos-fonte foram marcados como `[INFORMAÇÃO A PREENCHER]`. Não há estimativa de valor, pois não havia pesquisa de preços concluída nos documentos de origem; isso está registrado como pendência explícita no próprio ETP e no relatório.

**Pendência crítica de maior destaque:** o modelo oficial de Minaçu não possui marca d'água nem numeração de página — ambas as ausências foram mantidas fielmente ao padrão institucional, e não supridas com invenção. Se a Prefeitura desejar esses elementos, é uma decisão de padrão institucional a ser tomada separadamente. Além disso, o TR (arquivo 2) permanece **não alterado** e precisa da revisão detalhada na tabela da seção 9 deste relatório antes de seguir para a fase externa da licitação.
