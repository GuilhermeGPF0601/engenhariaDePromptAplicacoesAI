def calculadora():
    print("--- Calculadora Simples ---")
    
    # Entrada de dados
    num1 = float(input("Digite o primeiro número: "))
    operacao = input("Escolha a operação (+, -, *, /): ")
    num2 = float(input("Digite o segundo número: "))

    # Processamento e Saída
    if operacao == "+":
        resultado = num1 + num2
    elif operacao == "-":
        resultado = num1 - num2
    elif operacao == "*":
        resultado = num1 * num2
    elif operacao == "/":
        # Verificação básica para não dividir por zero
        if num2 == 0:
            return "Erro: Não é possível dividir por zero!"
        resultado = num1 / num2
    else:
        return "Operação inválida!"

    return f"Resultado: {resultado}"

# Executa a função
print(calculadora())
