# ansible-webserver
Configuração de apache, php e mysql em distribuições Debian, Ubutnu, CentOS e RedHat

## Configurações:
- Adicionar no arquivo /etc/ansible/hosts
> #Grupo de hosts
> [grupoA] 

> #ip's exemplo:
> 192.168.1.1
> 192.168.1.2

- Alterar no arquivo /etc/ansible/palybooks/webserver.yml
> - hosts: nome_do_host
> para
> - hosts: grupoA

-Não esqueça de alterar para sua senha
> command:  mysql -u root --execute="UPDATE mysql.user SET authentication_string = PASSWORD('senha') WHERE User = 'root' AND Host = 'localhost';"
