# Exploring DeepSeek-R1’s Reasoning Capabilities for News Recommendation

We propose an approach that seeks to explore and exploit DeepSeek-R1’s reasoning capabilities and apply them to news recommendation. Our method begins with a user profile generation stage, where we construct a descriptive user profile. We then leverage Chain-of-Thought (CoT) and step-by-step reasoning capabilities of DeepSeek-R1 to rank ten candidate articles for each user.

<p align="center">  
    <img src="Pictures/FrameWorkPIC.jpg" alt="DeepSeek-R1-Based Proposed Method" width="400" height="300"/>
</p>
To execute the project, follow these steps :

1. Install all the packages listed in the `requirements.txt` file.
2. Set up your tokens :

```json

"general" :
    {
        "HGF":"YOUR HUGGING FACE TOKEN",
        "WNB":"YOUR WNB TOKEN"
    }

```
1. Preprocess the data . Run the notebook  : `1-Preprocess-Data.ipynb`
2. Generate descriptions. Run the notebook : `2-Description-generator.ipynb`
3. Build the recommender. Run the notebook  : `3-Recommender-generator-cot.ipynb`
4. Evaluate the results. Run the notebook : `Evaluation.ipynb`

Or you can test the framework without fine-tuning it by directly running the notebook `finalFrameWork.ipynb`

## Recommendation Performance:

| Model     | AUC          | MRR          | nDCG@5       | nDCG@10      |
|-----------|--------------|--------------|--------------|--------------|
| **Simple Model** |||||
| Random    | 50.89±2.23   | 30.30±1.17   | 30.47±1.99   | 46.22±0.99   |
| MostPop   | 52.47±0.04   | 34.99±0.01   | 34.68±0.05   | 49.77±0.01   |
| TopicPop  | 64.64±0.04   | 39.35±0.07   | 44.39±0.08   | 53.59±0.05   |
| **Deep Model** |||||
| LSTUR     | 67.17±0.22   | 43.76±0.30   | 47.84±0.23   | 57.00±0.23   |
| DKN       | 66.28±0.43   | 42.31±0.50   | 46.43±0.37   | 55.88±0.38   |
| NAML      | 66.79±0.10   | 44.03±0.46   | 48.03±0.35   | 57.18±0.34   |
| NPA       | 65.52±0.78   | 43.16±0.40   | 46.53±0.47   | 56.47±0.32   |
| NRMS      | 66.25±0.12   | 43.60±0.30   | 46.86±0.25   | 56.82±0.21   |
| **DeepSeekR1** |||||
| **OurFrameWork** | 64.88±0.85 | 44.43±0.41   | 47.15±0.52   | 57.37±0.32   |
