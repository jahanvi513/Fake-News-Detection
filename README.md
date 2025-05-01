# Fake News Detection Using AWS SageMaker and QuickSight

This project demonstrates a fake news detection system that classifies news headlines as **fake** or **real** using a pre-trained BERT model from Hugging Face, deployed through **Amazon SageMaker**. The system includes real-time inference, S3 storage, and a **QuickSight** dashboard for visualization.

---

## Features

- Classification of news headlines using a pre-trained NLP model.
- Serverless inference using Amazon SageMaker endpoints.
- Batch prediction pipeline using pandas and boto3.
- Result export to CSV and upload to S3.
- Dashboard with KPIs and charts via Amazon QuickSight.

---

## Tech Stack

- **Amazon SageMaker** – for deploying the Hugging Face model (`bert-base-uncased`)
- **Amazon S3** – for storing datasets and prediction results
- **Amazon QuickSight** – for visualizing model performance
- **Jupyter Notebooks** – for batch processing and testing

---

## Workflow Overview

1. Upload labeled CSV dataset (fake/real) to SageMaker.
2. Deploy a pre-trained text classification model via SageMaker JumpStart.
3. Use SageMaker notebook to:
   - Preprocess input text
   - Invoke the SageMaker endpoint for each row
   - Store predictions alongside original labels
4. Upload the resulting file (`predicted_fake_news.csv`) to the S3 bucket.
5. Connect S3 file to **QuickSight**, analyze:
   - Accuracy via calculated fields
   - Label distribution charts
   - Detailed prediction tables

---

## Demo Video

[Demo Video](https://drive.google.com/drive/folders/1t-Z3-YhWVh7_Qn9bn6Ze5P7XiViDvgwk?usp=sharing)
