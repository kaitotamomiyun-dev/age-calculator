# age-calculator
```
import tkinter as tk
from datetime import datetime
from time import sleep
def calculate_age():
    try:
        birth_year = int(entry.get())
        current_year = datetime.now().year

        if birth_year > current_year:
            result_label.config(text="Bruh...Are you a time traveler")
        elif birth_year in [18, 19 , 20]:
            result_label.config(text=f"technically...humm...your not an adult...yet")
        elif current_year - birth_year > 120:
            result_label.config(text="the oldest human lived 122years🤓☝")
        elif birth_year == current_year:
            result_label.config(text="GUGU GAGA?")
        else:
            age = current_year - birth_year
            result_label.config(text=f"you have {age} years")

    except:
        result_label.config(text="kid, just type a valid number")

root = tk.Tk()
root.title("Age Calculator")
root.geometry("600x400")

tk.Label(root, text="Type your birth year(preferably something valid):").pack()

entry = tk.Entry(root)
entry.pack()

tk.Button(root, text="show your age", command=calculate_age).pack()

result_label = tk.Label(root, text="")
result_label.pack()

root.mainloop()
```
