# 🌟 Awesome Explainable AI

<p align="center">
  <img src="assets/banner.svg" alt="Awesome Explainable AI Banner" width="100%">
</p>

<p align="center">
  <a href="https://github.com/ishandutta2007/Awesome-Awesome-Awesome"><img src="https://img.shields.io/badge/Awesome-%E2%9C%94-blueviolet?style=flat-square&logo=github" alt="Awesome"/></a>
  <a href="https://github.com/ishandutta2007/Awesome-Explainable-AI/stargazers"><img src="https://img.shields.io/github/stars/ishandutta2007/Awesome-Explainable-AI?style=flat-square" alt="Stars"/></a>
  <a href="https://github.com/ishandutta2007/Awesome-Explainable-AI/network/members"><img src="https://img.shields.io/github/forks/ishandutta2007/Awesome-Explainable-AI?style=flat-square" alt="Forks"/></a>
  <a href="https://github.com/ishandutta2007/Awesome-Explainable-AI/issues"><img src="https://img.shields.io/github/issues/ishandutta2007/Awesome-Explainable-AI?style=flat-square" alt="Issues"/></a>
  <a href="https://github.com/ishandutta2007/Awesome-Explainable-AI/blob/main/LICENSE"><img src="https://img.shields.io/github/license/ishandutta2007/Awesome-Explainable-AI?style=flat-square" alt="License"/></a>
  <a href="https://github.com/ishandutta2007"><img alt="GitHub followers" src="https://img.shields.io/github/followers/ishandutta2007?label=Follow" /></a>
</p>

---

## 📖 Explainable AI (XAI) Methods & Real-World Examples

Explainable AI (XAI) refers to a suite of processes, methods, and tools that make the outputs of machine learning algorithms understandable, transparent, and trustworthy to human users. Depending on scope, dependency, and methodology, several distinct XAI variations and examples exist.

---

## 1. Scope-Based Examples

These variants distinguish whether the explanation aims to demystify the model's overall logic or justify an individual prediction.

| Type | Concept | Example | Year First Used | First Used Paper |
| :--- | :--- | :--- | :--- | :--- |
| [**Global Explainability**](docs/global_explainability.md) | Summarizes the overarching behavior of a model across the entire dataset. | Creating a **Feature Importance Plot** for a random forest credit-scoring model. This shows stakeholders that "Debt-to-Income Ratio" and "Credit History Length" are universally the top two factors driving approval decisions across all applicants. | 2001 | [Random Forests](https://link.springer.com/article/10.1023/A:1010933404324) |
| [**Local Explainability**](docs/local_explainability.md) | Zooming into a singular data point to explain why the model made one specific decision. | Generating a **Waterfall Chart** for a single rejected loan applicant. The chart proves that this specific user was denied solely because their personal "Recent Missed Payments" value overrode their otherwise healthy income metrics. | 2016 | ["Why Should I Trust You?": Explaining the Predictions of Any Classifier (LIME)](https://arxiv.org/abs/1602.04938) |

---

## 2. Model-Dependency Examples

These variants are categorized by whether the explanation tool is locked to a specific model type or can be applied universally.

| Type | Concept | Examples | Year First Used | First Used Paper |
| :--- | :--- | :--- | :--- | :--- |
| [**Model-Specific (Intrinsic)**](docs/model_specific_intrinsic.md) | Relying on glass-box models that are inherently transparent due to their simple mathematical structure. | 1. A **Decision Tree diagram** used in medical diagnosis software, allowing a doctor to trace a patient's symptoms through a visible flowchart of IF-THEN rules to reach a conclusion.<br>2. **Linear Regression Coefficients** in housing price forecasting, where a real estate agent can point out that every additional square foot mathematically adds exactly $150 to the final appraisal. | 1805 | [Nouvelles méthodes pour la détermination des orbites des comètes (Linear Regression)](https://books.google.com/books?id=yS4PAAAAQAAJ) |
| [**Model-Agnostic (Post-Hoc)**](docs/model_agnostic_post_hoc.md) | Applying external interpretability tools to complex "black-box" models (like Transformers or Deep Neural Networks) after training is complete. | 1. **SHAP (Shapley Additive exPlanations)** on an ensemble gradient-boosting model to see how much each feature pushes a prediction away from the baseline average.<br>2. **LIME (Local Interpretable Model-agnostic Explanations)** to approximate a deep neural network's local decision boundary by creating perturbed, simplified models around a single prediction point. | 2016 | ["Why Should I Trust You?": Explaining the Predictions of Any Classifier (LIME)](https://arxiv.org/abs/1602.04938) |

---

## 3. Data-Modality Specific Examples

These specialized tools are tailored to extract intuitive explanations from specific types of unstructured data.

| Type | Concept | Examples | Year First Used | First Used Paper |
| :--- | :--- | :--- | :--- | :--- |
| [**Computer Vision (Image-Based)**](docs/computer_vision_image_based.md) | Highlighting spatial regions within an image that triggered a neural network's classification. | 1. **Grad-CAM (Gradient-weighted Class Activation Mapping)** generates a thermal heatmap over a chest X-ray image, highlighting the exact lung tissue regions that caused the AI to diagnose pneumonia.<br>2. **Saliency Maps** highlighting specific pixels that an autonomous vehicle's object-detection system focused on to identify a pedestrian crossing the street. | 2013 | [Deep Inside Convolutional Networks: Visualising Image Classification Models and Saliency Maps](https://arxiv.org/abs/1312.6034) |
| [**Natural Language Processing (Text-Based)**](docs/natural_language_processing_text_based.md) | Identifying key words or structural phrases that dictated an NLP model's final output. | 1. **Attention Rollout** visualizing **Attention Weights** in a transformer-based customer feedback tool to highlight which adjectives (e.g., "frustrating", "broken") caused a support ticket to be flagged as high-priority negative sentiment.<br>2. **Counterfactual Explanations** for an automated resume-screening tool telling an applicant: "If your resume had contained the keyword 'Python' instead of 'General Programming', your profile would have passed the initial automated screening filter." | 2017 | [Counterfactual Explanations Without Opening the Black Box: Automated Decisions and the GDPR](https://arxiv.org/abs/1711.00399) |
