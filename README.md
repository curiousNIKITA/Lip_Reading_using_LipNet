The LipNet model addresses the need for efficient and inclusive communication in varied domains.

Dataset : All videos are 3 seconds long with a frame rate of 25fps. The Dataset has 2 parts, first part the video and the other is alignment which is text format.

Loading Data: There are 2 functions for loading the video data and text alignment data each performing their corresponding operation
Load video: this function takes the video path as input & loads the video as frames, converts them into grayscale, extracts region of interest (mouth area) and then normalizes region.
Alignment function : This function loads the text file corresponding to the file loaded for the video, then it reads the text file and tokenize it, for further processing.
Lastly, the load data function calls both the load video and the load alignment function to parallely load both the video and the alignment files.

The core components include spatio-temporal convolutional neural networks (CNNs) for feature extraction, Bidirectional Long Short-Term Memory networks (Bi-LSTMs) for sequence modeling, and the Connectionist Temporal Classification (CTC) loss as a key element. This combination of methods enabled us to create a robust and effective model for this lipreading project.

The dataset is divided into batches, with each batch containing 500 samples.
Out of these 500 samples, 450 are designated for training, and 50 are set aside for testing. 
This separation is crucial for evaluating the model's performance.
The batches, consisting of both video frames and corresponding text data, are passed to the LipNet model for training. During training, the model learns to predict text sequences (spoken words) from the video data using lip movements.
