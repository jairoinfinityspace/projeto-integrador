# 🌡️ ESP32 Sensor Simulator & Oracle APEX Dashboard

Este projeto simula um sensor de temperatura/umidade utilizando um **ESP32** (via Wokwi) que envia dados em tempo real para uma aplicação **Oracle APEX** através de serviços REST.

## 🚀 Como funciona
1.  **Simulador:** O ESP32 no [Wokwi](https://wokwi.com) lê dados de um sensor (ex: DHT22).
2.  **Comunicação:** O código (MicroPython/C++) envia esses dados via protocolo HTTP para um endpoint REST no Oracle APEX.
3.  **Banco de Dados:** O **ORDS (Oracle REST Data Services)** recebe a requisição e insere os dados em uma tabela SQL.
4.  **Interface:** Uma página no Oracle APEX exibe os dados em gráficos com atualização automática.

## 🛠️ Tecnologias Utilizadas
*   [Wokwi](https://wokwi.com) (Simulação de Hardware)
*   [Oracle APEX](https://apex.oracle.com) (Low-code e Dashboard)
*   [Oracle REST Data Services (ORDS)](https://www.oracle.com) (API de comunicação)
*   Linguagem: C++/MicroPython (ESP32) e SQL/PLSQL (Backend)

## 📋 Como configurar
1.  **No Oracle APEX:**
    *   Crie a tabela `SENSORES_DATA`.
    *   Habilite o módulo REST em `SQL Workshop -> RESTful Services`.
    *   Crie um handler `POST` para inserir os dados.
2.  **No Wokwi:**
    *   Cole o código presente na pasta `/src` deste repositório.
    *   Troque a URL do endpoint pela sua URL gerada no APEX.
3.  **No Dashboard:**
    *   Crie um componente de **Chart** e configure o *Auto Refresh* para ver os dados em tempo real.

## 📸 Screenshots
*(Dica: Coloque prints do seu gráfico e do circuito aqui)*
