# Desenvolvimento-de-Sistema
Cód aula pratica de python
''' === MINHAS TAREFAS ===
1 - Adicionar tarefa
2 - Visualizar tarefas
3 - Ver quantidade de tarefas
4 - Verificar se uma tarefa está na lista
5 - Remover tarefa
0 - Sair '''


minhas_tarefas=[]

lista = " "
opcao = -99
while (opcao != 0):
    
    tarefa =    "1 - Adicionar tarefa : "
    tarefa += "\n2 - Visualizar tarefa: "
    tarefa += "\n3 - Quantidade de tarefas: "
    tarefa += "\n4 - Verificar se tarefa está na lista:"
    tarefa += "\n5 - Remover tarefa: "
    tarefa += "\n0 - Sair \n"

    opcao = int(input(tarefa))
    match(opcao):
        
        case 1:
            nome = input(f" Informe a descrição da tarefa: ")
            if nome not  in minhas_tarefas:
                minhas_tarefas.append(nome)
        
        case 2: 
            if(len(minhas_tarefas) >0 ):
                print(f"Visualizar tarefa: {minhas_tarefas}\n") 
                
            else:
                print("Não há tarefas: ")
            
    
        case 3:
            nome = input(f"Quantidade tarefas: {len(minhas_tarefas)}  Descrições: {minhas_tarefas}")
              
        
    
        case 4:
            nome = input("Verificar se tarefa está na lista: ")
            if nome in minhas_tarefas:
                print(f"Tarefa esta em sua lista: {minhas_tarefas}")
                
            else: 
                print(f"Item não está na lista{minhas_tarefas}\n")   
            
        case 5:
            nome = input("Remover tarefa: ")
            minhas_tarefas.remove(nome)
            print(f"{minhas_tarefas} removido da lista...")     
            
        case 0:
            nome = input("Para sair Digite 0 na proxima tela: ")
            print(f"Até logo")
            

            
        case _:  
            print( "Opção invalida, tente novamente! \n" )
            
            
    
            
            
    
            
            
                
