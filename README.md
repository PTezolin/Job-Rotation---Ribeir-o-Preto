# Job-Rotation---Ribeir-o-Preto
Realização da atividade

# 1) Observe o trecho de código abaixo:
int INDICE = 13, SOMA = 0, K = 0;
enquanto K < INDICE faça { K = K + 1; SOMA = SOMA + K;}
imprimir(SOMA);

Nesse codigo três variáveis são definidas: INDICE com valor 13, SOMA com valor 0 e K com valor 0. 
Em seguida, o laço de repetição é iniciado a condição de que enquanto K for menor que INDICE, o bloco de código dentro do laço será executado. Dentro do laço, K é incrementado em 1 a cada iteração e SOMA é atualizado adicionando-se K a ela.

Quando o valor de K for igual a 13, que é o valor de INDICE, a condição do laço deixará de ser verdadeira e a execução do laço será interrompida. Por fim, o valor atual de SOMA (1 + 2 + 3 + 4 + 5 + 6 + 7 + 8 + 9 + 10 + 11 + 12 + 13 = 91) é impresso na tela.

Assim, ao final do processamento, a variável SOMA terá o valor 91, que é a soma dos números de 1 a 13.

# 2) Dado a sequência de Fibonacci
Onde se inicia por 0 e 1 e o próximo valor sempre será a soma dos 2 valores anteriores (exemplo: 0, 1, 1, 2, 3, 5, 8, 13, 21, 34...), escreva um programa na linguagem que desejar onde, informado um número, ele calcule a sequência de Fibonacci e retorne uma mensagem avisando se o número informado pertence ou não a sequência.

print("-----------------------------------------------------------------")
print("      Verificador de pertencimento à sequência de Fibonacci      ")
print("-----------------------------------------------------------------")

while True:
    num_str = input("Informe o número que você deseja verificar ou digite 0 para sair: ")

    if num_str == "0":
        print("Programa encerrado!\n")
        break

    try:
        num_float = float(num_str)
        num_int = int(num_float)
        if num_int != num_float:
            print("Valor inválido. O número deve ser um inteiro.\n")
            continue
    except ValueError:
        print("Valor inválido. O número deve ser um inteiro.\n")
        continue

    if num_int <= 0:
        print("Valor inválido. O número deve ser maior que zero.\n")
        continue

    fib1, fib2 = 0, 1
    while fib2 < num_int:
        fib1, fib2 = fib2, fib1 + fib2

    if fib2 == num_int:
        print(num_int, "pertence à sequência de Fibonacci\n")
    else:
        print(num_int, "não pertence à sequência de Fibonacci\n")

# 3) Descubra a lógica e complete o próximo elemento:
      a) 1, 3, 5, 7, ___
          R: 9 (adição de 2 a cada elemento)
      b) 2, 4, 8, 16, 32, 64, ____
          R: 128 (multiplicação por 2 a cada elemento)
      c) 0, 1, 4, 9, 16, 25, 36, ____
          R: 49 (adição de 3 a cada elemento)
      d) 4, 16, 36, 64, ____
          R: 100 (adição de 4² a cada elemento)
      e) 1, 1, 2, 3, 5, 8, ____
          R: 13 (adição dos dois elementos anteriores)
      f) 2,10, 12, 16, 17, 18, 19, ____
          R: 27 (sequencia de soma seria 8, 2, 4, 1, 1, 1, 1, se iniciando novamente completar a sequencia)
        
