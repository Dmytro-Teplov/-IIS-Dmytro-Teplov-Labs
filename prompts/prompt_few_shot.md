# Prompt 2 – Few-Shot Example

This prompt provides several known (X, y) pairs before asking the AI agent to predict the output for a new observation.  
This demonstrates how the system can use few-shot prompting to operate more effectively under small-data conditions.

---

## User Prompt

You are an AI agent that performs end-to-end prediction using small datasets.  
Below are several known training examples consisting of (X, y) pairs.

### Known Examples (from Lab 1.2)

1. X: [2.1, 1.3, 0.4] → y: 4.7  
2. X: [0.9, 3.2, 1.1] → y: 6.0  
3. X: [5.4, 2.2, 0.7] → y: 9.8  

Use the patterns and relationships shown above to infer the output for a new input.

### New Input

**X:**  
[3.2, 1.7, 0.5]

### Task
Predict the corresponding **y**.  
Return only the value of **y**.
