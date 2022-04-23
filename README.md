# Jokenpo-Game.py
Jokenpo.py
import random
modo_jogo = 0
player_1 = 0
player_2 = 0
vitorias_player_1 = 0
vitorias_player_2 = 0
numero_partidas_total = 0
numero_empates = 0
jogar_novamente = 0
print("Bem vindo ao Jokenpo!")
print("Modos de jogo:")
while modo_jogo < 1 or modo_jogo > 3:
 print("1 - Humano X Humano")
 print("2 - Humano X Computador")
 print("3 - Computador X Computador")
 print()
 modo_jogo = int(input("Escolha o modo de jogo = "))
print()
print("Pedra = 1")
print("Papel = 2")
print("Tesoura = 3")
print()
while jogar_novamente != 2:
 jogar_novamente = 0
 if modo_jogo == 1:
 while player_1 < 1 or player_1 > 3:
 player_1 = int(input("player_1, digite um numero de 1 a 3 = "))
 while player_2 < 1 or player_2 > 3:
 player_2 = int(input("player_2, digite um numero de 1 a 3 = "))
 elif modo_jogo == 2:
 while player_1 < 1 or player_1 > 3:
 player_1 = int(input("player_1, digite um numero de 1 a 3 = "))
 player_2 = random.randint(1, 3)
 print("Computador jogou = ", player_2)
 elif modo_jogo == 3:
 player_1 = random.randint(1, 3)
 player_2 = random.randint(1, 3)
 print("Computador1 jogou = ", player_1)
 print("Computador2 jogou = ", player_2)
 numero_partidas_total = numero_partidas_total + 1
 if ((player_1 == 1) and (player_2 == 3)) or ((player_1 == 2) and (player_2 == 
1)) or ((player_1 == 3) and (player_2 == 2)):
 if(modo_jogo == 3):
 print("Computador1 ganhou")
 else:
 print("player_1 ganhou")
 vitorias_player_1 = vitorias_player_1 + 1
 elif (player_1 == player_2):
 print("Deu empate")
 numero_empates = numero_empates + 1
 else:
 if(modo_jogo == 3):
 print("Computador2 ganhou")
 elif(modo_jogo == 2):
 print("Computador ganhou")
 else: 
 print("player_2 ganhou")
 vitorias_player_2 = vitorias_player_2 + 1
 player_1 = 0
 player_2 = 0
 print()
 while jogar_novamente < 1 or jogar_novamente > 2:
 jogar_novamente = int(input("Deseja jogar novamente? 1 = sim 2 = nao: "))
 print()
print()
print("Numero total de partidas =", numero_partidas_total)
if(modo_jogo == 1):
 print("Porcentagem de vitorias do player_1 =", ((vitorias_player_1 / 
numero_partidas_total) * 100))
 print("Porcentagem de vitorias do player_2 =",((vitorias_player_2 / 
numero_partidas_total) * 100))
elif(modo_jogo == 2):
 print("Porcentagem de vitorias do player_1 =", ((vitorias_player_1 / 
numero_partidas_total) * 100))
 print("Porcentagem de vitorias do Computador =",((vitorias_player_2 / 
numero_partidas_total) * 100))
else:
 print("Porcentagem de vitorias do Computador1 =",((vitorias_player_1 / 
numero_partidas_total) * 100))
 print("Porcentagem de vitorias do Computador2 =",((vitorias_player_2 / 
numero_partidas_total) * 100))
print("Numero de empates =", numero_empates)
