<h1 align = center> Projeto: Simulador de Chuva </h1>
<h4> Professor: Frederico Martins Aguiar </h4>
<h4> Alunos: Danilo Santos, Erick Silva, Lucas Aquino, Marilene Araujo, Maycon Siqueira </h4>

<hr>
<h3> Introdução: </h3>

<p align="justify">
	Este projeto, Vigilante Hídrico, simula um sistema inteligente de monitoramento da qualidade da água. Utilizando uma combinação de hardware e software, ele coleta dados críticos em tempo real. O sistema foi desenvolvido como parte de uma atividade de grupo para o curso Técnico em Desenvolvimento de Sistemas, com o objetivo principal de aplicar conceitos de prototipagem e o uso de sensores e atuadores.
</p>

<hr>
<h3> Componentes Necessários: </h3>

- Arduino Uno: É a plataforma de microcontrolador, responsável por executar a lógica do projeto lendo os dados dos sensores.
- Sensor de pH: Essencial para medir a acidez ou alcalinidade da água. A maioria dos peixes vive em um pH neutro ou ligeiramente alcalino.
- Sensor de Turbidez: Mede a transparência da água. Alta turbidez pode ser um sinal de poluição ou excesso de sedimentos.
- Sensor de Temperatura: Muitos peixes são sensíveis a variações de temperatura.
- Sensor de Sólidos Totais Dissolvidos (TDS): Mede a concentração de substâncias orgânicas e inorgânicas dissolvidas na água, o que pode indicar poluição.
- Protoboard e Jumpers: Para montar as conexões entre o Arduino e os sensores.
- Cabo USB: Para conectar o Arduino ao computador.

<hr>
<h3> Montagem do Circuito </h3> 

<p align="justify"> 
	O circuito foi montado conforme o esquema abaixo. As conexões foram diretas e simples.

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
