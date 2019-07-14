----

# Lousa mágica & Lousa paramétrica

Ferramentas de desenhar com potenciômetros ([veja o repositório no GitHub!](https://github.com/villares/lousa-magica/))

> [![Vídeo da lousa mágica](https://img.youtube.com/vi/D5Ha1bhqBuQ/0.jpg)](https://www.youtube.com/watch?v=D5Ha1bhqBuQ)
> <br />vídeo - crédito: [João Adriano Freitas](https://github.com/jaafreitas)

#### Breve histórico

* A *Lousa mágica* foi apresentada inicialmente pelo [Estúdio Hacker](http://estudiohacker.io) na inauguração do Sesc 24 de Maio, em agosto de 2017 (vídeo acima), com 6 potenciômetros, permitia desenhar e apagar o desenho tombando a caixa de controle. Também era possível (por conta de uma biblioteca) postar *tweets* com o desenho.
* No Estúdio Hacker Day em 7 de setembro de 2017, também no Sesc 24 de maio, foi realizada atividade em que os participantes montavam uma versão da *Lousa mágica* com 4 potenciômetros em uma protoboard.
* Para o Circuito Sesc de Artes 2018 foram feitas montagens com 4 potenciômetros com uma variante do software da *Lousa mágica* e uma versão nova chamada *Lousa paramétrica* com um desenho paramétrico recursivo de uma árvore.
* Diversos desenhos do projeto [*sketch-a-day*](https://villares.github.com/sketch-a-day) podem ser usados com a mesma montagem.

#### Lista de materiais

* Arduino (ou variante) com pelo menos 4 portas analógicas;
* Cabo USB para ligar o Arduino ao computador;
* 4 a 6 potenciômetros lineares de 10kΩ (com 2 ou 3 dá mas tem menos graça);
* Protoboard e jumpers;
* botão instantâneo ou interruptor de mercúrio (opcional, pode ser usado o teclado do computador);
* Resistor 10kΩ (opcional, caso seja usado um botão/ interruptor conectado a um pino diferente do D13);
* Computador com monitor (ou laptop) Linux, Mac ou Windows. Para impressionar as visitas use uma TV grande ou um projetor.

![montagem](assets/montagem2.png)

#### Passos
0. Baixe e instale o IDE do [Arduino](http://arduino.cc) e o IDE do [Processing](http://processing.org);

1. Conecte o Arduino ao computador e pelo Arduino IDE suba o *sketch* **Firmata All Inputs** que está nos exemplos;

2. Abra o Processing e pelo próprio IDE baixe e instale o [Modo Python](https://github.com/villares/villares.github.io/blob/master/como-instalar-o-processing-modo-python/index.md) assim como a biblioteca Arduino (Firmata);

3. Faça a montagem dos potenciômetros:

   4.1 Conecte os terminais laterias aos pinos 5V e GND,

   4.2 Conecte os terminais centrais aos pinos analógicos do Arduino.

4. O interruptor (ou botão) para apagar o desenho da *Lousa mágica* deve ter um terminal conectado ao pino digital 13 e o outro à alimentação 5V.
   [Se não for usar o pino D13,  conecte simultaneamente o terminal do pino escolhido ao resistor de 10kΩ (é o chamado resistor  *pull-down*, e deve então ser conectado ao GND). O pino D13 já tem um *pull-down* embutido]

5. Copie o código [`LousaMagica.pyde`](LousaMagica/LousaMagica.pyde) deste repositório e altere o número da porta serial/USB

6. Explore as outras versões no repositório  [`github.com/villares/lousa-magica`](https://github.com/villares/lousa-magica/):

  * *Lousa mágica*: 
    - [versão com apenas 2 potenciômetros](https://github.com/villares/tree/master/lousa-magica/LousaMagica2pots)
    - [versão em Processing Modo Java](https://github.com/villares/lousa-magica/tree/master/LousaMagica_java)
    - [versão Circuito Sesc de Artes 2018](https://github.com/villares/lousa-magica/tree/master//lousa_magica_versao_circuito_sesc)

  * *Lousa paramétrica*:  
    - [*Árvore recursiva* (Circuito Sesc de Artes 2018)](https://github.com/villares/lousa-magica/tree/master/lousa_parametrica_arvore_circuito_sesc)
    - [*Grafos*](https://github.com/villares/lousa-magica/tree/master/lousa_parametrica_grafos)
    - [*Polígonos recursivos*](https://github.com/villares/lousa-magica/tree/master/lousa_parametrica_poligonos_recursivos)
    - Procure mais *sketches* no repositório [`villares.github.com/sketch-a-day`](https://villares.github.com/sketch-a-day)

#### Para uma montagem definitiva

* Alicate;
* Solda;
* Interruptor de mercúrio (no lugar do botão para apagar o desenho da *Lousa mágica*).
* Caixinha com frente transparente, furada para os potenciômetros.

#### Mais ideias

* Pong com potenciômetros, versão Dojo: [`github.com/arteprog/cursos/tree/master/DOJO-pong-com-pot`](https://github.com/arteprog/cursos/tree/master/DOJO-pong-com-pot)

* Versão "sem fio" feita pelo [João Adriano Freitas](https://github.com/jaafreitas): [`github.com/jaafreitas/LousaMagica`](https://github.com/jaafreitas/LousaMagica)

----

Alexandre B A Villares ([abav.lugaralgum.com](https://abav.lugaralgum.com)), [CC-BY-NC-SA-4.0 License](https://creativecommons.org/licenses/by-nc-sa/4.0/)
