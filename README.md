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
        
# 4) Dois veículos (um carro e um caminhão) saem respectivamente de cidades opostas pela mesma rodovia. O carro de Ribeirão Preto em direção 
a Franca, a uma velocidade constante de 110 km/h e o caminhão de Franca em direção a Ribeirão Preto a uma velocidade constante de 80 km/h. 
Quando eles se cruzarem na rodovia, qual estará mais próximo a cidade de Ribeirão Preto?

a) Considerar a distância de 100km entre a cidade de Ribeirão Preto <-> Franca.
b) Considerar 2 pedágios como obstáculo e que o caminhão leva 5 minutos a mais para passar em cada um deles e o carro possui tag de pedágio (Sem Parar)
c) Explique como chegou no resultado.

    Quando o carro e o caminhão se cruzarem na rodovia, eles terão percorrido juntos uma distância igual a 100 km (distância entre Ribeirão Preto e Franca). O tempo que cada veículo leva para percorrer essa distância é dado por:

    - Tempo do carro = Distância / Velocidade = 100 km / 110 km/h = 0,91 horas
    - Tempo do caminhão = Distância / Velocidade = 100 km / 80 km/h = 1,25 horas
    - No entanto, o caminhão leva mais 5 minutos (ou 0,0833 horas) em cada um dos dois pedágios, totalizando 10 minutos (ou 0,1667 horas) a mais em 
    todo o trajeto. Assim, o tempo total do caminhão será:
    - Tempo total do caminhão = Tempo do caminhão + tempo nos pedágios = 1,25 horas + 0,1667 horas = 1,4167 horas
    - Agora, para determinar qual veículo estará mais próximo de Ribeirão Preto quando se cruzarem, basta calcular a distância percorrida por cada um:
    - Distância percorrida pelo carro = Velocidade x Tempo do carro = 110 km/h x 0,91 horas = 100 km
    - Distância percorrida pelo caminhão = Velocidade x Tempo do caminhão = 80 km/h x 1,4167 horas = 113,33 km
    
    Portanto, quando se cruzarem, o carro estará mais próximo de Ribeirão Preto, pois terá percorrido uma distância de exatamente 100 km, enquanto o caminhão terá percorrido uma distância de 113,33 km.

# 5) Escreva um programa que inverta os caracteres de um string.
    a) Essa string pode ser informada através de qualquer entrada de sua preferência ou pode ser previamente definida no código;
    b) Evite usar funções prontas, como, por exemplo, reverse;

    print("--------------------------------------------")
    string = input("-  Informe uma string: ")
    print("--------------------------------------------")

    string_invertido = ""
    for i in range(len(string)-1, -1, -1):
        string_invertido += string[i]

    print("A string invertida é:", string_invertido)
