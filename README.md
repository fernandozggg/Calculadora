# Calculadora
class Calculadora:
    def __init__(self) -> None:
        pass
    def soma(self, n1, n2):
        return n1 + n2
    
    def subt(self, n1, n2):
        return n1 - n2
    
    def div(self, n1, n2):
        if n2 == 0:
            return "Erro: Divisão por zero!"
        else:
            return n1 / n2
    
    def vezes(self, n1, n2):
        return n1 * n2

Segunda Parte separada 
from calculadora import Calculadora
minha_calculadora = Calculadora()
while True:

    numero1 = float(input("Digite o primeiro número: "))
    numero2 = float(input("Digite o segundo número: "))
    operacao = input("Digite a operação desejada (+, -, *, /): ")

    if operacao == "s":
        print("Encerrando a calculadora")   
        break

    if operacao == '+':
        resultado = minha_calculadora.soma(numero1, numero2)
    elif operacao == '-':
        resultado = minha_calculadora.subt(numero1, numero2)
    elif operacao == '*':
        resultado = minha_calculadora.vezes(numero1, numero2)
    elif operacao == '/':
        resultado = minha_calculadora.div(numero1, numero2)
    else:
        resultado = "Operação inválida!"

    print("Resultado:", resultado)
