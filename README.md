# time_day_date_by_python
from tkinter import *
from time import *
def update():
    time_string = strftime("%H:%M:%S")
    time_label.config(text=time_string)
    day_string = strftime("%A")
    day_label.config(text=day_string)
    date_string = strftime("%B %d,%Y")
    date_label.config(text=date_string)
    time_label.after(1000,update)
    
window = Tk()
time_label = Label(window,font=('Arial',50),fg='red',bg='green')
time_label.pack()

day_label = Label(window,font=("Ink Free",25))
day_label.pack()
date_label = Label(window,font=("Ink Free",25))
date_label.pack()

update()
window.mainloop()
