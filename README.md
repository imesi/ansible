# ansible
Playbooks de ansible. Os roles utilizados nos playbooks estão disponíveis em: [ansible-roles](https://github.com/wgnann/ansible-roles).

A proposta dos playbooks é abrigar todos os roles que a classe de máquinas deve assumir. Não pretendemos, nesse momento, garantir muita reusabilidade de código, pois o escopo é pequeno.

## organização
Os playbooks são divididos entre Linux e Windows. Os playbooks de Windows têm o prefixo `win_`.

### linux
Para usar os playbooks de Linux é necessário que a máquina de destino esteja acessível via SSH. Geralmente é suficiente configurar chaves de SSH numa instalação nova.

Os playbooks:
  - `linux.yml`: playbook que compreende todos os casos gerais (e.g. máquinas na nuvem, servidores etc);
  - `classroom.yml`: salas de aula;
  - `lab.yml`: laboratório;
  - `staff.yml`: as raras máquinas de funcionário que usam Linux.

### windows
Aqui já é necessário instalar o WinRM antes de qualquer coisa. Depois recomendamos usar o playbook `win_ansible.yml` para configurar um usuário para o ansible usar nos outros playbooks.

Eis os playbooks:
  - `win_base.yml`: caso geral;
  - `win_classroom.yml`: salas de aula.
