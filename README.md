# login-page-python
from cgitb import text
from logging import root
from tkinter import *
from tkinter import messagebox
from turtle import Screen, screensize

def login():
    username=Entry1.get()
    password=Entry2.get()

    if (username=="" and password==""):
        messagebox.showinfo("","Blank Not Allowed")

    elif (username=="sumit" and password=="abhinav"):
        messagebox.showinfo("","login success")

    else:
      messagebox.showinfo("","incorrect username and password")

#Screen=Tk()
root=Tk()
#Screen.title("Login")
root.title("Login")
#Screen.geometry("300x200")
root.geometry("300x200")
#lbTitle=Label(text="Login",font=("arial",50,"bold"),fg="black",bg='#d7dae2')
#lbTitle.pack(pady=50)

#bordercolor= Frame(Screen,bg="black",width=800,height=400)
#bordercolor.pack()

#mainframe=Frame(bordercolor,bg="#d7dae2",width=800,height=400)
#mainframe.pack(padx=20,pady=20)
global Entry1
global Entry2

Label(root,text="Username").place(x=20,y=20)
Label(root,text="Password").place(x=20,y=70)

Entry1=Entry(root,bd=5)
Entry1.place(x=140,y=20)

Entry2=Entry(root,bd=5)
Entry2.place(x=140,y=70)

Button(root,text="Login",command=login,height=3,width=13,bd=6).place(x=100,y=120)

root.mainloop()
#Screen.mainloop()
