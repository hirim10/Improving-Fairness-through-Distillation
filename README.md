Improving Fairness in Visual Recognition through Feature Distillation
A Deep Learning Beyond Accuracy term project at North Carolina State University by Aravinda Jatavallabha, Aadithya Naresh, and Mihir Arora.

This project explores how to improve fairness in visual recognition models without sacrificing accuracy, using a novel Maximum Mean Discrepancy-based Fair Distillation (MFD) approach. We transfer fair and group-invariant information from a biased "teacher" model to a less biased "student" model using knowledge distillation principles enhanced by statistical fairness metrics.

📌 Overview
Many computer vision systems used in high-impact domains (e.g., facial recognition, hiring tools) suffer from demographic bias. Traditional fairness-improving techniques are often computationally intensive or impractical for pre-trained models.

We present a lightweight, efficient method for improving fairness:

MFD aligns feature distributions using Maximum Mean Discrepancy (MMD)

Reduces demographic bias (measured via Difference in Equalized Odds, DEO)

Maintains or even improves model accuracy

🔍 Key Concepts
Fairness Criterion: Difference in Equalized Odds (DEO)

Knowledge Distillation: Transferring only fair features from a teacher to student model

MMD Regularizer: Minimizes distance between subgroup and group-wide feature distributions in RKHS

Objective Function: Combines Cross Entropy loss and MFD loss with tunable hyperparameter λ

🧪 Experiments
We use:

Architectures: ResNet and ShuffleNet

Datasets: UTKFace (faces with age/gender/ethnicity labels) and CIFAR-10

Results:

Model	Accuracy	DEO
ResNet Teacher	72.5%	0.360
ResNet Student	73.5%	0.165
ShuffleNet Teacher	67.5%	0.390
ShuffleNet Student	62.0%	0.180

MFD reduces bias significantly (by up to 73%) while maintaining strong performance.

ResNet retains better accuracy–fairness tradeoff than ShuffleNet.
