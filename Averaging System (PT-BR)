#Banco De Dados

class BdNota:
    @staticmethod
    def add_nota(notas):
        with open("bd_nota.txt", "a") as arquivo:
            arquivo.write(f"Primeira nota: {notas.nota1}, Segunda Nota: {notas.nota2}\n")


-----------------------------------------------------------------------------------------------------------------------


#Classes


class Notas:
    def __init__(self, nota1, nota2):
        self._nota1 = nota1
        self._nota2 = nota2

    @property
    def nota1(self):
        return self._nota1

    @property
    def nota2(self):
        return self._nota2



-----------------------------------------------------------------------------------------------------------------------


#Main


from classes import Notas
from banco_de_dados import BdNota
from tkinter import *

app = Tk()
app.title("<<< P2 - Cálculo de Média >>>")
app.geometry("500x300")
app.configure(background="#008")

def calculcar_media():
    nota1 = float(edt_nota1.get())
    nota2 = float(edt_nota2.get())
    media = (nota1 + nota2) / 2

    nota1 = f"{nota1}"
    nota2 = f"{nota2}"
    n = Notas(f"{str(nota1)}", f"{str(nota2)}")
    bdnotas = BdNota()
    bdnotas.add_nota(n)

    if media >= 7:
        resultado = " / Aprovado!"
    else:
        resultado = " / Reprovado :("


    lbl_resultado["text"] = "Média = " + str(media) + resultado

txt1 = Label(app, text="Nota 1: ")
txt1.place(x=10, y=10)
edt_nota1 = Entry(app)
edt_nota1.place(x=65, y=10)

txt2 = Label(app, text="Nota 2: ")
txt2.place(x=10, y=40)
edt_nota2 = Entry(app)
edt_nota2.place(x=65, y=40)


lbl_resultado = Label(app, text="<<< RESULTADO >>>")
lbl_resultado.place(x=30, y=130)

btn_calcular = Button(app, text="Calcular", command=calculcar_media)
btn_calcular.place(x=30, y=150)

app.mainloop()
