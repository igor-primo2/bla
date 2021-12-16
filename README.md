# http-tupi:  _HTTP-simple_

## _Igor de Souza Carvalhal Primo_

 [HTTP](https://developer.mozilla.org/pt-BR/docs/Web/HTTP/Overview) é um protocolo que permite a obtenção de recursos na web. É um protocolo extensível com uso do  cabeçalho ( _headers_) para inclusão de novos campos e valores.  A especificação das mensagens HTTP e extensões estão definidas na [RFC 7230](https://datatracker.ietf.org/doc/html/rfc7230). Nesta RFC são definidos os conceitos de proxy, gateway e túneis HTTP como agentes intermediários capazes de interpretar campos de mensagens de cliente e servidor e em alguns casos traduzir para outros formatos não padronizados pelo HTTP ou redirecionar para servidores internos. Atualmente existe um [grupo de trabalho na Internet](https://httpwg.org/specs/) pesquisando novas extensões para o HTTP. 
 
__Proponha__ uma nova aplicação para resolver um problema específico de um usuário na web. Defina uma nova extensão para o HTTP denominada HTTP Tupi com a inclusão de novos campos de cabeçalho. __Implemente o cliente e servidor HTTP Tupi__, para sua solução proposta. O servidor HTTP Tupi deve ser capaz de reconhecer uma mensagem HTTP Tupi e realizar ações, incluindo a reposta com conteúdo diferente do HTTP/1.1. As respostas podem incluir dados em outros formatos diferentes do HTML, como XML e JSON, por exemplo, de acordo com a especificação de sua proposta.

Se seu servidor receber mensagens sem a extensão do campo proposto, o servidor deve agir de acordo com o protocolo HTTP/1.1. Se a mensagem originada do cliente incluir a extensão no cabeçalho, o servidor deve responder de acodo comm protocolo HTTP Tupi.

## Qual o problema considerado?  
_Justifique a aplicação de sua solução proposta_

> O problema proposto é a dificuldade de visualizar as liguações http de uma página utilizando as utilidades de desenvolvedores de navegodores populares. A variação do protocolo HTTP sugerida aqui, chamada HTTP Tupi, funciona retornando uma lista das ligações visíveis em formato text/plain de uma  página apontada por uma URL fornecida pelo usuário. Se o protocolo especificado for HTTP/1.1, a resposta consistirá numa resposta HTTP/1.1 com um arquivo de conteúdo text/html. Se o protocolo especificado for HTTP/Tupi, a resposta será um arquivo de conteúdo text/plain com uma lista das ligações visíveis na página apontada pela URL fornecida. Se nenhuma URL for fornecida, então será utilizada a URL da página inicial do DCI DEPARTAMENTO DE CIÊNCIA DA INFORMAÇÃO da UFS.

## Qual o público alvo?  
_Descreva quais os usuários em potencial para sua aplicação web_

> Qualquer pessoa.

## Qual a arquitetura?  
_Descreva quais os módulos de hardware, software e protocolos necessários para sua aplicação, restringindo-se às características dos protocolos da camada de aplicação_

> Python 3.7. Módulos bs4 e requests.

## Qual o formato do protocolo?
_Especifique o que um programador precisa saber para implementar seu protocolo em qualquer linguagem_

> Tem que ler o código, saber programar e ter conhecimentos sobre o protocolo HTTP.

### Como as mensagens são definidas?
_Especifique mensagens enviadas pelo cliente e respostas do servidor_

> O cliente não envia nenhuma mensagem. Mas, o servidor poder retornar uma página de erro em html ou uma página informando que entendeu a requisição, em html.

### Quais os campos definidos?
_campos devem seguir padrão NOME_DO_CAMPO: VALORES_ 

> DATE: %a, %d %b %Y %H:%M:%S %Z

> SERVER: SERVER

> CONTENT-LENGTH: [0-9]+

> CONTENT-TYPE: TEXT/HTML

> CONTENT-TYPE: TEXT/PLAIN

> HOST: UFS.CLIENT.BR

> ACCEPT-LANGUAGE: *

> URL-FIELD: <URL>

### Quais os possíveis valores de cada campo?
> Respondido acima.

## Como a aplicação pode ser testada no Core?

_Descreva como o servidor pode ser implantado e testado, apresentando um manual de uso_ 
> Não pode. Não pude utilizar o gerenciador pip, nem atualizar outros pacotes contidos na máquia virtual e a instalação manual dos módulos com suas dependências era inviável.

## Faça um registro do funcionamento de sua aplicação 
_Apresente um exemplo de teste mostrando que o cliente e o servior  HTTP Tupi funcionou corretamente_
> ![alt text](https://github.com/DCOMP-UFS/20211-lab-t1-igor-primo2/blob/main/1.png?raw=true)
> ![alt text](https://github.com/DCOMP-UFS/20211-lab-t1-igor-primo2/blob/main/2.png?raw=true)
> ![alt text](https://github.com/DCOMP-UFS/20211-lab-t1-igor-primo2/blob/main/3.png?raw=true)
> ![alt text](https://github.com/DCOMP-UFS/20211-lab-t1-igor-primo2/blob/main/4.png?raw=true)
> ![alt text](https://github.com/DCOMP-UFS/20211-lab-t1-igor-primo2/blob/main/5.png?raw=true)
