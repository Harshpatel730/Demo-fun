Automated YouTube Video Generator

This project is a Python-based script that automates the creation of short-form videos (like YouTube Shorts or TikToks) on any given topic. It leverages AI for generating the script, voiceover, and relevant imagery, then combines them into a final video file.

🎥 How it Works

The script follows a sequential pipeline to generate the video from a single topic input:

📝 Text Generation: You provide a topic (e.g., "The Roman Empire"). The script uses the OpenAI API (GPT-3) to generate a short, engaging script about that topic.

🗣️ Text-to-Speech: The generated script is then converted into a high-quality audio voiceover using the ElevenLabs API.

🖼️ Image Generation: The script extracts key sentences from the text and uses the OpenAI API (DALL-E) to generate relevant images for each part of the script.

🎬 Video Assembly: Finally, using the MoviePy library, the script combines everything:

A pre-existing background video (background_video.mp4).

The generated images, displayed sequentially.

The AI-generated voiceover.

The final output is a complete final_video.mp4 file, ready to be uploaded.

✨ Features

Fully Automated: From a single topic, generate a complete video.

AI-Powered Content: Utilizes OpenAI for both scriptwriting and image creation.

High-Quality Voiceovers: Integrates with ElevenLabs for realistic text-to-speech.

Customizable: Easily change the background video, AI prompts, or voice.

Simple to Use: Requires minimal setup to get started.

🛠️ Prerequisites

Before you begin, ensure you have the following:

Python 3.7+

An OpenAI API Key.

An ElevenLabs API Key.

🚀 Installation & Setup

Clone the repository:

Generated sh
git clone https://github.com/Harshpatel730/Demo-fun.git


Navigate to the project directory:

Generated sh
cd Demo-fun/Automate_You_tube_Generation
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Sh
IGNORE_WHEN_COPYING_END

Create a virtual environment (recommended):

Generated sh
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Sh
IGNORE_WHEN_COPYING_END

Install the required dependencies:

Generated sh
pip install -r requirements.txt
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Sh
IGNORE_WHEN_COPYING_END

Create an environment file:
Create a file named .env in the Automate_You_tube_Generation directory and add your API keys:

Generated env
OPENAI_API_KEY="your_openai_api_key_here"
ELEVENLABS_API_KEY="your_elevenlabs_api_key_here"
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Env
IGNORE_WHEN_COPYING_END
🏃‍♂️ How to Run

Set your video topic:
Open the main.py file and change the value of the topic variable on line 12 to whatever you want the video to be about.

Generated python
# main.py
topic = "The Secrets of Ancient Egypt" # <-- Change this line
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Python
IGNORE_WHEN_COPYING_END

Run the script:
Execute the main script from your terminal:

Generated sh
python main.py
IGNORE_WHEN_COPYING_START
content_copy
download
Use code with caution.
Sh
IGNORE_WHEN_COPYING_END

Find your video:
The script will run through all the generation steps. Once complete, you will find the final video saved as final_video.mp4 in the same directory.

🔧 Customization

You can easily customize the output by modifying the following:

Background Video: Replace the background_video.mp4 file with any other video you want to use as a background. Ensure the new video has a similar or longer duration than the generated audio.

AI Voice: To change the voice, open text_to_speach.py and modify the voice parameter in the elevenlabs.generate() function. You can find available voice IDs on your ElevenLabs account.

AI Prompts: To change the style of the script or images, you can edit the prompts sent to OpenAI in text_generation.py and image_generation.py.

💻 Technologies Used

Python

OpenAI API (GPT-3 & DALL-E)

ElevenLabs API

MoviePy for video editing

Pillow for image handling
