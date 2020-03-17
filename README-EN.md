----

# Lousa mágica & Lousa paramétrica

Lousa mágica: magic drawing board
Lousa paramétrica: parametric drawing board

Tools for drawing with wattmeters ([take a look at the GitHub repo!](https://github.com/villares/lousa-magica/))

> [![Magic Drawing Board video - Lousa Mágica](https://img.youtube.com/vi/D5Ha1bhqBuQ/0.jpg)](https://www.youtube.com/watch?v=D5Ha1bhqBuQ)
> <br />Lousa mágica video at Sesc 24 de maio - credits: [João Adriano Freitas](https://github.com/jaafreitas)

#### Brief history

* *Lousa mágica* was inititally presented by [Estúdio Hacker](http://estudiohacker.io) in the inauguration of [Sesc 24 de Maio](https://www.sescsp.org.br/unidades/36_24+DE+MAIO/#/uaba=programacao#/fdata=id%3D36), on August 2017 (video above). It used 6 wattmeters and supported drawing and erasing drawings by tilting the control box. It was also possible to post *tweets* with the drawing (due to a library).
* On Estúdio Hacker Day  (September 7th, 2017), also at Sesc 24 de maio, a workshop where the participants set up a version of *Lousa mágica* with 4 wattmeters in a protoboard was held.
* Setups with 4 wattmeters using a variation of the *Lousa mágica* software and a new version called *Lousa paramétrica* with a recursive parametric drawing of a tree were displayed at [Sesc Art Circuit 2018](https://circuito.sescsp.org.br/).
* Several [*sketch-a-day* project](https://villares.github.com/sketch-a-day) drawings can be used with the same setup.
* `TO DO: more 'usable' drawings links`

#### Materials

* Arduino (or variations) with at least 4 analog pins;
* USB cable to link up the Arduino to the computer;
* 4 to 6 linear  10kΩ wattmeters (type "B") (you can use 2 or 3 but it's not as cool);
* Protoboard and jumpers;
* Computer with monitor (or a laptop) Linux, Mac ou Windows. Use a big TV or a projector to make a bigger impact on the guests.
* Optional: button or mercury switch (the computer keyboard may be used) and 10kΩ resistor  (if it's a button/switch connected to a pin other than `D13`);

#### Setup instructions

![setup](assets/montagem-lousa-magica.png)

1. Download and install the [Arduino IDE](http://arduino.cc) and the [Processing IDE](http://processing.org);

2. Connect your Arduino/board to your computer, open the Arduino IDE, and in the menu `File > Examples > Firmata` look for the *sketch* called **Firmata All Inputs**. Next, select your board's model in `Tools > Board:` , and in `Tools > Port`, the USB/serial port the board is connected to. Lastly, click the `➔` button to upload the sketch to the board;

    > Known problems:
    > - Some Arduino clones need a special USB drive: [How to Install CH340 Drivers](https://learn.sparkfun.com/tutorials/how-to-install-ch340-drivers/all#drivers-if-you-need-them)
    > - If you use Linux, you might not have permission to access the USB/serial port, which can be corrected by typing the command `sudo usermod -a -G dialout <username>` in the terminal

3. Open the Processing IDE and download the **Arduino (Firmata)** library in `Sketch > Import Library... > Add Library...`. We suggest you select **Python mode** on top right corner menu of the IDE instead of the default `Java` ([detailed instructions (*portuguese*)](https://github.com/villares/villares.github.io/blob/master/como-instalar-o-processing-modo-python/index.md));

4. Connect your wattmeter to your Arduino/board according to the image:

    4.1 Connect the side terminals of each wattmeter to the `5V` e `GND` pins,

    4.2 Connect the central terminals to the board's analog pins: `A1`, `A2`, `A3` e `A4`;

5. Optionally, if you chose to use a button/switch to erase the *Lousa mágica*, it must be connected to the `Digital 13` pin and `5V` pin;

    > If not using the `D13` pin,  connect the chosen pin terminal to the 10kΩ resistor  (so called *pull-down* resistor) and to the `GND` pin simultaneously. The `D13` has a built in *pull-down*

6. Copy the code [`LousaMagica.pyde`](LousaMagica/LousaMagica.pyde) from this repo and  **alter the number of your serial/USB correctly!** Test using the number of ports that appear in the Processing console, starting from the top of the list: `NUM_PORTA = 0`.;

    > Known problems
    > - Linux: confirm you have access to the USB/serial port (as mentioned in item 2).
    > - 64-bits Windows: Processing might download the incorrect version (32 bits) of the Python mode library. You can solve this by deleting or renaming the file in `C:\Program Files\processing-3.X.X\modes\java\libraries\serial\library\windows32\jSSC-2.8.dll` as documented in [issue 227](https://github.com/jdf/Processing.py-Bugs/issues/227).

#### Explore other versions in the repo  [`github.com/villares/lousa-magica`](https://github.com/villares/lousa-magica/):

  * *Lousa mágica*:
    - [2 wattmeters version](https://github.com/villares/lousa-magica/tree/master/LousaMagica2pots)
    - [versão em Processing Modo Java](https://github.com/villares/lousa-magica/tree/master/LousaMagica_java)
    - [Sesc Art Circuit 2018 version](https://github.com/villares/lousa-magica/tree/master//lousa_magica_versao_circuito_sesc)

  * *Lousa paramétrica*:  
    - [*Recursive tree* (Sesc Art Circuit 2018)](https://github.com/villares/lousa-magica/tree/master/lousa_parametrica_arvore_circuito_sesc)
    - [*Graphs*](https://github.com/villares/lousa-magica/tree/master/lousa_parametrica_grafos)
    - [*Recursive polygons version*](https://github.com/villares/lousa-magica/tree/master/lousa_parametrica_poligonos_recursivos)
    - Look for more *sketches* in the repo [`villares.github.com/sketch-a-day`](https://villares.github.com/sketch-a-day)

#### Arduino Nano example

![setup](assets/montagem2.png)

#### Definitive setup suggestions

* Tools: pliers and solder;
* Use a mercury switch instead of a button on `D13` to erase *Lousa mágica*.
* Setup in a box with a transparent side, with holes for the wattmeters.

#### Other ideas

* Pong with wattmeters, Dojo version: [`github.com/arteprog/cursos/tree/master/DOJO-pong-com-pot`](https://github.com/arteprog/cursos/tree/master/DOJO-pong-com-pot)
* "Wireless" version made by [João Adriano Freitas](https://github.com/jaafreitas): [`github.com/jaafreitas/LousaMagica`](https://github.com/jaafreitas/LousaMagica)

----

Alexandre B A Villares ([abav.lugaralgum.com](https://abav.lugaralgum.com)), [CC-BY-NC-SA-4.0 License](https://creativecommons.org/licenses/by-nc-sa/4.0/)
Translated by Carolina Giorno
