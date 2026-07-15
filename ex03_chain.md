# Exercise 3: Chain It Into an Answer

## Step 1: User Request

```text
What's the weather like in Astana?
```

---

## Step 2: Model's JSON Tool Call

```json
{
  "tool": "get_weather",
  "args": {
    "location": "Astana"
  }
}
```

---

## Step 3: Tool Result

```json
{
  "temperature": 33,
  "condition": "Sunny"
}
```

### Final Answer

The weather in Astana is sunny with a temperature of 33°C.

---

## Answer

This chain could break if the model returns invalid JSON or the tool fails, so my code should validate the JSON and handle any errors before using the result.