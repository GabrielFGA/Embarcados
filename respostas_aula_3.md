

Para todas as questões, compile-as com o gcc e execute-as via terminal.

   1. Crie um "Olá mundo!" em C.
    
    int main(){
        
        printf("Ola mundo!\n");
        
        return 0;
    }
    
   2. Crie um código em C que pergunta ao usuário o seu nome, e imprime no terminal "Ola " e o nome do usuário. Por exemplo, considerando que o código criado recebeu o nome de 'ola_usuario_1':

   $ ./ola_usuario_1
   $ Digite o seu nome: Eu
   $ Ola Eu

    int main(){
    
        char nome[255];
        
        printf("Digite seu nome:/n");
        scanf("%s", nome);
        printf("Ola %s", nome);
        
        return 0;    
    }

   3. Apresente os comportamentos do código anterior nos seguintes casos:

   (a) Se o usuário insere mais de um nome.
   
   $ ./ola_usuario_1
   $ Digite o seu nome: Eu Mesmo
   
     O segundo nome é suprimido.

   (b) Se o usuário insere mais de um nome entre aspas duplas. Por exemplo:

   $ ./ola_usuario_1
   $ Digite o seu nome: "Eu Mesmo"
   
    O segundo nome é suprimido e as aspas do início permaneceram: Ola "Gabriel

   (c) Se é usado um pipe. Por exemplo:

   $ echo Eu | ./ola_usuario_1

    O programa é completamente executado, ou seja, ele reconhece a entrada do nome como no caso normal.

   (d) Se é usado um pipe com mais de um nome. Por exemplo:

   $ echo Eu Mesmo | ./ola_usuario_1

    Só aparece o primeiro nome.

   (e) Se é usado um pipe com mais de um nome entre aspas duplas. Por exemplo:

   $ echo "Eu Mesmo" | ./ola_usuario_1

    Aparece o primeiro nome apenas, porém, sem as aspas.   

(f) Se é usado o redirecionamento de arquivo. Por exemplo:

$ echo Ola mundo cruel! > ola.txt
$ ./ola_usuario_1 < ola.txt

    Crie um código em C que recebe o nome do usuário como um argumento de entrada (usando as variáveis argc e *argv[]), e imprime no terminal "Ola " e o nome do usuário. Por exemplo, considerando que o código criado recebeu o nome de 'ola_usuario_2':

$ ./ola_usuario_2 Eu
$ Ola Eu

    Apresente os comportamentos do código anterior nos seguintes casos:

(a) Se o usuário insere mais de um nome.

$ ./ola_usuario_2 Eu Mesmo

(b) Se o usuário insere mais de um nome entre aspas duplas. Por exemplo:

$ ./ola_usuario_2 "Eu Mesmo"

(c) Se é usado um pipe. Por exemplo:

$ echo Eu | ./ola_usuario_2

(d) Se é usado um pipe com mais de um nome. Por exemplo:

$ echo Eu Mesmo | ./ola_usuario_2

(e) Se é usado um pipe com mais de um nome entre aspas duplas. Por exemplo:

$ echo Eu Mesmo | ./ola_usuario_2

(f) Se é usado o redirecionamento de arquivo. Por exemplo:

$ echo Ola mundo cruel! > ola.txt
$ ./ola_usuario_2 < ola.txt

    Crie um código em C que faz o mesmo que o código da questão 4, e em seguida imprime no terminal quantos valores de entrada foram fornecidos pelo usuário. Por exemplo, considerando que o código criado recebeu o nome de 'ola_usuario_3':

$ ./ola_usuario_3 Eu
$ Ola Eu
$ Numero de entradas = 2

    Crie um código em C que imprime todos os argumentos de entrada fornecidos pelo usuário. Por exemplo, considerando que o código criado recebeu o nome de 'ola_argumentos':

$ ./ola_argumentos Eu Mesmo e Minha Pessoa
$ Argumentos: Eu Mesmo e Minha Pessoa

    Crie uma função que retorna a quantidade de caracteres em uma string, usando o seguinte protótipo: int Num_Caracs(char *string); Salve-a em um arquivo separado chamado 'num_caracs.c'. Salve o protótipo em um arquivo chamado 'num_caracs.h'. Compile 'num_caracs.c' para gerar o objeto 'num_caracs.o'.

    Re-utilize o objeto criado na questão 8 para criar um código que imprime cada argumento de entrada e a quantidade de caracteres de cada um desses argumentos. Por exemplo, considerando que o código criado recebeu o nome de 'ola_num_caracs_1':

$ ./ola_num_caracs_1 Eu Mesmo
$ Argumento: ./ola_num_caracs_1 / Numero de caracteres: 18
$ Argumento: Eu / Numero de caracteres: 2
$ Argumento: Mesmo / Numero de caracteres: 5

    Crie um Makefile para a questão anterior.

    Re-utilize o objeto criado na questão 8 para criar um código que imprime o total de caracteres nos argumentos de entrada. Por exemplo, considerando que o código criado recebeu o nome de 'ola_num_caracs_2':

$ ./ola_num_caracs_2 Eu Mesmo
$ Total de caracteres de entrada: 25

    Crie um Makefile para a questão anterior.

