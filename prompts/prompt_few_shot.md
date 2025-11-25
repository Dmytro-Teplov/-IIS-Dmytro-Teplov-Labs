# Prompt 2 – Few-Shot Example (Image-Based)

This prompt demonstrates how the AI agent can use several known (X, y) image pairs as examples before generating a prediction for a new image.

The annotated images in `/data/annotated/` contain the ground-truth labels (y) created during Lab 1.2.

---

## User Prompt

You are an AI agent implementing the full end-to-end pipeline of my thesis:  
**“INVESTIGATION OF THE EFFICIENCY OF ARTIFICIAL NEURAL NETWORKS TRAINED WITH A SMALL AMOUNT OF DATA.”**

Your task is to run the complete workflow while using the provided (X, y) examples to improve your performance.

---

### Example Training Data (Few-Shot Examples)

Below are several known (X, y) pairs from my Lab 1.2 dataset:

### Known (X, y) Examples from Lab 1.2

1. **X:** `/data/img_1.png`

    ![Original image](../data/img_1.png)

   **y:** `/data/img_1_annotated.png`

   ![Annotated image](../data/img_1_annotated.png)

2. **X:** `/data/img_2.png`

    ![Original image](../data/img_2.png)

   **y:** `/data/img_2_annotated.png`

    ![Annotated image](../data/img_2_annotated.png)

3. **X:** `/data/img_3.png`

    ![Original image](../data/img_3.png)

   **y:** `/data/img_3_annotated.png`

    ![Annotated image](../data/img_3_annotated.png)

Use the patterns in these examples (visual features, annotation style, object classes, segmentation masks, etc.) to infer the correct output for a new image.

---

### New Input Image (X)

`/data/img_4.png`

![Input image](../data/img_4.png)



### Task

Analyze the known examples (X, y), learn the relationship, then:

**Predict the output y for the new image `/data/img_4.png`.**  
Return the expected annotation or label **in the same format as the Lab 1.2 examples**.
