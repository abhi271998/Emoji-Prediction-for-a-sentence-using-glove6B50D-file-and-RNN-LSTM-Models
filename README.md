# Emoji-Prediction-for-a-sentence-using-glove6B50D-file
# Emoji Prediction

In this project, **classifier** is bulit that learns to associate emojis with sentences. Although there are many technical details, the principle behind the classifier is very simple: we start with a large amount of sentences that contain emojis collected from Twitter messages.  Then we look at features from those sentences (words, word pairs, etc.) and train our classifier to associate certain features with their (known) smileys.  For example, if the classifier sees the word "happy" in many sentences that also has the smiley 😂, it will learn to classify such messages as 😂.  On the other hand, the word "happy" could be preceded by "not" in which case we shouldn't rely on just single words to be associated with certain smileys. For this reason, we also look at word sequences, and in this case, would learn that "not happy" is more strongly associated with sadness, outweighing the "happy" part.  The classifier learns to look at the totality of many word sequences found in a sentence and figures out what class of smiley would best characterize that sentence. Although the principle is simple, if we have millions of words of text with known smileys associated with the sentences, we can actually learn to do pretty well on this task.

### Models and Results
Building a machine learning model involves mainly two steps. The first step is to train a model. After that, we evaluate the model on a separate data set---i.e. we don't evaluate performance on the same data we learned from. For this project, we use four classifiers and train each classier to see which one works better for this project. To train and test the performance of each model, we split the data set into a "training set" and a "test set", in the ratio of 80% and 20%. By separating the data, we can make sure that the model generalizes well and can perform well in the real world.


### Example/Demo
Here are four example sentences and the emojis the classifier associates them with:

😂 Thank you for dinner!       
😢 I don't like it          
😱 My car skidded on the wet street        
😢 My cat died       
