Documentação: Calculadora de Média
O que é?
Um sistema simples para calcular a média de notas e verificar a aprovação. Ele usa dois arquivos que trabalham juntos:

calcula_notas.sh: O arquivo que você executa. Ele inicia o programa.

calcula_notas.py: O arquivo que faz os cálculos (média, pontos extras, aprovação).

Como Usar
1. Preparação
Requisitos: Tenha Python 3 instalado e esteja em um sistema como o Linux.

Crie os arquivos:

Crie calcula_notas.py e cole este código Python nele:

Python

nota = input("qual sua nota? ")
nota2 = input("qual sua nota? ")
nota = int(nota)
nota2 = int(nota2)

media = (nota + nota2)/2
print(f"sua media é: {media}")

pontos_extra = input("quantos pontos extra você tem? ")
pontos_extra = int(pontos_extra)

media_final = media + pontos_extra
print(f"sua media final é: {media_final}")

if media_final >= 70:
  print("Parabéns, você passou!")
else:
  print("Estude mais!")
  faltou = 70 - media_final
  print(f"Faltou {faltou} pontos para passar.")
Crie calcula_notas.sh (na mesma pasta) e cole este código Bash nele (ajuste o nome do .py se necessário):

Bash

#!/bin/bash
echo "--- Iniciando o cálculo de notas ---"
python3 ./calcula_notas.py # Ou ./SEU_NOME_DO_ARQUIVO.py
echo "--- Cálculo de notas finalizado! ---"
2. Execução
Abra o terminal na pasta dos arquivos.

Dê permissão de execução ao .sh: chmod +x calcula_notas.sh

Execute: ./calcula_notas.sh

Siga as instruções no terminal (digite notas e pontos extras).
