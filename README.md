https://github.com/user-attachments/assets/ddb1b0b3-7b81-45b1-84cb-e487c5d5d392
Uploading Screen Recording 2026-06-09 141919.mp4…
The code for the above video :
import random
text_data = """
machine learning makes the world smart.
Smart machines can learn and machines can innovate.
Technologiy is the future of the world.
"""
words = text_data.split()
model = {}
for i in range(len(words) - 1):
    current_word = words[i]
    next_word = words[i + 1]

    if current_word not in model:
        model[current_word] = []
    model[current_word].append(next_word)
def generate_text(start_word, length=10):
    current = start_word
    result = [current]

    for _ in range(length):
        if current in model:
            next_word = random.choice(model[current])
            result.append(next_word)
            current = next_word
        else:
            break
    return " ".join(result)
print("Generated Text Output:")
print(generate_text("machine", length=8))

https://github.com/user-attachments/assets/129abf83-0db8-4c24-84b1-5a04f2666edf
The code for the above video:
import random
text_data = """
Python is a powerful programming language.
It is widely used in data science and machine learning.
many developers prefer python because it is easy to learn and use.
Data science helps in making better decisions for the future.
"""
words = text_data.split()
model = {}
for i in range(len(words) - 1):
    current_word = words[i]
    next_word = words[i + 1]

    if current_word not in model:
        model[current_word] = []
    model[current_word].append(next_word)
def generate_text(start_word, length=10):
    current = start_word
    result = [current]

    for _ in range(length):
        if current in model:
            next_word = random.choice(model[current])
            result.append(next_word)
            current = next_word
        else:
            break
    return " ".join(result)
print("Generated Text Output:")
print(generate_text("machine", length=8))

