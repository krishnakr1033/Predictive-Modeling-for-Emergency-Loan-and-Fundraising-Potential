# Multimodel-loan-grant-and-its-fundraising-resilliance-by-charity
---
I began by gathering and cleaning a large dataset—about 27,000 records—from Kiva (loans) and GoFundMe (charity) platforms using Selenium and BeautifulSoup. My goal was to build a system that could automatically analyze both applicant information and their images to help distinguish between loan and charity cases.

For the image analysis part, I trained a custom LeNet-5 CNN on the FER dataset to recognize applicants’ facial expressions, achieving 81% accuracy. To capture deeper visual context, I extracted flattened context vectors from a pre-trained VGG-16 model and applied PCA for dimensionality reduction.

On the text side, I preprocessed and tokenized applicant descriptions, converting them into dense vector representations with SentenceTransformer for richer semantic understanding.

Finally, I combined these insights by developing two classification models using the Keras Functional API—one for loan prediction (87% accuracy) and another for charity prediction (93% accuracy). This pipeline can assist in quickly categorizing applications, making the decision process more efficient and data-driven.
