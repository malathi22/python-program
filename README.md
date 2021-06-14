from tkinter import *
from tkinter import ttk

window = Tk()
#Declaring Window Title
window.title("Registration Screen")
#Declaring Window size
window.geometry('500x600')
#Declaring Window Color
window.configure(background = "skyblue");
#below four fields are declared
Employeename = Label(window ,text = "EmployeeName").grid(row = 0,column = 0)
Employeeid= Label(window ,text = "Employeeid").grid(row = 1,column = 0)
Email = Label(window ,text = "Email Id").grid(row = 2,column = 0)
Mobile = Label(window ,text = "Contact Number").grid(row = 3,column = 0)
address=Label(window ,text = "address").grid(row = 4,column = 0)
#List of country
list_of_country=['India','UK','US','China','Japan']

#Dropdown menu
a=StringVar()
dropdown = OptionMenu(window,a,*list_of_country)
dropdown.config(width=18)
a.set('Select Country')
dropdown.grid(row = 9,column = 0)
gender=Label(window,text = "gender").grid(row = 6,column = 0)
var=IntVar()
Radiobutton(window, text = "male",padx=30,variable=var, value=1 ).grid (row =7,column = 0)
Radiobutton(window ,text = "female",padx = 30,variable=var, value=2).grid (row=8,column = 0)
pincode = Label (window, text = "pincode").grid(row = 5,column = 0)
Employeename1 = Entry(window).grid(row = 0,column = 1)
Employeeid1 = Entry(window).grid(row = 1,column = 1)
Email1 = Entry(window).grid(row = 2,column = 1)
Mobile1 = Entry(window).grid(row = 3,column = 1)
address = Entry(window).grid(row = 4, column =1)
pincode  = Entry(window).grid(row=5,column=1)

#fubction declaration
def clicked():
     res = "Welcome to " + txt.get()
     lbl.configure(text= res)
btn = ttk.Button(window ,text="Submit").grid(row=12,column=1)
window.mainloop()
