<h1 align = center> Projeto: Simulador de Chuva </h1>
<h4> Professor: Frederico Martins Aguiar </h4>
<h4> Alunos: Danilo Santos, Erick Silva, Lucas Aquino, Marilene Araujo, Maycon Siqueira </h4>

<hr>

<h3> Introdução </h3>

<p align="justify">

 Este projeto implementa um sistema de automação para irrigação utilizando um microcontrolador **Arduino** para ler sensores e controlar uma bomba, e uma aplicação **C# WPF** para monitorar o status do sistema em tempo real via comunicação serial.
 
</p>

<hr>

<h3> Objetivo </h3>

<p align="justify">
	
Garantir que a irrigação do solo ocorra apenas quando:
1.  O **Solo** estiver seco (necessidade de água).
2.  Houver **Água Suficiente** no reservatório (segurança para a bomba).
   
</p>

<hr>

<h3> Funcionalidades Principais  </h3>

- Monitoramento de Umidade: Lê continuamente o sensor de umidade do solo para determinar se a planta está seca e precisa de irrigação.
- Monitoramento de Nível de Água (Segurança): Lê o sensor de nível do reservatório para garantir que a bomba nunca seja ligada se a água estiver abaixo do limite mínimo.
- Decisão Inteligente de Irrigação:	A bomba só é acionada se ambos os critérios forem atendidos: Solo Seco E Água Suficiente no reservatório.
- Proteção da Bomba (Anti-Seco)	Desliga imediatamente a bomba se o nível de água no reservatório cair abaixo do limite de segurança.
- Feedback de Status Serial: O Arduino envia constantemente dados e mensagens de status (leituras e estado da bomba) pela porta serial para fins de monitoramento e depuração.
- Monitoramento Gráfico (WPF):	A aplicação C# WPF recebe e exibe os dados seriais em uma interface de usuário amigável em tempo real.

<hr>

<h3> Componentes Necessários: </h3>

* **Arduino Uno**: Atua como o Cérebro do Sistema, Executa a lógica de controle, lê sensores e decide o acionamento da bomba.
* **Sensor de Umidade do Solo** - (Analógico) Entrada: Mede a umidade para determinar se o solo está seco e precisa de água.
* **Sensor de Nível de Água** - Entrada de Segurança: Verifica se há água suficiente no reservatório para a bomba operar.
* **Módulo Relé** de 1 canal -  Atuador: Interruptor eletrônico que permite ao Arduino ligar/desligar a bomba (alta voltagem/corrente).
* **Bomba de Água** - Executora: Move fisicamente a água do reservatório para a planta quando acionada.
* **Fonte de alimentação** externa. Energia: Fornece a corrente necessária para alimentar a bomba de água, separadamente do Arduino.

<hr>
<h3> Montagem do Circuito </h3> 

<p align="justify"> 
	O circuito foi montado conforme o esquema abaixo.
 </p>

<hr>

<h3> Esquema de Conexão </h3> 

 <p align="justify">
	Este é o esquema de conexão para ligar os componentes ao Arduino:
	 
 1. Conexões de Entrada (Sensores Analógicos)
- Sensor de Umidade do Solo: Pino digital A5 VCC (5V) e GND no Arduino.
- Sensor de Nível de Água: Pino digital	A1	VCC (5V) e GND no Arduino.

2. Conexão de Saída (Controle da Bomba)
  O relé é controlado por uma porta digital e, por sua vez, controla a bomba.  <br>
- Módulo Relé (IN): Pino digital 7	VCC (5V) e GND no Arduino.

</p>

<hr>

<h3> Código do Arduino </h3> 

 <p align="justify">
	O código abaixo controla a leitura do sensor. 
</p>

<hr>

<h3>Interface da aplicação em C# (WPF)</h3> 

<hr>

<h3> O Frontend (Interface Visual com XAML)</h3> 

<hr>

