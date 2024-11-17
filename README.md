# # READ ME

# # DESCRIÇÃO DO PROJETO

Este projeto foi desenvolvido para monitorar a presença de fumaça em um ambiente e emitir alertas em tempo real tanto localmente quanto remotamente. Ele utiliza um sensor de fumaça conectado a um ESP32, que lê os valores analógicos do sensor e os processa para determinar a existência de fumaça. Um buzzer é acionado para emitir um alerta sonoro enquanto a fumaça é detectada, e uma mensagem informativa é enviada ao broker MQTT para notificar sobre o estado do ambiente.

O ESP32 conecta-se à internet via Wi-Fi e utiliza o protocolo MQTT para comunicação com o broker, permitindo que as informações coletadas sejam acessadas por outros dispositivos conectados. As mensagens publicadas indicam o status do ambiente, como "Fumaça detectada" ou "Sem fumaça", e são enviadas para o tópico configurado no broker. Este sistema garante monitoramento em tempo real e pode ser integrado com aplicativos de automação ou painéis de controle.

O projeto é fácil de reproduzir, ideal para aplicações em residências, escritórios ou pequenos negócios, onde a detecção de fumaça pode ser crítica para a segurança. Além disso, ele é modular, podendo ser expandido para incluir outros sensores ou dispositivos de alerta, como notificações por celular ou integração com sistemas de sprinklers. O uso do protocolo MQTT possibilita escalabilidade e flexibilidade na comunicação entre dispositivos, tornando este projeto uma solução eficiente e adaptável para diversas necessidades.

# # HARDOWARE UTILIZADOS E SUAS FUNÇÕES

**ESP32:** Processamento dos dados do sensor e comunicação com o broker MQTT;

**Sensor de Fumaça (MQ-2 ou similar):** Detecta a presença de fumaça no ambiente;

**Buzzer:** Emite alerta sonoro quando a fumaça é detectada;

**Protoboard e Fios Jumper:** Conectam os componentes entre si e ao ESP32;

**Fonte de Alimentação (5V):** Fornece energia para o ESP32 e os componentes conectados;


# # Passo a Passo para Executar o Projeto

Configuração do Ambiente:

Instale a Arduino IDE e adicione o suporte para ESP32.
Instale as bibliotecas PubSubClient e WiFi.
Montagem do Hardware:

Conecte o sensor de fumaça (MQ-2) e o buzzer ao ESP32.
Configuração do Código:

No código, configure o Wi-Fi e o broker MQTT (Mosquitto).
Defina o tópico MQTT e o limiar para ativação do buzzer.
Execução:

Faça o upload do código para o ESP32.
O ESP32 se conectará ao broker MQTT e ativará o buzzer ao detectar fumaça.
Monitoramento:

Use o MQTTBox para visualizar as mensagens enviadas pelo ESP32 em tempo real.
