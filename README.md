# Neural Dialogue Audiolizer

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/olaviinha/NeuralDialogueAudiolizer/blob/main/NeuralDialogueAudiolizer.ipynb)

Neural Dialogue Audiolizer is a **".txt to .wav converter"** that turns textual dialogue (e.g. an interview, a chat) between two individuals to audio dialogue with two freely selectable voices, currently by using any of the following APIs:
- [Google Cloud Text-to-Speech API](https://cloud.google.com/text-to-speech) (wavenet voices only)
- [Amazon Polly Text-to-Speech API](https://aws.amazon.com/polly/) (neural engine voices only)
- [Microsoft Azure Text-to-Speech API](https://azure.microsoft.com/en-us/services/cognitive-services/text-to-speech/) (neural voices only).

It was made to run in [Google Colaboratory](https://colab.research.google.com/) (i.e. your browser), using [your Google Drive](https://drive.google.com/drive/my-drive) as data source and storage.

## Audio demos

Source text | Google Cloud TTS | Amazon Polly TTS | Microsoft Azure TTS
------------ | ------------ | ------------ | ------------
[gpt-3_chat-1.txt](https://storage.googleapis.com/olaviinha/github/neural-interview-audiolizer/gpt-3_chat-1.txt) | [WAV](https://storage.googleapis.com/olaviinha/github/neural-interview-audiolizer/chat-1_google_tts_kzcl.wav) (loser) | [WAV](https://storage.googleapis.com/olaviinha/github/neural-interview-audiolizer/chat-1_polly_mpfi.wav) |  [WAV](https://storage.googleapis.com/olaviinha/github/neural-interview-audiolizer/chat-1_azure_zzwo.wav) (winner)

## API access

**Access with necessary access keys is required to use any of the provided TTS APIs.** More information on obtaining access:
- to Google Cloud TTS API: [Before you begin](https://cloud.google.com/text-to-speech/docs/quickstart-client-libraries#before-you-begin)
- to Amazon Polly TTS API: [AWS Account and Access Keys](https://docs.aws.amazon.com/powershell/latest/userguide/pstools-appendix-sign-up.html)
- to Microsoft Azure TTS API: [Create the Azure resource](https://docs.microsoft.com/en-us/azure/cognitive-services/speech-service/overview#create-the-azure-resource)

Note that neural voices are available only in specific regions in all of these services. Select location accordingly when enabling the service/API where necessary.

Note that **costs may apply**. At the time of writing this, to the best of my knowledge, account creation to all of these services as well as limited monthly usage of these TTS APIs is free of charge, even if billing/credit card information is already required upon registration. You should also be aware that each **line** in each text file you audiolize, consumes one TTS API call. TODO: consume only 2 API calls and slice+merge returned audio files in Colab.

## Input text
Input should be path to a .txt file located in your Google Drive, containing the dialogue in one of the following formats, with no other text. If your input material is a copy-paste from the interwebs, make sure to clean it up first to strictly follow one of these formats.
1) `question_and_answer` expects an empty line between every time speaker changes. [See example](https://raw.githubusercontent.com/olaviinha/NeuralInterviewAudiolizer/main/example_question_and_answer.txt)
2) `dialogue_with_names` expects `Name:` (e.g. _John: Hello Bob! How are you?_) every time speaker changes. Speaker is changed despite the name in the beginning, i.e. if there are two consecutive lines beginning with _John:_, the notebook will still interpret the second as _Bob_, and your result is messed up. This will be improved in the distant future, perhaps. [See example](https://raw.githubusercontent.com/olaviinha/NeuralInterviewAudiolizer/main/example_dialogue_with_names.txt)

## Languages
This notebook has only English and Finnish voices by default. To add other languages, add the correct language names to `p1_voice` and `p2_voice` menus from [Google Cloud TTS voice list](https://cloud.google.com/text-to-speech/docs/voices), [Amazon Polly TTS voice list](https://docs.aws.amazon.com/polly/latest/dg/voicelist.html) or [Microsoft Azure TTS voice list](https://docs.microsoft.com/azure/cognitive-services/speech-service/language-support#text-to-speech)

---

⇨ [Run NeuralDialogueAudiolizer.ipynb](https://colab.research.google.com/github/olaviinha/NeuralDialogueAudiolizer/blob/main/NeuralDialogueAudiolizer.ipynb)
