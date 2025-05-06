# Exploring DeepSeek-R1’s Reasoning Capabilities for News Recommendation

We propose an approach that seeks to explore and exploit DeepSeek-R1’s reasoning capabilities and apply them to news recommendation. Our method begins with a user profile generation stage, where we construct a descriptive user profile. We then leverage Chain-of-Thought (CoT) and step-by-step reasoning capabilities of DeepSeek-R1 to rank ten candidate articles for each user.

![DeepSeek-R1-Based Proposed Method](Pictures/FrameWorkPIC.jpg)

To Execute the project, first run install all the packegs existing in the reuiqremnts file then set up your tokens :

```json

"general" :
    {
        "HGF":"YOUR HUGGING FACE TOKEN",
        "WNB":"YOUR WNB TOKEN"
    }

```

You can run the framework directly by executing
