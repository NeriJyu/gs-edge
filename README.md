# 💧 Solução IoT para Monitoramento de Enchentes

## Url do Projeto
- [Wokwi](https://wokwi.com/projects/432408126780728321)
- [Vídeo Explicativo](https://www.youtube.com/watch?v=c-JunqTGOkQ)

## 🌍 Problema Abordado

O Brasil registra milhares de eventos climáticos extremos todos os anos. Um dos mais graves é a enchente urbana, que impacta diretamente a vida de milhares de pessoas com alagamentos repentinos, perdas materiais, interrupção de serviços e até vítimas fatais.
Muitas comunidades não recebem alertas em tempo real, o que agrava a situação e dificulta a prevenção.

## 🚀 Visão Geral da Solução

Este projeto apresenta uma solução de baixo custo baseada em IoT, capaz de:
- Monitorar o nível da água em tempo real.
- Exibir os dados em um dashboard visual.
- Enviar alertas automáticos quando há risco de alagamento.

A arquitetura envolve sensores conectados a um ESP32, que envia os dados via MQTT para um sistema em Node-RED. A visualização é feita em tempo real com gauges e alertas.

## ⚙️ Tecnologias Utilizadas

- 💻 ESP32 (simulado via Wokwi)
- 🌡️ Sensor ultrassônico (nível de água)
- 🌦️ Sensor DHT (temperatura e umidade)
- 🔄 Protocolo MQTT
- 🧠 Node-RED (dashboard e lógica de alerta)

## 🛠️ Instruções para Execução e Simulação
1. Acesse e execute o projeto no [Wokwi](https://wokwi.com/projects/432408126780728321)
2. Simule o sensor
- Aumente/diminua a altura da água simulada (sensor ultrassônico).
- O valor será enviado automaticamente ao Node-RED via MQTT.
3. Configure o Node-RED
- Importe o fluxo flow.json no seu Node-RED local.
- Conecte ao broker MQTT.
- Veja os dados no painel: nível da água, temperatura, umidade e alertas.

## 🧑‍💻 Equipe
- Diogo Cecchini Bueno       RM 560427
- Gustavo Neri Santos        RM 560239
- Gustavo Pandolfo Meroni    RM 560271
