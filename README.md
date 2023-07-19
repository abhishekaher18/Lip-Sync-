# Lip-Sync-
The Lip Sync project aims to create an AI model proficient in synchronizing audio and video, accurately matching lip movements with the corresponding audio. The model utilizes the Moviepy library in Python to manipulate video and audio files seamlessly.

You can utilize the pre-trained lip-syncing model provided in the links to accurately synchronize audio and video, creating a seamless and natural visual and auditory experience.
Video - https://openinapp.co/5cwva
Audio - https://openinapp.co/o9vuj

Step 1: Install MoviePy and Necessary Modules
Before running the code, ensure you have Python installed. Install MoviePy and other necessary modules using the following commands:
pip install moviepy

Step 2: Import Required Libraries
In your Python script or notebook, import the necessary libraries:

from moviepy.editor import VideoFileClip, AudioFileClip

Step 3: Load Video and Audio Files
Specify the file paths for your video and audio files. For example:

video_path = "path/to/video.mp4"
audio_path = "path/to/audio.wav"

video = VideoFileClip(video_path)
audio = AudioFileClip(audio_path)

Step 4: Get Durations of Video and Audio
Obtain the durations of the video and audio:

video_duration = video.duration
audio_duration = audio.duration

Step 5: Adjust Video Duration to Match Audio Duration
Check if the video duration is shorter or longer than the audio duration, and adjust accordingly:

if video_duration < audio_duration:
    video = video.fx('loop', duration=audio_duration)
else:
    video = video.subclip(0, audio_duration)
    
Step 6: Synchronize Video and Audio Durations
Set the audio duration of the video to match the audio file's duration:

video = video.set_audio(audio.set_duration(video.duration))

Step 7: Save the Synchronized Video with Lip-Synced Audio
Specify the output file path and save the synchronized video:

output_path = "path/to/synchronized_video.mp4"
video.write_videofile(output_path, codec="libx264", audio_codec="aac")
