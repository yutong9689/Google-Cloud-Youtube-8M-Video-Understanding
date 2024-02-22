# Google-Cloud-Youtube-8M-Video-Understanding
## Project Description
In this challenge, it is expected to develop classification algorithms which accurately assign video-level labels using the new and improved YT-8M V2 dataset. The dataset was created from over 7 million YouTube videos (450,000 hours of video) and includes video labels from a vocabulary of 4716 classes (3.4 labels/video on average). It also comes with pre-extracted audio & visual features from every second of video (3.2B feature vectors in total). The goal is not only to play a pivotal role in setting state-of-the-art benchmarks, but also to improve search and organization of video archives.
## About Dataset
As the main goal is to predict the labels of a YouTube video. The challenge provides with extracted frame-level and video-level features. The feature data and detailed feature information can be found on the YouTube-8M dataset webpage. 

The training dataset in this competition contain videos and labels that are publicly available on YouTube, while the test data is not publicly available. The test data also has anonymized video IDs to ensure the fairness of the competition.

### File descriptions
video-level data
Available on Google Cloud at gs://us.data.yt8m.org/1/video_level/train , gs://us.data.yt8m.org/1/video_level/validate , and gs://us.data.yt8m.org/1/video_level/test
You can access the data on Google Cloud, or download to your local computer with instructions here
Total size of 31GB 
Each video has
"video_id": unique id for the video, in train set it is a Youtube video id, and in test/validation they are anonymized
"labels": list of labels of that video
"mean_rgb": float array of length 1024
"mean_audio": float array of length 128
Files are in TFRecords format, TensorFlow python readers are available in the github repo, and simple reader available in Kaggle Kernels
frame-level data
Available on Google Cloud at gs://us.data.yt8m.org/1/frame_level/train ,  gs://us.data.yt8m.org/1/frame_level/validate , and gs://us.data.yt8m.org/1/frame_level/test
You can access the data on Google Cloud, or download to your local computer with instructions here
Total size of 1.71TB (Large file warning!)
Each video has
"video_id": unique id for the video, in train set it is a YouTube video id, and in test/validation they are anonymized.
"labels": list of labels of that video.
Each frame has "rgb": float array of length 1024,
Each frame has "audio": float array of length 128
Files are in TFRecords format, TensorFlow python readers are available in the github repo, and simple reader available in Kaggle Kernels
train.csv, validation.csv - the training and validation sets ground truth are also available on Google Cloud: train_labels.csv and validate_labels.csv, or downloadable with gsutil: gs://us.data.yt8m.org/1/ground_truth_labels/train_labels.csv ,gs://us.data.yt8m.org/1/ground_truth_labels/validate_labels.csv
VideoId - the id of the video
Labels - the correct labels of the video (space delimited)
label_names.csv - a mapping between label_id and label_name (available on Kaggle)
sample_submission.csv - a sample submission file in the correct format (available on Kaggle)
VideoId - the id of the video
LabelConfidencePair - space delimited predictions and their probabilities. For example, 1 0.6 2 0.4 means label 1 with 0.6 probability, and label 2 with 0.4 probability for this video.
