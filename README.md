# exer-python
Exercícios retirados do curso de python no canal curso em video no Youtube

DESAFIO (088) - Faça um programa que ajuda um jogador da MEGA SENA a criar palpites.  O programa vai perguntar quantos jogos serão gerados vai sortear 6 números entre 1 e 60 para cada jogo.cadastrando tudo em uma lista composta.

Resolução :
```from random import randint
from time import sleep
lista = list()
palpite = list()
print(f'{"Palpites na Mega-Sena":=^60}')
while True :
    palpite.clear()
    jogo = int(input("Quantos palpites deseja ver : "))
    limit = 0
    while jogo > limit :    
        cont = 0
        while True :
            num = randint(1,60)
            if num not in lista :
                lista.append(num)
            cont += 1
            if cont >= 6 :
                lista.sort()
                palpite.append(lista[:])
                lista.clear()
                break
        limit += 1
    print(f'Gerando {jogo} palpites...')
    sleep(1)
    for indice ,p in enumerate(palpite):
        print(f'jogo {indice + 1} : {p}')
        sleep(1)
    conf = str(input("Quer Novos Palpites [S/N] : ")).strip()[0]
    while conf not in "SsNn" :
        conf = str(input("Tente Novamente!!!. Quer Novos Palpites [S/N] : ")).strip()[0]
    print("-=" * 30)
```
testando o termux!!!
testando novamente???!!!
