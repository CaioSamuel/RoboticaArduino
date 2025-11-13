#include <robo_hardware2.h> 
#include <Servo.h>

//-----PINOS PARA SENSORES REFLETANCIA-----//
//SENSOR_LINHA_ESQUERDO			    A2
//SENSOR_LINHA_DIREITO			    A1	
//-----PINOS PARA SENSORES REFLETANCIA-----//

//-----REFERÊNCIAS BRANCO E PRETO------//
// BRANCO = 1
// PRETO = 0
// BRANCO > 70
// PRETO >= 70
//CASO 1: Esq: 1; Dir: 1
//CASO 2: Esq: 1; Dir: 0
//CASO 3: Esq: 0; Dir: 1
//CASO 4: Esq: 0; Dir: 0

float valorSensorEsq;
float valorSensorDir;

void setup(){
	Serial.begin(9600);
	robo.configurar();
}

void loop(){
	valorSensorEsq = robo.lerSensorLinhaEsq();         //le um valor do sensor. O sensor retornar um valor de 0 100
	valorSensorDir = robo.lerSensorLinhaDir();         //le um valor do sensor. O sensor retornar um valor de 0 100

	//Impressão dos valores dos sensores
	if (valorSensorEsq > 70 && valorSensorDir > 70) {
		//ROBÔ SEGUIR RETO
	}
	else if (valorSensorEsq > 70 && valorSensorDir <= 70) {
		//ROBÔ FAZER CURVA LEVE PARA A DIREITA
	}
	else if(valorSensorEsq <= 70 && valorSensorDir > 70) {
		//ROBÔ FAZER CURVA LEVE PARA A ESQUERDA
	}
	else {
		//AINDA VOU DESCOBRIR
	}

	delay(1000);

}

