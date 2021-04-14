---
title: "Lâmpada + arduino - Parte 1"
date: 2021-04-12T22:38:45-03:00
draft: false
---

# Fita de led RGB + Led alto brilho + arduino = lâmpada colorida

Já fazem ~7 anos que tenho um clone de arduino duemilanove parado na gaveta de microcontroladores. Há muito tempo ele foi substiuído por arduinos nano e, depois, ESP8266/32 e outras plataformas mais modernas. Entretanto, ainda é uma placa respeitável: ATmega328 como microcontrolador, 32KB flash, 2k de SRAM, 6 portas analógicas e 14 portas digitais ― mais do que o suficiente para muitas aplicações.

Estava incomodado que tinha esse equipamento perfeitamente funcional coletando pó e, aproveitando que havia comprado algumas fitas led RGB da china e tinha mais alguns leds de alto brilho, resolvi fazer uma lâmpada.

Comecei a prototipar algumas coisas na protoboard até chegar em um resultado satisfatório:

{{< giphy 8CrHYU3b9si6OpSSBc >}}

<iframe src="https://giphy.com/embed/8CrHYU3b9si6OpSSBc"></iframe>

O circuito é bastante simples: As fitas de led que comprei tem um ânodo para cada uma das cores e um cátodo comum. Deste modo, conectei os emissores de três transistores 2n2222 no polo negativo do circuito e os coletores em cada um dos ânodos dos leds. Adicionei um botão e um potenciômetro para controlar as cores: o potenciômetro controla a intensidade da luz e o botão permite selecionar uma cor específica para ser controlada. Posteriormente adicionei um botão adicional para controlar os leds de alta intensidade, que controlo utilizando um mosfet (por sua vez controlado por um 2n2222) e um lm7805 + um resistor para diminuir a tensão. O código pode ser encontrado [aqui](https://github.com/guilherme-kenzo/arduino-desk-lamp).  

Posteriormente, soldei o circuito em uma perfboard (sem o arduino, obviamente).

![circuito lampada](/perfboard_lampada-fs8.png)

Os próximos passos são 1. Fazer o projeto da estrutura 2. fazer a estrutura de madeira e 2. juntar as peças. Na medida em que for avançando no projeto, vou postando aqui.

