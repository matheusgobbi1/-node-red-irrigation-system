# **Node-RED Irrigation System**

## **Objetivo do Projeto**
Este projeto tem como objetivo oferecer uma **solução inteligente** para sistemas de irrigação agrícola utilizando **Node-RED**. A proposta é integrar dados em tempo real de sensores e APIs climáticas para otimizar o uso de recursos naturais, como água, promovendo uma **agricultura sustentável e eficiente**.

---

## **Como Funciona**

### **Coleta de Dados**
- **Dados são obtidos de:**
  - **Sensores de Umidade do Solo:** Monitoram o nível de umidade do solo em tempo real.
  - **API OpenWeather:** Fornece informações climáticas, como temperatura, umidade e probabilidade de chuva.

### **Processamento de Dados**
- Os dados coletados são processados em um fluxo no **Node-RED**.
- **Regras inteligentes** definem se o sistema de irrigação deve ser ligado ou desligado com base nos seguintes critérios:
  - Solo com umidade abaixo de **20%** ativa o sistema.
  - Previsão de chuva acima de **70%** ou solo com umidade acima de **60%** desativa o sistema.
  - Temperatura elevada e baixa umidade atmosférica também influenciam na decisão.

### **Automação**
- O comando final (**"ligar"** ou **"desligar"**) é enviado ao dispositivo responsável pela irrigação, como uma bomba de água conectada via **MQTT**.

---
## **Tecnologias Utilizadas**

- **Node-RED**  
  Ferramenta para criação de fluxos baseados em eventos e IoT.

- **MQTT**  
  Protocolo de comunicação para enviar comandos ao dispositivo de irrigação.

- **OpenWeather API**  
  Para dados climáticos em tempo real.

- **Sensor de Umidade do Solo**  
  Fornece dados locais sobre a umidade do solo.

- **Node.js**  
  Necessário para rodar o Node-RED.

---

## **Principais Componentes**

- **flows.json**  
  Arquivo contendo os fluxos do **Node-RED**.

- **Sensores**  
  Integração com dispositivos de IoT (umidade do solo, entre outros).

- **Conexão com APIs**  
  Configurada para acessar informações meteorológicas em tempo real.

- **Dashboard**  
  Visualização de dados e controle manual (se aplicável).
