# jokenpo
Código de jogo desenvolvido para fim acadêmico.

from random import randint
from time import sleep
itens = ( 'pedra', 'papel', 'tesoura')
computador = randint(0, 2)



print('#'*20)
print("JOKENPO!")
print('#'*20)
print("Você não desiste mesmo.. Se chegou até aqui, sabe das consequências!")
jogar = str(input("Sim ou Não: ")).strip().upper()

if jogar in 'SIM':
    print("Vamos lá, o JokenPo pode separar vidas e agora não será diferente!"
          "que a sorte te acompanhe.")

else:
    print("Te pegaremos na próxima!")
    exit()


print('suas opções:'
'[ 0 ] PEDRA',
'[ 1 ] PAPEL',
'[ 2 ] TESOURA')
jogador = int(input('Qual é a sua jogada?'))


print('Jo')
sleep(1.5)
print('Ken')
sleep(1)
print('Po !!')

print('#' * 15)
print('computador jogou {}'.format(itens[computador]))
print('o jogador jogou {}'.format(itens[jogador]))
print('#' * 15)
if computador == 0: #computador jogou PEDRA
    if jogador == 0:
        print('empate. não foi dessa vez.')
    elif jogador == 1:
        print('papel enrola a pedra. Você deu sorte..')
    elif jogador == 2:
        print('pedra quebra a tesoura. Mais sorte na próxima! haha')
    else:
        print('JOGADA INVÁLIDA!')

elif computador == 1: #computador jogou PAPEL
    if jogador == 0:
        print('papel enrola a pedra. Mais sorte na próxima! haha')
    elif jogador == 1:
        print('empate. não foi dessa vez.')
    elif jogador == 2:
        print('tesoura corta o papel. Você deu sorte..')
    else:
        print('JOGADA INVÁLIDA!')

elif computador == 2: #computador jogou TESOURA
    if jogador == 0:
        print('pedra quebra a tesoura. Você deu sorte..')
    elif jogador == 1:
        print('tesoura corta o papel. Mais sorte na próxima! haha ')
    elif jogador == 2:
        print('empate. não foi dessa vez.')
    else:
        print('JOGADA INVÁLIDA!')
