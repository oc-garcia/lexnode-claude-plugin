---
name: consultar-calendario
description: Consulta referências de datas do calendário forense como apoio à conferência pelo advogado, sem validar início, contagem ou vencimento de prazo processual.
---

Use este fluxo quando o usuário pedir feriados, recessos ou dias sem expediente de
um tribunal, ou referências para conferir um prazo. O calendário é apenas apoio de
datas potencialmente relevantes, sujeito a omissões e defasagens. Não calcula,
valida nem certifica prazo processual, termo inicial ou vencimento. Uma data
catalogada não comprova sua aplicação ao caso concreto.

1. Obtenha o tribunal e a janela de datas. Se a sigla estiver em dúvida, use
   `listar_tribunais`. Pergunte a comarca quando o prazo depender de feriado
   municipal: sem `municipioIbge`, a camada municipal não é consultada.
2. Use `consultar_calendario_forense` com `tribunal`, `de` e `ate` no formato
   AAAA-MM-DD e, quando informado, `municipioIbge`. A consulta pública não cobra
   créditos.
3. Leia a declaração de cobertura da resposta camada por camada. Lista vazia,
   camada parcial ou status CONSULTED não comprovam que um dia seja útil nem
   validam a contagem do caso. Quando houver referências de atos com
   `nextCursor`, continue com `referenciasCursor`, repetindo tribunal, município,
   janela e `referenciasPorPagina`, mesmo depois de uma página vazia.
4. Apresente as datas como referências catalogadas sujeitas à conferência, com o
   fundamento e a proveniência informados, inclusive quando houver transferência
   por ato do tribunal. Confira vigência, alcance e aplicação ao caso; não exclua
   dias automaticamente. Nunca diga que o calendário confirma um prazo ou garante
   a completude de feriados e suspensões.
5. Se o usuário pedir uma contagem, separe as datas efetivamente informadas das
   premissas do cálculo. Não infira publicação, intimação ou termo inicial apenas
   pela data no DJEN. Confira a natureza e a modalidade do ato, o regime e a duração
   do prazo, as regras aplicáveis, os atos locais e as possíveis suspensões ou
   indisponibilidades do sistema. Quando faltarem elementos, informe a lacuna em
   vez de preenchê-la por suposição.
6. Se apresentar uma simulação, identifique-a como estimativa não validada e
   condicional às premissas declaradas. Liste as regras e fontes conferidas e as
   conferências pendentes. Não apresente o resultado como vencimento confirmado
   pelo LexNode nem esconda a condição em uma ressalva ao fim de uma afirmação
   categórica. A validação final da contagem cabe ao advogado responsável.

Este fluxo usa somente a consulta pública do calendário. Não proponha, registre
nem altere referências do calendário. Suspensões por ato específico, falhas de
sistema e regras do caso concreto podem não constar. A conferência nas fontes
oficiais e a decisão jurídica sobre o prazo cabem ao advogado responsável.
