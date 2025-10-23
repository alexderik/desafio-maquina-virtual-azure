# Desafio DIO: Criação e Documentação de Máquina Virtual (VM) no Azure

Este projeto faz parte do Desafio de Projeto da Digital Innovation One (DIO) e tem como objetivo principal consolidar os conhecimentos na criação e gerenciamento de Máquinas Virtuais (VMs) na plataforma Microsoft Azure, além de praticar a documentação técnica usando o GitHub e a formatação Markdown.

---

## 1. Visão Geral do Projeto

| Configuração | Detalhe |
| :--- | :--- |
| **Plataforma Cloud** | Azure |
| **Sistema Operacional** | **Windows Server 2019 Datacenter** |
| **Objetivo** | Aplicar conceitos de IaaS (Infrastructure as a Service) e documentar o processo. |
| **Ferramentas de Documentação** | GitHub, Markdown, Capturas de Tela. |

---

## 2. Processo de Criação da VM no Azure
 
A Máquina Virtual (VM) foi criada seguindo a documentação oficial da Microsoft e as instruções fornecidas nas aulas da DIO. Abaixo estão os detalhes das configurações principais:

### 2.1. Configurações de Localização e Recursos

| Configuração | Detalhe Utilizado | Importância |
| :--- | :--- | :--- |
| **Grupo de Recursos** | `RG-MaquinaVirtual-DIO` | Utilizado para agrupar, organizar e gerenciar o ciclo de vida (custo/exclusão) de todos os recursos da VM. |
| **Região (Local)** | `Korea Central` | Localização física do datacenter que hospeda a VM. |
| **Zona de Disponibilidade** | `Zona 1` | Garante alta disponibilidade ao isolar a VM contra falhas de hardware ou software. |
| **Sistema Operacional (Imagem)** | **Windows Server 2019 Datacenter** | Imagem selecionada para definir o ambiente de trabalho da VM. |
| **Nome da VM** | `vm-dio-lab` | Nome do recurso principal da máquina virtual. |

### 2.2. Configurações de Rede e Acesso (Segurança)

Para permitir a conexão remota ao Windows Server 2019, foi necessário configurar o acesso de entrada:

| Recurso | Detalhe | Função |
| :--- | :--- | :--- |
| **Recurso de Rede** | Grupo de Segurança de Rede (NSG) | Atua como um firewall, filtrando o tráfego de rede para a VM. |
| **Porta de Acesso Aberta** | **3389** (RDP) | Porta padrão do serviço de Área de Trabalho Remota (Remote Desktop Protocol). |
| **IP Público** | `20.39.186.42` | Endereço IP roteável pela internet para permitir a conexão externa via RDP. |

---

## 3. Evidências do Processo

As capturas de tela relevantes para documentar o processo de implantação e a VM em execução foram salvas na pasta `/images`.

* [Visão Geral da Implantação Concluída (Deployment)](images/visao_geral.png)
* [Detalhe da VM em Execução (Local, IP e Configurações)](images/vm_detalhes_parte_1.png) 
* [Configurações de Disponibilidade e Segurança Adicionais](images/vm_detalhes_parte_2.png) 

---

## 4. Conclusão e Aprendizados

Com este desafio, o conhecimento sobre a infraestrutura como serviço (IaaS) do Azure foi consolidado, destacando-se:

1.  **Gerenciamento de Recursos:** A importância de utilizar Grupos de Recursos para organizar e controlar o ambiente de nuvem.
2.  **Disponibilidade:** A função da Zona de Disponibilidade para aumentar a resiliência da aplicação.
3.  **Segurança de Rede:** O papel fundamental do NSG na proteção da VM, permitindo apenas o tráfego essencial (porta RDP 3389).

---

## 5. Recursos Úteis

* [Página Principal de Máquinas Virtuais do Azure (Microsoft Learn)](https://learn.microsoft.com/pt-br/azure/virtual-machines/)
* [Início Rápido: Criar uma máquina virtual do Windows no Portal do Azure](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal)
* [Meu Repositório GitHub](https://github.com/alexderik/desafio-maquina-virtual-azure)
