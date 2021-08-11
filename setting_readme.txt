
Settings in Windows:

--------
Known issue: version incompatible
Don't use yml file to install

conda install -c anaconda keras-gpu==2.2.4 ??? Not working!
Issue: https://github.com/akshaybahadur21/Facial-Recognition-using-Facenet/issues/11
 
Resolve: use python3.6, tensorflow-1.14


--------
conda activate py36-gpu

Then, Install with the following:

conda install -c anaconda keras-gpu==2.1.6 (this will also install tensor flow)
pip install opencv-python sklearn


--------
Test if installed successfully:

python
>> import keras
(should be 0 errors)

--------
GPU setting:

Then modify the train.py code, add the following line:

import os
os.environ['TF_FORCE_GPU_ALLOW_GROWTH'] = 'true'

This will fix this erro:
"keras  Could not create cudnn handle: CUDNN_STATUS_ALLOC_FAILED"
https://github.com/tensorflow/tensorflow/issues/24496


--------
Reference about tuning parameters
https://towardsdatascience.com/faster-r-cnn-object-detection-implemented-by-keras-for-custom-data-from-googles-open-images-125f62b9141a





