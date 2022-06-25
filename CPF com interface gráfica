from tkinter import *
from tkinter import messagebox
import string
import clipboard as clip

class LimparDocumento:
 def __init__(self):

  self.janela_principal = Tk()
  self.janela_principal.geometry('500x150')
  
  self.frame_cima  = Frame(self.janela_principal) 
  self.frame_baixo = Frame(self.janela_principal) 
  
  self.label = Label(self.frame_cima, text='Cole aqui o documento:')
  
  self.entrada = Entry(self.frame_cima, width=30)
  
  self.label.pack(side='left')
  self.entrada.pack(side='left')
  
  self.botao = Button(self.frame_baixo, text='Iniciar', command=self.CPF)
  self.botao_sair = Button(self.frame_baixo, text='Encerrar', command=self.janela_principal.destroy)
  
  self.botao.pack(side='left')
  self.botao_sair.pack(side='left')
  
  self.botao.pack()
  self.botao_sair.pack()
  
  self.frame_cima.pack()
  self.frame_baixo.pack()
  
  mainloop()

 def CPF(self):
  try:
          CPF = str(self.entrada.get())
          saida = ''.join([i for i in CPF if i not in string.punctuation])
          if int(saida) > 0:
                clip.copy(saida)
                messagebox.showinfo('limpando documento', 'documento ' + saida + ' copiado para a área de transferência')
          elif int(saida) == 0:
                  exit()
  except:
          messagebox.showinfo('limpando documento', 'entrada inválida - lembre-se de não digitar nenhuma letra, apenas números e caracteres especiais')
           
gui = LimparDocumento()
