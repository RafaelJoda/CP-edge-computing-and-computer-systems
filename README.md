# 📘 Monitoramento de Temperatura e Luminosidade - ESP32
 
# 🚀Integrantes:
🔹Rafael Joda - RM561939
🔹Luis Miguel Gonçalves - RM561232
 
## 🔹 Visão Geral
Este projeto é uma **prova de conceito (PoC)** que monitora **temperatura e luminosidade** utilizando um **ESP32 DOIT DEVKIT V1**.  
O protótipo foi desenvolvido em duas etapas:  
1. **Simulação no Wokwi** com sensor **DHT22** e **LDR**.  
2. **Montagem física** com sensor **DHT11** e **LDR**.  
 
Os dados são enviados por **ThingSpeak**.
 
---

Codigo ino
 [cp_arduino-1.zip](https://github.com/user-attachments/files/22128297/cp_arduino-1.zip)

## 🚀 Parte 1 – Simulação no Wokwi (DHT22 + LDR)

Foto 
 
🔗 [Link Wokwi](https://wokwi.com/projects/441026358521815041))  
 
![Image](https://github.com/user-attachments/assets/5dd41ecc-9536-449d-9d99-bc8119405094) 

🔗 [Thingspeak Channel]((https://thingspeak.mathworks.com/channels/3058720))

🔗 [Youtube](https://youtu.be/AKgNLOY8nAw?si=oMOQDENU1Ub3mvqR)  


   
 
### 🔌 Hardware virtual
- ESP32 DOIT DEVKIT V1  
- Sensor **DHT22** (temperatura e umidade)  
- Módulo **LDR com resistor** (luminosidade)
  #
### ⁉️ Como funciona:
#Após rodar o código, o sistema captará temperatura, umidade e pressão, enviando assim os dados obtidos para um Dashboard no Thingspeak. Desta forma, **os dados serão expostos em tempo real.**
 
# 🔌 Parte 2 – Conectando o ESP32 ao Computador e Usando com o ThingSpeak
 
Agora que o circuito físico já está montado (ESP32 + DHT11 + LDR com resistor embutido), vamos conectar o ESP32 no computador e visualizar os dados no **ThingSpeak**.
 
---
 
## 1️⃣ Conectando o ESP32 no computador
 
1. Pegue um **cabo USB** (micro-USB ou USB-C, depende do modelo do seu ESP32).  
2. Conecte o ESP32 ao computador.  
3. O sistema deve reconhecer a porta serial.  
   - No **Windows**, aparece como `COMX` (ex.: `COM3`, `COM7`).  
   - No **Linux/Mac**, aparece como `/dev/ttyUSB0` ou `/dev/tty.SLAB_USBtoUART`.  
4. No **Arduino IDE**:
   - Vá em **Ferramentas > Placa > ESP32 > DOIT ESP32 DEVKIT V1**.  
   - Vá em **Ferramentas > Porta** e selecione a porta do ESP32.  
 
---
 
## 2️⃣ Subindo o código
 
1. Abra o código no Arduino IDE.  
2. Confirme se os pinos estão configurados corretamente:
   ```cpp
   #define DHTPIN 5
   #define DHTTYPE DHT11
   #define LDR_PIN 34
