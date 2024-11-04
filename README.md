def calculate():
    operation = input('''
Selecione o tipo da equacao desejada
+ para adicao
- para subtracao
* para multiplicacao
/ para divisao
''')

    number_1 = int(input('Insira o primeiro numero: '))
    number_2 = int(input('Insira o segundo numero: '))

    if operation == '+':
        print('{} + {} = '.format(number_1, number_2))
        print(number_1 + number_2)

    elif operation == '-':
        print('{} - {} = '.format(number_1, number_2))
        print(number_1 - number_2)

    elif operation == '*':
        print('{} * {} = '.format(number_1, number_2))
        print(number_1 * number_2)

    elif operation == '/':
        print('{} / {} = '.format(number_1, number_2))
        print(number_1 / number_2)

    else:
        print('Valor nao suportado')

    # Add again() function to calculate() function
    again()

def again():
    calc_again = input('''
Voce gostaria de calcular uma nova equacao?
Digite S para SIM ou N para NAO.
''')

    if calc_again.upper() == 'S':
        calculate()
    elif calc_again.upper() == 'N':
        print('Ate logo')
    else:
        again()

calculate()

