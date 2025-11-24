# Prompt 2 – Few-Shot Example

This prompt provides several known (X, y) pairs before asking the AI agent to predict the output for a new observation.  
This demonstrates how the system can use few-shot prompting to operate more effectively under small-data conditions.

---

## User Prompt

You are an AI agent that performs end-to-end prediction using small datasets.  
Below are several known training examples consisting of (X, y) pairs.

### Input Image (X)
Please load and analyze the following image:

`/data/img_1.png`

### New Input

**X:**  
[3.2, 1.7, 0.5]

### Task
Predict the corresponding **y**.  
Return only the value of **y**.
