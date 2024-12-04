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
