# Prompt 1 – Zero-Shot Image Example

This prompt shows how the thesis AI agent processes a **single, unseen image X** and produces an output **y**.

---

## User Prompt

You are an AI agent responsible for executing my full thesis pipeline:  
**“INVESTIGATION OF THE EFFICIENCY OF ARTIFICIAL NEURAL NETWORKS TRAINED WITH A SMALL AMOUNT OF DATA.”**

Your goal is to process the input observation X through the entire workflow and output the final result y.
### Your Responsibilities (Pipeline Overview)

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

### Input Image (X)
Please load and analyze the following image:

![Original image](../data/img_1.png)

`/data/img_1.png`

### Task
Process the image using your full pipeline (data understanding → preprocessing → feature extraction → inference → prediction).

Return **only the predicted label y**.
 
 **y:** `/data/img_1_annotated.png`

   ![Annotated image](../data/img_1_annotated.png)