# Análise Experimental de Efeitos de Envelhecimento em Controladores SDN

## 📄 Sobre o Projeto
O objetivo deste trabalho é realizar um estudo experimental para investigar os efeitos de **Envelhecimento** em controladores de Redes Definidas por Software (SDN). O estudo consiste em submeter um controlador SDN a uma carga de trabalho contínua e prolongada para observar e medir a degradação de desempenho e o consumo de recursos de redes e do sistema ao longo do tempo.

## 🎯 Objetivo
O objetivo principal é analisar se o software de um controlador SDN exibe sinais de envelhecimento, como vazamento de memória, aumento do uso de CPU e tráfego de rede, quando exposto a uma alta e constante taxa de criação e remoção de fluxos de rede.

## 🛠️ Ferramental Utilizado
Para a realização deste estudo, foram utilizadas as seguintes ferramentas:

* **Mininet:** Simulador utilizado para criar topologias de rede virtuais com hosts, switches OpenFlow e controladores, permitindo a emulação de uma Rede Definida por Software.
* **Controlador SDN (ex: Ryu/POX):** O software central da rede, responsável por gerenciar as regras de fluxo nos switches. É o alvo do nosso estudo de envelhecimento.
* **Wireshark:** Ferramenta para captura e análise de pacotes, utilizada para validar o tráfego e o funcionamento dos protocolos na rede simulada.
* **Scripts (Python/Bash):** Scripts customizados para automatizar a geração de tráfego na rede e para monitorar o consumo de recursos (memória e CPU) do processo do controlador em intervalos regulares.

## 🔬 Cenários e Estudo de Caso
O experimento foi conduzido da seguinte forma:

1.  **Configuração:** Uma topologia de rede foi criada no Mininet e conectada a um controlador SDN externo.
2.  **Geração de Carga:** Um script foi executado para gerar tráfego de forma contínua e aleatória entre os hosts da rede simulada. Esse processo força o controlador a processar um grande volume de mensagens `Packet-In` e a instalar novas regras de fluxo constantemente.
3.  **Monitoramento:** Durante a execução do experimento, um segundo script coletou dados de uso de memória RAM e CPU do processo do controlador em intervalos periódicos.
4.  **Análise:** Os dados coletados foram compilados e utilizados para gerar gráficos que demonstram a evolução do consumo de recursos ao longo do tempo, permitindo identificar tendências que caracterizam o *software aging*.

## 📈 Resultados
Os resultados detalhados, incluindo os gráficos de consumo de recursos e a análise conclusiva sobre os efeitos de envelhecimento observados, estão consolidados no relatório do projeto.
