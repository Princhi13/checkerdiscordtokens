import keyboard
import time
import os
import sys
import pyperclip
from tkinter import *
from tkinter import ttk
import colorama
from colorama import Fore, Back, Style
colorama.init()
file_path = '1.txt'
keyword = 'https://discord.com/channels/@me'
keywordtwo = 'https://discord.com/app'

print(' ')
print('soft for discord by princhi')
print(' ')

print('1 - discord token checker')
print('wrote mode.')
mode = input()
if mode == '1':
    print('Write the token.')
    token = input()
    print('У вас есть 5 секунд чтобы альтабнуться в браузер')
    time.sleep(5)
    keyboard.press('ctrl+t')
    keyboard.write('https://discord.com/login#tokenlogin')
    keyboard.press('ENTER')
    time.sleep(5)
    keyboard.write(token)
    keyboard.press('ENTER')
    time.sleep(7)
    keyboard.press('ctrl+a')
    keyboard.press_and_release('ctrl+c')
    os.system('start 1.txt')
    time.sleep(2)
    keyboard.press('ctrl+a')
    keyboard.press('DELETE')
    keyboard.press('ctrl+v')
    keyboard.press('ctrl+s')
    time.sleep(2)
    root = Tk()
    root.title("Окно")
    root.geometry("250x150")
    label = ttk.Label()
    label.pack(anchor=NW)
    with open(file_path, 'r') as file:
        for line in file:
            if keyword in line:
                os.system('cls')
                label["text"] = "Token is Works\nНажмите контрол дабы избежать баги."
            else:
                os.system('cls')
                label["text"] = "Token is Nor Works\nНажмите контрол дабы избежать баги."
else:
    print('ERROR')
print('press enter to continue')
input()
time.sleep(0.75)
print('Напишите 1 чтобы выйти из программы.')
print('Напишите 2 чтобы перезагрузить программу.')
questionquit = input()
if questionquit == '1':
    os.system('cls')
    print('1')
    time.sleep(1)
    print('2')
    time.sleep(1)
    print('3')
    time.sleep(1)
    exit()
elif questionquit == '2':
    print('Как у вас называеться программа? С форматом.')
    hownameofprogramm = input()
    os.system('cls')
    print('1')
    time.sleep(1)
    print('2')
    time.sleep(1)
    print('3')
    time.sleep(1)
    os.system('cls')
    os.system('start ' + hownameofprogramm)
    exit()
input()