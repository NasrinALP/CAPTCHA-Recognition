# CAPTCHA-Recognition
A deep learning project for CAPTCHA recognition using OpenCV, TensorFlow, and Keras, including full data preprocessing, feature extraction, and model training. It integrates CNN-BiLSTM architecture with CTC loss for accurate sequence prediction from CAPTCHA images.

Command: python3 main_al.py
(or Command: python3 main_al.py >> output.txt  for save results in output.txt )
(if this file there is not in your python path please add path of file like: python3 /Users/nasrinalipour/Downloads/main_al.py)

    the program is object-orinted 
    Utils and Data Utils files exist in folder
    tensorflow.image & tensorflow.data is used in data utils file
    results are shown in report named "AImedic_exam_report.docx"


* Data Utils-------> data_utilsss.py (this file contains functions which are used in processing data: split_data, preprocess, create_dataset function)

            ~~split_data function Description: split data to x_train, y_train, x_valid, y_valid

            ~~preprocess function Description: is preprocessing function which will be used in creating dataset.it contains of reading image,convert to grayscale image float32, resize it to desired size and transpose(because we want the time-dimension to correspond to the width of the image) 

            ~~create_dataset function Description: is a utility function to create a dataset(As tensorflow.python.data.ops.dataset_ops.PrefetchDataset Class) which will be prepared for training step(it contains preprocess(mapped by preprocess function), batch, prefetch)


* Utils------------> utilsss.py (this file contains function which is utils in main program: decode_batch_predictions function)
            ~~decode_batch_predictions function Description: is a utility function to decode the output of the inference network
