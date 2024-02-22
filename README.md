# Google-Cloud-Youtube-8M-Video-Understanding
## Project Description
In this challenge, it is expected to develop classification algorithms which accurately assign video-level labels using the new and improved YT-8M V2 dataset. The dataset was created from over 7 million YouTube videos (450,000 hours of video) and includes video labels from a vocabulary of 4716 classes (3.4 labels/video on average). It also comes with pre-extracted audio & visual features from every second of video (3.2B feature vectors in total). The goal is not only to play a pivotal role in setting state-of-the-art benchmarks, but also to improve search and organization of video archives.
## About Dataset
As the main goal is to predict the labels of a YouTube video, the challenge provides with extracted frame-level and video-level features. The feature data and detailed feature information can be found on the YouTube-8M dataset webpage. 

The training dataset in this competition contain videos and labels that are publicly available on YouTube, while the test data is not publicly available. The test data also has anonymized video IDs to ensure the fairness of the competition.

### File descriptions
video-level data<br />
Available on Google Cloud at gs://us.data.yt8m.org/1/video_level/train , gs://us.data.yt8m.org/1/video_level/validate , and gs://us.data.yt8m.org/1/video_level/test<br />

Each video has<br />
"video_id": unique id for the video, in train set it is a Youtube video id, and in test/validation they are anonymized<br />
"labels": list of labels of that video<br />
"mean_rgb": float array of length 1024<br />
"mean_audio": float array of length 128<br />
Files are in TFRecords format, TensorFlow python readers are available in the github repo
frame-level data

Each video has<br />
"video_id": unique id for the video, in train set it is a YouTube video id, and in test/validation they are anonymized.<br />
"labels": list of labels of that video.<br />
Each frame has "rgb": float array of length 1024,<br />
Each frame has "audio": float array of length 128<br />
Files are in TFRecords format, TensorFlow python readers are available in the github repo<br />


