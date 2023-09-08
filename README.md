# -Sample-code-for-a-basic-calculator-using-Tkinter
# Sample code for a basic calculator using Tkinter
import tkinter as tk

def calculate():
    expression = entry.get()
    try:
        result = eval(expression)
        result_label.config(text=f"Result: {result}")
    except Exception as e:
        result_label.config(text="Error")

app = tk.Tk()
app.title("Calculator")

entry = tk.Entry(app)
entry.pack()

calculate_button = tk.Button(app, text="Calculate", command=calculate)
calculate_button.pack()

result_label = tk.Label(app, text="Result:")
result_label.pack()

app.mainloop()
