# EmbarcaTechProjetoFinal
Projeto final do programa de capacitação EmbarcaTech - TIC 37 - Fase 1

# Vídeo Demonstração

https://youtu.be/mjIRMKBfFYA

# Hardware/Firmware

Projeto desenvolvido em uma placa de desenvolvimento BitDogLab, versão 6.3.<br>
Desenvolvimento de firmware feito através do PicoSDK, versão 2.1.0, com a IDE Visual Studio Code.

# Instruções

O projeto simula um sistema de sensores em um veículo.<br><br>

<h3>Sensor de proximidade(Eixo X)<h3>

O joystick, no eixo X, demonstra a entrada de dados de um sensor de proximidade. Quanto mais distante do ponto central, mais próximo de "bater" em algo.<br>
Isso é representado no Dysplay OLED com uma barra se movendo, simulando o sensor, em direção a um objeto na extremidade oposta. Além disso, é utilizado o LED vermelho
para indicar essa aproximação.<br>
Juntamente a um sinal sonoro emitido pelos Buzzers presentes na placa, o LED pisca de forma mais rápida de acordo a proximidade com o objeto de colisão.<br>

<h3>Sensor de temperatura(Eixo Y)<h3>

O joystick, no eixo Y, simula os dados recebidos por um sensor térmico que poderia estar localizado em um motor, por exemplo.<br>
No ponto central do Joystick é feita a "leitura" de uma temperatura em torno de 100°C, um valor comum para um motor de carro. Movendo o Joystick para baixo pode-se chegar até o valor de 0°C, e para cima o valor pode chegar a 200°C.<br>
Esse valor é enviado através da UART, com a possibilidade de ser lido em um monitor serial.<br>
Caso se aperte o Botão A da placa o valor alterna entre sua representação em graus Celsius e graus Fahrenheit. O indicativo de qual está sendo utilizado no momento é feito na matriz de LEDs presentes na placa, onde se escreve °C ou °F. Além disso, a grandeza é descrita no corpo da mensagem obtida por serial.