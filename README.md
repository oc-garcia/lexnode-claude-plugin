# LexNode

Consulte processos e publicações do Judiciário brasileiro e pesquise jurisprudência
com precedentes qualificados do STJ pela sua conta LexNode. O pacote oferece dois
fluxos: consultar ou retomar um processo com as publicações disponíveis e pesquisar
jurisprudência com leitura das referências encontradas.

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
anterior. A consulta pode continuar em segundo plano; o limite de tentativas não
é uma previsão de entrega. As publicações incluídas na consulta são as já
disponíveis no acervo. Essa leitura não busca novamente o diário nem inicia seu
acompanhamento contínuo. As continuações permitem acessar o conteúdo completo.

Na pesquisa jurídica, informe a questão, a matéria e eventuais limites de tribunal
ou período. Leia as decisões encontradas e confira as referências na fonte
oficial. O registro de precedentes qualificados disponível corresponde ao STJ;
não inclui automaticamente os temas de outros tribunais.

Cobertura e disponibilidade variam. A data de captura descreve o dado recebido,
sem garantir a ausência de atos posteriores. Calendários são apenas referência;
cabe ao advogado conferir as fontes oficiais e calcular seu próprio prazo.

## Conexão e suporte

O único serviço remoto declarado é https://api.lexnode.com.br/mcp. As skills
utilizam as ferramentas dessa conexão, sem executar scripts, instalar programas
ou ler arquivos locais. Os dados enviados nas chamadas são tratados pelo LexNode
conforme a política de privacidade, e as respostas são compartilhadas com o
assistente escolhido. Nenhuma skill cria vigília sem pedido de acompanhamento.

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
