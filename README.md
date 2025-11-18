Procedure (For the implementation OF BERT-based Text Documentation Customization)

I uploaded the CSV dataset into Google Colab so the code could read it.

I cleaned the data by removing rows that had missing values and changed all text to lowercase to keep everything uniform.

I converted the text labels into numbers using a label encoder because the BERT model works with numeric labels.

I split the data into training data (for learning) and testing data (for checking accuracy), using an 80/20 ratio.

I used the BERT tokenizer to break each text into small tokens, and padded/truncated them so every input had the same length.

I created a dataset class that holds the input IDs, attention masks, and labels so the HuggingFace Trainer can easily load batches during training.

I loaded the pre-trained BERT model along with its configuration from HuggingFace.

I set up the training arguments such as number of training epochs, batch size, and where to save the results.

I trained the BERT model on the training data so it could learn patterns and understand how to classify the text.

After training, I evaluated the model using the test data to check how accurate it is.

I saved both the trained model and the tokenizer so I can reuse them later without retraining.

I loaded the saved model again to verify that everything works correctly.

I created a prediction function that allows me to type any new sentence, and the model returns the predicted category based on what it learned.
