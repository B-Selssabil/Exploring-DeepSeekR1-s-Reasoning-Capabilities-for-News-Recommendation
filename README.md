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

| AUC          | MRR          | nDCG@5       | nDCG@10      |
|--------------|--------------|--------------|--------------|
| 64.88 ± 0.85 | 44.43 ± 0.41 | 47.15 ± 0.52 | 57.37 ± 0.32 |

