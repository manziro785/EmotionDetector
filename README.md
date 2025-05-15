# Emotion Detection in Kyrgyz Texts

## What We Did
Our group worked on emotion detection in Kyrgyz-language texts. The goal was to take a pretrained model, fine-tune it on our own dataset, and try to figure out what emotion the person is expressing - happiness, sadness, fear, anger, and so on. We chose the lm-roberta-base model because it already supports the Kyrgyz language.

## How We Did It
First, we collectd a dataset in CSV format, where each row had a text and its emotion.  
Then, we used LabelEncoder to turn the emotion labels into numbers - the model needs that for training.  
We loaded the model and tokenizer to prepare the text for training.  
We split the data into training and test sets (90% training, 10% testing)  
We trained the model using the Trainer class from the transformers library.  
After training, we saved the model, the tokenizer, and the label encoder so we could use them later without retraining.  
We also fine-tuned the model for 10 more epochs to help it better understand emotions in Kyrgyz.

## What We Got
The model trained successfully. We tested it on Kyrgyz text - for example, we gave it the sentence “Ыйлагым келет” and it correctly predicted the emotion as fear.

## Conclusion
The model really works. You just give it a text, and it returns the emotion. We didn’t build anything complex - we just used existing tools and made small changes. This shows that you don’t need deep knowledge to build something useful if you have good libraries.  
The model is OP, works perfectly - that’s it :)
