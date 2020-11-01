# Neural Interview Audiolizer

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/olaviinha/NeuralInterviewAudiolizer/blob/main/NeuralInterviewAudiolizer.ipynb)

Neural Interview Audiolizer is a **".txt to .wav converter"** that turns textual dialogue (e.g. an interview, a chat) of two individuals to audio dialogue of two different voices, currently using either [Google Cloud Text-to-Speech API](https://cloud.google.com/text-to-speech) (wavenet voices only) or [Amazon Polly Text-to-Speech API](https://aws.amazon.com/polly/) (neural engine voices only).

It was made to run in [Google Colaboratory](https://colab.research.google.com/) (i.e. your browser), using [your Google Drive](https://drive.google.com/drive/my-drive) as data source and storage.

**Note** that you will need your own access keys to use either Google Cloud TTS or Amazon Polly TTS. More information on obtaining required keys:
- Google TTS: [Before you begin](https://cloud.google.com/text-to-speech/docs/quickstart-client-libraries#before-you-begin)
- Amazon Polly: [AWS Account and Access Keys](https://docs.aws.amazon.com/powershell/latest/userguide/pstools-appendix-sign-up.html)

**Input should be a .txt file containing dialogue in one of the following formats:**
1) `question_and_answer` expects an empty line between every time speaker changes.
2) `dialogue_with_names` expects `Name:` (e.g. _John: Hello Bob! How are you?_) every time speaker changes. Speaker is changed despite the name in the beginning, will probably improve this later to take names into account.

See [the notebook](https://colab.research.google.com/github/olaviinha/NeuralInterviewAudiolizer/blob/main/NeuralInterviewAudiolizer.ipynb) for more details.

## Audio demos

Source text | Google Cloud TTS | Amazon Polly TTS
------------ | ------------ | ------------
[gpt-3_chat-1.txt](https://storage.googleapis.com/olaviinha/github/neural-interview-audiolizer/gpt-3_chat-1.txt) | [WAV](https://storage.googleapis.com/olaviinha/github/neural-interview-audiolizer/chat-1_google_tts_kzcl.wav) | [WAV](https://storage.googleapis.com/olaviinha/github/neural-interview-audiolizer/chat-1_polly_mpfi.wav)
