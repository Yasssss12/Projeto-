# Projeto-
def mostrar_menu():

print("=== Diário de Reflexões ===")

print("1. Adicionar reflexão"

print("2. Ver reflexões")

print("3. Sair")

def adicionar_reflexao():

reflexao = input("Digite sua reflexão: ")

with open("reflexoes.txt", "a") as arquivo: arquivo.write(reflexao + "\n")

print("Reflexão adicionada com sucesso!")

def ver_reflexoes():

try:

with open("reflexoes.txt", "r") as arquivo: reflexoes = arquivo.readlines() if reflexoes: print("\n=== Suas Reflexões ===") for i, r in enumerate (reflexoes, 1): print(f"{i}. {r.strip())")

else:

print("Nenhuma reflexão salva ainda.")

except FileNotFoundError: print("Nenhuma reflexão salva ainda.")

def main():

while True:

mostrar_menu() escolha = input("Escolha uma opção: ")

if escolha == "1":

adicionar_reflexao()

elif escolha == "2":

ver_reflexoes()

elif escolha == "3": print("Saindo do diário. Até mais!") break

else:

print("Opção inválida! Tente novamente.")

if __name__ == "__main__":

main()
