**Fruits & Vegetable Detection for YOLOv4** is an object detection dataset comprising 4592 images with 5628 labeled objects spanning 14 classes like *lemon*, *chili-bag*, *banana*, *tomato-bag*, and others. The dataset is divided into a *train* set of 3942 images and a *test* set of 650 images. It addresses the challenge of automating the classification of fresh fruits and vegetables at self-checkout portals in supermarkets. These portals aim to save time for customers but manually entering produce during checkout can be time-consuming and error-prone. Leveraging machine learning, the dataset seeks to automate the identification of items, particularly overcoming the challenge of detecting objects through semi-transparent bags, a common issue in object detection models.

## Motivation

The Fruits & Vegetable Detection for YOLOv4 dataset originates from the growing popularity of Machine Learning, widely integrated in technologies like YouTube Recommendations and Robotics Object Detection. The dataset addresses an observed issue in self-checkout stations at major grocery stores, primarily designed for items with barcodes, not loose produce like fresh fruits and vegetables. Integrating machine learning into the existing checkout station cameras enables accurate categorization of these loose items (e.g., grapes, lemon, banana), streamlining the checkout process and eliminating the need for manual item entry by customers.

## About Fruits & Vegetable Detection dataset

The most important part of the Dataset Acquisition is how to capture the images, which can give you a good result after model training. Authors start from the basic where they make small datasets through the big datasets. All of the images were captured, With Default settings in the camera of iPhone 11. 

- To train an object detection model, the datasets play an important role. There are different datasets available on Kaggle, Open Image Dataset By Google, and Some other websites.
- During the initial stage of the project, authors reviewed many data set from them Fruit 360 one of them, but the limitation of that dataset is it is specifically developed to reticular fruit detection by segmented portion.
- For the YOLO object detection, authors need to label a bunch of images with the background.
- Although Fruit 360 dataset works with R-CNN as per research, it will struggle with seeing through the semi-transparent plastic bag, which is the most crucial part.
- To Conclude All this Scenario, authors decided to make a custom dataset for a custom model. 

To achieve these goals, the authors achieved the result through several iterations. 

## Iteration 1

- First Iteration contains only 1 class with 69 photos of the tomatoes with a bag and without a bag, which is such a small dataset for any object detection model.
- It is developed for the experimental purpose for checks how it can behave with the YOLO object detection model. 

<img width="800" alt="fruit_and_veg_preview_1" src="https://github.com/dataset-ninja/fruits-and-vegetable-detection/assets/123257559/a7f5c031-9d87-43d8-b3d4-7d2a9067f704">

<span style="font-size: smaller; font-style: italic;">Tomato with bag & without bag.</span>

## Iteration 2

The second iteration contains three different classes, which include lemons, chilies, apples. These classes are with and without a bag. Here, there were 165 images taken during the 2nd iteration. It is randomly captured images without worrying about the background and other things. 

<img width="681" alt="fruit_and_veg_preview_2" src="https://github.com/dataset-ninja/fruits-and-vegetable-detection/assets/123257559/24370573-be13-4b7a-a61c-5652d6f5b63b">

<span style="font-size: smaller; font-style: italic;">Tomato with bag & without bag.</span>

## Iteration 3

During the 3rd Iteration, authors got exposure to dataset creation. Here authors decided to make a platform that depicts the environment at the self-checkout stations. To depict the same environment as self-checkout stations, authors put the chrome plate as a background, and for steadiness in all photos, authors set up the phone in one place until they got
the entire dataset.

Here is a little look at the DIY-home setup of the platform:

<img width="585" alt="fruit_and_veg_preview_3" src="https://github.com/dataset-ninja/fruits-and-vegetable-detection/assets/123257559/597a187e-4d4c-4f8b-a9be-2b24103d3b0c">

Here, during the 3rd iteration, authors create 14 separate classes in which they took approx 50 images of every individual class. 14 class are banana-bag, banana, blackberries, raspberry, lemon-bag, lemon, grapes-bag,
grapes, tomato-bag, tomato, apple-bag, apple, chili-bag, chili

For proper lighting, authors set up a lamp backside of the phone stand. Authors took photos by putting an object near and far to the camera. That way their model can learn for all of the scenarios.

<img width="652" alt="fruit_and_veg_preview_4" src="https://github.com/dataset-ninja/fruits-and-vegetable-detection/assets/123257559/3c9d8db0-78d9-4347-b8fc-16e36f2b4830">

<span style="font-size: smaller; font-style: italic;">14 Classes with & without bag.</span>

Authors took a total number of 656 images with a different angle and
different distance from the camera. To give a feel like a self-checkout station they put chrome plate so when it will get to the production model have a little more accuracy due to the identical background.

In some of the images, authors intentionally keep their hands in the images. It will give the feel of a customer's hand during the detection of the item.

Some of the images authors keep half in the bag half outside of the bag. That way, one can assume if some of the items keep outside of the bag, then it can still perform the detection.
