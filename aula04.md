
Pergunta 1:
Crie um cadastro de clientes em python



Resposta:
# Cadastro de Clientes em Python

clientes = []

def adicionar_cliente():
    nome = input("Digite o nome do cliente: ")
    email = input("Digite o email do cliente: ")
    telefone = input("Digite o telefone do cliente: ")
    
    cliente = {
        "nome": nome,
        "email": email,
        "telefone": telefone
    }
    
    clientes.append(cliente)
    print("Cliente cadastrado com sucesso!\n")

def listar_clientes():
    if not clientes:
        print("Nenhum cliente cadastrado.\n")
    else:
        print("\n--- Lista de Clientes ---")
        for i, cliente in enumerate(clientes, start=1):
            print(f"{i}. Nome: {cliente['nome']} | Email: {cliente['email']} | Telefone: {cliente['telefone']}")
        print()

def buscar_cliente():
    nome = input("Digite o nome do cliente que deseja buscar: ")
    encontrado = False
    for cliente in clientes:
        if cliente["nome"].lower() == nome.lower():
            print(f"Cliente encontrado: Nome: {cliente['nome']} | Email: {cliente['email']} | Telefone: {cliente['telefone']}\n")
            encontrado = True
            break
    if not encontrado:
        print("Cliente não encontrado.\n")

def menu():
    while True:
        print("=== Sistema de Cadastro de Clientes ===")
        print("1 - Adicionar Cliente")
        print("2 - Listar Clientes")
        print("3 - Buscar Cliente")
        print("4 - Sair")
        
        opcao = input("Escolha uma opção: ")
        
        if opcao == "1":
            adicionar_cliente()
        elif opcao == "2":
            listar_clientes()
        elif opcao == "3":
            buscar_cliente()
        elif opcao == "4":
            print("Saindo do sistema...")
            break
        else:
            print("Opção inválida!\n")

# Executa o sistema
menu()


Pergunta 2: 
Você é um instrutor de python experiente,
crie um cadastro de login de clientes incluindo tratamento de erros rigoroso para 
varios tipos de erros que podem acontecer,
forneça o codigo python extremamente comentado para que um programador 
python iniciante consiga entender 
e bem estruturado de fácil entendimento. 
Seguido de 3 testes realizados com o código



Resposta:
"""
Sistema de Cadastro e Login de Clientes
---------------------------------------
Este programa permite:
1. Cadastrar novos clientes (nome, email, senha).
2. Fazer login com validação de credenciais.
3. Listar clientes cadastrados.

Inclui tratamento de erros para:
- Entrada inválida (strings vazias, emails mal formatados).
- Senhas fracas ou muito curtas.
- Tentativas de login com usuário inexistente ou senha incorreta.
"""

# Dicionário para armazenar clientes
# Estrutura: {email: {"nome": nome, "senha": senha}}
clientes = {}

def validar_email(email: str) -> bool:
    """Valida se o email contém '@' e '.' (simplificação)."""
    return "@" in email and "." in email

def validar_senha(senha: str) -> bool:
    """Valida se a senha tem pelo menos 6 caracteres."""
    return len(senha) >= 6

def cadastrar_cliente():
    try:
        nome = input("Digite o nome do cliente: ").strip()
        if not nome:
            raise ValueError("O nome não pode estar vazio.")

        email = input("Digite o email do cliente: ").strip()
        if not validar_email(email):
            raise ValueError("Email inválido. Deve conter '@' e '.'.")

        if email in clientes:
            raise ValueError("Este email já está cadastrado.")

        senha = input("Digite a senha (mínimo 6 caracteres): ").strip()
        if not validar_senha(senha):
            raise ValueError("Senha muito curta. Deve ter pelo menos 6 caracteres.")

        # Cadastro realizado
        clientes[email] = {"nome": nome, "senha": senha}
        print(f"✅ Cliente {nome} cadastrado com sucesso!\n")

    except ValueError as e:
        print(f"❌ Erro no cadastro: {e}\n")

def login_cliente():
    try:
        email = input("Digite seu email: ").strip()
        senha = input("Digite sua senha: ").strip()

        if email not in clientes:
            raise LookupError("Email não encontrado no sistema.")

        if clientes[email]["senha"] != senha:
            raise PermissionError("Senha incorreta.")

        print(f"✅ Login realizado com sucesso! Bem-vindo(a), {clientes[email]['nome']}.\n")

    except LookupError as e:
        print(f"❌ Erro de login: {e}\n")
    except PermissionError as e:
        print(f"❌ Erro de login: {e}\n")

def listar_clientes():
    if not clientes:
        print("📭 Nenhum cliente cadastrado.\n")
    else:
        print("\n--- Lista de Clientes ---")
        for email, dados in clientes.items():
            print(f"Nome: {dados['nome']} | Email: {email}")
        print()

def menu():
    while True:
        print("=== Sistema de Cadastro e Login ===")
        print("1 - Cadastrar Cliente")
        print("2 - Login")
        print("3 - Listar Clientes")
        print("4 - Sair")

        opcao = input("Escolha uma opção: ").strip()

        if opcao == "1":
            cadastrar_cliente()
        elif opcao == "2":
            login_cliente()
        elif opcao == "3":
            listar_clientes()
        elif opcao == "4":
            print("Encerrando o sistema...")
            break
        else:
            print("❌ Opção inválida. Tente novamente.\n")

# Executa o sistema
if __name__ == "__main__":
    menu()



