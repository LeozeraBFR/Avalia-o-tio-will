# AVALIAÇÃO TIO WILL

lista_nomes = []  
primeira_nota = []  
segunda_nota = []  
terceira_nota = []  
lista_medias = []  
status_aluno = []  


total_alunos = int(input("Quantos alunos você quer cadastrar? "))


for contador in range(total_alunos):
    print(f"\n--- Cadastrando aluno {contador + 1} ---")
    
    # Pedindo o nome
    nome_aluno = input("Nome do aluno: ")
    lista_nomes.append(nome_aluno)  
    
    # Pedindo as 3 notas
    nota_1 = float(input("Primeira nota: "))
    primeira_nota.append(nota_1)
    
    nota_2 = float(input("Segunda nota: "))
    segunda_nota.append(nota_2)
    
    nota_3 = float(input("Terceira nota: "))
    terceira_nota.append(nota_3)
    
    # Calculando a média
    media_final = (nota_1 + nota_2 + nota_3) / 3
    lista_medias.append(media_final)
    
    # Media
    if media_final >= 7.0:
        resultado = "Aprovado 👌"  
    elif media_final >= 5.0:
        resultado = "Recuperação 😒"  
    else:
        resultado = "Reprovado 😢"  
    
    status_aluno.append(resultado)

# Boletin
print("\n" + "="*50)
print("BOLETIM DA TURMA")
print("="*50)

# Cadastro dos alunos
for posicao in range(total_alunos):
    print(f"\nAluno: {lista_nomes[posicao]}")
    print(f"Notas: {primeira_nota[posicao]} | {segunda_nota[posicao]} | {terceira_nota[posicao]}")
    print(f"Média final: {lista_medias[posicao]:.2f}")
    print(f"Situação: {status_aluno[posicao]}")
    print("-"*30)
