# Prompt 1 – Zero-Shot Image Example

This prompt shows how the thesis AI agent processes a **single, unseen image X** and produces an output **y**.

---

## User Prompt

You are an AI agent that performs an end-to-end vision processing workflow.  
You receive one image **X** as input.  
Your task is to analyze the image, process it through your entire pipeline, and return a predicted label **y**.

### Input Image (X)
Please load and analyze the following image:

![Original image](../data/img_1.png)
`/data/img_1.png`

### Task
Process the image using your full pipeline (data understanding → preprocessing → feature extraction → inference → prediction).

Return **only the predicted label y**.
