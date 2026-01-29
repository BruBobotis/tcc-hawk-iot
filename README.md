<p align="center">
<img src="https://img.shields.io/github/last-commit/sharandac/My-TTGO-Watch.svg?style=for-the-badge" alt="Último Commit"/>
&nbsp;
</p>
<hr/>

# Projeto de TCC: Interface para Smartwatch ESP32

> **Faculdade Salvador Arena**<br/>
> **Curso:** Engenharia de Controle e Automação<br/>
> **Trabalho de Conclusão de Curso (TCC)**

---

## Sobre o Projeto

Este repositório contém a implementação e documentação técnica do projeto de TCC focado no desenvolvimento de sistemas embarcados para vestíveis (wearables).

O projeto baseia-se no "My-TTGO-Watch", uma Interface Gráfica de Usuário (GUI) denominada "hedge", projetada para dispositivos smartwatch baseados no microcontrolador ESP32.

Atualmente, oferece suporte para os seguintes hardwares:
* T-Watch2020 (V1, V2, V3)
* T-Watch2021 (V1 e V2, sem atualizações OTA)
---

## Funcionalidades (Features)

O sistema operacional embarcado oferece um conjunto robusto de funcionalidades:

* **Comunicação BLE:** Conectividade Bluetooth Low Energy.
* **Sincronização de Tempo:** Ajuste automático de hora via BLE.
* **Notificações:** Recebimento de notificações do smartphone via BLE.
* **Contagem de Passos:** Podômetro integrado.
* **Wake-up por Gesto:** Ativação da tela ao girar o pulso.
* **Ações Rápidas (Quick Actions):**
    * Controle de WiFi
    * Controle de Bluetooth
    * GPS
    * Luminosidade da tela
    * Volume do som
* **Múltiplos Mostradores (Watch Faces):**
    * Embarcados (digitais)
    * [Watchfaces desenvolvidas pela comunidade](https://sharandac.github.io/My-TTGO-Watchfaces/)
* **Múltiplos Aplicativos Embarcados ('Apps'):**
    * Música (controle de reprodução no smartphone)
    * Navegação (exibe instruções vindas do app companheiro)
    * Mapa (exibição de mapas)
    * Notificações (histórico recente)
    * Cronômetro (com funções play, pause, stop)
    * Alarme
    * Contador de Passos (com histórico e objetivo diário)
    * Clima/Tempo
    * Calendário
    * Controle Remoto IR (Infravermelho)
    * Entre outros...
* **Aplicativos Companheiros (Companion Apps):** Compatível com Gadgetbridge.

## Instalação e Compilação

Para utilizar este projeto, clone o repositório e abra-o utilizando o **PlatformIO**. Selecione o ambiente (env) correto para o seu hardware, compile e faça o upload.

Alternativamente, siga este excelente [tutorial passo a passo](https://www.youtube.com/watch?v=wUGADCnerCs) (em inglês) do canal [ShotokuTech](https://github.com/ShotokuTech).

**Nota sobre WiFi:** Verifique o arquivo [`src/hardware/wifictl.cpp`](https://github.com/sharandac/My-TTGO-Watch/blob/709ed0c5863435aa966c1d6f44552ddc0909a57c/src/hardware/wifictl.cpp#L256-L261) para configurar as credenciais WiFi caso o WPS ou a entrada via display não sejam possíveis.

### Suporte Nativo Linux

Se você estiver interessado em rodar o emulador nativo no Linux para desenvolvimento, instale as dependências de desenvolvimento (`sdl2`, `curl` e `mosquitto`) e altere o ambiente no PlatformIO para `emulator_*`.

```bash
sudo apt-get install libsdl2-dev libcurl4-gnutls-dev libmosquitto-dev build-essential
