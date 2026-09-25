# Relatório de Padronização Visual — TR Inteligência Contábil (Minaçu/GO)

## Escopo da tarefa
Padronização exclusivamente visual/institucional do Termo de Referência (TR) já
aprovado tecnicamente. Nenhum conteúdo técnico, numeração, POC, quantitativo ou
redação foi alterado — apenas a diagramação (cabeçalho, rodapé, margens, brasão).

## Fonte do padrão visual utilizado
O padrão institucional real de Minaçu foi extraído do arquivo
`ETP_Inteligencia_Contabil_Minacu_REVISADO_V2.docx` (mesmo município, documento já
aprovado e com o padrão oficial da Prefeitura de Minaçu, incluindo o brasão real).
Esse foi o arquivo priorizado como fonte de identidade visual, conforme solicitado.

O PDF de referência `termo_de_referencia_natal.pdf` (modelo institucional de outro
município, Natal) foi consultado apenas como referência genérica de estrutura de um
TR (organização de cabeçalho, forma de apresentação de títulos/seções). Nenhum
conteúdo textual, brasão ou elemento gráfico de Natal foi copiado ou reaproveitado
no documento final — apenas o ETP de Minaçu forneceu os elementos gráficos reais.

## Elementos visuais reaproveitados do ETP V2 (Minaçu)
- `word/header1.xml` — cabeçalho com o brasão/logomarca "Prefeitura de Minaçu"
  (imagem `word/media/image1.png`), incluindo a moldura/faixa gráfica institucional
  no canto superior direito.
- `word/footer1.xml` — rodapé com o papel timbrado institucional
  (imagem `word/media/image2.png`), contendo o texto "Prefeitura Municipal de
  Minaçu", endereço, telefone, e-mail e site oficiais.
- Relacionamentos (`word/_rels/header1.xml.rels`, `word/_rels/footer1.xml.rels`) e
  as imagens correspondentes em `word/media/`.
- Configuração de página da seção (`sectPr`): tamanho de página A4
  (11906 x 16838 twips), margens (topo/rodapé 1417, laterais 1701, cabeçalho/rodapé
  708 twips) e as referências de cabeçalho/rodapé padrão — idênticas às usadas no
  ETP, garantindo o posicionamento correto das imagens de moldura institucional
  (que são âncoras posicionadas em relação à margem/página).
- `Content_Types` e `document.xml.rels` do TR foram ajustados para declarar as
  novas partes (`header1.xml`, `footer1.xml`, `image1.png`, `image2.png`).

Os estilos de título (`Ttulo1`, `Ttulo2`, `Ttulo3`...) e de tabela
(`Tabelacomgrade`) já existentes no TR V2 foram mantidos como estavam: o ETP V2 não
possui estilos de título/tabela ricos equivalentes (usa apenas estilos mínimos de
um documento gerado a partir de texto simples), portanto não havia um padrão de
título/tabela institucional distinto a reaplicar. Os estilos de título e tabela do
TR já seguiam um padrão visual coerente (cores institucionais em azul/petróleo),
que foi preservado para não descaracterizar a formatação já aprovada.

## Ajuste de diagramação aplicado
Foi identificado, na primeira renderização, um corte ruim de uma linha da tabela de
matriz de riscos entre duas páginas (linha dividida ao meio, deixando conteúdo
órfão no topo da página seguinte). Corrigido adicionando `<w:cantSplit/>` a todas
as linhas de todas as 7 tabelas do documento, impedindo que uma linha seja
fragmentada entre páginas. O cabeçalho de tabela (`<w:tblHeader/>`) já estava
marcado em todas as tabelas, garantindo a repetição do cabeçalho quando a tabela
atravessa página — mantido.

Após a correção, todas as 30 páginas foram revisadas visualmente (renderização
PDF a 90 DPI): não há títulos órfãos no fim de página, não há tabelas cortadas de
forma ruim, não há sobreposição de texto com o rodapé/cabeçalho institucional, e a
legibilidade está preservada.

## Quantidade final de páginas
**30 páginas** (o TR V2 original, sem o padrão visual, também totalizava 30
páginas com a formatação original; a reformatação para o padrão institucional de
Minaçu manteve a mesma contagem).

## Confirmação de integridade do conteúdo técnico
O texto foi extraído com `pandoc -t markdown` do TR V2 original e do TR final
diagramado e comparado com `diff`:

```
diff original.md final.md
(saída vazia — nenhuma diferença)
```

Ambos os arquivos Markdown extraídos têm exatamente 1609 linhas, sem nenhuma
diferença de conteúdo. Isso confirma que nenhuma palavra do corpo do texto,
nenhuma numeração de item/seção/subitem, nenhum valor quantitativo (1 licença
corporativa, 20 usuários simultâneos, 36 meses, SLA, matriz de riscos, lote único
etc.) e nenhuma referência interna ("seção X", "item Y", "subitem Z") foi alterada.
A Prova de Conceito (POC) e sua numeração (POC-01 a POC-06, itens 8.x) permanecem
idênticas.

Nenhum campo `[INFORMAÇÃO A PREENCHER]` foi preenchido; nenhum dado administrativo,
número de processo, secretaria, nome de servidor ou data foi inventado. Nenhuma
marca d'água foi adicionada (o ETP V2, fonte do padrão visual, também não possui).

## Validação técnica do arquivo .docx
`scripts/office/validate.py` (verificação XSD/estrutural do pacote OOXML) executado
contra o original: **"All validations PASSED!"**, com contagem de parágrafos
idêntica (536 → 536, 0 de diferença).

## Entregas
1. `TR_Inteligencia_Contabil_Minacu_FINAL_MODELO_PREFEITURA.docx`
2. `TR_Inteligencia_Contabil_Minacu_FINAL_MODELO_PREFEITURA.pdf`
3. Este relatório.

O `ETP_Inteligencia_Contabil_Minacu_REVISADO_V2.docx` não foi modificado em nenhum
momento (usado somente como leitura/extração).
