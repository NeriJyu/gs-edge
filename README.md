# 💧 Solução IoT para Monitoramento de Enchentes

---

## Url do Projeto
- [Wokwi](https://wokwi.com/projects/432408126780728321)
- [Vídeo Explicativo](https://youtu.be/tdp-419xu-c)

---

## 🌍 Problema Abordado

O Brasil registra milhares de eventos climáticos extremos todos os anos. Um dos mais graves é a enchente urbana, que impacta diretamente a vida de milhares de pessoas com alagamentos repentinos, perdas materiais, interrupção de serviços e até vítimas fatais.
Muitas comunidades não recebem alertas em tempo real, o que agrava a situação e dificulta a prevenção.

---

## 🚀 Visão Geral da Solução

Este projeto apresenta uma solução de baixo custo baseada em IoT, capaz de:
- Monitorar o nível da água em tempo real.
- Exibir os dados em um dashboard visual.
- Enviar alertas automáticos quando há risco de alagamento.
- O led acende no local para avisar pessoas próximas

---

## 🧱 Arquitetura da Solução

A solução foi estruturada em três camadas principais, garantindo comunicação eficiente entre sensores, rede e visualização dos dados em tempo real:
1. 🌊 Camada de Dispositivos (IoT)
- ESP32
- Sensor ultrassônico
- Sensor DHT
- LED
- Protocolo de Comunicação: MQTT
2. 📡 Camada de Conectividade e Processamento
- Wi-Fi (Wokwi Guest): Conecta o ESP32 à internet durante a simulação.
- Broker MQTT (Mosquitto - test.mosquitto.org): Intermediador que recebe e distribui mensagens publicadas pelo ESP32.
3. 📊 Camada de Visualização e Ação
- Recebe os dados MQTT em tempo real.
- Exibe no dashboard os valores de temperatura, umidade e nível da água.
- Envia alertas visuais (ex: mudança de cor ou mensagem de risco).

---

## ⚙️ Tecnologias Utilizadas

- 💻 ESP32 (simulado via Wokwi)
- 🌡️ Sensor ultrassônico (nível de água)
- 🌦️ Sensor DHT (temperatura e umidade)
- 💡 LED
- 🔄 Protocolo MQTT
- 🧠 Node-RED ou HiveMQ Web Client (para visualização dos dados)

---

## 🚀 Simulação no Wokwi
1. Acesse e execute o projeto no 👉 [Wokwi](https://wokwi.com/projects/432408126780728321)
2. O ESP32 lê os dados do sensor DHT22 e publica via MQTT nos tópicos:
- `vitalcare/geral` (com temperatura, umidade e nível da água)
- `vitalcare/alerta` (quando o nível de água for < 10 cm)
3. Broker utilizado:
- Host: `test.mosquitto.org`
- Porta: `1883`

---

## 📡 Visualizar os dados com Node-RED
- Importe o fluxo flow.json no seu Node-RED local.
- Conecte ao broker MQTT.
- Veja os dados no painel: nível da água, temperatura, umidade e alertas.

---

## 📡 Visualizar os dados com HiveMQ Web Client
1. Acesse: [HiveMQ WebSocket Client](https://www.hivemq.com/demos/websocket-client/)
2. Preencha:

| Campo     | Valor                |
| --------- | -------------------- |
| Host      | `test.mosquitto.org` |
| Port      | `8081`               |
| Use SSL   | Assinale             |
| Client ID | Qualquer nome        |

3. Clique em Connect
4. Em Subscription, digite:
- `vitalcare/geral`
- `vitalcare/alerta`
5. Clique em Messages para visualizar os dados em tempo real.

---

## 🧑‍💻 Equipe
- Diogo Cecchini Bueno       RM 560427
- Gustavo Neri Santos        RM 560239
- Gustavo Pandolfo Meroni    RM 560271
