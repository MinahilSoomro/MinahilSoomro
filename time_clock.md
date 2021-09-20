#Clock project by coding with evan
from tkinter import *
from tkinter.ttk import *

from time import strftime

master = Tk()
master.title("Digital Clock")

def time():
    string = strftime('%I %M %S %p')
    label.config(text=string)
    label.after(1000, time)

label = Label(master, font = ("ds-digital", 80), background = "Black", foreground = "white")
label.pack(anchor = 'center')
time()

master.mainloop()
