# SOC-Automation-Project
Configurando e subindo uma Home Lab para um projeto de Automação de SOC (Security Operations Center), baseado no projeto original "SOC Automation Project (Home Lab)" por MyDFIR (https://www.youtube.com/@MyDFIR).

## Ferramentas Usadas

[Wazuh](https://wazuh.com)

[TheHive](https://thehive-project.org)

[Shuffle](https://shuffler.io)

[VirtualBox](https://www.virtualbox.org)

## Demonstração e Funcionamento

![fluxograma copy](https://github.com/finotti94/SOC-Automation-Project/assets/7770279/5460545a-d906-4726-82ad-c1c5a8e22627)

Serão criadas 4 máquinas virtuais, cada uma com uma função específica:

Máquina Virtual #1: TheHive

Máquina Virtual #2: Gerente Wazuh

Máquina Virtual #3: Shuffle

Máquina Virtual #4: Windows 10 (com o agente do Wazuh)

![explicacao](https://github.com/finotti94/SOC-Automation-Project/assets/7770279/3d9ced65-fb53-47cd-a535-addb52bb08db)

Fluxograma:

VM#4 irá enviar eventos para a VM#2
VM#2 recebrá eventos, criará um alerta e enviará para a VM#3
