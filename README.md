# CS50 AI Project: Traffic

### Project Aims:

The aim of this project is to write an AI to identify which traffic sign appears in a photograph.


### Project Requirements:

Complete the implementation of load_data and get_model in traffic.py.
- The load_data function should accept as an argument data_dir, representing the path to a directory where the data is stored, and return image arrays and labels for each image in the data set.
  - You may assume that data_dir will contain one directory named after each category, numbered 0 through NUM_CATEGORIES - 1. Inside each category directory will be some number of image files.
  - Use the OpenCV-Python module (cv2) to read each image as a numpy.ndarray (a numpy multidimensional array). To pass these images into a neural network, the images will need to be the same size, so be sure to resize each image to have width IMG_WIDTH and height IMG_HEIGHT.
  - The function should return a tuple (images, labels). images should be a list of all of the images in the data set, where each image is represented as a numpy.ndarray of the appropriate size. labels should be a list of integers, representing the category number for each of the corresponding images in the images list.
  - Your function should be platform-independent: that is to say, it should work regardless of operating system. Note that on macOS, the / character is used to separate path components, while the \ character is used on Windows. Use os.sep and os.path.join as needed instead of using your platform’s specific separator character.
- The get_model function should return a compiled neural network model.
  - You may assume that the input to the neural network will be of the shape (IMG_WIDTH, IMG_HEIGHT, 3) (that is, an array representing an image of width IMG_WIDTH, height IMG_HEIGHT, and 3 values for each pixel for red, green, and blue).
  - The output layer of the neural network should have NUM_CATEGORIES units, one for each of the traffic sign categories.
  - The number of layers and the types of layers you include in between are up to you. You may wish to experiment with:
   - different numbers of convolutional and pooling layers
   - different numbers and sizes of filters for convolutional layers
   - different pool sizes for pooling layers
   - different numbers and sizes of hidden layers
   - dropout
   - 
### Usage:

- After cloning the repository, download the dataset at https://cdn.cs50.net/ai/2023/x/projects/5/gtsrb.zip, unzip it and move it to the project directory
- Run `pip3 install -r requirements.txt` to install this project’s dependencies: `opencv-python` for image processing, `scikit-learn` for ML-related functions, and `tensorflow` for neural networks.
- Run `python3 traffic.py gtsrb` to train and evaluate the model.
