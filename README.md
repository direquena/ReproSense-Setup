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

---

## Download

| Versão | Data | Arquivo | |
|--------|------|---------|---|
| v2.10.6 | 02/10/2026 | `ReproSense_Setup.exe` | [**Baixar**](https://github.com/direquena/ReproSense-Setup/releases/latest/download/ReproSense_Setup.exe) |
| v2.10.5 | 02/10/2026 | `ReproSense_Setup.exe` | — |
| v2.10.4 | 02/10/2026 | `ReproSense_Setup.exe` | — |
| v2.10.2 | 30/09/2026 | `ReproSense_Setup.exe` | — |
| v2.10.1 | 30/09/2026 | `ReproSense_Setup.exe` | — |
| v2.10.0 | 30/09/2026 | `ReproSense_Setup.exe` | — |
| v2.9.8 | 29/09/2026 | `ReproSense_Setup.exe` | — |
| v2.9.7 | 29/09/2026 | `ReproSense_Setup.exe` | — |
| v2.9.6 | 29/09/2026 | `ReproSense_Setup.exe` | — |
| v2.9.5 | 29/09/2026 | `ReproSense_Setup.exe` | — |
| v2.9.4 | 29/09/2026 | `ReproSense_Setup.exe` | — |
| v2.9.3 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.9.2 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.9.1 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.9.0 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.8.2 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.8.1 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.8.0 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.7.9 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.7.8 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.7.7 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.7.6 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.7.5 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.7.4 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.7.3 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.7.2 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.7.1 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.7.0 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.6.0 | 28/09/2026 | `ReproSense_Setup.exe` | — |
| v2.5.1 | 30/06/2026 | `ReproSense_Setup.exe` | — |
| v2.5.0 | 22/06/2026 | `ReproSense_Setup.exe` | — |
| v2.4.1 | 13/06/2026 | `ReproSense_Setup.exe` | — |

---

## Instalação

1. Baixe o instalador acima
2. Execute como **Administrador**
3. Siga o assistente de instalação — informe a URL do seu servidor ReproSense quando solicitado

---

## Requisitos

### Geral (balança, impressora, scanner, congeladora, RMM)

| | Mínimo | Recomendado |
|---|---|---|
| SO | Windows 10 64-bit | Windows 11 64-bit |
| CPU | Dual-core moderno (Intel i3 / Ryzen 3 ou equivalente) | Quad-core ou superior (Intel i5 / Ryzen 5+) |
| RAM | 4 GB | 8 GB |
| Armazenamento | 1 GB livre | SSD, 5 GB livre |
| Monitor | 1920×1080, 60Hz | 1920×1080 (ou superior), 120Hz+ |
| Internet | Conexão estável (comunicação com o ReproSense) | — |
| Navegador | Chrome/Edge atualizado (últimos 2 anos) | Chrome/Edge sempre atualizado |
| Driver USB-Serial PL23XX | Necessário para equipamentos seriais via USB | — |

### Adicional para EvoCASA (análise de motilidade com câmera)

| | Mínimo | Recomendado |
|---|---|---|
| CPU | Quad-core (i5/Ryzen 5) | 6+ núcleos (i7/Ryzen 7) — análise ao vivo + codificação de vídeo em tempo real pesam |
| RAM | 8 GB | 16 GB |
| Monitor | 60Hz | 120Hz+ — percepção fluida do movimento das células em câmeras de alto FPS (a análise em si não depende do monitor) |
| Câmera industrial USB3 Vision (ex.: GOX-3200M) | Porta USB 3.0 dedicada, direto na placa-mãe (não em hub) | Porta USB3 exclusiva pra câmera (nada mais dividindo a banda) |
| Câmera industrial GigE Vision (ex.: CM-040GE) | Placa de rede própria, só pra câmera (não a mesma rede do escritório) | Placa de rede Gigabit dedicada + Jumbo Frames habilitado |
| Software extra | Python 3.12 + eBUS SDK (só p/ câmera GigE — o instalador oferece isso) | — |

> Uma câmera entregando menos FPS do que o configurado costuma ser gargalo de hardware (porta USB compartilhada, placa de rede genérica) — vale conferir a dedicação de porta/rede antes de suspeitar do software.

---

## Suporte

Em caso de dúvidas, entre em contato com o suporte ReproSense.
