def soma(a, b):
    return a + b

def subtracao(a, b):
    return a - b

def multiplicacao(a, b):
    return a * b

def divisao(a, b):
    if b == 0:
        return "Erro: Divisão por zero!"
    return a / b

def main():
    print("Calculadora Simples")
    print("Selecione a operação:")
    print("1. Soma")
    print("2. Subtração")
    print("3. Multiplicação")
    print("4. Divisão")

    while True:
        operacao = input("Escolha uma operação (1/2/3/4): ")

        if operacao in ('1', '2', '3', '4'):
            try:
                num1 = float(input("Digite o primeiro número: "))
                num2 = float(input("Digite o segundo número: "))
            except ValueError:
                print("Por favor, insira um número válido.")
                continue

            if operacao == '1':
                print(f"{num1} + {num2} = {soma(num1, num2)}")

            elif operacao == '2':
                print(f"{num1} - {num2} = {subtracao(num1, num2)}")

            elif operacao == '3':
                print(f"{num1} * {num2} = {multiplicacao(num1, num2)}")

            elif operacao == '4':
                print(f"{num1} / {num2} = {divisao(num1, num2)}")

            # Pergunta se o usuário quer fazer outra operação
            nova_operacao = input("Deseja fazer outra operação? (s/n): ")
            if nova_operacao.lower() != 's':
                break
        else:
            print("Operação inválida. Por favor, escolha uma operação válida.")

if __name__ == "__main__":
    main()
