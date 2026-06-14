https://github.com/user-attachments/assets/4ab51be4-d8bf-49ad-9ab1-fc322b6a95f6
The code for the above video:
index.html
import random
text_data = """
Artificial intelligence is changing the world. 
Machine learning makes the world smart. 
Smart machines can learn and machines can innovate. 
Technology is the future of the world.
"""
words = text_data.split()
model = {}
for i in range(len(words) - 1):
    current_word = words[i]
    next_word = words[i+1]
    
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

script.jss
import random
text_data = """
Python is a powerful programming language. 
It is widely used in data science and machine learning. 
Many developers prefer Python because it is easy to learn and use. 
Data science helps in making better decisions for the future.
"""
words = text_data.split()
model = {}
for i in range(len(words) - 1):
    current_word = words[i]
    next_word = words[i+1]
    
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
