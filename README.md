# Lip-Sync-
The Lip Sync project aims to create an AI model proficient in synchronizing audio and video, accurately matching lip movements with the corresponding audio. The model utilizes the Moviepy library in Python to manipulate video and audio files seamlessly.

You can utilize the pre-trained lip-syncing model provided in the links to accurately synchronize audio and video, creating a seamless and natural visual and auditory experience.
Video - https://openinapp.co/5cwva
Audio - https://openinapp.co/o9vuj

# Installation
To run the Lip Sync project, ensure you have Python 3.6 or above installed. Install the necessary libraries using pip install -r requirements.txt.

# Usage

# Place your video file and audio file in the designated paths 
("path/to/video.mp4" and "path/to/audio.wav").
# Load the video and audio files using the VideoFileClip and AudioFileClip functions.
# Get the durations of the video and audio using the duration attribute.
video_duration = video.duration
audio_duration = audio.duration
# Adjust the video duration to match the audio duration. If the video is shorter, loop it; if longer, trim it accordingly.
# Synchronize the video and audio durations using the set_audio and set_duration functions.
# Save the final synchronized video with lip-synced audio to the specified output path using write_videofile.

# Sample Output
You can find a sample output of the synchronized video with lip-synced audio in the "lipsync.mp4" folder.


# Note
Ensure that the paths for the video and audio files are correctly specified in the code before running the program. The project is designed to handle video and audio files with different durations and synchronize them accordingly. For more details on how to evaluate lip-sync accuracy and performance, please refer to the accompanying documentation in the repository.
