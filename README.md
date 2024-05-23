
## Link to Google Drive
https://drive.google.com/drive/folders/1n6T2kae9nbmYHZVH_PIMNqTsZV1dwbYA?usp=drive_link

I have added the trained model file and dataset on the drive link
## Approach for Dataset


For finding dataset I first started by searching dataset for human faces with masks. I did not find any labelled data for that. Later, I decided to first find a dataset for people's faces and put masks on them but it was a complete disaster. It was such a labour, I discarded it as well. At last, I decided to manually label the data. For that I took help of google and found a code to divide the images into 2 folders one by one. So I manually labelled the data of about 2000 images that I had in that data.

## Approach for problem
For the problem I decided to use transfer learning. As the base model I used VGG16 as base model and added a hidden dense layer and an output layer. The model was trained in 2 steps. In the first it is train while freezing VGG16 training. Then in the second time we unfreeeze some layers and retrain it. There were a lot of problems.
- First was with the dataset. Although I seperated the images but I still could not train it directly. So I made a csv file out of it. It stored the directory of images along with their labels.
- The while training model an error of OUT_OF_RANGE kept popping although I ensured that my steps in an epoch was calculated properly. Then after trying a little differently written model, it worked out.
- Third was the device problem. I had macbook air and it was crying while training. It was taking a lot of time to train. After training when I saved and loaded the model, it threw an error i couldn't get. I made a one line change and trained it on my friend's gaming laptop. When I got the files on whatsapp and tried to load the model, I wasn't able to. So at last I have to retrain it on my laptop. At that time I was unaware of benifits of Google Colab.

I have added a function to randomly select an image from my dataset and predict the gender along with the image being printed.

While I was trying to develop a model. I tried other known models for transfer learning but they were giving less accuracy hence I used VGG16 at last.

## How to use the model
I have added the trained model and the ipynb file for it. If you want to train it once again use the ipynb file, the dataset and csv file. Keep them in the same folder. Else use "Load_in_it.ipynb" to load and run the model. In that I have function for prediction. If you want to check its functioning on the images in dataset all you have to do is run the code. It will select an image randomly , show it on the screen with the predicted class. Else if you want to check on your images.
Use the predict_and_display_image function as instructed in the code.

## Screenshots of Model

### Test on an image from the dataset
[![Screenshot-64.png](https://i.postimg.cc/ZnmFJr0h/Screenshot-64.png)](https://postimg.cc/ygfSP3Ff)

### Accuracy Test on val_dataset
[![Screenshot-65.png](https://i.postimg.cc/B6TH7Xp7/Screenshot-65.png)](https://postimg.cc/ZBqWCY16)

### Test on a random image from internet
[![Screenshot-63.png](https://i.postimg.cc/L6CfWdkS/Screenshot-63.png)](https://postimg.cc/56z6HRkK)




##

