﻿
## Vagrant - Provisionando VMs para testes ou desenvolvimento

Será criado de forma rápida e objetiva, com poucos comandos, um conjunto de VMs que poderá servir de base para testes, como cluster ou desenvolvimento de algo.

Inclusive é possível definir uma série de configurações e já subi-las no momento da criação das VMs. Assim quando se acessar as VMs, elas já estarão configuradas e prontas para uso, conforme a necessidade.

No exemplo a seguir será criado 3 VMs no VirtualBox, que terão as seguintes identificações:

| Hostname   | IP       |
| :---------- | :--------- |
| vm1 | 192.168.56.150 |
| vm2 | 192.168.56.151 |
| vm3 | 192.168.56.152 |

Tudo que for implementado ou criado na pasta raiz desse tutorial, já ficará disponível dentro do diretório da VM em:

**/home/vagrant/projeto**

### Observação

Vagrant só é recomendado para ambientes de testes e desenvolvimento, conforme pode ser visto no link abaixo.

https://developer.hashicorp.com/vagrant/intro/vs/terraform

### Versões de softwares utilizados nesse tutorial

SO Windows 11, Vagrant 2.3.3 e VirtualBox 7.0.6

### Requisitos mínimos

Ter em seu SO os seguintes softwares.
Abaixo de cada um segue o link para download.

- VirtualBox (Software de virtualização)

  https://www.virtualbox.org/wiki/Downloads

- Vagrant (Software para configurar ambientes)

  https://developer.hashicorp.com/vagrant/downloads

- Putty (Software de cliente remoto)

  https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html

- Vagrant - plugin vbguest, via linha de comando, execute:

  vagrant plugin install vagrant-vbguest

### Siga as etapas

#### Observação

Antes de executar os passos abaixo, instale o plugin vagrant-vbguest no host, para habilitar o compartilhamento de pasta entre HOST e VMs.

**vagrant plugin install vagrant-vbguest**

![App Screenshot](images/img0.png)

1 - Crie uma pasta com nome de sua preferência em qualquer lugar do seu SO. No meu caso vou chama lá de **projeto**.

2 - Entre na pasta **projeto** e dentro dela crie um arquivo chamado **Vagrantfile**, apenas o nome sem extensão, adicione o seguinte conteúdo e salve.

![App Screenshot](images/img1.png)

https://github.com/tiagotsc/vagrant-basico_vms/blob/fe57b6b656a125c59b3dcb774271aac53b3f87be/Vagrantfile#L1-L66

3 - Ainda dentro da pasta **projetos**, vamos subir nossas VMs, via linha de comando, execute:

```bash
# Liga ou cria as VMs, caso ainda não existam
vagrant up
```

![App Screenshot](images/img2.png)

O processo demora um pouco e todos os passos que são executados podem ser acompanhados em tempo real via linha de comando.

![App Screenshot](images/img3.png)

Vms disponibilizadas no VirtualBox e já em execução.

![App Screenshot](images/img4.png)

4 - Quando todo o processo terminar, abra o putty e forneça o IP de umas das VMs, no exemplo, vou acessar a VM1:

**IP:** 192.168.56.150

**Usuário:** root ou vagrant

**Senha:** vagrant

![App Screenshot](images/img5.png)

Logado com sucesso. VM pronta para uso!

![App Screenshot](images/img6.png)

O mesmo pode ser feito nas outras VMs, caso queira acessá-las.

### Alguns comandos úteis

Via linha de comando, é preciso estar na pasta "**projeto**", pasta aonde está o Vagrantfile,  para executar os comando.

```bash
# Desliga VMs
vagrant up

# Reiniciar VMs
vagrant reload

# Destruir VMs
vagrant destroy
```

#### Documentação oficial do Vagrant

https://developer.hashicorp.com/vagrant/docs

## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/tiago-s-costa)
