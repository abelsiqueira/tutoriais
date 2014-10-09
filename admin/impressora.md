# Impressora

A marca e modelo da impressora atual é Samsung SL-C460FW.

## Wireless

A impressora atual está conectada na rede wireless, e no servidor.
O endereço dela no wireless é 192.168.1.100, mas não deve ser necessário
utilizar.

## Servidor

Instale o samba e o cups.

Copie os arquivos de configuração em `etc/samba` e `etc/cups`.

Acesse http://143.106.118.132:631/ e adicione a impressora.

## Usuários

A impressora deve ser buscada por ipp no endereço

ipp://143.106.118.132:631/printers/samsung-lpoo

## Usuários - CLI - Antigo

Primeiro adicione o endereço de IP da impressora em `/etc/cups/client.conf` ou
`~/.cups/client.conf`:

~~~
ServerName 143.106.118.132:631
~~~

Talvez você precise reiniciar o CUPS.

Para listar as impressoras:

~~~
$ lpstat -p -d
~~~

Para imprimir:

~~~
$ lp filename
~~~

Para adicionar a impressora padrão:

~~~
$ lpoptions -d nome-da-impressora
~~~
