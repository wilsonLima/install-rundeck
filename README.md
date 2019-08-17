install-rundeck
=========

Role do Ansible para instalação de um servidor Rundeck (com OpenJDK 8).

Distribuições Suportadas pela Role
------------

- RedHat ou CentOS


Tags da Role 
--------------

- main: Tag a ser utilizada em conjunto com outras tags, se alguma tag for especificada no comando.
- deps: Instala as dependências do Rundeck.
- repo: Insere o repositório do Rundeck.
- rundeck: Realiza a instalação do pacote do Rundeck.
- config: Realiza a configuração de pós instalação do Rundeck.


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

Exemplo de Comandos
----------------

Comando para executar todas as tasks:

    ansible-playbook -i <caminho_inventario> <caminho_playbook>

Comando para executar a tag "config" (em caso de uso de tags, a tag "main" é obrigatória):

    ansible-playbook -i <caminho_inventario> <caminho_playbook> --tags "main, config"
