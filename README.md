![GitHub License](https://img.shields.io/github/license/kellileni/rote-arduino)


Aluno: kelli leni, Daniel, Jõao ricardo 

Professor: José de Assis

Data: 11/03/2026

## 1. Objetivo
Fazer os testes de Arduino IDE e no tinkercad 

🛠️ Hardware Utilizado (Detalhado)
Com base nos componentes utilizados no seu laboratório:

Arduino Uno R3: O cérebro do projeto.

Ethernet Shield W5100: Responsável pela conectividade via cabo RJ45.

Cabo USB tipo A/B: Para transferência do código e alimentação inicial.

Protoboard (Mini): Utilizada para prototipagem rápida.

Jumpers (Macho-Macho): Cabos para conexões auxiliares.

Sensores Extras (Visíveis na caixa):

Sensor Ultrassônico HC-SR04 (Medição de distância).

Sensor de Umidade e Temperatura DHT11 (Azul).

Buzzer e LEDs (Para alertas visuais e sonoros de conexão).

Resistores variados.

---

## 2. codigos q utilizamos 

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

---

## 3. Passo a Passo do Setup

fase 1: Montagem Física
Encaixe o Ethernet Shield sobre o Arduino, alinhando todos os pinos cuidadosamente.

Conecte o Arduino ao roteador via cabo RJ45.

Alimente o Arduino via USB ou fonte externa.

Fase 2: Configuração de Rede (Roteador)
Nesta etapa, o objetivo é isolar e organizar os endereços IP para evitar conflitos:

Criação da Rede Privada: Acesse a interface do roteador (geralmente 192.168.1.1 ou 192.168.0.1).

Reserva de IP (Static DHCP): * Identifique o MAC Address do seu Ethernet Shield (geralmente adesivado na placa ou definido no código).

No menu "DHCP Server" ou "Address Reservation", vincule o MAC ao IP desejado (ex: 192.168.1.50).

Isso garante que o Arduino sempre terá o mesmo endereço após reiniciar.

Fase 4: Implementação do Código
Recomenda-se incluir um exemplo básico de Webserver ou Ping Test no repositório. Use blocos de código formatados:












---

## 4. imagens do preçedimento 
![]()<img width="584" height="727" alt="image" src="https://github.com/user-attachments/assets/9658272f-58d6-4f30-b2a0-d51e65fd37dc" />


![]()<img width="1020" height="781" alt="image" src="https://github.com/user-attachments/assets/fbc7ebed-3206-4bb2-9d6b-fa957b59510a" />




