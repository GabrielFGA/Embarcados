  1. Cite as vantagens e desvantagens das comunicação serial:
  (a) Assíncrona (UART).
  
      Necessita apenas de dois fios e possui a vantagem de trafegar dados nas duas direções ao mesmo tempo. Entretanto, tem a            desvantagem de ser síncrona,
      fazendo necessária a pré-configuração em ambos os dispositivos para que estes saibam qual a frequencia, qual a baud-rate e etc, além de ser mais suscetível
      a erros. 
      
  (b) SPI.
  
      Necessita 3 fios, porém, por ser síncrona, estabelecer a conexão exige menos configurações e a chance de erro é menor.

  2. Considere o caso em que a Raspberry Pi deve receber leituras analógico/digitais de um MSP430, e que a comunicação entre os dois é UART.
  É tecnicamente possível que o MSP430 mande os resultados da conversão A/D a qualquer hora, ou ele deve aguardar a Raspberry Pi fazer um
  pedido ao MSP430? Por quê?
  
      Sim, é possível que ele mande a qualquer hora, pois o início de uma comunicação UART é definido pelo pelo dispositivo a qualquer momento
      bastando mandar um bit de start.      

  3. Considere o caso em que a Raspberry Pi deve receber leituras analógico/digitais de um MSP430, que a comunicação entre os dois seja SPI, e que o 
  MSP430 seja o escravo. É tecnicamente possível que o MSP430 mande os resultados da conversão A/D a qualquer hora, ou ele deve aguardar a Raspberry 
  Pi fazer um pedido ao MSP430? Por quê?
  
      Não, no SPI o mestre deve requisitar a leitura de dado e só aí o escravo manda.

  4. Se o Raspberry Pi tiver de se comunicar com dois dispositivos via UART, como executar a comunicação com o segundo dispositivo?
  
      Adiciona-se um bit adicional em que permite direcionar a comunicação para um endereço específico. Esse bit de endereço define se
      o valor anterior a ele se referia a um dado ou a um endereço.

  5. Se o Raspberry Pi tiver de se comunicar com dois dispositivos via SPI, como executar a comunicação com o segundo dispositivo?
  
      Adiciona-se mais um fio para seleção do dispositivo escravo. Para cada escravo é adicionado um fio extra de endereçamento.
