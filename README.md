# Live Face Recognition Using K nearest neighbors
For Face recognition, K nearest neighbors is used.
Find more for kNN algorithm here : https://medium.com/@chiragsehra42/k-nearest-neighbors-explained-easily-c26706aa5c7f


## Haarcascades:
Haar-like features are digital image features used in object recognition. They owe their name to their intuitive similarity with Haar wavelets and were used in the first real-time face detector.
A simple rectangular Haar-like feature can be defined as the difference of the sum of pixels of areas inside the rectangle, which can be at any position and scale within the original image. This modified feature set is called 2-rectangle feature. There is also defined 3-rectangle features and 4-rectangle features. The values indicate certain characteristics of a particular area of the image. Each feature type can indicate the existence (or absence) of certain characteristics in the image, such as edges or changes in texture. For example, a 2-rectangle feature can indicate where the border lies between a dark region and a light region.

You can use different haarcascade files for different tasks. Here is the link to github repository:
https://github.com/opencv/opencv/tree/master/data/haarcascades

## face_data.py
`` face_data.py`` is created to store the data points and features of face in front of the webcam. Image from the webcam acts as input which is in RGB format. This input is converted into grayscale images so that processing takes less time. This data is stored in ``.npy`` format. This data is stored 20 lines or till the user presses ``Esc`` key.


## face_reco.py
``face_reco.py`` is used to recognize the face with the information stored in the same directory by loading all the data in ``.npy ``format we have. We label the data and more LOC by adding more label to this file and adding thier names in the ``names `` directory. After loading the ``.npy`` files, input taken from camera is converted from RGB format to GrayScale and text is put over a box plotted where the face is detected.
To exit the console, press ``Esc`` key.






















## Direct Use
For implementation download the repository and run`` face_data.py``. This will store the face information as ``face_00.npy``. To store the next face change the save command by renaming it as ``face_01``.

Repeat the same process for the number of faces you want to store. 
For corresponding face_data files, load corresponding face_data to the ``face_reco.py`` file.

For the corresponding face information add names to be displayed in the ``names`` dictionary in ``face_reco.py``

Finally, open terminal or command prompt and enter ``python face_reco.py``.
