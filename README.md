<h1 align = center> Projeto: Simulador de Chuva </h1>
<h4> Professor: Frederico Martins Aguiar </h4>
<h4> Alunos: Danilo Santos, Erick Silva, Lucas Aquino, Marilene Araujo, Maycon Siqueira </h4>

<hr>
<h3> Visão Geral do Projeto </h3>

<p align="justify">
	Este projeto é um sistema de automação residencial que monitora as condições de um solo e controla um sistema de irrigação de forma inteligente e autônoma simulando uma chuva. Diferente de soluções simples, ele toma decisões com base em múltiplos fatores ambientais e oferece um painel de controle local para monitoramento em tempo real.
	
	O sistema é dividido em duas partes principais:
- Hardware (Arduino): A "inteligência" que lê os sensores, executa a lógica e controla a bomba d'água.
- Software (C# com WPF): Um painel de controle de desktop que se conecta ao Arduino via USB para exibir os dados dos sensores e permitir o controle manual.
</p>

<hr>

<h3> Funcionalidades Principais  </h3>

- Automação Inteligente: Rega automática baseada na umidade do solo, luminosidade e umidade do ar.<br>
- Painel de Controle Local: Interface gráfica em C# (WPF) que exibe todos os dados dos sensores em tempo real.<br>
- Controle Manual: Possibilidade de ligar ou desligar a bomba diretamente pelo painel de controle.<br>
- Proteção do Sistema: Sensor de nível de água que impede que a bomba funcione sem água, prevenindo danos.<br>
- Dados Detalhados: Monitoramento da umidade do solo, temperatura, umidade do ar, luminosidade e nível do reservatório.<br>

<hr>

<h3> Componentes Necessários: </h3>

- Arduino Uno: O cérebro do projeto;
- Módulo Relé de 1 Canal: Para ligar e desligar a bomba com segurança;
- Mini Bomba d'Água (3V a 6V): Para irrigar a maquete;
- Sensor de Umidade do Solo: Para medir a umidade da terra;
- Sensor de Nível de Água: Para monitorar o reservatório;
- Protoboard: Plataforma para montagem dos circuitos eletrônicos;
- Cabos de Conexão (Jumpers): Conexão dos componentes;
- Fonte de Alimentação Externa (12V).

<hr>
<h3> Montagem do Circuito </h3> 

<p align="justify"> 
	O circuito foi montado conforme o esquema abaixo.
 </p>

<hr>

<h3> Esquema de Conexão </h3> 

 <p align="justify">
	Este é o esquema de conexão para ligar os componentes ao Arduino:
	 
- Relé da Bomba: Pino digital 7.
- Sensor de Umidade do Solo: Pino analógico A0.
- Sensor de Nível de Água: Pino digital 8.
- Sensor DHT11: Pino digital 4.
- Sensor LDR: Pino analógico A1.
- Conecte as outras extremidades dos componentes às fontes de energia apropriadas (+5V e GND).
</p>

<hr>

<h3> Código do Arduino </h3> 

 <p align="justify">
	O código abaixo controla a leitura do sensor. 
</p>

<hr>

<h3> Explicação do Código </h3> 

<p align="justify">
  <h5> Como Funciona </h5>
</p>

<hr>

<h3>Interface da aplicação em C# (WPF)</h3> 

<hr>

<h3> O Frontend (Interface Visual com XAML)</h3> 

<hr>

<h3> Explicação do Código </h3> 

<p align="justify">
	<h5> Como Funciona </h5>
</p>

<hr>

<h3> O Backend (Lógica com C#) </h3> 

<hr>

<h3> Explicação do Código </h3> 

<p align="justify">
	<h5> Como Funciona </h5>
</p>

<hr>

<h5> Sistema de Alerta: </h5>

- Visual: A interface mudará de cor quando a caixa dágua estiver vazia.

<hr>

<h3> O Processo de Comunicação: Serial e Assíncrono </h3>

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