<h3> O Backend (Lógica com C#) </h3> 

<hr>

<h5> Sistema de Alerta: </h5>

- Visual: A interface mudará de cor quando a caixa dágua estiver vazia.

<hr>

<h3> O Processo de Comunicação: Serial e Assíncrono </h3>

<p align="justify">
	
A comunicação entre o Arduino (o controlador) e o C# WPF (o monitor) é realizada através da Porta Serial Virtual estabelecida via USB, seguindo um fluxo de dados simples e unidirecional (do Arduino para o PC).

1. Estabelecimento da Conexão
   
- Setup:	O código inicia a comunicação serial na taxa de 9600 bps com Serial.begin(9600). A aplicação C# instancia o objeto SerialPort e o configura para a mesma porta COM e taxa (9600).
- Abertura: O Arduino está sempre enviando dados após a inicialização. O C# chama o método arduinoPort.Open() para estabelecer a escuta ativa na porta.

2. Fluxo de Dados (Transmissão)

- Arduino atua como o transmissor, enviando informações importantes a cada ciclo do loop() (a cada 2 segundos).
- Envia Leituras: O Arduino envia os valores dos sensores em uma única linha formatada, como: Umidade do Solo: 750 | Nivel da Agua: 300.
- Envia Status: Em seguida, ele envia a mensagem de status da bomba (por exemplo: LIGANDO BOMBA. ou Solo umido. Bomba permanece desligada.).
- Terminação: O Arduino finaliza cada mensagem (linha) com um caractere de nova linha (\n) usando Serial.println().


</p>

<hr>

<h3> Dificuldades: </h3>

<hr>

<h3> Montagem do Protótipo: </h3>

<p align="center"> <img src="https://github.com/MaysCroft/Documentacao-Projeto-Simulador-de-Chuva/blob/main/Imagens/IMG-20250924-WA0016.jpg" height="700" width="700"/> </p>
<p align="center"> <img src="https://github.com/MaysCroft/Documentacao-Projeto-Simulador-de-Chuva/blob/main/Imagens/IMG-20250924-WA0018.jpg" height="700" width="700"/> </p>
<p align="center"> <img src="https://github.com/MaysCroft/Documentacao-Projeto-Simulador-de-Chuva/blob/main/Imagens/IMG-20250924-WA0025.jpg" height="700" width="700"/> </p>
<p align="center"> <img src="https://github.com/MaysCroft/Documentacao-Projeto-Simulador-de-Chuva/blob/main/Imagens/IMG-20250924-WA0026.jpg" height="700" width="700"/> </p>
<p align="center"> <img src="https://github.com/MaysCroft/Documentacao-Projeto-Simulador-de-Chuva/blob/main/Imagens/IMG-20250924-WA0029.jpg" height="700" width="700"/> </p>
<p align="center"> <img src="https://github.com/MaysCroft/Documentacao-Projeto-Simulador-de-Chuva/blob/main/Imagens/IMG-20250924-WA0031.jpg" height="700" width="700"/> </p>
<p align="center"> <img src="https://github.com/MaysCroft/Documentacao-Projeto-Simulador-de-Chuva/blob/main/Imagens/IMG-20250924-WA0041.jpg" height="700" width="700"/> </p>
<p align="center"> <img src="https://github.com/MaysCroft/Documentacao-Projeto-Simulador-de-Chuva/blob/main/Imagens/IMG-20250924-WA0044.jpg" height="700" width="700"/> </p>
<p align="center"> <img src="https://github.com/MaysCroft/Documentacao-Projeto-Simulador-de-Chuva/blob/main/Imagens/IMG-20250924-WA0027.jpg" height="700" width="700"/> </p>
<p align="center"> <img src="https://github.com/MaysCroft/Documentacao-Projeto-Simulador-de-Chuva/blob/main/Imagens/IMG-20250924-WA0028.jpg" height="700" width="700"/> </p>
<p align="center"> <img src="https://github.com/MaysCroft/Documentacao-Projeto-Simulador-de-Chuva/blob/main/Imagens/IMG-20250924-WA0036.jpg" height="700" width="700"/> </p>
<p align="center"> <img src="https://github.com/MaysCroft/Documentacao-Projeto-Simulador-de-Chuva/blob/main/Imagens/IMG-20250924-WA0045.jpg" height="700" width="700"/> </p>
<p align="center"> <img src="https://github.com/MaysCroft/Documentacao-Projeto-Simulador-de-Chuva/blob/main/Imagens/IMG-20250924-WA0043.jpg" height="1000" width="700"/> </p>
<p align="center"> <img src="https://github.com/MaysCroft/Documentacao-Projeto-Simulador-de-Chuva/blob/main/Imagens/IMG-20250924-WA0047.jpg" height="1000" width="700"/> </p>
<hr>

<h3> Protótipo Pronto: </h3>
