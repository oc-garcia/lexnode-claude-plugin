# LexNode

Consulte processos e publicações do Judiciário brasileiro, acompanhe sua carteira e
pesquise jurisprudência com precedentes qualificados do STJ pela sua conta LexNode.
O pacote oferece cinco fluxos:

- `consultar-processo`: ler o que o acervo já guarda de um processo, atualizar a
  consulta quando pedido ou retomar uma consulta anterior;
- `pesquisar-jurisprudencia`: pesquisar decisões e conferir precedentes do STJ;
- `acompanhar-carteira`: criar e gerenciar acompanhamentos por processo, OAB,
  nome de parte, termo ou CNPJ, somente quando você pedir;
- `conferir-novidades`: ler o que chegou dos acompanhamentos, com o conteúdo
  completo de cada achado;
- `consultar-calendario`: consultar o calendário forense como referência.

Ative o plugin quando quiser usá-lo e autorize a conexão com sua conta. A conexão
usa OAuth: a senha é digitada na tela de login do LexNode, nunca na conversa. A
tela de consentimento informa a conta escolhida, as permissões e o teto diário de
créditos. O uso pode consumir créditos dessa conta; a instalação não inicia
consultas nem cria monitores.

## Instalação no Claude Code

No Claude Code 2.1.275 ou posterior, execute:

```text
/plugin install lexnode --marketplace oc-garcia/lexnode-claude-plugin
```

O marketplace deste repositório se chama `lexnode-plugins`. Depois de instalar,
ative `lexnode@lexnode-plugins` no gerenciador de plugins e autorize a conexão
OAuth quando solicitado. O pacote começa desativado por padrão. Use o gerenciador
para atualizar o marketplace e o plugin, conferir a versão instalada ou removê-lo.
Remover o plugin e revogar a conexão no LexNode são ações independentes.

Este repositório distribui o pacote para instalação direta. Sua disponibilidade
aqui não representa aprovação ou inclusão no marketplace oficial da Anthropic.

## Consultas e conteúdo

Informe o número do processo e o tribunal, ou o identificador de uma consulta
anterior. A leitura do acervo entrega o que já está disponível, com a data de cada
informação, sem pedir atualização; a atualização é uma consulta própria, que pode
continuar em segundo plano. O limite de tentativas não é uma previsão de entrega.
As publicações incluídas são as já disponíveis no acervo. Ler ou consultar não
busca novamente o diário nem inicia acompanhamento contínuo. As continuações
permitem acessar o conteúdo completo.

Acompanhamentos só são criados quando você pede, com o alvo confirmado, e ocupam
vagas do plano; o acompanhamento de um processo pode incluir também as publicações
do número, ocupando uma vaga a mais de monitores de tema. A leitura das novidades sem filtros
marca os eventos entregues como lidos para essa conexão.

Na pesquisa jurídica, informe a questão, a matéria e eventuais limites de tribunal
ou período. Leia as decisões encontradas e confira as referências na fonte
oficial. O registro de precedentes qualificados disponível corresponde ao STJ;
não inclui automaticamente os temas de outros tribunais.

Cobertura e disponibilidade variam. A data de captura descreve o dado recebido,
sem garantir a ausência de atos posteriores. O calendário só apoia a conferência
de datas potencialmente relevantes e pode conter omissões ou defasagens. Não
calcula, valida nem certifica prazo, termo inicial ou vencimento. Qualquer
simulação é uma estimativa não validada, condicionada às premissas declaradas e
às conferências pendentes. A data no diário, isolada, não define publicação,
intimação ou termo inicial. Cabe ao advogado verificar fontes oficiais, regras e
atos aplicáveis ao caso e validar a contagem final.

## Conexão e suporte

O único serviço remoto declarado é https://api.lexnode.com.br/mcp. As skills
utilizam as ferramentas dessa conexão, sem executar scripts, instalar programas
ou ler arquivos locais. Os dados enviados nas chamadas são tratados pelo LexNode
conforme a política de privacidade, e as respostas são compartilhadas com o
assistente escolhido. Nenhuma skill cria acompanhamento sem pedido seu.

Se a sessão expirar, reconecte a conta. Se uma operação estiver indisponível por
permissão, saldo ou situação da conta, confira a informação retornada e procure
quem administra a conta ou o suporte. Revogue a conexão no portal quando quiser
encerrar seu acesso.

- [Conector LexNode](https://claude.ai/directory/lexnode)
- [Guia de conexão](https://www.lexnode.com.br/docs/agentes)
- [Suporte](https://www.lexnode.com.br/contato)
- [Privacidade](https://www.lexnode.com.br/legal/privacidade)
- [Termos](https://www.lexnode.com.br/legal/termos)

## Licença

Os arquivos deste pacote são distribuídos sob a [licença MIT](LICENSE). A licença
abrange o manifesto, as instruções e os assets incluídos neste repositório; não
licencia o motor LexNode, o serviço remoto ou conteúdo jurídico de terceiros.
O acesso ao serviço continua sujeito aos Termos e às permissões da conta.
