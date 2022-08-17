# Exerc-cio-1-timmer-micros

#include "stm32f4xx.h"

float calcula();
void delay();

int main(void)
{
RCC->APB2ENR|=0x40000;
RCC->AHB1ENR=0x87;
TIM11->CR1=0x05;
TIM11->PSC=calcula();
TIM11->ARR=999;
GPIOC->MODER|=0x28555501;

  while (1)
  {
		  delay();
		  GPIOC->ODR ^= 0x1;
  }
}

void delay()
{
	while ((TIM11->SR&0x01)==0){}
	TIM11->SR&=~(0x01);
}

float calcula()
{
	float psc;
	int freq;
	freq=5;
	psc=(16000000/(1000*freq))-1;
	return psc;
}


