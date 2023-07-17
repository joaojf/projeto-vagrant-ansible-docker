# Projeto Vagrant Ansible Docker Nginx

O objetivo deste projeto é fornecer uma maneira fácil e automatizada de criar uma máquina virtual usando o Vagrant, configurar o provisionamento com o Ansible e criar roles para instalação e configuração do Docker. Além disso, a role do Docker inclui a criação de um container Nginx e a execução do mesmo na porta 8080.

## Pré-requisitos

Antes de começar, certifique-se de que o seguinte software esteja instalado em seu sistema:

- [Vagrant](https://www.vagrantup.com/downloads)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)

## Configuração

1. Clone o repositório do projeto para o seu ambiente local:

   ```shell
   git clone https://github.com/joaojf/projeto-vagrant-ansible-docker.git

2. Acesse o diretório do projeto:
   ```shell
   cd projeto-vagrant-ansible-docker

3. Execute o comando `vagrant up` para iniciar a máquina virtual e a configuração do ansiblex:
   ```shell
   vagrant up
   ```
   Após a criação da máquina, o provisionamento com o Ansible será automaticamente executado.
4. Após a criação da máquina você pode acessa-lá usando `vagrant ssh`.
5. Alterar o user para root `sudo su` e colocar a senha desejada para o usuário criado durante o provisionamento:
  ```shell
   passwd sysadm
  ```
7. Após a conclusão do provisionamento, você pode listar o container em execução:
   ```shell
   docker ps
   ```
8. Após a conclusão do provisionamento, você pode acessar o container Nginx em `http://localhost:8080`:
   ```shell
   curl localhost:8080
   ```
   - Pode fazer pelo navegador também acessando `htt://localhost:8080` para ver a página welcome do nginx.

## Notas

- Verifique se possui uma conexão de rede adequada para acessar o Nginx no navegador.
- Você pode modificar a configuração do Nginx editando o arquivo de configuração dentro do container.

## Contribuição
Contribuições são bem-vindas! Se você encontrar algum problema ou tiver sugestões para melhorar este projeto, sinta-se à vontade para abrir uma issue ou enviar um pull request.
