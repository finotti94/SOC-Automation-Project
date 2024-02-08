# SOC-Automation-Project
Configurando e subindo uma Home Lab para um projeto de Automação de SOC (Security Operations Center), baseado no projeto original "SOC Automation Project (Home Lab)" por MyDFIR (https://www.youtube.com/@MyDFIR).

## Ferramentas Usadas

[Wazuh](https://wazuh.com)

[TheHive](https://thehive-project.org)

[Shuffle](https://shuffler.io)

[VirtualBox](https://www.virtualbox.org)

## Demonstração e Funcionamento

![fluxograma copy 2](https://github.com/finotti94/SOC-Automation-Project/assets/7770279/89918e45-a188-4dca-adce-ddda07162024)

Serão criadas 4 máquinas virtuais, cada uma com uma função específica:

Máquina Virtual #1: Windows 10 (com o agente do Wazuh)

Máquina Virtual #2: Gerente do Wazuh

Máquina Virtual #3: Shuffle

Máquina Virtual #4: TheHive

![explicacao](https://github.com/finotti94/SOC-Automation-Project/assets/7770279/3d9ced65-fb53-47cd-a535-addb52bb08db)

Fluxograma:

- Máquina Windows 10 enviará eventos para o Gerente Wazuh;
- Gerente Wazuh receberá os eventos, criará alertas e os enviará direto para o Shuffle;
- O Shuffle, por sua vez, atuará como um OSINT (Open-Source Intelligence) para enriquecer o nosso IOC (Indicator of Compromise);
- Assim que obtido informações da Internet, o Shuffle enviará alertas para o TheHive e irá disparar um e-mail para o analista SOC;
- O analista SOC receberá o e-mail com o evento, respondendo com a tomada de decisão escolhida por ele, assim, dependendo da resposta, a ação será enviada para o Shuffle, depois para o Wazuh, e finalmente chegando ao cliente Windows, onde será executada a tomada de decisão
