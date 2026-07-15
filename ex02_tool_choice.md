# Exercise 2: Let the Model Pick the Tool

## Prompt

You have two available tools:

- get_weather(location) -> returns the weather for a location
- define_word(word) -> returns the dictionary definition of a word

Reply with only a JSON object naming the tool and its arguments in the following format:

```json
{
  "tool": "...",
  "args": {
    "...": "..."
  }
}
```

Do not include any explanations or additional text.

---

## Request 1

```text
What's the weather like in Paris?
```

### Model Output

```json
{
  "tool": "get_weather",
  "args": {
    "location": "Paris"
  }
}
```

---

## Request 2

```text
What does "recursion" mean?
```

### Model Output

```json
{
  "tool": "define_word",
  "args": {
    "word": "recursion"
  }
}
```

---

## Answer

Yes, the model picked the correct tool for each request. After the model replies, my code is responsible for calling the selected tool with the provided arguments and returning the result.