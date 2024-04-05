import tkinter as tk
from tkinter import filedialog
import PyPDF4

pdf_file_path = ""
password_list_path = ""

def select_pdf_file():
    global pdf_file_path
    pdf_file_path = filedialog.askopenfilename(filetypes=[("PDF Files", "*.pdf")])
    if pdf_file_path:
        pdf_file_label.config(text=f"PDF File: {pdf_file_path}")
    else:
        pdf_file_label.config(text="No PDF File Selected")

def select_password_list():
    global password_list_path
    password_list_path = filedialog.askopenfilename(filetypes=[("Text Files", "*.txt")])
    if password_list_path:
        password_list_label.config(text=f"Password List: {password_list_path}")
    else:
        password_list_label.config(text="No Password List Selected")

def guess_pdf_password():
    if pdf_file_path and password_list_path:
     
        with open(password_list_path, "r") as file:
            password_list = file.readlines()

       
        pdf = PyPDF4.PdfFileReader(pdf_file_path)
        for password in password_list:
            password = password.strip() 
            if pdf.decrypt(password) == 1:
                output_label.config(text=f"Password found: {password}")
                return

     
        output_label.config(text="Password not found.")
    else:
        output_label.config(text="Please select both PDF file and Password list.")


window = tk.Tk()
window.title("PDF Password Guesser")


pdf_file_button = tk.Button(window, text="Select PDF File", command=select_pdf_file)
pdf_file_button.pack(pady=10)


pdf_file_label = tk.Label(window, text="No PDF File Selected")
pdf_file_label.pack()


password_list_button = tk.Button(window, text="Select Password List", command=select_password_list)
password_list_button.pack(pady=10)

password_list_label = tk.Label(window, text="No Password List Selected")
password_list_label.pack()


guess_button = tk.Button(window, text="Guess Password", command=guess_pdf_password)
guess_button.pack(pady=10)

output_label = tk.Label(window, text="")
output_label.pack()

window.mainloop()
