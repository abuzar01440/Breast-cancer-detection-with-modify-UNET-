# 🎀 Breast Cancer Detection with MODIFY U-Net++ Deep Learning 🧠💻

Welcome to my project! 👋 I am Abuzar Shahid (@abuzar01440), a Data Scientist and Machine Learning Engineer. This project focuses on a very important topic in Medical Imaging: Finding breast tumors in ultrasound images using Deep Learning! 🏥✨

🌟 What is this project about?

In this project, we teach an AI model to look at an ultrasound image of a breast and draw a clear boundary around the tumor (this is called Image Segmentation). 🖼️🔍

To do this, I built a custom U-Net architecture using Python, TensorFlow, and Keras. U-Net is one of the best models for medical image segmentation! 🏆

🛠️ Step-by-Step: What happens in the code? 🕵️‍♂️

Here is a simple explanation of everything my code does:

## 1️⃣ Loading the Data 📂

First, the code looks into the folder containing the dataset (Dataset_BUSI_with_GT/benign).

It finds the normal images (ultrasound scans). 📸

It finds the "masks" (these are black-and-white images drawn by doctors to show exactly where the tumor is). 🎭

## 2️⃣ Preprocessing the Images 🧼✂️

Computers need clean and uniform data!

Resizing: The code changes the size of every image and mask to exactly 256 x 256 pixels. 📏

Normalization: The image pixel values are changed to be between 0 and 1 (by dividing by 255). This helps the AI learn much faster! ⚡

Cleaning Masks: It ensures all masks are single-channel (grayscale) so the model doesn't get confused. 🧹

## 3️⃣ Splitting the Data 🪓

We split the dataset into two parts:

Training Data (85%): Used to teach the model. 📚

Testing Data (15%): Kept a secret from the model to test how smart it became later! 🤫

# 4️⃣ Building the Modify U-Net++ Model 🏗️🧠

This is the heart of the project! The U-Net++ looks like a giant "U" shape. It has three main parts:

📉 The Encoder (Going Down): It uses Conv2D and MaxPooling2D layers to shrink the image and find important patterns (like edges and shapes).
    -  Used Elu activation function
    - Spatial DropOut

🌉 The Bottleneck (The Bottom): The deepest part of the network that holds the most compressed information.

📈 The Decoder (Going Up): It uses UpSampling2D to make the image big again. It also uses concatenate to mix the detailed patterns from the Encoder with the big picture!

🏁 The Output: A final layer with a sigmoid activation function guesses if a pixel is a tumor (1) or normal tissue (0). 🎯

5️⃣ Training the AI 🏋️‍♂️🔥

We use the AdamW optimizer (to learn efficiently). 📉

The model studies the training data for  several epochs (rounds of learning) in small batches of 2 images. ⏱️

6️⃣ Checking the Results 📊👀

After training, the code does some really cool things:

📈 Plots Graphs: It draws charts showing how the "Accuracy" went up and the "Loss" (errors) went down during training.

🖼️ Visualizes Predictions: It takes some random images from the test set and shows 3 things side-by-side:

The Original Ultrasound Image 📸

The True Mask (Doctor's drawing) 👨‍⚕️

The Predicted Mask (What our AI guessed!) 🤖

### 🚀 How to Run this Code?

Clone this repository to your computer. 💻

Make sure you have the dataset folder correctly placed and update the folder path in the code. 📂

Install the required libraries:

- pip install numpy pandas opencv-python matplotlib scikit-learn tensorflow keras


Open the breast tumor detection.ipynb notebook in Jupyter or VS Code. 📓

Run all cells and watch the AI learn! 🍿🥳

👨‍💻 About the Author

Abuzar Shahid 🚀

AI Scientist | Machine Learning Engineer | Data Scientist

I love transforming complex data into real-world solutions, especially in Medical Imaging and deep learning! Feel free to check out my other projects on my GitHub profile! 🌟

🌐 GitHub: @abuzar01440

💡 Interests: Data Science | Machine Learning | Deep Learning | NLP | Gen. AI | Medical Imaging 🏥

If you like this project, please give it a ⭐!
