<h1 align = center> Projeto: Simulador de Chuva </h1>
<h4> Professor: Frederico Martins Aguiar </h4>
<h4> Alunos: Danilo Santos, Erick Silva, Lucas Aquino, Marilene Araujo, Maycon Siqueira </h4>

<hr>
<h3> Introdução: </h3>

<p align="justify">
	Este projeto é um simulador de chuva que combina hardware e software para criar um sistema de irrigação ou um efeito visual interativo. Ele utiliza um microcontrolador Arduino para controlar uma bomba d'água, simulando a queda de chuva de forma controlada.
Neste projeto iremos apresentar sobre eletrônica básica, programação de microcontroladores e a interface entre código e componentes físicos.
</p>

<hr>
<h3> Componentes Necessários: </h3>

- Arduino Uno: É a plataforma de microcontrolador, responsável por executar a lógica do projeto lendo os dados dos sensores.
- Sensor de Umidade do Solo: Para medir a quantidade de água no solo, sendo a principal informação para determinar se a irrigação é necessária.
- Sensor DHT11: Para medir a temperatura e a umidade do ar, permitindo uma lógica de rega mais inteligente e precisa.
- Sensor LDR (Resistor Dependente de Luz):  Detecta a quantidade de luz no ambiente, permitindo ao sistema diferenciar o dia da noite e otimizar o horário de rega.
- Sensor de Nível de Água (Flutuador): Avisa quando o nível de água no reservatório está baixo, protegendo a bomba e enviando um alerta.
- Mini Bomba d'Água (3V a 6V): Responsável por mover a água do reservatório para a planta, criando o efeito de chuva.
- Módulo Relé de 1 Canal: Atua como um interruptor eletrônico, permitindo que o arduino, opera em baixa voltagem, controle a bomba d'água, que requer mais energia.
- Cabos de Conexão (Jumpers): Fios para conectar todos os sensores, o relé e a bomba.
- Protoboard (Breadboard):Uma placa para montar e testar as conexões dos componentes sem precisar de solda.
- Fonte de Alimentação Externa (12V): É necessária para alimentar o arduino e, principalmente, a bomba d'água e o relé, que consomem mais energia.
- Mangueira Pequena (para a bomba): Para direcionar o fluxo de água do reservatório até a planta.
- Cabo USB: Para conectar o Arduino ao computador.

<hr>
<h3> Montagem do Circuito </h3> 

<p align="justify"> 
	O circuito foi montado conforme o esquema abaixo.

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

 <h5> Variáveis: </h5>

 <h5> Pinos: </h5>

</p>

<hr>

<h3> Controle da Água: </h3>

<h5> Indicadores Visuais: (LEDs): </h5>

A sinalização da qualidade da água utiliza três LEDs, cada um com uma cor específica para indicar o estado da água:

- LED Verde (ledAguaBoa): Indica que a água está em condições boas e seguras para a vida aquática. <br>
- LED Amarelo (ledAguaEmAlerta): Sinaliza que a água está em um estado de alerta, indicando o início de uma possível contaminação. <br>
- LED Vermelho (ledAguaContaminada): Alerta para um estado crítico, indicando que a água está contaminada e perigosa para a vida no ecossistema.

<h5> Sistema de Alerta: </h5>

- Visual: A interface mudará de cor (verde para bom, amarelo para alerta, vermelho para crítico) com base nos limites predefinidos dos sensores.<br>
- Sonoro: Um alarme sonoro será ativado quando os níveis críticos forem alcançados.

<hr>

<h3>Interface da aplicação em C#(WPF)</h3> 

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

<h3> O Processo de Comunicação: Serial e Assíncrono </h3>

<hr>

<h3> Dificuldades: </h3>

<hr>

<h3> Montagem do Protótipo: </h3>

<hr>

<h3> Protótipo Pronto: </h3>
