![GitHub License](https://img.shields.io/github/license/kellileni/rote-arduino)


Aluno: kelli leni, Daniel, Jõao ricardo 

Professor: José de Assis

Data: 11/03/2026

## 1. Objetivo
Fazer os testes de Arduino IDE e no tinkercad 

## 2.Equipamentos utilizados neste laboratorio 

-Cabo USB (Tipo A/B)
-Resistores
-LEDs
-Jumpers
-Protoboard
-Arduino UNO
-Buzzer
-Sensor DHT11
-Ethernet Shield
-sensor Ultrassônico

## 3. codigos q utilizamos 

1-/**
  (Arduino Ethernet(configurações básicas da rede)
  @author kelli leni (Github:kellileni)
*/

//biblioteca usadas para este projeto 
#include <SPI.h>
#include <Ethernet.h>

//pinos digitais que não podem ser usadas: 0,1,4,10,11,12 e 13

// Gerar um endereço físico (MAC ADDRES) para esta placa 
// https://ssl.crox.net/arduinomac
byte mac[6] = { 0x90; 0xA2, 0xDA, 0x68, 0xEF, 0xDB}

//Instanciar (criar) um servidor 
EthernetServer server(80); //80 é a porta http

void setup() {
  serial.begin(9600)
  // As linhas abaixo iniciam o servidor 
  // e atribuim automaticamente um IP para o Arduino
  Ethernet.being(mac); //atribui o endereço MAC ao shield Ethernet 
  server.being(); //inicia o servidor 
  // As linhas abaixo exibem o IP da placa Arduino 
  Serial.println("Arduino Ethernet Shield:");
  Serial.print("IP: ");
  Serial.println(Ethernet.localIP()); //identifique o IP 
  Serial.print("Mascára: ");
  Serial.println(Ethernet.subnetMask());
  Serial.print("Gateway: ");
  Serial.println(Ethernet.gatewayIP());
  Serial.print("DNS: ");
  Serial.println(Ethernet.dnsServerIP());
}

void loop() {
  // put your main code here, to run repeatedly:

}







