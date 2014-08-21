# Ansible Hello World - TDC 2014

Este é um exemplo simples de como automatizar a instalação de um servidor web Nginx utilizando o Ansible.

## Requisitos

Para utilizar este projeto você precisará do seguinte stack:

- Vagrant: simplifica a utilização do `Virtualbox` e do provisionamento com o Ansible
- Virtualbox: software que permite a criação de máquinas virtuais
- Ansible: ferramenta para automação

## O projeto

O projeto consiste dos seguintes arquivos:

- `example.com.j2` - Virtual Server do Nginx, no formato de template exigido pelo Ansible `jinja2`.
- `index.html` - Hello World
- `playbook.yml` - Contém o playbook, arquivo que descreve o estado a ser atingido
- `Vagrantfile` - Define configurações a serem utilizadas pelo [Vagrant](http://vagrantup.com)

## Como utilizar
Instale o Ansible (tanto o Vagrant como o Virtualbox podem ser obtidos nos respectivos websites dos projetos, ou via `homebrew-cask` se você utiliza o OSX :] )

    pip install ansible

Iniciar a VM:

    vagrant up

Você deverá colocar então sua senha para que a última tarefa do playbook seja executada (adição de entrada no /etc/hosts)
