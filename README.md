# paint
# Библиотека для работы с графическим интерфейсом
import tkinter as tk
from tkinter import colorchooser

def choose_color():
    # Открываем окно выбора цвета
    color_code = colorchooser.askcolor(title="Выберите цвет краски")
    # Изменяем цвет фона окна на выбранный цвет
    if color_code[1] is not None:
        window.config(bg=color_code[1])

# Создаем главное окно
window = tk.Tk()
window.title("Выбор цвета краски")
window.geometry("400x300")

# Кнопка для вызова диалога выбора цвета
choose_color_button = tk.Button(window, text="Выбрать цвет краски", command=choose_color)
choose_color_button.pack(pady=20)

# Запуск главного цикла обработки событий
window.mainloop()
