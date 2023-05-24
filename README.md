# herr-ai
Low-latency and natural video conversations with LLMs. 

## Plan

We will use "turn based" conversation in our pilot. After reducing latency, we will move to streaming
 
1. User presses a "speak" button, talks to the target AI
[FACILITATED BY [VOCODE](https://github.com/vocodedev/vocode-python)]
3. A speech-to-text model like Whisper converts speech to text (AUDIO -> TEXT)
4. Text is submitted into a low-latency LLM like [GPT3.5](https://openai.com/blog/openai-api) (TEXT -> TEXT) 
5. A text to speech model like [Rime.ai](https://rime.ai) transforms the speech into an audio stream (TEXT -> AUDIO)
[END FACILITATED BY [VOCODE](https://github.com/vocodedev/vocode-python)]
7. A audio to "talking head" model like [Wav2Lip](https://github.com/Rudrabha/Wav2Lip) transforms it into the output video (AUDIO -> VIDEO)
8. The video is stitched into the current video stream, cycle repeats
