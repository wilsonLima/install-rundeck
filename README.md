install-rundeck
=========

Role do Ansible para instalação de um servidor Rundeck.

Distribuições Suportadas pela Role
------------

- RedHat ou CentOS

Variáveis da Role 
--------------

- rundeck_port: Valor da porta a ser utilizada pelo serviço do Rundeck. o valor padrão é 4440.


Example Playbook
----------------

Exemplo de uso da Role, com as configurações padrão:

    - hosts: servers
      roles:
         - install-rundeck

Exemplo de uso da Role passando o número da porta por uma variável:

    - hosts: servers
      roles:
         - { role: install-rundeck, rundeck_port: 4440 }

License
-------

BSD
