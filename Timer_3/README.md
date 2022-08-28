#  Timer 3:
O led de status de um equipamento é utilizado para sinalizar sua condição de
operação, através de uma mensagem visual codificada como piscadas. O
período da mensagem é de 1s e o tempo de cada piscada é de 100 ms,
seguido por 100ms com o led apagado.
As mensagens seguem a codificação dada pela tabela abaixo:
                                                ____________________________________________________________________
                                                | Código |       Número piscadas      |        Significado         |
                                                |   0    |         Sempre aceso       |      Funcionamento ok      |
                                                |   1    |              1             |    Falha de comunicação    |
                                                |   2    |              2             |  Entradas digitais abertas |
                                                |   3    |              3             |       Termopar aberto      |
                                                |   4    |              4             |        Curto na saída      |
                                                |   5    |              5             |        Fusível aberto      |
                                                |________|____________________________|____________________________|
O led é ativo em HIGH, conectado ao PA8.
Utilize os pinos PB3, PB4 e PB5 para entrada do código. Podem ser
utilizados botões, chaves ou mesmo jumpers.
