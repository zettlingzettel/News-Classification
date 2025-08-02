# News-Classification
![IMG_5285](https://github.com/user-attachments/assets/cacace7e-b0ef-4142-9b79-64cc1b41ddb4)
![IMG_5286](https://github.com/user-attachments/assets/898eb622-4c1f-4200-8a2a-70aae58b089a)
![IMG_5287](https://github.com/user-attachments/assets/6c99ab29-7ee3-4b02-a3cb-ba5ad7b36afb)
![IMG_5288](https://github.com/user-attachments/assets/b2cd0946-028c-4e01-96b4-b594be3d1f60)
![IMG_5289](https://github.com/user-attachments/assets/c3b027ec-8195-43cd-ba50-269431f0029a)
![IMG_5290](https://github.com/user-attachments/assets/2d14b557-7c69-419b-bdc7-4c034e31ce4c)
![IMG_5291](https://github.com/user-attachments/assets/11101447-2016-48c8-b54c-c4044e2b053a)
![IMG_5292](https://github.com/user-attachments/assets/88300332-6545-4106-8571-071a5e0a05ac)


This Jupyter Notebook, titled "News_Article_Classification_Health_&_Wellness.ipynb," details a machine learning workflow for classifying news articles as either "Health & Wellness" or "not Health & Wellness".

The notebook's process includes:

Environment Setup: Google Drive is mounted, and essential libraries such as tensorflow, transformers, and ktrain are installed.

Data Loading and Preparation: A JSON file (training_data.json) containing news article data is loaded into a pandas DataFrame. The 'headline' and 'short_description' columns are then combined into a single 'combined_text' column for text processing.

Data Labeling and Balancing: Articles with categories "HEALTHY LIVING" or "WELLNESS" are labeled as 1 (healthy_wellness), while all others are labeled as 0. To address class imbalance, 20,000 articles from the 'not Health & Wellness' category are randomly sampled and combined with all 'Health & Wellness' articles.

Data Splitting and Preprocessing: The balanced dataset is divided into training and validation sets. The text data is preprocessed using ktrain.text.texts_from_df with a 'standard' mode and a maximum sequence length of 32.

Model Building and Training: A text classifier is constructed using the 'fasttext' architecture from ktrain.text.text_classifier. A learner object is initialized, and the optimal learning rate is determined using learner.lr_find(). The model is then trained for 16 epochs with early stopping, using a triangular learning rate policy.

Model Saving and Evaluation: The trained model and its predictor are saved for future use. The model's performance is evaluated on a validation set, and a classification report is printed. The notebook also demonstrates the predictor's functionality by classifying example news articles and outputting the probability of each being "Health & Wellness".




