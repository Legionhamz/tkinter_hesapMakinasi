# tkinter_hesapMakinasi
import tkinter as tk


def topla():
    s1 = float(sayi1.get())
    s2 = float(sayi2.get())
    sonuc.configure(text= str(s1+s2))

def cikar():
    s1 = float(sayi1.get())
    s2 = float(sayi2.get())
    sonuc.configure(text= str(s1-s2))

def carp():
    s1 = float(sayi1.get())
    s2 = float(sayi2.get())
    sonuc.configure(text= str(s1*s2))

def bol():
    s1 = float(sayi1.get())
    s2 = float(sayi2.get())
    sonuc.configure(text= str(s1/s2))



form = tk.Tk()
form.title("Hesap Makinesi")
form.geometry("500x400")

sonuc = tk.Label(form,text="Cevap",font="Courier 16 bold",width=30, justify="center")
sonuc.place(x=200,y=320)


sayi1 = tk.Entry(form,font="Courier 14 bold",width=15,justify="right")
sayi1.place(x=150,y=80)
sayi2 = tk.Entry(form,font="Courier 14 bold",width=15,justify="right")
sayi2.place(x=150,y=110)

tus1 = tk.Button(form,text="+",font="Times 16 bold",width=3,command=topla)
tus1.place(x=145,y=138)
tus2 = tk.Button(form,text="-",font="Times 16 bold",width=3,command=cikar)
tus2.place(x=185,y=138)
tus3 = tk.Button(form,text="*",font="Times 16 bold",width=3,command=carp)
tus3.place(x=230,y=138)
tus4 = tk.Button(form,text="/",font="Times 16 bold",width=3,command=bol)
tus4.place(x=275,y=138)



form.mainloop()

