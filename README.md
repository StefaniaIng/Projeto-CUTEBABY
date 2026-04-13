#  👶 CuteBaby - Sistema de Monitoramento Acessivel para Pais com Deficiência Auditiva.

## 📋 Objetivo do Projeto
O **CuteBaby** é um sistema embarcado desenvolvido para a placa BitDogLab (RP2040) que auxilia pais com deficiência auditiva no monitoramento de seus bebês. O sistema detecta o choro por meio de um microfone e aciona alertas visuais e sonoros. O alerta aumenta de intensidade caso o recebimento do aviso não seja confirmado.

## 🚀 Funcionalidades
- **Inicialização e Monitoramento Contínuo**:
   Ao ligar a placa o display exibe a mensagem "CuteBaby monitorando" enquanto o LED de status permanece aceso, indicando que o sistema está ativo e realizando o monitoramento do ambiente.
- **Calibração Inteligente:** 
Ajusta o sensor automaticamente ao ruído do ambiente em 5 segundos.
- **Ajuste Manual:** Controla a sensibilidade via Joystick (50% a 100%).
- **Alerta em Duas Fases:** 
  - Alerta imediato: Ao detectar o choro o sistema ativa simultaneamente a matriz 5x5 dos LEDs, o buzzer e o display que exibe a mensagem "Alerta! Bebê chorando". O responsável deve confirmar o recebimento do alerta pressionando o botão A.
  - Notificação para rede de apoio: Caso o botão A não seja pressionado em até 10 segundos, o sistema envia automaticamente uma notificação para a rede de apoio cadastrada.
- **Retorno ao Monitoramento**:
Ao pressionar o botão A o sistema confirma o recebimento do alerta e retorna ao modo de monitoramento contínuo.


## 📌 Componentes de Hardware Utilizados
Para o projeto na BitDogLab foram utilizados os seguintes pinos do microcontrolador RP2040:
- Microfone: GPIO28.
- Joystick (Eixo Y): GPIO26.
- Botão A - GPIO5.
- Botão B - GPIO6.
- Matriz de LEDs - GPIO7 (ws2812).
- Display OLED - GPIO14 (SDA) e GPIO15 (SDL).
- Buzzer - GPIO21
- Led Status (Verde) - GPIO11

## 📊 Como Executar o projeto

1. **Configuração do Ambiente**
   - Baixe o **VS Code** em seu computador.
   - Instale a extensão: **Raspberry Pi Pico** dentro do VS Code.
   - Certifique-se de ter o **Pico SDK** instalado e configurado.

2. **Preparação do Repositório**:
   - Faça o download ou clone este repositório para seu computador.
   - Abra a pasta do projeto no VS Code.
  
3. **Compilação**
   - Clique no botão **Compile Project** dentro do VS Code.
   - Coloque a placa em modo **Bootsel**.
   - Conecte a placa **BitDogLab** ao computador via cabo USB.
   - Clique no botão **Run Project(USB)**.

4. **Verificação do sistema**
   - Ligando: Verifique se o LED verde acende e o display exibe a mensagem "CuteBaby Monitorando" após clicar no run project.
   - Calibrando o Ambiente: Pressione o **Botão B** e observe a contagem regressiva de 5 segundos no display OLED para verificação do som ambiente.
   - Testando a sensibilidade: Movimente o Joystick para cima e para baixo. Verifique se o valor de "SENS %" no display muda conforme o deslocamento manual.
   - Simulando o Choro: Abra o arquivo no seu celular (Link 1). A Matriz de LEDs deve exibir um "X" imediatamente acompanhada de uma mensagem no display e som do buzzer.
   - Confirmando o Recebimento: Com o visor piscando, pressione o Botão A. O sistema deve silenciar e voltar ao modo de monitoramento.
   - Teste de Notificação: Abra novamente o arquivo (Link 1) no celular mas não pressione o botão A por 10 segundos. Verifique se o display OLED muda para "Sem Resposta! Notificando Apoio".

"💡O sistema envia informações em tempo real pelo Monitor Serial (UART), permitindo acompanhar a calibração e os disparos de alerta."

   ## 📚 Bibliotecas e Créditos
- Pico SDK (RP2040).
- Biblioteca SSD1306 (Display OLED).
- Biblioteca ws2812 (Matriz 5x5).
- **EmbarcaTech**: Projeto desenvolvido para avaliação final da capacitação em Sistemas Embarcados.

## 📺 Recursos de Mídia e Testes

Para facilitar a verificação do funcionamento do sistema, utilize os recursos abaixo:

* **Link 1: Áudio de Referência (Choro do Bebê)** - [Clique aqui para acessar o áudio utilizado nos testes](https://youtube.com/clip/UgkxLFucoGxB1lV9XipPq36UKc_hOz32ZrSx?si=lhl_1qlx60A6BcHX)

* **Link 2: Vídeo Demonstrativo da Execução do Projeto** - [Assista à demonstração prática do CuteBaby na BitDogLab](https://youtube.com/shorts/L8Dgp1WPwdU)
   


## 📄 Licença
Este projeto está sob a licença MIT - veja o arquivo LICENSE para detalhes.

## ⭐ Projeto


[README.md](https://github.com/user-attachments/files/26664132/README.md)
[Tarefa7.c](https://github.com/user-attachments/files/26664131/Tarefa7.c)




