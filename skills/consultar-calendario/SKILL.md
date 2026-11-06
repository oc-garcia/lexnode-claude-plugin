---
name: consultar-calendario
description: Consulta o calendário forense do LexNode como referência dos dias sem expediente de um tribunal numa janela, deixando a contagem final do prazo com o advogado.
---

Use este fluxo quando o usuário pedir feriados, recessos ou dias sem expediente de
um tribunal, ou referências para conferir um prazo. O resultado é referência: ele
não calcula nem certifica prazo processual.

1. Obtenha o tribunal e a janela de datas. Se a sigla estiver em dúvida, use
   `listar_tribunais`. Pergunte a comarca quando o prazo depender de feriado
   municipal: sem `municipioIbge`, a camada municipal não é consultada.
2. Use `consultar_calendario_forense` com `tribunal`, `de` e `ate` no formato
   AAAA-MM-DD e, quando informado, `municipioIbge`. A consulta pública não cobra
   créditos.
3. Leia a declaração de cobertura da resposta camada por camada. Lista vazia ou
   camada parcial não prova dias úteis. Quando houver referências de atos com
   `nextCursor`, continue com `referenciasCursor`, repetindo tribunal, município,
   janela e `referenciasPorPagina`, mesmo depois de uma página vazia.
4. Apresente os dias conhecidos com o fundamento informado, inclusive feriado
   transferido por ato do tribunal. Atos marcados como referência precisam ter
   vigência, alcance e aplicação ao caso conferidos; não os some à lista nem
   exclua dias sem essa conferência.

Este fluxo usa somente a consulta pública do calendário. Não proponha, registre
nem altere referências do calendário. Suspensões por ato específico, falhas de
sistema e regras do caso concreto podem não constar. A contagem final do prazo e a
conferência nas fontes oficiais cabem ao advogado responsável.
