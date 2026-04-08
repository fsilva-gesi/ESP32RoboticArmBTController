
Controlo de Braço Robótico via Bluetooth

Este projeto foi concebido para permitir a manipulação precisa de um braço robótico articulado através de uma ligação sem fios.

O ecossistema baseia-se na comunicação entre um dispositivo móvel (Telemóvel Android) e um microcontrolador ESP32.

1. Arquitetura do Sistema

  - Front-end (Aplicação): Interface gráfica que converte as interações do utilizador em comandos de dados.

  - Back-end (Firmware ESP32): Código carregado no microcontrolador que recebe as Strings de dados via Bluetooth clássico, processando-as para gerar sinais PWM (Pulse With Modulation) que movem os servomotores.

2. Funcionalidades principais.

  - Controlo multi-eixo: Deslizadores (sliders) dedicados para controlar individualmente cada articulação do braço (Base, Ombro, Cotovelo e Garra).

3. Fluxo de Operação

O funcionamento segue uma lógica de baixa latência para garantir uma resposta imediata:

  - Emparelhamento: O utilizador liga o Bluetooth e conecta-se ao endereço MAC do ESP32.

  - Transmissão: Ao mover um slider na App (Ex: Garra), a aplicação envia um pacote de dados (Ex: G120, indicando que o servo da garra deve ir para a posição 120).

  - Execução: O ESP32 descodifica o pacote e ajusta o ângulo do servo correspondente instantaneamente.


[Instalar] (https://fsilva-gesi.github.io/ESP32RoboticArmBTController/flash.html)
fsilva-gesi.github.io/ESP32RoboticArmBTController/flash.html


