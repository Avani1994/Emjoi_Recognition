# Emjoi_Recognition

## Training using FRCNN (Faster Region Based Convolutional Neural Networks)
### Training data generation
Generated training data using PIL Image:
* Traning data is generated in format: 
    - `{'id': 'image'+ str(id), 'boxes' : [], 'char' : }}`
    - example = `{'id':'image0', 'boxes': [471, 250, 495, 274], 'char': '😋'}`
    - These dictionaries were then wriiten to training.csv and test.csv
### Training
* We tried using Faster RCNN for training.
    - However we couldn't obtain desired results
    - And following are the reason for bad outputs:
        - Both in test and training had 88 emoji classes to be predicted
        - The blue tick class had too many occurences, hence prediction output was mostly blue ticks. [class imbalance toward one class]
        - Emoji size was pretty small
    - We didnt have time and resources to retrain our model after handling class imbalance
    - Hence we shifted our focus to using classical image processing techniques such as SIFT (Scale-Invariant Feature Transform) Features matching using keypoints and descriptors, which resulted in proming results.
### BLOG 
* [Emoji detection and recognition](https://towardsdatascience.com/chat-images-to-textual-conversation-part-2-8260c09a032e)
* [Github Repo](https://github.com/Avani1994/ChatToText)



