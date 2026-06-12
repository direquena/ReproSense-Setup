# ReproSense — Coletor Local

> Utilitário local para integração de equipamentos de laboratório com o sistema ReproSense.

---

## O que é o Coletor Local?

O **Coletor Local ReproSense** é um serviço que roda em segundo plano na máquina do laboratório e faz a comunicação entre os equipamentos físicos e o servidor ReproSense.

Com ele instalado, o sistema passa a suportar:

- Impressoras de etiquetas (ZPL, TSPL, EPL)
- Balanças e diluidores via porta serial
- Leitores de código de barras (HID / USB)
- Congeladora DigitCool / Mini-DigitCool
- Software de análise seminal CASA / HTCore
- Sensores de condutividade e temperatura
- Estação meteorológica Ambient Weather
- **Monitoramento remoto da máquina (RMM)** — métricas de CPU, RAM, disco, eventos Windows e comandos remotos

---

## Download

| Versão | Arquivo | |
|--------|---------|---|
| Mais recente | `ReproSense_Setup.exe` | [**Baixar**](https://github.com/direquena/ReproSense-Setup/releases/latest/download/ReproSense_Setup.exe) |

---

## Instalação

1. Baixe o instalador acima
2. Execute como **Administrador**
3. Siga o assistente de instalação — informe a URL do seu servidor ReproSense quando solicitado (ex: `https://reprosense.com`, `https://seleon.reprosense.com`)
4. Após instalar, o Coletor estará disponível em `http://localhost:5150`
5. A máquina aparecerá automaticamente no módulo **RMM** do servidor para ser vinculada à empresa

---

## Requisitos

- Windows 10 ou superior (64-bit)
- Conexão com o servidor ReproSense
- Driver USB-Serial PL23XX (para equipamentos seriais via USB)

---

## Suporte

Em caso de dúvidas, entre em contato com o suporte ReproSense.
