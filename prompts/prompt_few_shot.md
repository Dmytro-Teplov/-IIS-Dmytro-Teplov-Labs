# Prompt 2 – Few-Shot Example (Image-Based)

This prompt demonstrates how the AI agent can use several known (X, y) image pairs as examples before generating a prediction for a new image.

The annotated images in `/data/annotated/` contain the ground-truth labels (y) created during Lab 1.2.

---

## User Prompt

You are an AI agent implementing the full end-to-end pipeline of my thesis:  
**“INVESTIGATION OF THE EFFICIENCY OF ARTIFICIAL NEURAL NETWORKS TRAINED WITH A SMALL AMOUNT OF DATA.”**

Your task is to run the complete workflow while using the provided (X, y) examples to improve your performance.
You must execute the full pipeline:

1. **Data Acquisition**
   - Download the relevant images from the TACO dataset.
   - Extract, filter, or organize data based on the specified target object classes.

2. **Baseline Object Detection**
   - Run an object detection model (YOLOv8/YOLOv5/SSD/etc.).
   - Train using a *small subset* of the dataset (low-data baseline).
   - Produce baseline metrics:
     - mAP@50
     - precision
     - recall
     - confusion matrix

3. **Dataset Modification / Low-Data Optimizations**
   Apply one or more of the following:
   - Data augmentation (rotation, noise, brightness, cropping)
   - Transfer learning with frozen layers
   - Synthetic dataset generation
   - Few-shot fine-tuning
   - Active learning sampling
   - Semi-supervised pseudo-labelling
   - Class-balancing through oversampling/undersampling

4. **Retrain the model**
   - Train with the enriched dataset.
   - Compute improved performance metrics.

5. **Compare the results**
   - Provide a numerical and qualitative comparison.
   - Highlight the performance gain.
   - Provide a conclusion (output y).
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
