import tkinter as tk
import random

# List of motivational quotes
quotes = [
    "Believe you can and you're halfway there.",
    "The harder you work, the luckier you get.",
    "Push yourself, because no one else is going to do it for you.",
    "Success doesn’t come to you. You go to it.",
    "Dream big and dare to fail.",
    "Your only limit is your mind.",
    "Great things never come from comfort zones.",
    "Don’t stop when you’re tired. Stop when you’re done."
]

# Function to display a random quote
def show_quote():
    quote = random.choice(quotes)
    label_quote.config(text=quote)

# Create main window
root = tk.Tk()
root.title("Motivation Booster 💪")
root.geometry("400x300")
root.config(bg="#F9F9F9")

# Title label
title = tk.Label(root, text="✨ Motivation Booster ✨", font=("Helvetica", 16, "bold"), bg="#F9F9F9", fg="#333")
title.pack(pady=20)

# Quote label
label_quote = tk.Label(root, text="", font=("Helvetica", 12), wraplength=350, bg="#F9F9F9", fg="#555")
label_quote.pack(pady=30)

# Button
btn = tk.Button(root, text="Show me a Quote", command=show_quote, bg="#4CAF50", fg="white", font=("Helvetica", 12, "bold"), padx=10, pady=5)
btn.pack(pady=10)

# Run the app
root.mainloop()
