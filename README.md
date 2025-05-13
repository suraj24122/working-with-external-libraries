🐍 Python Basics: Virtual Environment, Requests, Regex & Multithreading
This repository serves as a beginner-friendly guide to essential Python concepts that are often used in real-world projects:

✅ Virtual Environment & Package Management

🌐 HTTP Requests with requests module

🔍 Regular Expressions (re module)

🧵 Multi-threading with threading module

📁 1. Virtual Environment & Package Management
🔹 Why Use a Virtual Environment?
A virtual environment is an isolated Python environment that helps manage dependencies for a specific project without affecting system-wide Python settings.

🔹 Commands
bash
Copy
Edit
# Create a virtual environment
python -m venv venv

# Activate the virtual environment
# Windows:
venv\Scripts\activate
# Mac/Linux:
source venv/bin/activate

# Install packages
pip install <package-name>

# Save dependencies to requirements.txt
pip freeze > requirements.txt

# Install all dependencies from requirements.txt
pip install -r requirements.txt
🌐 2. HTTP Requests with requests Module
🔹 What is requests?
requests is a simple and elegant HTTP library for Python. It allows you to send HTTP/1.1 requests with methods like GET, POST, PUT, DELETE, etc.

🔹 Installation
bash
Copy
Edit
pip install requests
🔹 Example Usage
python
Copy
Edit
import requests

response = requests.get("https://jsonplaceholder.typicode.com/posts/1")
print(response.status_code)
print(response.json())
🔍 3. Regular Expressions in Python
🔹 What is re?
The re module lets you work with Regular Expressions — patterns used to match character combinations in strings.

🔹 Example Patterns
python
Copy
Edit
import re

text = "Email me at suraj@example.com or visit https://example.com"

# Find email
email = re.findall(r'\b[\w.-]+?@\w+?\.\w+?\b', text)
print(email)

# Find all URLs
urls = re.findall(r'https?://\S+', text)
print(urls)
🧵 4. Multi-threading with threading Module
🔹 Why Use Threads?
Threading enables concurrent execution of tasks in a single process — useful for I/O-bound tasks like network calls or file operations.

🔹 Example Usage
python
Copy
Edit
import threading
import time

def print_numbers():
    for i in range(5):
        print(f"Number: {i}")
        time.sleep(1)

def print_letters():
    for ch in 'abcde':
        print(f"Letter: {ch}")
        time.sleep(1)

# Creating threads
t1 = threading.Thread(target=print_numbers)
t2 = threading.Thread(target=print_letters)

# Starting threads
t1.start()
t2.start()

# Wait for both to finish
t1.join()
t2.join()

print("Done with multi-threading!")
📚 Summary
Topic	Module	Use Case
Virtual Environment	venv	Isolate dependencies
HTTP Requests	requests	Fetch APIs, send data over web
Regular Expressions	re	Text pattern matching & search
Multi-threading	threading	Concurrent execution of functions

📌 Prerequisites
Python 3.x installed

Basic understanding of Python syntax

💡 Contributions
Feel free to fork, clone, and submit PRs to improve or expand this repository!
