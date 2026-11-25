# Rock-Paper-Scissors
Rock, Paper, Scissors
import random


def getcomputer_choice():
  choice = ['камень', 'ножницы', 'бумага']
  return random.choice(choice)


def detmine_win(player, computer):
  if player == computer:
    return 'equal'

  if (
      (player == 'камень' and computer == 'ножницы')
      or (player == 'ножницы' and computer == 'бумага')
      or (player == 'бумага' and computer == 'камень')
  ):
    return 'player'
  else:
    return 'computer'


def main():
  i = 0
  n = 0
  print('Приветствую тебя в игре Камень-Ножницы-Бумага!')
  print('Введите: камень / ножницы / бумага')

  while True:
    player = input('Выбери свой ход: ')
    computer = getcomputer_choice()
    result = detmine_win(player, computer)
    if result == 'equal':
      comp_score = i = i + 0
      player_score = n = n + 0
      print(f'НИЧЬЯ! счет: Я {comp_score}|{player_score} Вы')
    elif result == 'player':
      comp_score = i = i + 0
      player_score = n = n + 1
      print(
          f'ВЫ ПОБЕДИЛИ ЭТУ БИТВУ, НО НЕ ВОЙНУ! счет: Я {comp_score}|{player_score} Вы'
      )
    else:
      comp_score = i = i + 1
      player_score = n = n + 0
      print(
          f'Я ПОБЕДИЛ ЭТУ БИТВУ, НО У ТЕБЯ ЕСТЬ ШАНС ПОБЕДИТЬ ВОЙНУ! счет: Я {comp_score}|{player_score} ВЫ'
      )
    if i == 3:
      print('ЖАЛКИЙ ЧЕЛОВЕК! ТЫ ПРОИГРАЛ МОЕМУ МОГУЩЕСТВУ!!!')
      break
    elif n == 3:
      print('Вы Разгромили Мой Флот :( ')
      break


main()
