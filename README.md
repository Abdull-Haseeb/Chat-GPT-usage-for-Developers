## 1. Code Generation

### Description:

ChatGPT can generate code snippets based on given requirements or pseudo-code.

### Code Snippet:

```python
import openai

def generate_code(prompt):
    response = openai.Completion.create(
        engine="text-davinci-002",
        prompt=prompt,
        max_tokens=150,
        n=1,
        stop=None,
        temperature=0.7,
    )
    return response['choices'][0]['text'].strip()

# Example usage
code_prompt = "Write a Python function to calculate the factorial of a number."
generated_code = generate_code(code_prompt)
print(generated_code)
```

## 2. Language Translation

### Description:

ChatGPT can be used to translate text between different languages.

### Code Snippet:

```python
import openai

def translate_text(text, source_language, target_language):
    response = openai.Completion.create(
        engine="text-davinci-002",
        prompt=f"Translate the following text from {source_language} to {target_language}: {text}",
        max_tokens=150,
        n=1,
        stop=None,
        temperature=0.7,
    )
    return response['choices'][0]['text'].strip()

# Example usage
input_text = "Hello, how are you?"
translated_text = translate_text(input_text, "English", "French")
print(translated_text)
```

## 3. Text Summarization

### Description:

ChatGPT can be used to summarize long passages of text into shorter, coherent summaries.

### Code Snippet:

```python
import openai

def summarize_text(text):
    response = openai.Completion.create(
        engine="text-davinci-002",
        prompt=f"Summarize the following text: {text}",
        max_tokens=100,
        n=1,
        stop=None,
        temperature=0.7,
    )
    return response['choices'][0]['text'].strip()

# Example usage
long_text = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, ..."
summary = summarize_text(long_text)
print(summary)
```

## 4. Text Classification

### Description:

ChatGPT can classify text into predefined categories or tags.

### Code Snippet:

```python
import openai

def classify_text(text, categories):
    response = openai.Completion.create(
        engine="text-davinci-002",
        prompt=f"Classify the following text: {text}",
        max_tokens=100,
        n=1,
        stop=None,
        temperature=0.7,
    )
    classified_category = response['choices'][0]['text'].strip()
    return [category for category in categories if category.lower() in classified_category.lower()]

# Example usage
input_text = "This is an informative article about technology advancements."
categories = ["technology", "science", "politics", "sports"]
classified_categories = classify_text(input_text, categories)
print(classified_categories)
```

## 5. Code Commenting

### Description:

ChatGPT can generate comments for code to improve code readability.

### Code Snippet:

```python
import openai

def generate_code_comments(code):
    response = openai.Completion.create(
        engine="text-davinci-002",
        prompt=f"Add comments to the following code:\n{code}",
        max_tokens=150,
        n=1,
        stop=None,
        temperature=0.7,
    )
    return response['choices'][0]['text'].strip()

# Example usage
sample_code = """
def factorial(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial(n - 1)
"""
comments = generate_code_comments(sample_code)
print(comments)
```

## 6. Writing Technical Documentation

### Description:

ChatGPT can assist in writing technical documentation for projects.

### Code Snippet:

```python
import openai

def generate_technical_doc(topic):
    response = openai.Completion.create(
        engine="text-davinci-002",
        prompt=f"Write technical documentation for {topic}",
        max_tokens=300,
        n=1,
        stop=None,
        temperature=0.7,
    )
    return response['choices'][0]['text'].strip()

# Example usage
topic = "Using RESTful APIs in Python"
doc = generate_technical_doc(topic)
print(doc)
```

## 7. Code Refactoring

### Description:

ChatGPT can suggest code refactoring to improve code quality and performance.

### Code Snippet:

```python
import openai

def suggest_code_refactoring(code):
    response = openai.Completion.create(
        engine="text-davinci-002",
        prompt=f"Suggest refactoring for the following code:\n{code}",
        max_tokens=200,
        n=1,
        stop=None,
        temperature=0.7,
    )
    return response['choices'][0]['text'].strip()

# Example usage
sample_code = """
def calculate_area(radius):
    return 3.14 * radius * radius
"""
refactored_code = suggest_code_refactoring(sample_code)
print(refactored_code)
```

## 8. Stack Overflow Answers

### Description:

ChatGPT can generate concise and helpful answers to programming questions for Stack Overflow.

### Code Snippet:

```python
import openai

def generate_stackoverflow_answer(question):
    response = openai.Completion.create(
        engine="text-davinci-002",
        prompt=f"Provide an answer to the following Stack Overflow question:\n{question}",
        max_tokens=150,
        n=1,
        stop=None,
        temperature=0.7,
    )
    return response['choices'][0]['text'].strip()

# Example usage
stackoverflow_question = "How do I sort a list of dictionaries by a specific key in Python?"
answer = generate_stackoverflow_answer(stackoverflow_question)
print(answer)
```

## 9. Generating Release Notes

### Description:

ChatGPT can help generate release notes for software projects.

### Code Snippet:

```python
import openai

def generate_release_notes(version):
    response = openai.Completion.create(
        engine="text-davinci-002",
        prompt=f"Generate release notes for version {version}",
        max_tokens=300,
        n=1,
        stop=None,
        temperature=0.7,
    )
    return response['choices'][0]['text'].strip()

# Example usage
version = "v2.0.0"
release_notes = generate_release_notes(version)
print(release_notes)
```

## 10. Chatbot Integration

### Description:

ChatGPT can be integrated into chatbots to provide human-like conversational responses.

### Code Snippet:

```python
import openai

def chat_with_gpt(user_input):
    response = openai.Completion.create(
        engine="text-davinci-002",
        prompt=f"User: {user_input}\nBot:",
        max_tokens=150,
        n=1,
        stop=None,
        temperature=0.7,
    )
    return response['choices'][0]['text'].strip()

#

 Example usage
while True:
    user_input = input("You: ")
    if user_input.lower() in ["exit", "quit", "bye"]:
        break
    bot_response = chat_with_gpt(user_input)
    print("Bot:", bot_response)
```
