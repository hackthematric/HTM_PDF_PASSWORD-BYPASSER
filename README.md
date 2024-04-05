# HTM_PDF_PASSWORD-BYPASSER



 PDF Password Guesser Tool

This tool is designed to assist in guessing passwords for PDF files. It provides a simple graphical user interface (GUI) built using Python's `tkinter` library.

 Getting Started

To use this tool, you need to have Python installed on your system. You can download Python from the [official website](https://www.python.org/downloads/).

Once Python is installed, you can run the script `pdf_password_guesser.py` to launch the tool.

```bash
python pdf_password_guesser.py
```

 Functionality

 Select PDF File

Click on the "Select PDF File" button to choose the PDF file for which you want to guess the password. Only PDF files with the extension `.pdf` are supported.

 Select Password List

Click on the "Select Password List" button to choose a text file containing a list of passwords. Each password should be on a separate line in the text file.

 Guess Password

Once both a PDF file and a password list are selected, click on the "Guess Password" button to start the password guessing process. The tool will iterate through each password in the list and attempt to decrypt the PDF file using that password.

 Output

The tool will display the outcome of the password guessing process in the output area below the buttons. If a matching password is found, it will be displayed. Otherwise, a message indicating that the password was not found will be shown.

 Dependencies

This tool relies on the following Python libraries:

- tkinter: Used for creating the graphical user interface.
- PyPDF4: Used for handling PDF files and attempting to decrypt them.

You can install the dependencies using the following command:

```bash
pip install -r requirements.txt
```

 Contributing

Contributions are welcome! If you have any suggestions, improvements, or bug fixes, feel free to open an issue or create a pull request.

 License

This tool is licensed under the MIT License. See the [htm) file for details.
```
